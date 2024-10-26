# Class: network

The `network` class provides a data structure for managing and controlling network communications in NGT. It allows you to set up both client and server, handle peer connections, send packets, manage bandwidth, and monitor network events.

## Constructors

### `network()`
- **Description**: Constructs an empty `network` object ready to be configured and used for networking.

## Methods

### `uint64 connect(string&in host, int port)`
- **Parameters**:
  - `host` (string&): The hostname or IP address of the server to connect to.
  - `port` (int): The port number on which the server is listening.
- **Return Type**: uint64
- **Description**: Connects to a network server and returns a unique peer ID for this connection.

### `bool destroy()`
- **Return Type**: bool
- **Description**: Closes all connections and destroys the network object, freeing up resources.

### `bool disconnect_peer(uint64 peer_id)`
- **Parameters**:
  - `peer_id` (uint64): The unique identifier of the peer to disconnect.
- **Return Type**: bool
- **Description**: Disconnects a peer gracefully and returns `true` if successful; otherwise, returns `false`.

### `bool disconnect_peer_forcefully(uint64 peer_id)`
- **Parameters**:
  - `peer_id` (uint64): The unique identifier of the peer to disconnect forcefully.
- **Return Type**: bool
- **Description**: Disconnects a peer forcefully and returns `true` if successful; otherwise, returns `false`.

### `string get_peer_address(uint64 peer_id) const property`
- **Parameters**:
  - `peer_id` (uint64): The unique identifier of the peer.
- **Return Type**: string
- **Description**: Returns the address of a connected peer as a property.

### `double get_peer_average_round_trip_time(uint64 peer_id) const property`
- **Parameters**:
  - `peer_id` (uint64): The unique identifier of the peer.
- **Return Type**: double
- **Description**: Returns the average round-trip time with a specific peer as a property.

### `array<uint64>@ get_peer_list()`
- **Return Type**: array<uint64>
- **Description**: Retrieves an array containing the unique identifiers of all connected peers.

### `network_event@ request(int timeout = 0)`
- **Parameters**:
  - `timeout` (int): Optional timeout for waiting for a network event.
- **Return Type**: network_event@
- **Description**: Waits for and returns a network event or times out if specified, with an optional timeout.

### `bool send_reliable(uint64 peer_id, string&in packet, int channel)`
- **Parameters**:
  - `peer_id` (uint64): The unique identifier of the destination peer.
  - `packet` (string&): The data to be sent.
  - `channel` (int): The communication channel for sending the packet.
- **Return Type**: bool
- **Description**: Sends a reliable packet to a specific peer and returns `true` if successful; otherwise, returns `false`.

### `bool send_unreliable(uint64 peer_id, string&in packet, int channel)`
- **Parameters**:
  - `peer_id` (uint64): The unique identifier of the destination peer.
  - `packet` (string&): The data to be sent.
  - `channel` (int): The communication channel for sending the packet.
- **Return Type**: bool
- **Description**: Sends an unreliable packet to a specific peer and returns `true` if successful; otherwise, returns `false`.

### `bool set_bandwidth_limits(double incomingBandwidth, double outgoingBandwidth)`
- **Parameters**:
  - `incomingBandwidth` (double): The maximum incoming bandwidth in bytes per second.
  - `outgoingBandwidth` (double): The maximum outgoing bandwidth in bytes per second.
- **Return Type**: bool
- **Description**: Sets the bandwidth limits for incoming and outgoing traffic and returns `true` if successful; otherwise, returns `false`.

### `bool setup_client(int channels, int64 max_peers)`
- **Parameters**:
  - `channels` (int): The number of communication channels to use.
  - `max_peers` (int64): The maximum number of peers that can connect.
- **Return Type**: bool
- **Description**: Configures the network for client mode and returns `true` if successful; otherwise, returns `false`.

### `bool setup_server(int port, int channels, int64 max_peers)`
- **Parameters**:
  - `port` (int): The port number on which to listen.
  - `channels` (int): The number of communication channels to use.
  - `max_peers` (int64): The maximum number of peers that can connect.
- **Return Type**: bool
- **Description**: Configures the network for server mode and returns `true` if successful; otherwise, returns `false`.

### `void flush() const`
- **Description**: Flushes any pending outgoing packets from all channels.

### `int64 get_connected_peers() const property`
- **Return Type**: int64
- **Description**: Returns the number of currently connected peers as a property.

### `double get_bytes_sent() const property`
- **Return Type**: double
- **Description**: Returns the total number of bytes sent through the network as a property.

### `double get_bytes_received() const property`
- **Return Type**: double
- **Description**: Returns the total number of bytes received through the network as a property.
