## Rendering

### `renderer@ request_renderer()`
- **Return Type**: renderer@
- **Description**: Requests and returns a new rendering context.

### `int get_num_render_drivers() property`
- **Return Type**: int
- **Description**: Returns the number of available rendering drivers as a property.

### `int get_render_driver(int index)`
- **Parameters**:
  - `index` (int): The index of the rendering driver.
- **Return Type**: int
- **Description**: Retrieves the identifier for the specified rendering driver.

### `surface@ render_text_solid(font@ font, const string&in text, int color)`
- **Parameters**:
  - `font` (font@): The font to use for rendering.
  - `text` (string): The text to render.
  - `color` (int): The color of the rendered text.
- **Return Type**: surface@
- **Description**: Renders solid text using the specified font and color.

### `surface@ render_text_solid(font@ font, const string&in text, int color, int wrapLength)`
- **Parameters**:
  - `font` (font@): The font to use for rendering.
  - `text` (string): The text to render.
  - `color` (int): The color of the rendered text.
  - `wrapLength` (int): The maximum width before wrapping.
- **Return Type**: surface@
- **Description**: Renders solid text with word wrapping using the specified font and color.

### `surface@ render_text_shaded(font@ font, const string&in text, int fgColor, int bgColor)`
- **Parameters**:
  - `font` (font@): The font to use for rendering.
  - `text` (string): The text to render.
  - `fgColor` (int): The foreground color of the rendered text.
  - `bgColor` (int): The background color of the rendered text.
- **Return Type**: surface@
- **Description**: Renders shaded text using the specified font, foreground color, and background color.

### `surface@ render_text_shaded(font@ font, const string&in text, int fgColor, int bgColor, int wrapWidth)`
- **Parameters**:
  - `font` (font@): The font to use for rendering.
  - `text` (string): The text to render.
  - `fgColor` (int): The foreground color of the rendered text.
  - `bgColor` (int): The background color of the rendered text.
  - `wrapWidth` (int): The maximum width before wrapping.
- **Return Type**: surface@
- **Description**: Renders shaded text with word wrapping using the specified font, foreground color, and background color.

### `surface@ render_text_blended(font@ font, const string&in text, int color)`
- **Parameters**:
  - `font` (font@): The font to use for rendering.
  - `text` (string): The text to render.
  - `color` (int): The color of the rendered text.
- **Return Type**: surface@
- **Description**: Renders blended text using the specified font and color.

### `surface@ render_text_blended(font@ font, const string&in text, int color, int wrapWidth)`
- **Parameters**:
  - `font` (font@): The font to use for rendering.
  - `text` (string): The text to render.
  - `color` (int): The color of the rendered text.
  - `wrapWidth` (int): The maximum width before wrapping.
- **Return Type**: surface@
- **Description**: Renders blended text with word wrapping using the specified font and color.

### `surface@ render_text_lcd(font@ font, const string&in text, int fgColor, int bgColor)`
- **Parameters**:
  - `font` (font@): The font to use for rendering.
  - `text` (string): The text to render.
  - `fgColor` (int): The foreground color of the rendered text.
  - `bgColor` (int): The background color of the rendered text.
- **Return Type**: surface@
- **Description**: Renders LCD text using the specified font, foreground color, and background color.

### `surface@ render_text_lcd(font@ font, const string&in text, int fgColor, int bgColor, int wrapWidth)`
- **Parameters**:
  - `font` (font@): The font to use for rendering.
  - `text` (string): The text to render.
  - `fgColor` (int): The foreground color of the rendered text.
  - `bgColor` (int): The background color of the rendered text.
  - `wrapWidth` (int): The maximum width before wrapping.
- **Return Type**: surface@
- **Description**: Renders LCD text with word wrapping using the specified font, foreground color, and background color.
