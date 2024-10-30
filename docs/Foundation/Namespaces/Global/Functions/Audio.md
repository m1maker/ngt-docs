## Audio

### `void set_audio_period_size(uint) property`
- **Parameters**:
  - The size of the audio period in milliseconds.
- **Description**: Sets the audio period size for sound playback.

### `void set_sound_storage(const string&in folder_name) property`
- **Parameters**:
  - `folder_name` (const string&): The path to the folder where sound files are stored.
- **Description**: Sets the folder where sound files are stored.

### `string get_sound_storage() property`
- **Return Type**: string
- **Description**: Retrieves the current sound storage folder as a property.

### `void set_sound_pack(pack@ pack_handle) property`
- **Parameters**:
  - `pack_handle` (pack@): The handle to the sound pack.
- **Description**: Sets the active sound pack.

### `pack@ get_sound_pack() property`
- **Return Type**: pack@
- **Description**: Retrieves the current active sound pack as a property.

### `void set_master_volume(float volume) property`
- **Parameters**:
  - `volume` (float): The master volume level (-100 to 0).
- **Description**: Sets the master volume level for all sound output.

### `float get_master_volume() property`
- **Return Type**: float
- **Description**: Retrieves the current master volume level as a property.

### `void mixer_start()`
- **Description**: Starts the audio device.

### `void mixer_stop()`
- **Description**: Stops the audio device.

### `bool mixer_play_sound(const string&in sound_path)`
- **Parameters**:
  - `sound_path` (const string&): The path to the sound file to play.
- **Return Type**: bool
- **Description**: Plays a sound file and returns `true` if successful; otherwise, returns `false`.

### `void mixer_reinit(int channels = 2, int sample_rate = 44100)`
- **Parameters**:
  - `channels` (int): The number of audio channels (default is 2).
  - `sample_rate` (int): The audio sample rate in Hz (default is 44100).
- **Description**: Reinitializes the audio mixer with specified parameters.

### `array<string>@ get_output_audio_devices()`
- **Return Type**: array<string>
- **Description**: Retrieves an array of available output audio device names as a property.

### `bool set_output_audio_device(uint index)`
- **Parameters**:
  - `index` (uint): The index of the audio device to set.
- **Return Type**: bool
- **Description**: Sets the active audio output device and returns `true` if successful; otherwise, returns `false`.

### `void set_sound_global_hrtf(bool) property`
- **Parameters**:
  - `enable` (bool): Whether to enable HRTF (Head-Related Transfer Function).
- **Description**: Enables or disables HRTF for sound output.

### `bool get_sound_global_hrtf() property`
- **Return Type**: bool
- **Description**: Retrieves whether HRTF is enabled as a property.

### `void set_spatial_blend_max_distance(float distance) property`
- **Parameters**:
  - `distance` (float): The maximum distance at which spatial blending is applied.
- **Description**: Sets the maximum distance up to which spatial audio blending occurs as a property.

### `float get_spatial_blend_max_distance()`
- **Return Type**: float
- **Description**: Retrieves the current maximum distance at which spatial audio blending is applied as a property.
