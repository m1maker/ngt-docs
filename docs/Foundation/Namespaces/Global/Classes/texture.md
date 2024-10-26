# Class: texture

The `texture` class provides a data structure for representing and managing textures in NGT. It includes properties and methods to handle various aspects of texture management such as size, color modes, alpha modification, rendering, and blending.

## Constructors

### `texture()`
- **Description**: Constructs an empty `texture` object.

## Methods

### `renderer@ get_renderer() const property`
- **Return Type**: renderer@
- **Description**: Returns the renderer associated with this texture as a property.

### `bool get_size(float&out w, float&out h)`
- **Parameters**:
  - `w` (float&out): Output parameter for the width.
  - `h` (float&out): Output parameter for the height.
- **Return Type**: bool
- **Description**: Retrieves the dimensions of the texture and stores them in the output parameters.

### `bool set_color_mode(uint8 r, uint8 g, uint8 b)`
- **Parameters**:
  - `r` (uint8): The red component of the color mode.
  - `g` (uint8): The green component of the color mode.
  - `b` (uint8): The blue component of the color mode.
- **Return Type**: bool
- **Description**: Sets the color mode using RGB values.

### `bool set_color_mode(float r, float g, float b)`
- **Parameters**:
  - `r` (float): The red component of the color mode.
  - `g` (float): The green component of the color mode.
  - `b` (float): The blue component of the color mode.
- **Return Type**: bool
- **Description**: Sets the color mode using floating-point RGB values.

### `bool get_color_mode(uint8&out r, uint8&out g, uint8&out b)`
- **Parameters**:
  - `r` (uint8&out): Output parameter for the red component of the color mode.
  - `g` (uint8&out): Output parameter for the green component of the color mode.
  - `b` (uint8&out): Output parameter for the blue component of the color mode.
- **Return Type**: bool
- **Description**: Retrieves the current color mode as RGB values.

### `bool get_color_mode(float&out r, float&out g, float&out b)`
- **Parameters**:
  - `r` (float&out): Output parameter for the red component of the color mode.
  - `g` (float&out): Output parameter for the green component of the color mode.
  - `b` (float&out): Output parameter for the blue component of the color mode.
- **Return Type**: bool
- **Description**: Retrieves the current color mode as floating-point RGB values.

### `bool set_alpha_mod(uint8 a)`
- **Parameters**:
  - `a` (uint8): The alpha modification value.
- **Return Type**: bool
- **Description**: Sets the alpha modification using an 8-bit value.

### `bool set_alpha_mod(float a)`
- **Parameters**:
  - `a` (float): The alpha modification value.
- **Return Type**: bool
- **Description**: Sets the alpha modification using a floating-point value.

### `bool get_alpha_mod(uint8&out a)`
- **Parameters**:
  - `a` (uint8&out): Output parameter for the alpha modification value.
- **Return Type**: bool
- **Description**: Retrieves the current alpha modification as an 8-bit value.

### `bool get_alpha_mod(float&out a)`
- **Parameters**:
  - `a` (float&out): Output parameter for the alpha modification value.
- **Return Type**: bool
- **Description**: Retrieves the current alpha modification as a floating-point value.

### `bool update(rect@ r, uint64 pixels, int pitch)`
- **Parameters**:
  - `r` (rect@): The rectangle area to update.
  - `pixels` (uint64): The memory buffer containing the pixel data.
  - `pitch` (int): The pitch of the pixel data.
- **Return Type**: bool
- **Description**: Updates a specific area of the texture with new pixel data.

### `void set_blend_mode(blendmode mode) const property`
- **Parameters**:
  - `mode` (blendmode): The blend mode to set.
- **Description**: Sets the blending mode for rendering operations using a property.

### `blendmode get_blend_mode() const property`
- **Return Type**: blendmode
- **Description**: Returns the current blending mode as a property.

### `void set_scale_mode(scalemode mode) const property`
- **Parameters**:
  - `mode` (scalemode): The scale mode to set.
- **Description**: Sets the scaling mode for rendering operations using a property.
