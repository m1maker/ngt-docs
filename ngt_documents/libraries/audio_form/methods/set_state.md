# audio_form

audio_form object

This method will set the enabled and visible states of a control.

# bool set_state(int control_id, bool enabled, bool visible)

## Parameters

variable | description
---|---
control_id | The ID of the control you wish to change.
enabled | A boolean value indicating whether the control should be enabled.
visible | A boolean value indicating whether the control should be visible.

## Return value

true on success, false on failure.

## Remarks

The enabled/disabled flag refers to whether the control may be manipulated in any way. If set to disabled, the audio feedback will announce this and the control is unusable.

The visibility flag refers to whether the control is accessible whilst tabbing through the dialog. If it is set to invisible, the form's cursor will skip the control but the control may still be used and/or modified by the script.

## Example

```
// Make a simple form with a few buttons and a listbox.

#include "form.ngt"

void main()
{
form.create_window("Example Form", true);
int list=form.create_list("&People", 0);
form.add_list_item(list, "jack", -1);
form.add_list_item(list, "rose", -1);
int ok=form.create_button("OK");
form.set_state(ok, false, false);
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