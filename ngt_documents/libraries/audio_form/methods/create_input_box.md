# audio_form

audio_form object

This method will create a text field and return a control ID.

## int create_input_box(string caption, string default_text, string password_mask, int max_length, bool read_only, bool multiline)

## Parameters

variable | description
---|---
caption | The title for the text field.
default_text | An optional parameter specifying the default text that is to be shown initially.
password_mask | An optional parameter specifying the character that is to be used to hide the characters of the text (if any). Passing an empty string will cause all characters to be shown.
maximum_length | An optional parameter specifying the maximum length of the text field. A value of 0 means there is no set limit to the number of characters that can be entered.
read_only | An optional parameter indicating whether the text field is to be read only. true means the control is read only, false means the control can be modified.
multiline | An optional parameter indicating whether the control is to be multiline. true means the control is multiline, false means that it can only accept one line.

## Return value

A control ID that can be used to check the status of the control, or -1 on error.

## Remarks

Prepending any letter in the caption string with an ampersand (`&`) sign will cause a shortcut to be created for the text field. For example, &Name will cause alt+n to be the shortcut for the Name field.

## Example

```
// Make a simple form with a few buttons and a text field.

#include "form.ngt"

void main()
{
form.create_window("Example Form", true);
int name=form.create_input_box("&Name");
int password=form.create_input_box("&Password", "", "*");
int message=form.create_input_box("&Message", "This is a read only input box.", "", 0, true);
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