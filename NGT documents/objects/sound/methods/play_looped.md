# sound

sound object

  


This method will start the sound playback and set it to loop forever.

# bool play_looped()

## Parameters

None.

## Return value

true on success, false on failure.

## Remarks

This method initiates the playback of the sound in a looped state, continuously repeating until explicitly paused, stopped, or until the sound object is destroyed. 

## Example


```
// Play a sound and loop it until the user presses space.
void main()
{
init_engine();
sound ambience;
ambience.load("ding.ogg");
show_game_window("Sound Test");
if(!ambience.is_active())
{
alert("Error", "The sound could not be loaded.");
quit();
}
ambience.play_looped();
while(key_pressed(SDLK_SPACE) == false)
{
update_game_window();
}
}

```
