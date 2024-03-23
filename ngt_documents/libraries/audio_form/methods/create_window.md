# audio_form

audio_form object

This method will create a window and activate the form.

# void create_window(string window_title, bool change_screen_title, bool say_dialog)

## Parameters

variable | description
---|---
window_title | The title of the window.
change_screen_title | An optional parameter determining whether the title should be changed on screen. If it is, the onscreen window will be created/changed to that name.
say_dialog | An optional parameter determining whether the speech source should say the word "dialog" after the window title.

## Return value

none.

## Remarks

As all operations are performed instantaneously, the window must be created first before any controls can be created or used.

An audio_form object can hold up to 300 controls by default, but changing is not generally recommended.

## Example

```
// Make a simple form.

#include "form.ngt"
void main()
{
form.create_window("Example Form");
int ok=form.create_button("OK", true, false);
int cancel=form.create_button("Cancel", false, true);
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