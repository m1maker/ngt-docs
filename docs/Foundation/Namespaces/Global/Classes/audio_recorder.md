# Class: audio_recorder

The `audio_recorder` class provides a data structure for managing and controlling audio recording in NGT. It allows you to start, stop, retrieve recorded audio data, and clear the recorded data.

## Constructors

### `audio_recorder()`
- **Parameters**: None
- **Description**: Constructs an `audio_recorder` object with default settings.


## Methods

### `void start() const`
- **Return Type**: void
- **Description**: Starts recording audio.


### `void stop() const`
- **Return Type**: void
- **Description**: Stops the current audio recording.


### `string get_data(uint64&out size = void) const`
- **Parameters**:
  - `size` (uint64&): Optional parameter to store the size of the recorded data.
- **Return Type**: string
- **Description**: Retrieves the recorded audio data as a PCM raw string. If `size` is provided, it will be set to the size of the returned data.


### `void clear() const`
- **Parameters**: None
- **Return Type**: void
- **Description**: Clears any recorded audio data.
