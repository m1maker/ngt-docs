# audio_form

audio_form object

This method will clear a listbox, deleting all items.

# bool clear_list(int control_id)

## Parameters

variable | description
---|---
control_id | The control ID of the listbox.

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
form.add_list_item(list, "mMaker", -1);
form.add_list_item(list, "jon", 0);
form.clear_list(list);
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