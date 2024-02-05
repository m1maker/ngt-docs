# sound

sound object

  


This method will start the sound playback and wait for it to finish before returning.

# bool play_wait()

## Parameters

None.

## Return value

true on success, false on failure.

## Remarks

This method halts the entire script until the sound has completed playing, regardless of its duration. To perform other actions such as checking for keystrokes while the sound is playing, use the "play" method and the "is_playing" method to detect when the sound has stopped. 

## Example


```
// Load a sound into memory, play it, and close it.
void main()
{
init_engine();
sound test;
test.load("c:\\windows\\media\\ding.wav");
test.play_wait();
test.close();
}

```
