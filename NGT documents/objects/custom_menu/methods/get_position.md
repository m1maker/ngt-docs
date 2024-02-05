# custom_menu

custom_menu object

  


This function returns the current position of the focus.

# double get_position()

## Parameters

None

## Return Value

The current position that is being focused.

## Remarks

This function returns the current position of the focus. It is thus useful to know the current position in which the focus is.

## Example


```
// Make a simple menu.
#include "custom_menu.ngt"
void main()
{
show_game_window("menu test");
custom_menu c;
double currentPosition = c.get_position();
// Use the currentPosition as needed.
}

```
