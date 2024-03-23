# audio_form

audio_form object

This method will reset the form and cause it to become inactive.

# void reset()

## Example

```
// Make a simple form.

#include "form.ngt"
void main()
{
form.create_window("Example Form", true);
int ok=form.create_button("OK");
int cancel=form.create_button("Cancel");
while(true)
{
form.monitor();
delay(5);
update_game_window();
if(form.is_pressed(ok))
{
form.reset();
exit();
}
if(form.is_pressed(cancel))
{
exit();
}
}
}
```