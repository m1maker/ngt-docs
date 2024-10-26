# Class: surface

The `surface` class provides a data structure for handling bitmap images and surfaces in NGT. It allows you to create, modify, and manipulate images with various properties and operations.

## Constructors

### `surface(int width, int height, pixelformat format)`
- **Parameters**:
  - `width` (int): The width of the surface.
  - `height` (int): The height of the surface.
  - `format` (pixelformat): The pixel format for the surface.
- **Description**: Constructs a new `surface` object with the specified dimensions and pixel format.

### `surface(int width, int height, pixelformat format, uint64 pixels, int pitch)`
- **Parameters**:
  - `width` (int): The width of the surface.
  - `height` (int): The height of the surface.
  - `format` (pixelformat): The pixel format for the surface.
  - `pixels` (uint64): The memory buffer containing the pixel data.
  - `pitch` (int): The pitch of the pixel data.
- **Description**: Constructs a new `surface` object with the specified dimensions, pixel format, and initial pixel data.

### `surface(const string&in filename)`
- **Parameters**:
  - `filename` (const string&): The path to the image file.
- **Description**: Constructs a new `surface` object by loading an image from a file.

## Methods

### `void set_colorspace(int colorspace) const property`
- **Parameters**:
  - `colorspace` (int): The new color space.
- **Description**: Sets the color space for the surface using a property.

### `int get_colorspace() const property`
- **Return Type**: int
- **Description**: Returns the current color space as a property.

### `bool add_alternate_image(surface@ s)`
- **Parameters**:
  - `s` (surface@): The alternate image to add.
- **Return Type**: bool
- **Description**: Adds an alternate image to the surface and returns `true` if successful; otherwise, returns `false`.

### `bool has_alternate_images()`
- **Return Type**: bool
- **Description**: Checks if the surface has any alternate images and returns `true` if it does; otherwise, returns `false`.

### `void remove_alternate_images()`
- **Description**: Removes all alternate images from the surface.

### `bool lock()`
- **Return Type**: bool
- **Description**: Locks the surface for pixel manipulation. Returns `true` if successful; otherwise, returns `false`.

### `void unlock()`
- **Description**: Unlocks the surface after pixel manipulation is complete.

### `bool save_to_file(const string&in filename)`
- **Parameters**:
  - `filename` (const string&): The path to save the image file.
- **Return Type**: bool
- **Description**: Saves the current state of the surface to an image file and returns `true` if successful; otherwise, returns `false`.

### `void set_rle(bool rle) const property`
- **Parameters**:
  - `rle` (bool): The new RLE (Run-Length Encoding) setting.
- **Description**: Enables or disables RLE for the surface using a property.

### `bool get_rle() const property`
- **Return Type**: bool
- **Description**: Returns whether RLE is enabled as a property.

### `bool set_color_key(bool enabled, uint key)`
- **Parameters**:
  - `enabled` (bool): Whether to enable color keying.
  - `key` (uint): The color key value.
- **Return Type**: bool
- **Description**: Sets the color key for transparency and returns `true` if successful; otherwise, returns `false`.

### `bool has_color_key()`
- **Return Type**: bool
- **Description**: Checks if color keying is enabled and returns `true` if it is; otherwise, returns `false`.

### `bool set_color_mod(uint8 r, uint8 g, uint8 b)`
- **Parameters**:
  - `r` (uint8): The red component of the color modification.
  - `g` (uint8): The green component of the color modification.
  - `b` (uint8): The blue component of the color modification.
- **Return Type**: bool
- **Description**: Modifies the color by multiplying each channel with the given factors and returns `true` if successful; otherwise, returns `false`.

### `bool get_color_mod(uint8&out r, uint8&out g, uint8&out b)`
- **Parameters**:
  - `r` (uint8&out): Output parameter for the red component of the color modification.
  - `g` (uint8&out): Output parameter for the green component of the color modification.
  - `b` (uint8&out): Output parameter for the blue component of the color modification.
- **Return Type**: bool
- **Description**: Retrieves the current color modification factors and stores them in the output parameters.

### `void set_alpha_mod(uint8 alpha) const property`
- **Parameters**:
  - `alpha` (uint8): The new alpha modulation value.
- **Description**: Sets the alpha modulation for transparency using a property.

### `uint8 get_alpha_mod() const property`
- **Return Type**: uint8
- **Description**: Returns the current alpha modulation value as a property.

### `void set_blend_mode(blendmode mode) const property`
- **Parameters**:
  - `mode` (blendmode): The new blend mode.
- **Description**: Sets the blending mode for rendering operations using a property.

### `blendmode get_blend_mode() const property`
- **Return Type**: blendmode
- **Description**: Returns the current blend mode as a property.

### `void set_clip_rect(rect@ r) const property`
- **Parameters**:
  - `r` (rect@): The new clipping rectangle.
- **Description**: Sets the clipping rectangle for rendering operations using a property.

### `rect@ get_clip_rect() const property`
- **Return Type**: rect@
- **Description**: Returns the current clipping rectangle as a property.

### `bool flip(flipmode flip)`
- **Parameters**:
  - `flip` (flipmode): The flip mode.
- **Return Type**: bool
- **Description**: Flips the surface in the specified direction and returns `true` if successful; otherwise, returns `false`.

### `bool clear(float r, float g, float b, float a)`
- **Parameters**:
  - `r` (float): The red component of the background color.
  - `g` (float): The green component of the background color.
  - `b` (float): The blue component of the background color.
  - `a` (float): The alpha component of the background color.
- **Return Type**: bool
- **Description**: Clears the surface to a solid color and returns `true` if successful; otherwise, returns `false`.

### `bool fill_rect(rect@ r, uint color)`
- **Parameters**:
  - `r` (rect@): The rectangle to fill.
  - `color` (uint): The color to use for filling the rectangle.
- **Return Type**: bool
- **Description**: Fills a rectangle with the specified color and returns `true` if successful; otherwise, returns `false`.

### `bool blit(rect@ srcrect, surface@ dst, rect@ dstrect)`
- **Parameters**:
  - `srcrect` (rect@): The source rectangle in the source surface.
  - `dst` (surface@): The destination surface.
  - `dstrect` (rect@): The destination rectangle on the destination surface.
- **Return Type**: bool
- **Description**: Blits a portion of the source surface to the destination surface and returns `true` if successful; otherwise, returns `false`.

### `bool blit(rect@ srcrect, surface@ dst, rect@ dstrect, scalemode scale_mode)`
- **Parameters**:
  - `srcrect` (rect@): The source rectangle in the source surface.
  - `dst` (surface@): The destination surface.
  - `dstrect` (rect@): The destination rectangle on the destination surface.
  - `scale_mode` (scalemode): The scaling mode.
- **Return Type**: bool
- **Description**: Blits a portion of the source surface to the destination surface with scaling and returns `true` if successful; otherwise, returns `false`.

### `bool blit(rect@ srcrect, int left_width, int right_width, int top_height, int bottom_height, float scale, scalemode scale_mode, surface@ dst, rect@ dstrect)`
- **Parameters**:
  - `srcrect` (rect@): The source rectangle in the source surface.
  - `left_width` (int): The left width for tiling.
  - `right_width` (int): The right width for tiling.
  - `top_height` (int): The top height for tiling.
  - `bottom_height` (int): The bottom height for tiling.
  - `scale` (float): The scaling factor.
  - `scale_mode` (scalemode): The scaling mode.
  - `dst` (surface@): The destination surface.
  - `dstrect` (rect@): The destination rectangle on the destination surface.
- **Return Type**: bool
- **Description**: Blits a portion of the source surface to the destination surface with custom tiling and scaling and returns `true` if successful; otherwise, returns `false`.

### `bool blit_unchecked(rect@ srcrect, surface@ dst, rect@ dstrect)`
- **Parameters**:
  - `srcrect` (rect@): The source rectangle in the source surface.
  - `dst` (surface@): The destination surface.
  - `dstrect` (rect@): The destination rectangle on the destination surface.
- **Return Type**: bool
- **Description**: Blits a portion of the source surface to the destination surface without bounds checking and returns `true` if successful; otherwise, returns `false`.

### `bool blit_unchecked(rect@ srcrect, surface@ dst, rect@ dstrect, scalemode scale_mode)`
- **Parameters**:
  - `srcrect` (rect@): The source rectangle in the source surface.
  - `dst` (surface@): The destination surface.
  - `dstrect` (rect@): The destination rectangle on the destination surface.
  - `scale_mode` (scalemode): The scaling mode.
- **Return Type**: bool
- **Description**: Blits a portion of the source surface to the destination surface without bounds checking and with scaling and returns `true` if successful; otherwise, returns `false`.

### `bool blit_tiled(rect@ srcrect, surface@ dst, rect@ dstrect)`
- **Parameters**:
  - `srcrect` (rect@): The source rectangle in the source surface.
  - `dst` (surface@): The destination surface.
  - `dstrect` (rect@): The destination rectangle on the destination surface.
- **Return Type**: bool
- **Description**: Blits a portion of the source surface to the destination surface in a tiled pattern and returns `true` if successful; otherwise, returns `false`.

### `bool blit_tiled(rect@ srcrect, float scale, scalemode scale_mode, surface@ dst, rect@ dstrect)`
- **Parameters**:
  - `srcrect` (rect@): The source rectangle in the source surface.
  - `scale` (float): The scaling factor.
  - `scale_mode` (scalemode): The scaling mode.
  - `dst` (surface@): The destination surface.
  - `dstrect` (rect@): The destination rectangle on the destination surface.
- **Return Type**: bool
- **Description**: Blits a portion of the source surface to the destination surface in a tiled pattern with scaling and returns `true` if successful; otherwise, returns `false`.

### `uint map(uint8 r, uint8 g, uint8 b)`
- **Parameters**:
  - `r` (uint8): The red component.
  - `g` (uint8): The green component.
  - `b` (uint8): The blue component.
- **Return Type**: uint
- **Description**: Maps RGB values to a single color value based on the surface's pixel format.

### `uint map(uint8 r, uint8 g, uint8 b, uint8 a)`
- **Parameters**:
  - `r` (uint8): The red component.
  - `g` (uint8): The green component.
  - `b` (uint8): The blue component.
  - `a` (uint8): The alpha component.
- **Return Type**: uint
- **Description**: Maps RGBA values to a single color value based on the surface's pixel format.

### `bool read_pixel(int x, int y, uint8&out r, uint8&out g, uint8&out b, uint8&out a)`
- **Parameters**:
  - `x` (int): The x-coordinate of the pixel.
  - `y` (int): The y-coordinate of the pixel.
  - `r` (uint8&out): Output parameter for the red component.
  - `g` (uint8&out): Output parameter for the green component.
  - `b` (uint8&out): Output parameter for the blue component.
  - `a` (uint8&out): Output parameter for the alpha component.
- **Return Type**: bool
- **Description**: Reads a pixel at the specified coordinates and stores its color values in the output parameters.

### `bool read_pixel(int x, int y, float&out r, float&out g, float&out b, float&out a)`
- **Parameters**:
  - `x` (int): The x-coordinate of the pixel.
  - `y` (int): The y-coordinate of the pixel.
  - `r` (float&out): Output parameter for the red component.
  - `g` (float&out): Output parameter for the green component.
  - `b` (float&out): Output parameter for the blue component.
  - `a` (float&out): Output parameter for the alpha component.
- **Return Type**: bool
- **Description**: Reads a pixel at the specified coordinates and stores its color values as floating-point in the output parameters.

### `bool write_pixel(int x, int y, uint8 r, uint8 g, uint8 b, uint8 a)`
- **Parameters**:
  - `x` (int): The x-coordinate of the pixel.
  - `y` (int): The y-coordinate of the pixel.
  - `r` (uint8): The red component.
  - `g` (uint8): The green component.
  - `b` (uint8): The blue component.
  - `a` (uint8): The alpha component.
- **Return Type**: bool
- **Description**: Writes a pixel at the specified coordinates with the given color values and returns `true` if successful; otherwise, returns `false`.

### `bool write_pixel(int x, int y, float r, float g, float b, float a)`
- **Parameters**:
  - `x` (int): The x-coordinate of the pixel.
  - `y` (int): The y-coordinate of the pixel.
  - `r` (float): The red component.
  - `g` (float): The green component.
  - `b` (float): The blue component.
  - `a` (float): The alpha component.
- **Return Type**: bool
- **Description**: Writes a pixel at the specified coordinates with the given floating-point color values and returns `true` if successful; otherwise, returns `false`.
