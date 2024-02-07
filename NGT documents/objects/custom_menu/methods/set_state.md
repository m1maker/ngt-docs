# custom_menu

custom_menu object




this method sets the states of the menu item.

# bool set_state(string ref, bool clickable)

## Parameters

Variable| Description
---|---
ref | The reference name for the item.
clickable | toggle whether the item is clickable.

## Return Value

True on success, false on failure.

## Remarks

this method sets the states of the menu item. Make sure that the reference name is exist.

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
bool ksuc=c.set_state("i1",false);
if(ksuc) //the clickable is false.
}
```