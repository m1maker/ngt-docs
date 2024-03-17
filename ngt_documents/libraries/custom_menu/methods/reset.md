# custom_menu

custom_menu object


This function resets the menu data.

# void reset(bool completely)

## Parameters

Variable| Description
---|---
completely | Toggle whether the function should reset all values completely. Default: false.

## Return Value

None

## Remarks

The function resets the value depending on the bool value set.

## Example

```
// Make a simple menu.
#include "custom_menu.ngt"

custom_menu menu;

void main()
{
menu.create("Example menu", true);
menu.add("item", "i");
while(true)
{
menu.monitor();
update_game_window();
if(key_pressed(SDLK_RETURN))
{
alert("result", menu.get_current_ref());
menu.reset(true); // Reset all values completely
exit();
}
}
}
```
