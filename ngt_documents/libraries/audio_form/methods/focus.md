# audio_form

audio_form object

This method will focus a specified control.

# bool focus(int control_id)

## Parameters

variable | description
---|---
control_id | The ID of the control you wish to focus.

## Return value

true on success, false otherwise.

## Remarks

None.

## Example

```
// Make a simple form with a few buttons.
#include "form.ngt"
void main()
{
form.create_window("Example Form", true);
int ok=form.create_button("OK");
int cancel=form.create_button("E&xit");
form.focus(ok);
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