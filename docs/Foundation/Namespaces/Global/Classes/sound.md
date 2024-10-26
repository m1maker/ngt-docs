# Class: sound

The `sound` class provides a data structure for managing and controlling audio playback in NGT. It allows you to load, play, pause, stop, and manipulate various properties of audio files.

## Constructors

### `sound(const string&in filename = "")`
- **Parameters**:
  - `filename` (const string&): The path to the audio file.
- **Description**: Constructs an `sound` object with the specified audio.


## Methods

### `bool load(const string&in filename) const`
- **Parameters**:
  - `filename` (const string&): The path to the audio file.
- **Return Type**: bool
- **Description**: Loads an audio file and returns `true` if successful; otherwise, returns `false`.

### `bool load_from_memory(string memory, uint64 memory_size = 0) const`
- **Parameters**:
  - `memory` (string): The memory buffer containing the audio data.
  - `memory_size` (uint64): The size of the memory buffer.
- **Return Type**: bool
- **Description**: Loads audio data from memory and returns `true` if successful; otherwise, returns `false`.

### `bool load_pcm(string memory, uint64 memory_size = 0, int channels = 0, int sample_rate = 0) const`
- **Parameters**:
  - `memory` (string): The memory buffer containing the audio data.
  - `memory_size` (uint64): The size of the memory buffer.
  - `channels` (int): The number of audio channels.
  - `sample_rate` (int): The sample rate of the audio.
- **Return Type**: bool
- **Description**: Loads PCM-encoded audio data from memory and returns `true` if successful; otherwise, returns `false`.

### `bool stream(const string&in filename) const`
- **Parameters**:
  - `filename` (const string&): The path to the streaming audio file.
- **Return Type**: bool
- **Description**: Streams an audio file and returns `true` if successful; otherwise, returns `false`.

### `bool load_url(const string&in url) const`
- **Parameters**:
  - `url` (const string&): The URL to the audio file.
- **Return Type**: bool
- **Description**: Loads an audio file from a URL and returns `true` if successful; otherwise, returns `false`.

### `uint64 push_memory() const`
- **Return Type**: uint64
- **Description**: Pushes memory into the sound system and returns a handle for managing that memory.

### `string get_file_path() const property`
- **Return Type**: string
- **Description**: Returns the file path of the currently loaded audio file as a property.

### `void set_fade_time(float volume_beg, float volume_end, float time) const`
- **Parameters**:
  - `volume_beg` (float): The starting volume.
  - `volume_end` (float): The ending volume.
  - `time` (float): The duration of the fade in milliseconds.
- **Description**: Sets the fade-in or fade-out effect for the sound.

### `bool play() const`
- **Return Type**: bool
- **Description**: Plays the sound and returns `true` if successful; otherwise, returns `false`.

### `bool play_looped() const`
- **Return Type**: bool
- **Description**: Starts playing the sound in a loop and returns `true` if successful; otherwise, returns `false`.

### `bool pause() const`
- **Return Type**: bool
- **Description**: Pauses the sound and returns `true` if successful; otherwise, returns `false`.

### `bool play_wait() const`
- **Return Type**: bool
- **Description**: Plays the sound and waits for it to finish before returning `true` if successful; otherwise, returns `false`.

### `bool stop() const`
- **Return Type**: bool
- **Description**: Stops the sound and returns `true` if successful; otherwise, returns `false`.

### `bool close() const`
- **Return Type**: bool
- **Description**: Closes the currently loaded audio file and returns `true` if successful; otherwise, returns `false`.

### `void set_fx(const string&in effect_name) const`
- **Parameters**:
  - `effect_name` (const string&): The name of the effect to apply.
- **Description**: Applies an audio effect to the sound.

### `void delete_fx(const string&in effect_name) const`
- **Parameters**:
  - `effect_name` (const string&): The name of the effect to remove.
- **Description**: Removes an audio effect from the sound.

### `void set_reverb_parameters(float dry, float wet, float room_size, float damping, float mode) const`
- **Parameters**:
  - `dry` (float): The level of direct sound.
  - `wet` (float): The level of reverb sound.
  - `room_size` (float): The size of the simulated room.
  - `damping` (float): The damping factor for reverb.
  - `mode` (float): The mode of reverb.
- **Description**: Sets the parameters for the reverb effect.

### `void set_delay_parameters(float dry, float wet, float decay) const`
- **Parameters**:
  - `dry` (float): The level of direct sound.
  - `wet` (float): The level of delayed sound.
  - `decay` (float): The decay time for the delay effect.
- **Description**: Sets the parameters for the delay effect.

### `void set_position(float listener_x, float listener_y, float listener_z, float source_x, float source_y, float source_z, double theta = 0.0, float pan_step = 5, float volume_step = 0.6, float behind_pitch_decrease = 0.0, float start_pan = 0, float start_volume = 0, float start_pitch = 0) const`
- **Parameters**:
  - `listener_x` (float): The x-coordinate of the listener.
  - `listener_y` (float): The y-coordinate of the listener.
  - `listener_z` (float): The z-coordinate of the listener.
  - `source_x` (float): The x-coordinate of the audio source.
  - `source_y` (float): The y-coordinate of the audio source.
  - `source_z` (float): The z-coordinate of the audio source.
  - `theta` (double): Optional angle for positioning.
  - `pan_step` (float): Optional pan step for spatialization.
  - `volume_step` (float): Optional volume step for spatialization.
  - `behind_pitch_decrease` (float): Optional pitch decrease behind the listener.
  - `start_pan` (float): Optional starting pan value.
  - `start_volume` (float): Optional starting volume value.
  - `start_pitch` (float): Optional starting pitch value.
- **Description**: Sets the spatial position and properties of the audio source.

### `void set_position(const vector@ listener, const vector@ source, double theta = 0.0, float pan_step = 5, float volume_step = 0.6, float behind_pitch_decrease = 0.0, float start_pan = 0, float start_volume = 0, float start_pitch = 0) const`
- **Parameters**:
  - `listener` (vector@): The position of the listener.
  - `source` (vector@): The position of the audio source.
  - `theta` (double): Optional angle for positioning.
  - `pan_step` (float): Optional pan step for spatialization.
  - `volume_step` (float): Optional volume step for spatialization.
  - `behind_pitch_decrease` (float): Optional pitch decrease behind the listener.
  - `start_pan` (float): Optional starting pan value.
  - `start_volume` (float): Optional starting volume value.
  - `start_pitch` (float): Optional starting pitch value.
- **Description**: Sets the spatial position and properties of the audio source using vector objects.

### `void set_hrtf(bool hrtf = true) const property`
- **Parameters**:
  - `hrtf` (bool): The HRTF setting.
- **Description**: Enables or disables Head Related Transfer Function for spatialization.

### `bool get_hrtf() const property`
- **Return Type**: bool
- **Description**: Returns the current state of the HRTF setting as a property.

### `vector@ get_listener_position() const property`
- **Return Type**: vector@
- **Description**: Returns the position of the listener as a property.

### `vector@ get_source_position() const property`
- **Return Type**: vector@
- **Description**: Returns the position of the audio source as a property.

### `bool seek(float pos) const`
- **Parameters**:
  - `pos` (float): The position in milliseconds to seek to.
- **Return Type**: bool
- **Description**: Seeks to a specific position in the audio file and returns `true` if successful; otherwise, returns `false`.

### `bool get_looping() const property`
- **Return Type**: bool
- **Description**: Returns whether the sound is set to loop as a property.

### `void set_looping(bool looping) const property`
- **Parameters**:
  - `looping` (bool): The new looping state.
- **Description**: Sets whether the sound should loop or not using a property.

### `float get_pan() const property`
- **Return Type**: float
- **Description**: Returns the current pan value of the audio source as a property.

### `void set_pan(float pan) const property`
- **Parameters**:
  - `pan` (float): The new pan value.
- **Description**: Sets the pan value of the audio source using a property.

### `float get_volume() const property`
- **Return Type**: float
- **Description**: Returns the current volume level of the sound as a property.

### `void set_volume(float volume) const property`
- **Parameters**:
  - `volume` (float): The new volume level.
- **Description**: Sets the volume level of the sound using a property.

### `float get_pitch() const property`
- **Return Type**: float
- **Description**: Returns the current pitch level of the sound as a property.

### `void set_pitch(float pitch) const property`
- **Parameters**:
  - `pitch` (float): The new pitch level.
- **Description**: Sets the pitch level of the sound using a property.

### `float get_speed() const property`
- **Return Type**: float
- **Description**: Returns the current playback speed of the sound as a property.

### `void set_speed(float speed) const property`
- **Parameters**:
  - `speed` (float): The new playback speed.
- **Description**: Sets the playback speed of the sound using a property.

### `bool get_active() const property`
- **Return Type**: bool
- **Description**: Returns whether the sound is currently active as a property.

### `bool get_playing() const property`
- **Return Type**: bool
- **Description**: Returns whether the sound is currently playing as a property.

### `bool get_paused() const property`
- **Return Type**: bool
- **Description**: Returns whether the sound is currently paused as a property.

### `float get_position() const property`
- **Return Type**: float
- **Description**: Returns the current position in milliseconds of the sound as a property.

### `float get_length() const property`
- **Return Type**: float
- **Description**: Returns the total length of the sound in milliseconds as a property.

### `void set_length(float length = 0.0) const property`
- **Parameters**:
  - `length` (float): The new length of the sound.
- **Description**: Sets the length of the sound using a property.

### `float get_sample_rate() const property`
- **Return Type**: float
- **Description**: Returns the sample rate of the audio file as a property.
