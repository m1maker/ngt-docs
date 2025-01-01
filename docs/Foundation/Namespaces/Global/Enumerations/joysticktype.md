# Enum: joysticktype

The `joysticktype` enum defines the different types of joystick devices that can be detected and managed by NGT. Each type represents a specific category of joystick, which affects how the device is handled and interpreted.

## Syntax
```angelscript
enum joysticktype {
    JOYSTICK_TYPE_UNKNOWN,
    JOYSTICK_TYPE_GAMEPAD,
    JOYSTICK_TYPE_WHEEL,
    JOYSTICK_TYPE_ARCADE_STICK,
    JOYSTICK_TYPE_FLIGHT_STICK,
    JOYSTICK_TYPE_DANCE_PAD,
    JOYSTICK_TYPE_GUITAR,
    JOYSTICK_TYPE_DRUM_KIT,
    JOYSTICK_TYPE_ARCADE_PAD,
    JOYSTICK_TYPE_THROTTLE,
    JOYSTICK_TYPE_COUNT
};
```

## Enum Values

- **JOYSTICK_TYPE_UNKNOWN (0)**: Represents an unknown or unspecified type of joystick.
- **JOYSTICK_TYPE_GAMEPAD (1)**: A general-purpose gamepad with buttons and axes, commonly used for gaming.
- **JOYSTICK_TYPE_WHEEL (2)**: A steering wheel device, often used in racing games.
- **JOYSTICK_TYPE_ARCADE_STICK (3)**: An arcade-style joystick, typically with a single axis for movement and buttons for actions.
- **JOYSTICK_TYPE_FLIGHT_STICK (4)**: A flight stick, commonly used in flight simulation games.
- **JOYSTICK_TYPE_DANCE_PAD (5)**: A dance pad, often used in rhythm games.
- **JOYSTICK_TYPE_GUITAR (6)**: A guitar-shaped controller, typically with buttons and axes for strumming and bending notes.
- **JOYSTICK_TYPE_DRUM_KIT (7)**: A drum kit controller, often with pads and cymbals that can be pressed to simulate drum hits.
- **JOYSTICK_TYPE_ARCADE_PAD (8)**: An arcade-style game pad, typically with multiple buttons and axes for various actions.
- **JOYSTICK_TYPE_THROTTLE (9)**: A throttle control, commonly used in racing games to adjust the speed of a vehicle.
- **JOYSTICK_TYPE_COUNT (10)**: The total number of joystick types defined in this enum.
