# network_event

network_event object

# Connection properties.

Property | Description | Type
---|---|---
EVENT_NONE | 0, none type. | const int
EVENT_CONNECT | 1, an event is just connected. | const int
EVENT_RECEIVE | 2, the event has received a data. | const int
EVENT_DISCONNECT | 3, an event is just disconnected. | const int

# Other properties.

Property | Description | Type
---|---|---
type | Determines the type of the received data. | const int
peer_id | The peer id of the current connection. | const int
channel | The channel that the data is received from. | const int
message | The message. | const string