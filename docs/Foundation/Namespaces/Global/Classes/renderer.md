# Class: renderer

The `renderer` class provides a data structure for handling rendering operations in NGT. It includes properties and methods to manage various aspects of rendering such as output size, textures, targets, color settings, blending modes, and drawing primitives.

## Constructors

### `renderer()`
- **Description**: Constructs an empty `renderer` object.

## Methods

### `string get_name() const property`
- **Return Type**: string
- **Description**: Returns the name of the renderer as a property.

### `bool get_output_size(int&out w, int&out h)`
- **Parameters**:
  - `w` (int&out): Output parameter for the width.
  - `h` (int&out): Output parameter for the height.
- **Return Type**: bool
- **Description**: Retrieves the output size of the renderer and stores it in the output parameters.

### `bool get_current_output_size(int&out w, int&out h)`
- **Parameters**:
  - `w` (int&out): Output parameter for the current width.
  - `h` (int&out): Output parameter for the current height.
- **Return Type**: bool
- **Description**: Retrieves the current output size of the renderer and stores it in the output parameters.

### `texture@ create_texture(pixelformat format, textureaccess access, int w, int h)`
- **Parameters**:
  - `format` (pixelformat): The pixel format for the texture.
  - `access` (textureaccess): The access mode for the texture.
  - `w` (int): The width of the texture.
  - `h` (int): The height of the texture.
- **Return Type**: texture@
- **Description**: Creates a new texture with the specified properties and returns it.

### `texture@ create_texture(surface@ s)`
- **Parameters**:
  - `s` (surface@): A surface object to use for creating the texture.
- **Return Type**: texture@
- **Description**: Creates a new texture from a surface object and returns it.

### `void set_target(texture@ target) const property`
- **Parameters**:
  - `target` (texture@): The texture to set as the rendering target.
- **Description**: Sets the specified texture as the rendering target using a property.

### `texture@ get_target() const property`
- **Return Type**: texture@
- **Description**: Returns the current rendering target as a property.

### `bool set_logical_presentation(int w, int h, rendererlogicalpresentation mode)`
- **Parameters**:
  - `w` (int): The logical width.
  - `h` (int): The logical height.
  - `mode` (rendererlogicalpresentation): The presentation mode.
  **Return Type**: bool
- **Description**: Sets the logical presentation properties of the renderer.

### `bool get_logical_presentation(int&out w, int&out h, rendererlogicalpresentation&out mode)`
- **Parameters**:
  - `w` (int&out): Output parameter for the logical width.
  - `h` (int&out): Output parameter for the logical height.
  - `mode` (rendererlogicalpresentation&out): Output parameter for the presentation mode.
- **Return Type**: bool
- **Description**: Retrieves the logical presentation properties of the renderer.

### `bool set_render_scale(float x, float y)`
- **Parameters**:
  - `x` (float): The horizontal scale factor.
  - `y` (float): The vertical scale factor.
- **Return Type**: bool
- **Description**: Sets the render scale for the renderer.

### `bool get_render_scale(float&out x, float&out y)`
- **Parameters**:
  - `x` (float&out): Output parameter for the horizontal scale factor.
  - `y` (float&out): Output parameter for the vertical scale factor.
- **Return Type**: bool
- **Description**: Retrieves the current render scale of the renderer.

### `bool set_draw_color(uint8 r, uint8 g, uint8 b, uint8 a)`
- **Parameters**:
  - `r` (uint8): The red component of the draw color.
  - `g` (uint8): The green component of the draw color.
  - `b` (uint8): The blue component of the draw color.
  - `a` (uint8): The alpha component of the draw color.
- **Return Type**: bool
- **Description**: Sets the drawing color using RGB values.

### `bool set_draw_color(float r, float g, float b, float a)`
- **Parameters**:
  - `r` (float): The red component of the draw color.
  - `g` (float): The green component of the draw color.
  - `b` (float): The blue component of the draw color.
  - `a` (float): The alpha component of the draw color.
- **Return Type**: bool
- **Description**: Sets the drawing color using floating-point RGB values.

### `bool get_draw_color(uint8&out r, uint8&out g, uint8&out b, uint8&out a)`
- **Parameters**:
  - `r` (uint8&out): Output parameter for the red component of the draw color.
  - `g` (uint8&out): Output parameter for the green component of the draw color.
  - `b` (uint8&out): Output parameter for the blue component of the draw color.
  - `a` (uint8&out): Output parameter for the alpha component of the draw color.
- **Return Type**: bool
- **Description**: Retrieves the current drawing color as RGB values.

### `bool get_draw_color(float&out r, float&out g, float&out b, float&out a)`
- **Parameters**:
  - `r` (float&out): Output parameter for the red component of the draw color.
  - `g` (float&out): Output parameter for the green component of the draw color.
  - `b` (float&out): Output parameter for the blue component of the draw color.
  - `a` (float&out): Output parameter for the alpha component of the draw color.
- **Return Type**: bool
- **Description**: Retrieves the current drawing color as floating-point RGB values.

### `void set_color_scale(float scale) const property`
- **Parameters**:
  - `scale` (float): The color scale factor.
- **Description**: Sets the overall color scale for rendering operations using a property.

### `float get_color_scale() const property`
- **Return Type**: float
- **Description**: Returns the current color scale as a property.

### `void set_draw_blend_mode(blendmode mode) const property`
- **Parameters**:
  - `mode` (blendmode): The blend mode to set for rendering operations.
- **Description**: Sets the blend mode for rendering operations using a property.

### `blendmode get_draw_blend_mode() const property`
- **Return Type**: blendmode
- **Description**: Returns the current blend mode as a property.

### `void clear()`
- **Description**: Clears the renderer's drawing surface to a default color or texture.

### `bool render_point(float x, float y)`
- **Parameters**:
  - `x` (float): The x-coordinate of the point.
  - `y` (float): The y-coordinate of the point.
- **Return Type**: bool
- **Description**: Renders a single point at the specified coordinates.

### `bool render_line(float x1, float y1, float x2, float y2)`
- **Parameters**:
  - `x1` (float): The x-coordinate of the first endpoint.
  - `y1` (float): The y-coordinate of the first endpoint.
  - `x2` (float): The x-coordinate of the second endpoint.
  - `y2` (float): The y-coordinate of the second endpoint.
- **Return Type**: bool
- **Description**: Renders a line between two points.

### `bool render_rect(frect@ r)`
- **Parameters**:
  - `r` (frect@): The rectangle to render.
- **Return Type**: bool
- **Description**: Renders a rectangle with the specified dimensions.

### `bool render_fill_rect(frect@ r)`
- **Parameters**:
  - `r` (frect@): The rectangle to fill.
- **Return Type**: bool
- **Description**: Fills a rectangle with the current drawing color.

### `bool render_texture(texture@ t, frect@ srcrect, frect@ dstrect)`
- **Parameters**:
  - `t` (texture@): The texture to render.
  - `srcrect` (frect@): The source rectangle in the texture.
  - `dstrect` (frect@): The destination rectangle on the rendering surface.
- **Return Type**: bool
- **Description**: Renders a portion of a texture onto the rendering surface.

### `bool render_texture(texture@ t, frect@ srcrect, float scale, frect@ dstrect)`
- **Parameters**:
  - `t` (texture@): The texture to render.
  - `srcrect` (frect@): The source rectangle in the texture.
  - `scale` (float): The scaling factor for the texture.
  - `dstrect` (frect@): The destination rectangle on the rendering surface.
- **Return Type**: bool
- **Description**: Renders a scaled portion of a texture onto the rendering surface.

### `bool render_texture(texture@ t, frect@ srcrect, float left_width, float right_width, float top_height, float bottom_height, float scale, frect@ dstrect)`
- **Parameters**:
  - `t` (texture@): The texture to render.
  - `srcrect` (frect@): The source rectangle in the texture.
  - `left_width` (float): The left width for tiling.
  - `right_width` (float): The right width for tiling.
  - `top_height` (float): The top height for tiling.
  - `bottom_height` (float): The bottom height for tiling.
  - `scale` (float): The scaling factor for the texture.
  - `dstrect` (frect@): The destination rectangle on the rendering surface.
- **Return Type**: bool
- **Description**: Renders a portion of a texture with custom tiling onto the rendering surface.

### `bool flush()`
- **Return Type**: bool
- **Description**: Flushes any buffered rendering commands to the actual rendering device.

### `void set_viewport(rect@ r) const property`
- **Parameters**:
  - `r` (rect@): The new viewport rectangle.
- **Description**: Sets the viewport for rendering operations using a property.

### `rect@ get_viewport() const property`
- **Return Type**: rect@
- **Description**: Returns the current viewport as a property.

### `rect@ get_render_safe_area() const property`
- **Return Type**: rect@
- **Description**: Returns the safe area for rendering to avoid being cropped by device-specific artifacts as a property.

### `void set_render_clip_rect(rect@ r) const property`
- **Parameters**:
  - `r` (rect@): The new clipping rectangle.
- **Description**: Sets the clipping rectangle for rendering operations using a property.

### `rect@ get_render_clip_rect() const property`
- **Return Type**: rect@
- **Description**: Returns the current clipping rectangle as a property.

### `bool get_render_clip_enabled() const property`
- **Return Type**: bool
- **Description**: Returns whether clipping is enabled as a property.
