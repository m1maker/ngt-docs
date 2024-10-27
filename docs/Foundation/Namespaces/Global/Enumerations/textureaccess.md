# textureaccess Enum

## Overview
The `textureaccess` enum defines the access mode for a texture, which determines how it can be used and modified in an application. The different access modes affect memory usage and performance, so choosing the right one is important.

## Syntax
```angelscript
enum textureaccess {
    TEXTUREACCESS_STATIC,
    TEXTUREACCESS_STREAMING,
    TEXTUREACCESS_TARGET
};
```

## Enum Values
- **TEXTUREACCESS_STATIC (0)**: The texture is created once and does not change after that. This mode uses the least amount of memory but offers the best performance.
- **TEXTUREACCESS_STREAMING (1)**: The texture can be modified frequently, such as updating it in real-time or streaming video data into it. This mode requires more memory than `TEXTUREACCESS_STATIC` but allows for dynamic updates.
- **TEXTUREACCESS_TARGET (2)**: The texture is used as a render target, meaning it will be drawn to by other textures or rendering operations. This mode typically uses the most memory and has the highest performance impact.
