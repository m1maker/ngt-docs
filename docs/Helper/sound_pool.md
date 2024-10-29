## sound_pool_item Class

### Properties

- **upper_range**: float (Read/Write) - The upper range of the sound's spatial audio.
- **lower_range**: float (Read/Write) - The lower range of the sound's spatial audio.
- **left_range**: float (Read/Write) - The left range of the sound's spatial audio.
- **right_range**: float (Read/Write) - The right range of the sound's spatial audio.
- **backward_range**: float (Read/Write) - The backward range of the sound's spatial audio.
- **forward_range**: float (Read/Write) - The forward range of the sound's spatial audio.
- **rotation**: float (Read/Write) - The rotation of the sound source.
- **effects**: array<effect @> (Read/Write) - An array of effects attached to the sound instance.
- **sound_instance**: sound @ (Read/Write) - The internal sound instance.

### Methods

- **reset()**:
  - Resets the properties of the `sound_pool_item` and cleans up any associated resources.

- **update_listener_position(float listener_x, float listener_y, float listener_z, float rotation)**:
  - Updates the position and orientation of the listener relative to the sound source.
  - Adjusts the sound's position based on listener bounds and rotates the sound accordingly.

- **update_position(float x, float y, float z)**:
  - Updates the position of the sound source in space.

- **get_total_distance(float listener_x, float listener_y, float listener_z)**:
  - Calculates the total distance between the listener and the sound source.

- **play(bool loop = false)**:
  - Plays the sound.
  - Returns true if the sound is playing; otherwise, returns false.

- **attach_effect(effect @e)**:
  - Attaches an effect to the sound instance.
  - Returns the index of the attached effect or -1 if the effect is null.

- **detach_effect(int index)**:
  - Detaches an effect from the sound instance based on its index.

## sound_pool Class

### Properties

- **max_distance**: int (Read/Write) - The maximum distance for sound playback.
- **pool**: array<sound_pool_item @> (Read/Write) - An array of `sound_pool_item` instances.
- **max_sounds**: int (Read/Write) - The maximum number of sounds that can be managed.
- **effects**: array<effect @> (Read/Write) - An array of effects attached to all sound items.
- **use_hrtf**: bool (Read/Write) - Indicates whether HRTF (Head Related Transfer Function) is enabled for spatial audio.
- **in_window**: bool (Read/Write) - Indicates whether the application is in a windowed mode.
- **muted**: bool (Read/Write) - Indicates whether the sound pool is currently muted.

### Methods

- **set_maximum_sounds(int max)**:
  - Sets the maximum number of sounds that can be managed.

- **get_maximum_sounds()**:
  - Returns the current maximum number of sounds.

- **add_effect(effect @e)**:
  - Adds an effect to all sound items.
  - Returns the index of the added effect or -1 if the effect is null.

- **remove_effect(int index)**:
  - Removes an effect from all sound items based on its index.

- **set_hrtf(bool enable)**:
  - Enables or disables HRTF for all sound items.

- **get_hrtf()**:
  - Returns the current state of HRTF.

- **play_stationary(const string& in filename, bool looping, bool memory = false, bool persistent = false)**:
  - Plays a stationary sound with optional parameters.
  - Returns an index or -1 on failure.

- **play_stationary(const string& in filename, bool looping, float offset, float start_pan, float start_volume, float start_pitch, bool memory = false, bool persistent = false)**:
  - Plays a stationary sound with additional parameters.
  - Returns an index or -1 on failure.

- **play_1d(const string& in filename, float listener_x, float sound_x, bool looping, bool memory = false, bool persistent = false)**:
  - Plays a sound at a specific position relative to the listener.
  - Returns an index or -1 on failure.

- **play_1d(const string& in filename, float listener_x, float sound_x, float left_range, float right_range, bool looping, float offset, float start_pan, float start_volume, float start_pitch, bool memory = false, bool persistent = false)**:
  - Plays a sound at a specific position with additional parameters.
  - Returns an index or -1 on failure.

- **play_2d(const string& in filename, float listener_x, float listener_y, float sound_x, float sound_y, bool looping, bool memory = false, bool persistent = false)**:
  - Plays a sound in a 2D environment.
  - Returns an index or -1 on failure.

- **play_2d(const string& in filename, float listener_x, float listener_y, float sound_x, float sound_y, float left_range, float right_range, float backward_range, float forward_range, bool looping, float offset, float start_pan, float start_volume, float start_pitch, bool memory = false, bool persistent = false)**:
  - Plays a sound in a 2D environment with additional parameters.
  - Returns an index or -1 on failure.

- **play_3d(const string& in filename, float listener_x, float listener_y, float listener_z, float sound_x, float sound_y, float sound_z, float rotation, bool looping, bool memory = false, bool persistent = false)**:
  - Plays a sound in a 3D environment.
  - Returns an index or -1 on failure.

- **play_3d(vector @listener, vector @source, float rotation, bool looping, bool memory = false, bool persistent = false)**:
  - Plays a sound in a 3D environment with vector parameters.
  - Returns an index or -1 on failure.

- **play_3d(const string&in filename, vector @listener, vector @source, float rotation = 0, float left_range = 0, float right_range = 0, float backward_range = 0, float forward_range = 0, float upper_range = 0, float lower_range = 0, bool looping = false, float offset = 0, float start_pan = 0, float start_volume = 0, float start_pitch = 0, bool memory = false, bool persistent = false)**:
  - Plays a sound in a 3D environment with detailed parameters.
  - Returns an index or -1 on failure.

- **play_3d(const string&in filename, float listener_x = 0, float listener_y = 0, float listener_z = 0, float sound_x = 0, float sound_y = 0, float sound_z = 0, float rotation = 0, float left_range = 0, float right_range = 0, float backward_range = 0, float forward_range = 0, float upper_range = 0, float lower_range = 0, bool looping = false, float offset = 0, float start_pan = 0, float start_volume = 0, float start_pitch = 0, bool memory = false, bool persistent = false)**:
  - Plays a sound in a 3D environment with all parameters.
  - Returns an index or -1 on failure.

- **update_listener_position(float listener_x, float listener_y, float listener_z, float rotation = 0)**:
  - Updates the listener's position and orientation.
  - Pauses and resumes sounds based on window active state.

- **pause_all()**:
  - Pauses all currently playing sounds.

- **resume_all()**:
  - Resumes all paused sounds.

- **sound_active(int slot)**:
  - Checks if a sound is active at the specified slot.
  - Returns true if active, false otherwise.

- **sound_is_playing(int slot)**:
  - Checks if a sound is playing at the specified slot.
  - Returns true if playing, false otherwise.

- **pause_sound(int slot)**:
  - Pauses the sound at the specified slot.
  - Returns true on success, false otherwise.

- **destroy_all()**:
  - Resets all sound items and frees resources.

- **resume_sound(int slot)**:
  - Resumes the sound at the specified slot.
  - Returns true on success, false otherwise.

- **update_sound_position(int slot, float x = 0, float y = 0, float z = 0)**:
  - Updates the position of a sound at the specified slot.
  - Returns true on success, false otherwise.

- **update_sound_start_values(int slot, float start_pan, float start_volume, float start_pitch)**:
  - Updates the initial properties of a sound at the specified slot.
  - Returns true on success, false otherwise.

- **destroy_sound(int slot)**:
  - Resets and destroys the sound at the specified slot.
  - Returns true on success, false otherwise.

- **update_sound_range(int slot, float left_range = 0, float right_range = 0, float backward_range = 0, float forward_range = 0, float upper_range = 0, float lower_range = 0)**:
  - Updates the spatial range of a sound at the specified slot.
  - Returns true on success, false otherwise.

- **get_free_sound_id()**:
  - Finds a free slot for playing a new sound.
  - Returns the index of the free slot or -1 if none available.

- **fade(double time = 0.25, double targetVol = 0, bool destroy = false, sound_pool_fade_callback @cb = null, bool fadeIn = false)**:
  - Fades in or out all sounds over a specified time period.
  - Calls an optional callback function during the fade process.

## audio_source Class

### Properties

- **minimum_x**: float (Read/Write) - The minimum x-coordinate of the sound's spatial range.
- **maximum_x**: float (Read/Write) - The maximum x-coordinate of the sound's spatial range.
- **minimum_y**: float (Read/Write) - The minimum y-coordinate of the sound's spatial range.
- **maximum_y**: float (Read/Write) - The maximum y-coordinate of the sound's spatial range.
- **minimum_z**: float (Read/Write) - The minimum z-coordinate of the sound's spatial range.
- **maximum_z**: float (Read/Write) - The maximum z-coordinate of the sound's spatial range.
- **slot**: int (Read/Write) - The slot index in the `sound_pool` for this audio source.
- **file_name**: string (Read/Write) - The filename of the sound.

### Methods

- **reset()**:
  - Resets the audio source properties and stops any playing sounds.

- **update()**:
  - Updates the position and range of the audio source based on the listener's position.
  - Returns true if the update is successful; otherwise, returns false.

- **play()**:
  - Plays the sound at the current position.
  - Returns true if the sound starts playing; otherwise, returns false.

- **stop()**:
  - Stops and destroys the currently playing sound.
  - Returns true on success, false otherwise.
  