# Wave File Utilities for AngelScript

## Introduction

This document provides documentation for a set of utilities in AngelScript designed to handle wave file operations. These utilities include loading and saving entire wave files, reading and writing wave files sample by sample, and managing wave file headers.

## Overview

### Classes

1. **wave_file_data**: A class for handling wave files by loading and saving them in memory.
2. **wave_file_reader**: A class for streaming audio data from disk sample per sample.
3. **wave_file_writer**: A class for streaming audio data to disk sample per sample.
4. **wave_file_header**: A utility class for reading and writing wave file headers.

### Properties

- `length`: Property of `wave_file_data` class representing the length of the audio in samples.
- `channels_count`, `sample_rate`: Properties of `wave_file_reader` and `wave_file_writer` classes representing the number of audio channels and sample rate.

## Detailed Description

### wave_file_data Class

#### Properties

- **interleaved_samples**: An array containing interleaved audio samples.
- **channels_count**: Number of audio channels.
- **sample_rate**: Sample rate of the audio data.

#### Methods

- **load_file(string filePath)**: Loads an entire audio file from disk into `interleaved_samples`.
  - **Parameters**:
    - `filePath`: The path to the wave file.
  - **Returns**: `true` if the file is successfully loaded, `false` otherwise.

- **write_file(string filePath, uint bitDepth = 16)**: Writes audio data from `interleaved_samples` to disk as a wave file.
  - **Parameters**:
    - `filePath`: The path where the wave file will be saved.
    - `bitDepth`: Number of bits per sample (default is 16).
  - **Returns**: `true` if the file is successfully written, `false` otherwise.

### wave_file_reader Class

#### Properties

- **channels_count**: Property representing the number of audio channels.

#### Methods

- **open_file(string filePath, int maxChannelsCount = -1)**: Opens a wave file for reading.
  - **Parameters**:
    - `filePath`: The path to the wave file.
    - `maxChannelsCount`: Maximum number of channels to read (default is -1).
  - **Returns**: `true` if the file is successfully opened, `false` otherwise.

- **read_sample(array<double> oSample)**: Reads a single sample from the current position in the file.
  - **Parameters**:
    - `oSample`: Array to store the read sample data.
  - **Returns**: None.

- **set_pos(uint samplePosition)**: Sets the file cursor to a specific sample position.
  - **Parameters**:
    - `samplePosition`: Position of the sample in the file.
  - **Returns**: `true` if the operation is successful, `false` otherwise.

- **move_pos(int sampleOffset)**: Moves the file cursor by a specified number of samples.
  - **Parameters**:
    - `sampleOffset`: Offset to move the cursor by.
  - **Returns**: `true` if the operation is successful, `false` otherwise.

- **is_end_of_file()**: Checks if the end of the file has been reached.
  - **Returns**: `true` if at the end of the file, `false` otherwise.

- **close()**: Closes the wave file.
  - **Returns**: `true` if the file is successfully closed, `false` otherwise.

### wave_file_writer Class

#### Properties

- **header**: Header data for the wave file being written.

#### Methods

- **open_file(string filePath)**: Opens a wave file for writing and initializes the header.
  - **Parameters**:
    - `filePath`: The path where the wave file will be saved.
  - **Returns**: `true` if the file is successfully opened, `false` otherwise.

- **write_sample(const array<double>& iSample)**: Writes a single sample to the current position in the file.
  - **Parameters**:
    - `iSample`: Array containing the sample data to be written.
  - **Returns**: None.

- **close()**: Closes the wave file and updates the header with the correct size of the audio data.
  - **Returns**: `true` if the file is successfully closed, `false` otherwise.

### wave_file_header Class

#### Properties

- **channels_count**: Number of audio channels.
- **samples_count**: Number of audio samples.
- **sample_rate**: Sample rate of the audio data.
- **bytes_per_sample**: Number of bytes per sample.
- **header_size**: Size of the header in bytes.

#### Methods

- **read(file& f)**: Reads the wave file header from a file at position 0.
  - **Parameters**:
    - `f`: File object to read from.
  - **Returns**: `true` if the header is successfully read, `false` otherwise.

- **write(file& f)**: Writes the wave file header to a file at position 0.
  - **Parameters**:
    - `f`: File object to write to.
  - **Returns**: `true` if the header is successfully written, `false` otherwise.

## Example Usage

### Loading and Saving Wave Files

```angelscript
wave_file_data wf;
if (wf.load_file("path/to/input.wav"))
{
    // Process audio data...
    wf.write_file("path/to/output.wav");
}
```

### Reading and Writing Sample by Sample

```angelscript
wave_file_reader reader;
reader.open_file("path/to/input.wav");
array<double> sample(2); // Assuming stereo (2 channels)
while (!reader.is_end_of_file())
{
    reader.read_sample(sample);
    // Process sample data...
}
```

```angelscript
wave_file_writer writer;
writer.open_file("path/to/output.wav");
writer.header.sample_rate = 44100;
writer.header.channels_count = 2;
writer.header.bytes_per_sample = 2; // 16-bit samples

array<double> sample(2); // Assuming stereo (2 channels)
sample[0] = 0.5; // Left channel
sample[1] = -0.5; // Right channel
for (uint i = 0; i < 44100 * 5; i++) // 5 seconds of audio
{
    writer.write_sample(sample);
}
writer.close();
```
