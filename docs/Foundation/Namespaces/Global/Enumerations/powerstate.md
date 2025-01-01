# Enum: powerstate

The `powerstate` enum defines the different states of a system's power supply, indicating whether it is plugged in, on battery, or charging.

## Syntax
```angelscript
enum powerstate {
    POWER_STATE_ERROR,
    POWER_STATE_UNKNOWN,
    POWER_STATE_ON_BATTERY,
    POWER_STATE_NO_BATTERY,
    POWER_STATE_CHARGING,
    POWER_STATE_CHARGED
};
```

## Enum Values

- **POWER_STATE_ERROR (-1)**: Indicates an error in retrieving the power state.
- **POWER_STATE_UNKNOWN (0)**: Represents an unknown or unspecified power state.
- **POWER_STATE_ON_BATTERY (1)**: The system is running on battery power.
- **POWER_STATE_NO_BATTERY (2)**: The system does not have a battery installed.
- **POWER_STATE_CHARGING (3)**: The system is currently charging its battery.
- **POWER_STATE_CHARGED (4)**: The battery is fully charged.
