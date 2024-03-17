# custom_menu

custom_menu object


This function removes the item through its reference name.

# bool remove(string ref)

## Parameters

Variable| Description
---|---
ref | The name of the reference that you want to be removed.

## Return Value

True on success, false on failure.

## Remarks

This function is useful to remove an item through its reference. If the function fails, the error flag will be set to cme_faildelexist.

## Example

```ngt
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
if(menu.is_clicked("i"))
{
alert("result", menu.get_current_ref());
bool success = menu.remove("i");
if (success)
{
// Item removed successfully.
}
exit();
}
}
}
```
