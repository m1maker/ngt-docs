# Class: pcm_ring_buffer

The `pcm_ring_buffer` class provides a data structure for managing and controlling a ring buffer specifically designed to handle PCM (Pulse-Code Modulation) audio data. It allows you to write audio data into the buffer, read audio data from the buffer, reset the buffer, and manage its properties.

## Constructors

### `pcm_ring_buffer(uint channels = 2, uint sample_rate = 44100, uint size = 1024)`
- **Parameters**:
  - `channels` (uint): The number of audio channels. Default is 2.
  - `sample_rate` (uint): The sample rate of the audio data. Default is 44100 Hz.
  - `size` (uint): The size of the ring buffer in bytes. Default is 1024 bytes.
- **Description**: Constructs a `pcm_ring_buffer` object with the specified parameters.


## Methods

### `void write(const string&in data)`
- **Parameters**:
  - `data` (const string&): The PCM audio data to be written into the buffer.
- **Return Type**: void
- **Description**: Writes PCM audio data into the ring buffer.


### `string read(uint64 size)`
- **Parameters**:
  - `size` (uint64): The number of bytes to read from the buffer.
- **Return Type**: string
- **Description**: Reads a specified amount of PCM audio data from the ring buffer and returns it as a string.


### `void reset()`
- **Return Type**: void
- **Description**: Resets the ring buffer, clearing all stored audio data.
