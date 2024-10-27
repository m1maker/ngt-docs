# pixelformat Enum

## Overview
The `pixelformat` enum defines various pixel formats that can be used to represent image data. Each format specifies how the pixels are stored and interpreted, which affects performance and compatibility when working with images in applications.

## Syntax
```angelscript
enum pixelformat {
    PIXELFORMAT_UNKNOWN,
    PIXELFORMAT_INDEX1LSB,
    PIXELFORMAT_INDEX1MSB,
    PIXELFORMAT_INDEX2LSB,
    PIXELFORMAT_INDEX2MSB,
    PIXELFORMAT_INDEX4LSB,
    PIXELFORMAT_INDEX4MSB,
    PIXELFORMAT_INDEX8,
    PIXELFORMAT_XRGB4444,
    PIXELFORMAT_XBGR4444,
    PIXELFORMAT_XRGB1555,
    PIXELFORMAT_XBGR1555,
    PIXELFORMAT_ARGB4444,
    PIXELFORMAT_RGBA4444,
    PIXELFORMAT_ABGR4444,
    PIXELFORMAT_BGRA4444,
    PIXELFORMAT_ARGB1555,
    PIXELFORMAT_RGBA5551,
    PIXELFORMAT_ABGR1555,
    PIXELFORMAT_BGRA5551,
    PIXELFORMAT_RGB565,
    PIXELFORMAT_BGR565,
    PIXELFORMAT_RGB24,
    PIXELFORMAT_BGR24,
    PIXELFORMAT_XRGB8888,
    PIXELFORMAT_RGBX8888,
    PIXELFORMAT_XBGR8888,
    PIXELFORMAT_BGRX8888,
    PIXELFORMAT_ARGB8888,
    PIXELFORMAT_RGBA8888,
    PIXELFORMAT_ABGR8888,
    PIXELFORMAT_BGRA8888,
    PIXELFORMAT_XRGB2101010,
    PIXELFORMAT_XBGR2101010,
    PIXELFORMAT_ARGB2101010,
    PIXELFORMAT_ABGR2101010,
    PIXELFORMAT_RGB48,
    PIXELFORMAT_BGR48,
    PIXELFORMAT_RGBA64,
    PIXELFORMAT_ARGB64,
    PIXELFORMAT_BGRA64,
    PIXELFORMAT_ABGR64,
    PIXELFORMAT_RGB48_FLOAT,
    PIXELFORMAT_BGR48_FLOAT,
    PIXELFORMAT_RGBA64_FLOAT,
    PIXELFORMAT_ARGB64_FLOAT,
    PIXELFORMAT_BGRA64_FLOAT,
    PIXELFORMAT_ABGR64_FLOAT,
    PIXELFORMAT_RGB96_FLOAT,
    PIXELFORMAT_BGR96_FLOAT,
    PIXELFORMAT_RGBA128_FLOAT,
    PIXELFORMAT_ARGB128_FLOAT,
    PIXELFORMAT_BGRA128_FLOAT,
    PIXELFORMAT_ABGR128_FLOAT,
    PIXELFORMAT_YV12,
    PIXELFORMAT_IYUV,
    PIXELFORMAT_YUY2,
    PIXELFORMAT_UYVY,
    PIXELFORMAT_YVYU,
    PIXELFORMAT_NV12,
    PIXELFORMAT_NV21,
    PIXELFORMAT_P010,
    PIXELFORMAT_EXTERNAL_OES
};
```

## Enum Values

### Indexed Formats
- **PIXELFORMAT_INDEX1LSB (286261504)**: 1-bit per pixel, using the least significant bit for color. 
- **PIXELFORMAT_INDEX1MSB (287310080)**: 1-bit per pixel, using the most significant bit for color.
- **PIXELFORMAT_INDEX2LSB (470811136)**: 2-bits per pixel, using the least significant bits for color.
- **PIXELFORMAT_INDEX2MSB (471859712)**: 2-bits per pixel, using the most significant bits for color.
- **PIXELFORMAT_INDEX4LSB (303039488)**: 4-bits per pixel, using the least significant bits for color.
- **PIXELFORMAT_INDEX4MSB (304088064)**: 4-bits per pixel, using the most significant bits for color.
- **PIXELFORMAT_INDEX8 (318769153)**: 8-bits per pixel, using all 8 bits for a single color index.

### Packed Formats
- **PIXELFORMAT_XRGB4444 (353504258)**: 16-bit packed format with the most significant bit reserved and the next 4 bits for each of red, green, and blue.
- **PIXELFORMAT_XBGR4444 (357698562)**: 16-bit packed format with the most significant bit reserved and the next 4 bits for each of blue, green, and red.
- **PIXELFORMAT_XRGB1555 (353570562)**: 16-bit packed format with the most significant bit reserved and the next 5 bits each for red, green, and blue, and one bit for alpha.
- **PIXELFORMAT_XBGR1555 (357764866)**: 16-bit packed format with the most significant bit reserved and the next 5 bits each for blue, green, and red, and one bit for alpha.
- **PIXELFORMAT_ARGB4444 (355602434)**: 16-bit packed format with the 4 most significant bits for alpha, followed by 4 bits each for red, green, and blue.
- **PIXELFORMAT_RGBA4444 (356651010)**: 16-bit packed format with the 4 least significant bits for alpha, followed by 4 bits each for red, green, and blue.
- **PIXELFORMAT_ABGR4444 (359796738)**: 16-bit packed format with the 4 most significant bits for alpha, followed by 4 bits each for blue, green, and red.
- **PIXELFORMAT_BGRA4444 (360845314)**: 16-bit packed format with the 4 least significant bits for alpha, followed by 4 bits each for blue, green, and red.
- **PIXELFORMAT_ARGB1555 (355667970)**: 16-bit packed format with the most significant bit reserved and 5 bits for alpha, followed by 5 bits each for red, green, and blue.
- **PIXELFORMAT_RGBA5551 (356782082)**: 16-bit packed format with the least significant bit reserved and 5 bits for red, green, and blue, followed by 1 bit for alpha.
- **PIXELFORMAT_ABGR1555 (359862274)**: 16-bit packed format with the most significant bit reserved and 5 bits for alpha, followed by 5 bits each for blue, green, and red.
- **PIXELFORMAT_BGRA5551 (360976386)**: 16-bit packed format with the least significant bit reserved and 5 bits for red, green, and blue, followed by 1 bit for alpha.
- **PIXELFORMAT_RGB565 (353701890)**: 16-bit packed format with the most significant bit reserved and 5 bits each for red, green, and blue.
- **PIXELFORMAT_BGR565 (357896194)**: 16-bit packed format with the most significant bit reserved and 5 bits each for blue, green, and red.

### Truecolor Formats
- **PIXELFORMAT_RGB24 (386930691)**: 24-bit truecolor format, using all 8 bits per component.
- **PIXELFORMAT_BGR24 (390076419)**: 24-bit truecolor format, using all 8 bits per component but in reverse order.

### 32-Bit Packed Formats
- **PIXELFORMAT_XRGB8888 (370546692)**: 32-bit packed format with the most significant bit reserved and 8 bits each for red, green, and blue.
- **PIXELFORMAT_RGBX8888 (371595268)**: 32-bit packed format with the least significant bit reserved and 8 bits each for red, green, and blue.
- **PIXELFORMAT_XBGR8888 (374740996)**: 32-bit packed format with the most significant bit reserved and 8 bits each for blue, green, and red.
- **PIXELFORMAT_BGRX8888 (375789572)**: 32-bit packed format with the least significant bit reserved and 8 bits each for blue, green, and red.
- **PIXELFORMAT_ARGB8888 (372645892)**: 32-bit packed format with 8 bits for alpha, followed by 8 bits each for red, green, and blue.
- **PIXELFORMAT_RGBA8888 (373694468)**: 32-bit packed format with 8 bits for red, green, and blue, followed by 8 bits for alpha.
- **PIXELFORMAT_ABGR8888 (376840196)**: 32-bit packed format with 8 bits for alpha, followed by 8 bits each for blue, green, and red.
- **PIXELFORMAT_BGRA8888 (377888772)**: 32-bit packed format with 8 bits for red, green, and blue, followed by 8 bits for alpha.

### 10-Bit Packed Formats
- **PIXELFORMAT_XRGB2101010 (370614276)**: 32-bit packed format with the most significant bit reserved, 10 bits each for red, green, and blue.
- **PIXELFORMAT_XBGR2101010 (374808580)**: 32-bit packed format with the most significant bit reserved, 10 bits each for blue, green, and red.
- **PIXELFORMAT_ARGB2101010 (372711428)**: 32-bit packed format with the most significant bit reserved, 10 bits each for red, green, and blue, followed by 2 bits for alpha.
- **PIXELFORMAT_ABGR2101010 (376905732)**: 32-bit packed format with the most significant bit reserved, 10 bits each for blue, green, and red, followed by 2 bits for alpha.

### Floating-Point Formats
- **PIXELFORMAT_RGB48_FLOAT (437268486)**: 48-bit floating-point format with 16 bits for each of red, green, and blue.
- **PIXELFORMAT_BGR48_FLOAT (440414214)**: 48-bit floating-point format with 16 bits for each of blue, green, and red.
- **PIXELFORMAT_RGBA64_FLOAT (438321160)**: 64-bit floating-point format with 16 bits for alpha, followed by 16 bits each for red, green, and blue.
- **PIXELFORMAT_ARGB64_FLOAT (439369736)**: 64-bit floating-point format with 16 bits for red, green, and blue, followed by 16 bits for alpha.
- **PIXELFORMAT_BGRA64_FLOAT (441466888)**: 64-bit floating-point format with 16 bits for red, green, and blue, followed by 16 bits for alpha.
- **PIXELFORMAT_ABGR64_FLOAT (442515464)**: 64-bit floating-point format with 16 bits for alpha, followed by 16 bits each for blue, green, and red.

### 96-Bit Floating-Point Formats
- **PIXELFORMAT_RGB96_FLOAT (454057996)**: 96-bit floating-point format with 32 bits for each of red, green, and blue.
- **PIXELFORMAT_BGR96_FLOAT (457203724)**: 96-bit floating-point format with 32 bits for each of blue, green, and red.

### 128-Bit Floating-Point Formats
- **PIXELFORMAT_RGBA128_FLOAT (455114768)**: 128-bit floating-point format with 32 bits for alpha, followed by 32 bits each for red, green, and blue.
- **PIXELFORMAT_ARGB128_FLOAT (456163344)**: 128-bit floating-point format with 32 bits for red, green, and blue, followed by 32 bits for alpha.
- **PIXELFORMAT_BGRA128_FLOAT (458260496)**: 128-bit floating-point format with 32 bits for red, green, and blue, followed by 32 bits for alpha.
- **PIXELFORMAT_ABGR128_FLOAT (459309072)**: 128-bit floating-point format with 32 bits for alpha, followed by 32 bits each for blue, green, and red.

### YUV Formats
- **PIXELFORMAT_YV12 (842094169)**: Planar YUV format where the Y component is stored first, followed by U and V components.
- **PIXELFORMAT_IYUV (1448433993)**: Planar I420 format with chroma subsampling.
- **PIXELFORMAT_YUY2 (844715353)**: Packed YUV format with interleaved Y, U, and V components.
- **PIXELFORMAT_UYVY (1498831189)**: Packed YUV format with interleaved U, Y, and V components.
- **PIXELFORMAT_YVYU (1431918169)**: Packed YUV format with interleaved Y, V, and U components.

### NV Formats
- **PIXELFORMAT_NV12 (842094158)**: Planar NV12 format where the Y component is stored first, followed by interleaved UV components.
- **PIXELFORMAT_NV21 (825382478)**: Similar to NV12, but with a different arrangement of UV components.

### P010 Formats
- **PIXELFORMAT_P010 (808530000)**: 10-bit packed YUV format where the Y component is stored first, followed by interleaved 10-bit U and V components.

### External OES Format
- **PIXELFORMAT_EXTERNAL_OES (542328143)**: Format used for rendering external surfaces in OpenGL ES.
