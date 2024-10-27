# transfercharacteristics Enum

## Overview
The `transfercharacteristics` enum defines the transfer function used to map linear optical intensity to digital values in various image and video formats. These functions affect how colors are displayed, especially for high dynamic range (HDR) content.

## Syntax
```angelscript
enum transfercharacteristics {
    TRANSFER_CHARACTERISTICS_UNKNOWN,
    TRANSFER_CHARACTERISTICS_BT709,
    TRANSFER_CHARACTERISTICS_UNSPECIFIED,
    TRANSFER_CHARACTERISTICS_GAMMA22,
    TRANSFER_CHARACTERISTICS_GAMMA28,
    TRANSFER_CHARACTERISTICS_BT601,
    TRANSFER_CHARACTERISTICS_SMPTE240,
    TRANSFER_CHARACTERISTICS_LINEAR,
    TRANSFER_CHARACTERISTICS_LOG100,
    TRANSFER_CHARACTERISTICS_LOG100_SQRT10,
    TRANSFER_CHARACTERISTICS_IEC61966,
    TRANSFER_CHARACTERISTICS_BT1361,
    TRANSFER_CHARACTERISTICS_SRGB,
    TRANSFER_CHARACTERISTICS_BT2020_10BIT,
    TRANSFER_CHARACTERISTICS_BT2020_12BIT,
    TRANSFER_CHARACTERISTICS_PQ,
    TRANSFER_CHARACTERISTICS_SMPTE428,
    TRANSFER_CHARACTERISTICS_HLG,
    TRANSFER_CHARACTERISTICS_CUSTOM
};
```

## Enum Values
- **TRANSFER_CHARACTERISTICS_UNKNOWN (0)**: Represents an unknown or unspecified transfer function.
- **TRANSFER_CHARACTERISTICS_BT709 (1)**: Transfer function used in HDTV, Blu-ray, and many modern displays. Also known as Rec. 709.
- **TRANSFER_CHARACTERISTICS_UNSPECIFIED (2)**: Indicates that the transfer function is not specified in the media data.
- **TRANSFER_CHARACTERISTICS_GAMMA22 (4)**: A common transfer function used for standard video signals. This is often referred to as "gamma correction".
- **TRANSFER_CHARACTERISTICS_GAMMA28 (5)**: Another form of gamma correction with a slightly different exponent.
- **TRANSFER_CHARACTERISTICS_BT601 (6)**: Transfer function used in NTSC, PAL, and SECAM television standards, also known as Rec. 601.
- **TRANSFER_CHARACTERISTICS_SMPTE240 (7)**: Transfer function used in studio lighting and photography.
- **TRANSFER_CHARACTERISTICS_LINEAR (8)**: A linear transfer function where the output is a direct proportion of the input.
- **TRANSFER_CHARACTERISTICS_LOG100 (9)**: A logarithmic transfer function designed for high dynamic range content.
- **TRANSFER_CHARACTERISTICS_LOG100_SQRT10 (10)**: Similar to `TRANSFER_CHARACTERISTICS_LOG100`, but with a different scaling factor.
- **TRANSFER_CHARACTERISTICS_IEC61966 (11)**: Transfer function defined by the International Electrotechnical Commission for wide gamut displays.
- **TRANSFER_CHARACTERISTICS_BT1361 (12)**: Transfer function used in consumer displays and digital cameras.
- **TRANSFER_CHARACTERISTICS_SRGB (13)**: Transfer function associated with the sRGB color space, commonly used on the web and in digital imaging software.
- **TRANSFER_CHARACTERISTICS_BT2020_10BIT (14)**: Transfer function for 10-bit high dynamic range content, defined by BT.2020.
- **TRANSFER_CHARACTERISTICS_BT2020_12BIT (15)**: Transfer function for 12-bit high dynamic range content, defined by BT.2020.
- **TRANSFER_CHARACTERISTICS_PQ (16)**: Perceptual quantization transfer function used in HDR displays and mastering workflows.
- **TRANSFER_CHARACTERISTICS_SMPTE428 (17)**: Transfer function based on SMPTE ST 428, designed for high dynamic range scenes with a larger gamut than Rec. 2020.
- **TRANSFER_CHARACTERISTICS_HLG (18)**: Hybrid Log-Gamma transfer function used in hybrid HDR formats like Dolby Vision and HDR10+.
- **TRANSFER_CHARACTERISTICS_CUSTOM (31)**: Indicates that the transfer function is custom-defined.
