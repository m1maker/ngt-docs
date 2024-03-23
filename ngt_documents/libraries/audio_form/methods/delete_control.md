# audio_form

audio_form object

This method will delete a specified control.

# bool delete_control(int control_id)

## Parameters

variable | description
---|---
control_id | The ID of the control you wish to delete.

## Return value

true on success, false otherwise.

## Remarks

none.

## Example

```
// Make a simple form with a few buttons. The delete button will delete the OK button.

#include "form.ngt"

void main()
{
form.create_window("Example Form", true);
int delete=form.create_button("&Delete Control");
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
if(form.is_pressed(delete))
{
form.delete_control(ok);
}
if((key_down(SDLK_ALT))&&(key_pressed(SDLK_F4)))
{
exit();
}
}
}
```