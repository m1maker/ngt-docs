# user_idle

user_idle object

  


The user_idle object is used to measure elapsed time of the computer inactivity.

# user_idle()

## Parameters

None.

## Remarks

user_idle objects are mostly used inside loops to measure elapsed time of the computer inactivity, for example, to trigger events after a certain amount of time the computer is inactive.

user_idle objects have high precision and do not significantly impact script execution even when used in large quantities.

## Example


```
// Simple, wait for the users to press enter to exit.
void main()
{
alert("Welcome", "On the next screen, you can press enter to exit.");
show_game_window("Test user_idle");
user_idle c;
while (true)
{
update_game_window();
if (key_pressed(SDLK_RETURN))
{
wait(3000);
c.pause();
alert("OK", "The user_idle stopped and indicates that it was elapsed to " + c.elapsed_millis());
break;
}
}
quit();
}

```
