# custom_menu

custom_menu object

The custom menu object is a customizable menu. It can be useful for in your program to display a menu with the available options. There are some required libraries, see remarks.

# custom_menu()

## Parameters

None

## Remarks

Welcome to the custom menu object (a customizable menu). It can be useful for in your program to display a menu with the available options. Everything is made customizable to your every needs.

The custom_menu object requires the following libraries:

1. key_hold.ngt: The keyhold object is used to press keys repeatedly, like walking.



Without the above libraries, the compiler will issue an error, indicating which files are required.

## Example

```
// Make a menu.
#include "custom_menu.ngt"
void main()
{
show_game_window("menu test");
custom_menu c;
c.add("item1", "i1");
c.add("item2", "i2");
c.add("go back", "back");
while (c.is_running())
{
update_game_window();
}
}
```
