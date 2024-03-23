# audio_form

audio_form object

This method will add or append text to an input box or status bar without interfering with any text that is already present.

# bool add_text(int control_id, string text, int position)

## Parameters

variable | description
---|---
control_id | The control ID of the input box.
text | The text that is to be added.
position | An optional parameter specifying the 0-based position where the new text should be added. A value of -1 will append the text to the end of the original.

## Return value

true on success, false on failure.

## Remarks

None.

## Example

``
// Make a simple form with a few buttons and an input box.

#include "form.ngt"

void main()
{
form.create_window("Example Form", true);
int input=form.create_input_box("test", "Let's add!", "", 0, true, false);
int ok=form.create_button("&Add");
int cancel=form.create_button("E&xit");
while(true)
{
form.monitor();
delay(5);
update_game_window();
if(form.is_pressed(ok))
{
form.add_text(input, " text", 9);
}
if(form.is_pressed(cancel))
{
exit();
}
}
}
```