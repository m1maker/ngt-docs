# audio_form


audio_form object

This method will delete an existing item from a listbox.

# bool delete_list_item(int control_id, int list_index, bool reset_cursor=true, bool speak_highlighted_item=true)

## Parameters

variable | description
---|---
control_id | The control ID of the listbox.
list_index | The list index of the item to delete.
reset_cursor | An optional value specifying whether the cursor should be reset so that no item is highlighted. If set to false, the cursor will move to the previous item.
speak_highlighted_item | An optional parameter specifying whether speech should notify about the deleted item and announce the next highlighted item. If set to false, speech will remain silent.

## Return value

true on success, false on failure.

## Example

```
// Make a simple form with a few buttons and a listbox.

#include "form.ngt"
void main()
{
form.create_window("Example Form", true);
int list=form.create_list("&People", 0);
form.add_list_item(list, "ngt", -1);
form.add_list_item(list, "mMaker", -1);
form.delete_list_item(list, 1);
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
}
}
```