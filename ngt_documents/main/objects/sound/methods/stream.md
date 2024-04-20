# sound

sound object

This method will load a sound as a stream for playback.

# bool stream(string filename, bool set_3d)

## Parameters

Variable | Description
---|---
filename | The file to open.
set_3d | Toggle whether the 3d sound should be used, default is false.

## Return value

true on success, false on failure.

## Remarks

The location in which the engine searches for the file specified in the filename parameter is determined by a call to the "set_sound_storage" function. By default it will look on the users hard drive and in the directory where the program is stored, unless an absolute path is specified such as "C:\\Windows\\media\\ding.wav".

Note that both \ and / can be used to specify paths.

Be careful when creating streaming sounds. A streamed sound will be read from disk while it is playing which means that it does not have to be loaded into memory in its entirety. This in turn means that the engine will constantly have to retrieve new data, so playing many streams at once is not a good idea; especially not if they are in a compressed format which needs to be decoded on the fly. Streames should generally be used for longer sounds such as background music, cut scenes or ambiences.

## Example

```
// Load a sound for streaming, play it and close it.
void main()
{
sound test;
test.stream("c:\\windows\\media\\ding.wav");
test.play_wait();
test.close();
}
```