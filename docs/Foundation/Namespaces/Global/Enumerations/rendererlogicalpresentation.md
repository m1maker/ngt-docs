# rendererlogicalpresentation Enum

## Overview
The `rendererlogicalpresentation` enum defines the different logical presentation modes that can be used to control how a renderer scales and presents content. These modes affect how the application's graphics are displayed on the screen, ensuring they fit properly while maintaining performance.

## Syntax
```angelscript
enum rendererlogicalpresentation {
    LOGICAL_PRESENTATION_DISABLED,
    LOGICAL_PRESENTATION_STRETCH,
    LOGICAL_PRESENTATION_LETTERBOX,
    LOGICAL_PRESENTATION_OVERSCAN,
    LOGICAL_PRESENTATION_INTEGER_SCALE
};
```

## Enum Values
- **LOGICAL_PRESENTATION_DISABLED (0)**: Logical presentation is disabled. The renderer will display the content at its native size without any scaling or modification.
- **LOGICAL_PRESENTATION_STRETCH (1)**: The content is stretched to fit the entire screen, potentially distorting it.
- **LOGICAL_PRESENTATION_LETTERBOX (2)**: The content is displayed with letterboxing (black bars on top and bottom), ensuring that the aspect ratio is maintained but some parts of the content may be obscured.
- **LOGICAL_PRESENTATION_OVERSCAN (3)**: The content is displayed with overscan (black bars on sides or top/bottom), ensuring that no part of the content is obscured, but it may not fit perfectly on all devices.
- **LOGICAL_PRESENTATION_INTEGER_SCALE (4)**: The content is scaled up or down by integer factors to maintain sharpness and avoid blurriness.
