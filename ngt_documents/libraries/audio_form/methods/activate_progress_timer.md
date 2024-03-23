# audio_form

audio_form object




This method will activate the speech timer of a progress bar.

# bool activate_progress_timer(int control_id)

## parameters

variable | description
---|---
control_id | The control ID of the progress bar you wish to activate.

## Return value

true on success, false otherwise.

## Remarks

This function must be called if you intend the speak_interval parameter to be effective. When you are ready to start the operation that requires the use of the progress bar, the timer must be activated and the progress set whenever the need arises.

##Example

```
// Make a simple form with a few buttons and a dummy progress bar.
#include "form.ngt"
int dummy_counter;
void main()
{
dummy_counter=0;
form.create_window("Example Form", true);
int dummy=form.create_progress_bar("&Copying", 5, false);
int ok=form.create_button("OK");
int cancel=form.create_button("E&xit");
form.activate_progress_timer(dummy);
while(true)
{
form.monitor();
delay(5);
update_game_window();
dummy_counter++;
if(dummy_counter>=250)
{
if(form.get_progress(dummy)>=100)
{
form.pause_progress_timer(dummy);
}
else
{
form.set_progress(dummy, form.get_progress(dummy)+1);
}
dummy_counter=0;
}
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