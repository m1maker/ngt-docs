# Functions

reset_all_forced_keys

This function causes all keys to reset their state of being forced to pass control back to the user.

# bool reset_all_forced_keys()

## Return value

true if the keys' states are reset successfully, false if an error occurs.

## Remarks

Forcing keys is useful for controlling certain aspects of games. For example, if you wanted a game to completely replay itself in the player's style, you might record the code and length of each key pressed in a previous game, and code the replay so that all the keys are forced up or down at the right moments, thereby completely simulating the player's actions.

This function should be called after the use of either the `force_key_down` or `force_key_up` function. To reset the state of any key individually, use the `reset_forced_key` function.

## Example

```
/*
This is a small example that plays the Windows ding every second while the space bar is pressed. If the f key is pressed, the script will force the space key down, thereby triggering the ding to play whether the space bar is physically pressed or not. Pressing the r key will reset the state.
*/

void main()
{
sound ding;
timer time;
ding.load("c:/windows/media/ding.wav");
show_window("Ding Test");
while(true)
{
wait(5);
if((time.elapsed_millis<1000)||(!key_down(SDLK_SPACE)))
{
if(key_pressed(SDLK_ESCAPE))
{
exit();
}
if(key_pressed(SDLK_f))
{
force_key_down(SDLK_SPACE);
}
if(key_pressed(SDLK_r))
{
reset_all_forced_keys();
}
wait(5);
continue;
}
time.restart();
ding.play();
}
}
```