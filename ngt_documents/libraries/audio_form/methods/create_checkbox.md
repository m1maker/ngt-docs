# audio_form

audio_form object

This method will create a checkbox and return a control ID.

# int create_checkbox(string caption, bool initial_value, bool read_only)

## Parameters

variable | description
---|---
caption | The text for the checkbox.
initial_value | An optional parameter specifying the initial value for the checkbox. true is checked, false is unchecked.
read_only | An optional parameter indicating whether the checkbox should be read only. true means the checkbox will be read only, false means it can be modified.

## Return value

A control ID that can be used to check the status of the control, or -1 on error.

## Remarks

Prepending any letter in the caption string with an ampersand (`&`) sign will cause a shortcut to be created for the checkbox. For example, &Subscribe will cause alt+s to be the shortcut for the Subscribe checkbox.

## Example

```
// Make a simple form with a few buttons and a checkbox.

#include "form.ngt"

void main()
{
form.create_window("Example Form", true);
int ag=form.create_checkbox("I &agree to the license agreement", false, false);
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