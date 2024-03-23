# audio_form

audio_form object

This method returns a value indicating whether the specified control is checked.

# bool is_checked(int control_id)

## Parameters

variable | description
---|---
control_id | The ID of the control you wish to check.

## Return value

true if the control is checked, false if the control is unchecked or if an error occurred.

## Remarks

This method will only function on checkboxes.

## Example

```
// Make a simple form with a few buttons and a checkbox.

#include "form.ngt"
void main()
{
form.create_window("Example Form", true);
int check=form.create_checkbox("use audioform", false, false);
int ok=form.create_button("OK");
int cancel=form.create_button("E&xit");
while(true)
{
form.monitor();
delay(5);
update_game_window();
if(form.is_pressed(ok))
{
if(form.is_checked(check))
{
alert("Information", "The checkbox is checked.");
}
else
{
alert("Information", "The checkbox is unchecked.");
}
exit();
}
if(form.is_pressed(cancel))
{
exit();
}
}
}
```