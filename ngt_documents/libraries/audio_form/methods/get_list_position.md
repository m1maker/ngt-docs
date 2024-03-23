# audio_form

audio_form object

This method will return the position of the cursor in a listbox.

# int get_list_position(int control_id)

## Parameters

variable | description
---|---
control_id | The control ID of the listbox.

## Return value

The cursor position on success, -1 on failure or if the cursor is not focused on a value.

## Remarks

This is useful for acting based on the item that is currently highlighted on the listbox in question.

Please note that the position does not need to be manually set, since the audio_form class changes the position automatically when different items are selected.

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
int ok=form.create_button("OK");
int cancel=form.create_button("E&xit");
while(true)
{
form.monitor();
delay(5);
update_game_window();
if(form.is_pressed(ok))
{
alert("Information", "The listbox cursor is at position "+form.get_list_position(list));
exit();
}
if(form.is_pressed(cancel))
{
exit();
}
}
}
```