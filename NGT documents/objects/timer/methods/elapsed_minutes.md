# timer

timer object

  


This function returns the number of minutes that the timer has elapsed.

# uint64 elapsed_minutes()

## Parameters

None.

## Return Value

The number of minutes that the timer has elapsed.

## Remarks

This function is widely used to retrieve the elapsed time in minutes from the timer object.

## Example


```
// Simple, wait for the users to press enter to exit.
void main()
{
alert("Welcome", "On the next screen, you can press enter to exit.");
show_game_window("Test Timer");
timer c;
while (true)
{
update_game_window();
if (key_pressed(SDLK_RETURN))
{
c.pause();
alert("OK", "The timer stopped and indicates that it was elapsed to " + c.elapsed_minutes());
break;
}
}
quit();
}

```
