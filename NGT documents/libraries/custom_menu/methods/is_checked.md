# custom_menu

custom_menu object


this method checks whether a given reference is checked

# bool is_checked(string ref)

## Parameters

Variable| Description
---|---
ref | The name of the reference that you want to check.

## Return Value

True on success, false on failure.

## Remarks

This function is useful to check whether the given reference is checked. If the function fails, the error flag will be set to cme_invalid_type.

## Example

```
// Make a simple menu.
#include "custom_menu.ngt"

custom_menu menu;

void main()
{
menu.create("Example menu", true);
menu.add_checkbox("item", "i", true);
while(true)
{
menu.monitor();
update_game_window();
if(menu.is_clicked("i"))
{
alert("result", menu.get_current_ref());
bool success = menu.is_checked("i");
if (success)
{
// Item is checked.
}
exit();
}
}
}
```
