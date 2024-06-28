# functions

show_window


This function displays the main window of your game on the user's screen.


# void show_window(string title, int width, int height, bool closable)


## Parameters

variable| description
---|---
title | The title of the window.
width | the width of the window.
height | the height, of the window.
closable | toggle whether pressing alt+f4 should close. true is default

## Return value

none

## Remarks

Until this function is called your game window will be invisible, thus not allowing the user to set focus to it. This in turn means that you will not be able to accept keyboard input before you call this function, and so you will usually want to do this at the very beginning of your script.




It is never legal to call this function more than once during the course of your game's execution, doing so may result more than 1 windows appearrence. If you want to change the title of the window, use `set_game_window_title` method instead.

## Example

```
// Display the window and wait for the user to close it.
void main()
{
show_window("ngt test window",400,600);
while(true)
{
delay(5);
update_game_window();
}
}
```
