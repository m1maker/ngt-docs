# seek_origin Enum

## Overview
The `seek_origin` enum defines the origin point used in memory_stream object seeking operations. These origins specify where the seek position is relative to when the operation is performed.

## Syntax
```angelscript
enum seek_origin {
    SEEK_ORIGIN_START,
    SEEK_ORIGIN_CURRENT,
    SEEK_ORIGIN_END
};
```

## Enum Values
- **SEEK_ORIGIN_START (0)**: The seek position is relative to the beginning of the stream.
- **SEEK_ORIGIN_CURRENT (1)**: The seek position is relative to the current position in the stream.
- **SEEK_ORIGIN_END (2)**: The seek position is relative to the end of the stream.
