# functions

delay




This function pauses script execution for a specified time, as detailed in the remarks.


# void delay(int ms)

## Parameters

variable| description
---|---
ms | The number of milliseconds to pause before the next action is executed.

## Return value

None.

## Remarks

This function will delay the execution by a given number of milliseconds before the next action. Unlike the wait method, which completely pauses the script execution, the delay method only pauses for a specified duration before proceeding to the next action.

## Example

```
// This example shows the wait and delay methods.
int delayer = 5;
sound beep;
sound dswicher;
void main()
{
beep.load("C:/windows/media/Windows Ding.wav");
dswicher.load("C:/windows/media/Windows Navigation Start.wav");
show_game_window("Test");
wait(500);
speak("Waiting example. Waiting 3 seconds.");
wait(3000);
speak("Start delaying", false);
speak("Press F1 or F2 key to control delay. Press Tab key to play sound");
while (key_down(SDLK_ESCAPE) == false)
{
update_game_window();
delay(delayer);
if (delayer < 6) delayer = 5;
if (key_repeat(SDLK_F1))
{
dswicher.play();
delayer--;
speak("Delay set to " + delayer);
}
if (key_repeat(SDLK_F2))
{
dswicher.play();
delayer++;
speak("Delay set to " + delayer);
}
if (key_down(SDLK_TAB)) beep.play();
}
beep.close();
exit();
}
```
