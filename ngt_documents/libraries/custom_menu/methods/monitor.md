# custom_menu

custom_menu object


This method will monitor the menu for events.

# void monitor()

## Parameters

None

## Return Value

None

## Remarks

This method must be called at regular intervals, as it performs various checks, mainly keyboard activity, to ensure the menu and the focused control work as expected.

## Example

```
// Make a simple menu.
#include "custom_menu.ngt"
custom_menu menu;
void main()
{
menu.create("Example menu", true);
menu.add("item", "i");
while(menu.is_running())
{
menu.monitor();
update_game_window();
if(menu.is_clicked("i"))
{
alert("result", menu.get_current_ref());
exit();
}
}
}
```
