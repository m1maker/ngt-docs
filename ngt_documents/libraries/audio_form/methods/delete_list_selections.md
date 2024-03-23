# audio_form

audio_form object

This method will delete all the selected items from a listbox.

# bool delete_list_selections(int control_id, bool reset_cursor=true, bool speak_deletion_status=true)

## Parameters

variable | description
---|---
control_id | The control ID of the listbox.
reset_cursor | An optional value specifying whether the cursor should be reset so that it is not highlighting an item. If set to false, the cursor will either stay put, or move to the next available item.
speak_deletion_status | An optional parameter specifying whether speech should notify about the deleted items and announce the next highlighted item. If set to false, speech will remain silent.

## Return value

true on success, false on failure.

## Remarks

If more than one item is selected in the listbox, the speech will only state the number of items deleted, as opposed to the text of the item that is announced if only one item is deleted.

If this method is called on a listbox that is not set to accept multiple selections, the currently highlighted item will be deleted only.

## Example

```
// Make a simple form with a few buttons and a listbox.

#include "form.ngt"
void main()
{
form.create_window("Example Form", true);
int list=form.create_list("&People", 0, true);
form.add_list_item(list, "ngt", -1);
form.add_list_item(list, "mMaker", -1);
form.add_list_item(list, "jon", 1);
int delete=form.create_button("Delete");
int cancel=form.create_button("E&xit");
while(true)
{
form.monitor();
delay(5);
update_game_window();
if(form.is_pressed(delete))
{
form.delete_list_selections(list);
exit();
}
if(form.is_pressed(cancel))
{
exit();
}
}
}
```