# functions

set_game_window_title




This function changes the title of the window.


# void set_game_window_title(string new_title)

## Parameters

variable| description
---|---
new_title | The new title that should be changed.

## Return value

None

## Remarks

This function changes the title of the current window, overwriting whatever the window title is.

## Example

```
// Show a window, wait for three seconds, then another window, then wait three seconds, then quit.
void main()
{
show_game_window("first window");
wait(3000);
set_game_window_title("second window");
wait(3000);
quit();
}
```
