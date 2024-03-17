# custom_menu

custom_menu object


this method checks whether a given reference is clicked

# bool is_clicked(string ref)

## Parameters

Variable| Description
---|---
ref | The name of the reference that you want to check.

## Return Value

True on success, false on failure.

## Remarks

This function is useful to check whether the given reference is clicked.

## Example

```
// Make a simple menu.
#include "custom_menu.ngt"

custom_menu menu;

void main()
{
menu.create("Example menu", true);
menu.add_checkbox("item", "i", true);
while(menu.is_running())
{
menu.monitor();
update_game_window();
bool success = menu.is_clicked("i");
if (success)
{
// Item is clicked.
}
exit();
}
}
}
```
