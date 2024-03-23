# audio_form

audio_form object

This method will change the text of a given control.

# bool set_text(int control_id, string text)

## Parameters

variable | description
---|---
control_id | The ID of the control which is to receive the new text.
text | The new text for the control.

## Return value

true on success, false on failure.

## Remarks

This method will only function on text fields and status bars.

## Example

```
// Make a simple form with a few buttons and a text field.

#include "form.ngt"
void main()
{
form.create_window("Example Form", true);
int test=form.create_input_box("Test", "", "", 0, false, false);
int ok=form.create_button("OK");
int cancel=form.create_button("E&xit");
while(true)
{
form.monitor();
delay(5);
update_game_window();
if(form.is_pressed(ok))
{
form.set_text(test, "test message");
alert("Information", "The text entered in the text field is "+form.get_text(test));
exit();
}
if(form.is_pressed(cancel))
{
exit();
}
}
}
```