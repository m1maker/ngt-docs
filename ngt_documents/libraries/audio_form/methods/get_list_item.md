# audio_form

audio_form object

This method will return the text of a specified list index.

# string get_list_item(int control_id, int list_index)

## Parameters

control_id | The control ID of the listbox.
list_index | The index of the item to retrieve the text for.

## Return value

The text of the item on success, or an empty string on failure.

## Remarks

This method is useful for grabbing the text of the current cursor position (see example).

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
alert("Information", "The name selected is "+form.get_list_item(list, form.get_list_position(list)));
exit();
}
if(form.is_pressed(cancel))
{
exit();
}
}
}
```