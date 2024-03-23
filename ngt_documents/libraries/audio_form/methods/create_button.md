# audio_form

audio_form object

This method will create a push button and return a control ID.

# int create_button(string caption, bool primary, bool cancel, bool overwrite)

## Parameters

variable | description
---|---
caption | The text for the push button.
primary | An optional parameter which specifies whether this button should be the default on the form.
cancel | An optional parameter which specifies whether this button is the cancel button on the form.
overwrite | An optional parameter indicating whether certain button attributes should be overwritten (see remarks).

## Return value

A control ID that can be used to check the status of the control, or -1 on error.

## Remarks

Prepending any letter in the caption string with an ampersand (`&`) sign will cause a shortcut to be created for the button. For example, E&xit will cause alt+x to be the shortcut for the exit button.

The primary and cancel parameters specify how the button should be handled in certain situations. A primary or default button specifies that this should be activated if the Return key is pressed on any control other than a button or an editable multiline input box, while a cancel button is activated when the Escape key is pressed. Thus, each of these attributes can only apply to any one button at a time. If you choose to turn one or both of these attributes on, and any other button has these attributes set, you can choose whether they are overwritten or kept in tact. If you decide not to overwrite attributes and it turns out another button does indeed have these attributes set, the new button will still be created, but the attributes that are already set elsewhere will not be applied. Please note that it is possible to have one button with both attributes set.

## Example

```
// Make a simple form with a few buttons.

#include "form.ngt"

void main()
{
form.create_window("Example Form", true);
int ok=form.create_button("OK", true, false);
int cancel=form.create_button("E&xit", false, true);
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