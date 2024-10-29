## Typedefs

```angelscript
funcdef void menu_item_callback();
funcdef void menu_on_click_callback();
```

These typedefs define function signatures for callback functions that can be assigned to `menu_item` and `menu`.

## Class: `menu_item`

Represents an item in a menu. Each `menu_item` can either be a simple action or contain a submenu.

### Constructor

#### `menu_item(const string&in title, menu_item_callback @cb)`
- **Description**: Creates a new `menu_item` with a callback function.
- **Parameters**:
  - `title`: The text of the menu item.
  - `cb`: A pointer to the callback function that will be executed when the item is selected.

#### `menu_item(const string&in title, menu @submenu)`
- **Description**: Creates a new `menu_item` with a submenu.
- **Parameters**:
  - `title`: The text of the menu item.
  - `submenu`: A pointer to the `menu` object that will be displayed when this item is selected.

### Methods

#### `menu_item(const string&in title, menu_item_callback @cb)`
- **Description**: Creates a new `menu_item` with a callback function.
- **Parameters**:
  - `title`: The text of the menu item.
  - `cb`: A pointer to the callback function that will be executed when the item is selected.

#### `menu_item(const string&in title, menu @submenu)`
- **Description**: Creates a new `menu_item` with a submenu.
- **Parameters**:
  - `title`: The text of the menu item.
  - `submenu`: A pointer to the `menu` object that will be displayed when this item is selected.

## Class: `menu`

Represents a complete menu system, including navigation, callbacks, and screen reader support.

### Constructor

#### `menu(const string&in title, bool is_submenu = false)`
- **Description**: Creates a new `menu`.
- **Parameters**:
  - `title`: The title of the menu.
  - `is_submenu`: A boolean indicating whether this menu is a submenu (default is `false`).

#### `menu()`
- **Description**: Default constructor that initializes an empty menu.

### Methods

#### `reset()`
- **Description**: Resets the menu to its initial state, clearing all items and settings.

#### `add_item(const string&in item_title, menu_item_callback @callback)`
- **Description**: Adds a new item with a callback function.
- **Parameters**:
  - `item_title`: The title of the menu item.
  - `callback`: A pointer to the callback function that will be executed when the item is selected.
- **Returns**: The index of the newly added item.

#### `add_items(array<string> @items)`
- **Description**: Adds multiple items from an array of strings, each without a specific callback (useful for adding static text items).
- **Parameters**:
  - `items`: An array of string titles to add to the menu.

#### `add_submenu(const string&in item_title, menu @submenu)`
- **Description**: Adds a new submenu item.
- **Parameters**:
  - `item_title`: The title of the menu item.
  - `submenu`: A pointer to the `menu` object that will be displayed when this item is selected.
- **Returns**: The index of the newly added submenu item.

#### `remove_item(int index)`
- **Description**: Removes an item at a specified index.
- **Parameters**:
  - `index`: The index of the item to remove.

#### `navigate(int direction)`
- **Description**: Navigates within the menu using up/down arrows or the tab key (if enabled).
- **Parameters**:
  - `direction`: The direction to navigate (-1 for up, 1 for down).

#### `select()`
- **Description**: Executes the callback function of the currently selected item, either by calling a callback or entering a submenu.

#### `monitor()`
- **Description**: Monitors user input and updates the selection based on keyboard events. It also handles screen reader announcements and sound effects.
- **Parameters**: None

#### `speak_item(bool interrupt = true)`
- **Description**: Speaks the currently selected item's title using the screen reader, optionally interrupting any ongoing speech.
- **Parameters**:
  - `interrupt`: A boolean indicating whether to interrupt current speech (default is `true`).

#### `get_selected_item() const property`
- **Description**: Returns the index of the currently selected item.
- **Returns**: The index of the selected item.

#### `get_item_count() const property`
- **Description**: Returns the total number of items in the menu.
- **Returns**: The count of items.

### Properties

#### `selected_index` (protected)
- **Type**: int
- **Description**: The current index of the selected item in the menu.

#### `items` (private)
- **Type**: array<menu_item @>
- **Description**: An array containing all items in the menu.

#### `title` (private)
- **Type**: string
- **Description**: The title of the menu.

#### `is_submenu` (protected)
- **Type**: bool
- **Description**: A flag indicating whether this menu is a submenu.

#### `title_spoken` (protected)
- **Type**: bool
- **Description**: A flag indicating whether the menu title has been spoken by the screen reader.

#### `wrapp` (private)
- **Type**: bool
- **Description**: A flag indicating whether wrapping around the item list is enabled.

#### `on_click_callback` (protected)
- **Type**: menu_on_click_callback @
- **Description**: A pointer to a callback function that will be executed when an item is selected.

#### `in_submenu` (private)
- **Type**: bool
- **Description**: A flag indicating whether the menu is currently displaying a submenu.

#### `speak_index` (private)
- **Type**: bool
- **Description**: A flag indicating whether to speak the index of the current item in addition to its title.

#### `enable_tab_order` (private)
- **Type**: bool
- **Description**: A flag indicating whether tab order is enabled for navigation.

#### `sp` (private)
- **Type**: sound_pool
- **Description**: An instance of the `sound_pool` class for playing sounds.

#### `open_sound`, `close_sound`, `move_sound`, `click_sound`, `border_sound`, `wrapp_sound`
- **Type**: string
- **Description**: Paths to the sound files that are played in various scenarios, such as opening/closing a menu or moving through items.
