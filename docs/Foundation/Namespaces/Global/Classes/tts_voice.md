# Class: tts_voice

The `tts_voice` class provides a data structure for managing text-to-speech (TTS) functionality in NGT. It allows you to perform various TTS operations such as speaking text, retrieving voice options, and setting properties like rate and volume.

## Constructors

### `tts_voice()`
- **Description**: Constructs an empty `tts_voice` object ready for TTS operations.

## Methods

### `void speak(const string&in text) const`
- **Parameters**:
  - `text` (const string&): The text to be spoken.
- **Description**: Speaks the specified text asynchronously.

### `void speak_wait(const string&in text) const`
- **Parameters**:
  - `text` (const string&): The text to be spoken.
- **Description**: Speaks the specified text and waits for it to complete before returning.

### `void speak_interrupt(const string&in text) const`
- **Parameters**:
  - `text` (const string&): The text to be spoken.
- **Description**: Interrupts any ongoing TTS operation and starts speaking the new text asynchronously.

### `void speak_interrupt_wait(const string&in text) const`
- **Parameters**:
  - `text` (const string&): The text to be spoken.
- **Description**: Interrupts any ongoing TTS operation, speaks the new text, and waits for it to complete before returning.

### `string speak_to_memory(const string&in text, uint64&out buffer_size, int&out channels, int&out sample_rate, int&out bits_per_sample) const`
- **Parameters**:
  - `text` (const string&): The text to be spoken.
  - `buffer_size` (uint64&out): Output parameter for the size of the audio buffer.
  - `channels` (int&out): Output parameter for number of audio channels.
  - `sample_rate` (int&out): Output parameter for sample rate in Hz.
  - `bits_per_sample` (int&out): Output parameter for bits per sample (24 or 32).
- **Return Type**: string
- **Description**: Speaks the specified text and returns the generated audio data in memory, along with its size.

### `int get_rate() const property`
- **Return Type**: int
- **Description**: Returns the current speaking rate (speed) as a property.

### `void set_rate(int) property`
- **Parameters**:
  - `rate` (int): The new speaking rate.
- **Description**: Sets the speaking rate for TTS operations using a property.

### `int get_volume() const property`
- **Return Type**: int
- **Description**: Returns the current volume level as a property.

### `void set_volume(int) property`
- **Parameters**:
  - `volume` (int): The new volume level.
- **Description**: Sets the volume level for TTS operations using a property.

### `void set_voice(uint64) property`
- **Parameters**:
  - `voice_id` (uint64): The ID of the voice to use.
- **Description**: Sets the voice used for TTS operations using a property.

### `array<string>@ get_voice_names() const property`
- **Return Type**: array<string>
- **Description**: Returns an array containing the names of available voices as a property.
