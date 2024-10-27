# Properties

## Syntax
```angelscript
const int EVENT_NONE;
const int EVENT_CONNECT;
const int EVENT_RECEIVE;
const int EVENT_DISCONNECT;
const bool SCRIPT_COMPILED;
```

## Property Details

### EVENT_NONE
- **Type**: `int`
- **Description**: A constant indicating that no network event has occurred.

### EVENT_CONNECT
- **Type**: `int`
- **Description**: A constant indicating that a connection event has occurred, such as establishing a network connection or connecting to a server.

### EVENT_RECEIVE
- **Type**: `int`
- **Description**: A constant indicating that data has been received. This could be used in network systems where data is being processed upon arrival.

### EVENT_DISCONNECT
- **Type**: `int`
- **Description**: A constant indicating that a disconnection event has occurred, such as losing a network connection or disconnecting from a server.

### SCRIPT_COMPILED
- **Type**: `bool`
- **Description**: A boolean value indicating whether a script has been compiled into release executable or running from source.
