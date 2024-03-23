# audio_form

audio_form object




This method will add an item to a listbox.

# bool add_list_item(int control_id, string option, int position, bool selected,string lref)

## Parameters

variable | description
---|---
control_id | The control ID of the listbox.
option | The text of the item that is to be added.
position | An optional parameter specifying the 0-based position of the item. A value of -1 will append the item to the end of the list.
selected | An optional parameter indicating whether the item should be selected as part of a multiselect listbox.
lref | an optional parameter to set the list item reference. If empty is past, the item name is used.

## Return value

true on success, false on failure.

## Remarks

If a new item is to take the place of an old item, the old item, along with the rest of the list, will be moved to make room for the new item. No existing items will be overwritten under any circumstances. If the maximum limit of a list has been reached, an error will be flagged and the method will return false.

On a listbox that does not have multiselection capabilities, the selected flag is ignored.

## Example

```
// Make a simple form with a few buttons and a listbox.

#include "form.ngt"

void main()
{
form.create_window("Example Form", true);
int list=form.create_list("&People", 0);
form.add_list_item(list, "ngt", -1);
form.add_list_item(list, "harry", -1);
form.add_list_item(list, "mMaker", -1);
int ok=form.create_button("OK");
int cancel=form.create_button("E&xit");
while(true)
{
form.monitor();
delay(5);
update_game_window();
if(form.is_pressed(ok))
{
exit();
}
if(form.is_pressed(cancel))
{
exit();
}
if((key_down(SDLK_ALT))&&(key_pressed(SDLK_F4)))
{
exit();
}
}
}
```