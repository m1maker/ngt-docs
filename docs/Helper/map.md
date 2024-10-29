## Enum: `tiletype`

The `tiletype` enum defines different types of tiles that can be used in the map:

- **WALKABLE**: Represents a tile that is suitable for walking.
- **BLOCKED**: Represents a tile that cannot be walked through.
- **WATER**: Represents a water tile.
- **GRASS**: Represents a grass tile.
- **AIR**: Represents empty space or air.
- **WALL**: Represents a wall.

## Class: `map`

The `map` class manages the 3D map, including its dimensions and voxel data. It provides various methods to manipulate and access the map's contents.

### Constructor

#### `map()`
- **Description**: Default constructor that initializes an empty map with no voxels or tile names.
- **Parameters**: None
- **Returns**: A new instance of `map`.

#### `map(int w, int h, int d)`
- **Description**: Parameterized constructor that creates a map with specified dimensions and initializes all voxels to `tiletype::AIR`.
- **Parameters**:
  - `w`: Width of the map.
  - `h`: Height of the map.
  - `d`: Depth of the map.
- **Returns**: A new instance of `map` initialized with the given dimensions.

### Methods

#### `copy constructor`
- **Description**: Creates a copy of another `map`.
- **Parameters**:
  - `other`: The `map` to be copied.
- **Returns**: A new instance of `map` that is a copy of `other`.

#### `assignment operator`
- **Description**: Assigns the contents of one `map` to another.
- **Parameters**:
  - `other`: The `map` whose contents are to be assigned.
- **Returns**: A reference to this `map`.

#### `resize(int newWidth, int newHeight, int newDepth)`
- **Description**: Resizes the map to new dimensions. All new voxels are initialized to `tiletype::AIR`.
- **Parameters**:
  - `newWidth`: New width of the map.
  - `newHeight`: New height of the map.
  - `newDepth`: New depth of the map.

#### `set_tile(int x, int y, int z, tiletype type)`
- **Description**: Sets the type of a specific voxel at coordinates (x, y, z).
- **Parameters**:
  - `x`: X-coordinate of the voxel.
  - `y`: Y-coordinate of the voxel.
  - `z`: Z-coordinate of the voxel.
  - `type`: The new tile type for the voxel.

#### `set_tile_name(int x, int y, int z, const string&in name)`
- **Description**: Sets the name of a specific tile at coordinates (x, y, z).
- **Parameters**:
  - `x`: X-coordinate of the tile.
  - `y`: Y-coordinate of the tile.
  - `z`: Z-coordinate of the tile.
  - `name`: The new name for the tile.

#### `get_tile(int x, int y, int z)`
- **Description**: Retrieves the type of a specific voxel at coordinates (x, y, z).
- **Parameters**:
  - `x`: X-coordinate of the voxel.
  - `y`: Y-coordinate of the voxel.
  - `z`: Z-coordinate of the voxel.
- **Returns**: The tile type of the voxel. Returns `tiletype::BLOCKED` if the coordinates are out of bounds.

#### `get_tile_name(int x, int y, int z)`
- **Description**: Retrieves the name of a specific tile at coordinates (x, y, z).
- **Parameters**:
  - `x`: X-coordinate of the tile.
  - `y`: Y-coordinate of the tile.
  - `z`: Z-coordinate of the tile.
- **Returns**: The name of the tile. Returns an empty string if the coordinates are out of bounds.

#### `is_in_bounds(int x, int y, int z)`
- **Description**: Checks if the specified coordinates (x, y, z) are within the bounds of the map.
- **Parameters**:
  - `x`: X-coordinate to check.
  - `y`: Y-coordinate to check.
  - `z`: Z-coordinate to check.
- **Returns**: `true` if the coordinates are within bounds; otherwise, `false`.

#### `get_dimensions(int&out w, int&out h, int&out d)`
- **Description**: Retrieves the dimensions of the map.
- **Parameters**:
  - `w`: Output parameter for width.
  - `h`: Output parameter for height.
  - `d`: Output parameter for depth.

#### `print()`
- **Description**: Prints the map to the console, showing each layer as a grid. Different tile types are represented by different characters (e.g., '.' for walkable, '#' for blocked).

#### `add_wall(int startX, int startY, int startZ, int endX, int endY, int endZ)`
- **Description**: Creates a wall between two points in the map.
- **Parameters**:
  - `startX`: X-coordinate of the starting point.
  - `startY`: Y-coordinate of the starting point.
  - `startZ`: Z-coordinate of the starting point.
  - `endX`: X-coordinate of the ending point.
  - `endY`: Y-coordinate of the ending point.
  - `endZ`: Z-coordinate of the ending point.

#### `serialize()`
- **Description**: Serializes the map into a string format that can be easily stored or transmitted. The format includes dimensions and voxel data, with each tile's type and name separated by commas.
- **Returns**: A string representation of the map.

#### `deserialize(const string&in data)`
- **Description**: Deserializes the map from a string that was previously serialized using the `serialize` method.
- **Parameters**:
  - `data`: The string containing the serialized map data.
- **Returns**: `true` if deserialization is successful; otherwise, `false`.

### Example Usage

```angelscript
map myMap(10, 10, 10);

// Set a voxel type and name
myMap.set_tile(5, 5, 5, tiletype::WALL);
myMap.set_tile_name(5, 5, 5, "Wall");

// Get the voxel type and name
tiletype type = myMap.get_tile(5, 5, 5); // Should return tiletype::WALL
string name = myMap.get_tile_name(5, 5, 5); // Should return "Wall"

// Resize the map
myMap.resize(15, 15, 15);

// Print the map
myMap.print();

// Serialize and deserialize
string serialized = myMap.serialize();
map deserialized;
deserialized.deserialize(serialized);
```
