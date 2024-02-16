# custom_menu

custom_menu object


This adds the item to the menu.

# bool add(string i, string ref)

## Parameters

Variable| Description
---|---
i | The specified item.
ref | The reference name for the item.

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
bool success = c.add("item1", "i1");
if (success)
{
// Item added successfully.
}
}
```
