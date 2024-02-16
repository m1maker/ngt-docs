# custom_menu

custom_menu object


This adds the checkbox item to the menu.

# bool add_checkbox(string name, string ref, bool checked)

## Parameters

Variable| Description
---|---
name | The specified item.
ref | The reference name for the item.
checked | an optional parameter, to set the status of the checkbox. default is false, meaning the checkbox will not be checked.

## Return Value

True on success, false on failure.

## Remarks

This function adds the item into the menu. Make sure that the reference names are not the same as each other, as this will make the references unusable. The reference will be returned with the value after the menu is run (e.g., result == "back").

## Example

```
// Make a simple menu.
#include "custom_menu.ngt"
void main()
{
show_game_window("menu test");
custom_menu c;
bool success = c.add_checkbox("item1", "i1",true);
if (success)
{
// Item added successfully.
}
}
```
