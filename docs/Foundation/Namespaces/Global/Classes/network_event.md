# Class: network_event

The `network_event` class provides a data structure for representing events related to networking in NGT. It includes properties for the type of event, peer ID, channel, and any associated message.

## Constructors

### `network_event()`
- **Description**: Constructs an empty `network_event` object with default values.

## Methods

### `network_event& opAssign(const network_event&in)`
- **Parameters**:
  - `other` (const network_event&): The other `network_event` object to assign.
- **Return Type**: network_event&
- **Description**: Assigns the contents of another `network_event` object to this one and returns a reference to this object.

## Properties

### `type`
- **Type**: const int
- **Description**: A property representing the type of network event (e.g., connection, disconnection, message).

### `peer_id`
- **Type**: const uint64
- **Description**: A property representing the unique identifier of the peer involved in the event.

### `channel`
- **Type**: const int
- **Description**: A property representing the channel number associated with the event (if applicable).

### `message`
- **Type**: const string
- **Description**: A property representing any message or data associated with the network event.
