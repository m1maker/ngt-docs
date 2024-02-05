# user_idle

user_idle object

  


This function returns the number of hours that the user_idle has elapsed.

# uint64 elapsed_hours()

## Parameters

None.

## Return Value

The number of hours that the user_idle has elapsed.

## Remarks

This function is widely used to retrieve the elapsed time in hours from the user_idle object.

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
c.pause();
alert("OK", "The user_idle stopped and indicates that it was elapsed to " + c.elapsed_hours());
break;
}
}
quit();
}

```
