# audio_form

audio_form object

This method will create a listbox and return a control ID.

# int create_list(string caption, int maximum_items, bool multiselect,string listtype, bool ncable, double listfm)

## Parameters

variable | description
---|---
caption | The title for the listbox.
maximum_items | An optional parameter specifying how many items can be in the listbox. A value of 0 means there is no limit to the number of items that can be shown.
multiselect | An optional parameter indicating whether the listbox should have the capability to be able to manage multiple selections.
listtype | an optional parameter to set the out of the list. for instance, you may set this to something like, slider, listbox and so on. default is `list`
ncable | an optional parameter to set whether the list should have multiletter navigation. default is true.
listfm | an option parameter to set how many items should be moved in fast mode, that is, page up and page down. default is 5.

## Return value

A control ID that can be used to check the status of the control, or -1 on error.

## Remarks

Prepending any letter in the caption string with an ampersand (`&`) sign will cause a shortcut to be created for the listbox. For example, &People will cause alt+p to be the shortcut for the list of people.

If the listbox is a multiselect-enabled listbox, each item in the list can be manipulated like a checkbox with the space bar, and Control+A can be used to select the entire list.

## Example

```
// Make a simple form with a few buttons and a listbox.
#include "form.ngt"
void main()
{
form.create_window("Example Form", true);
int list=form.create_list("&People", 0);
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