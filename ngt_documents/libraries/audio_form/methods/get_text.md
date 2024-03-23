# audio_form

audio_form object

This method will return the text of a given control.

# string get_text(int control_id)

## Parameters

variable | description
---|---
control_id | The control ID to retrieve the text from.

## Return value

The text on success, or an empty string on failure.

## Remarks

The text that is retrieved is any additional text of the control, for example that found in text fields or status bars. To retrieve the control's title, use the `get_caption` method.

## Example

```
// Make a simple form with a few buttons and a text field.

#include "form.ngt"
void main()
{
form.create_window("Example Form", true);
int test=form.create_input_box("Test", "this is a test edit field box though!", "", 0, false, false);
int ok=form.create_button("OK");
int cancel=form.create_button("E&xit");
while(true)
{
form.monitor();
delay(5);
update_game_window();
if(form.is_pressed(ok))
{
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