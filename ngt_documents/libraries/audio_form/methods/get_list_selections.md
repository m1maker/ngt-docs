# audio_form

audio_form object

This method will return a list of the selected item's positions in a listbox.

# int[] get_list_selections(int control_id)

## Parameters

variable | description
---|---
control_id | The control ID of the listbox.

## Return value

An array containing a list of selected items on success, or an empty array on failure.

## Remarks

This is useful for looping through all the selected items and acting based on the results.

If no items are selected, the following rules apply

1. If the cursor is highlighting an item, the method will return the position of the cursor, as the only element in the array. 
2. If the cursor is not highlighting an item, an empty array will be returned. 

If you need to check for the success or failure of this method, it is necessary to check the error flag by using the `get_last_error()` method, since the returned array can be empty in various situations, even when the method has successfully done its work.

Please note that selections are automatically set by the audio_form and do not need to be manually set.

## Example

```
// Make a simple form with a few buttons and a listbox.

#include "form.ngt"
void main()
{
string text="The current highlights are ";
int[] selections;
form.create_window("Example Form", true);
int list=form.create_list("&People", 0, true);
form.add_list_item(list, "jon", -1);
form.add_list_item(list, "lili", -1);
form.add_list_item(list, "jack", 1);
form.add_list_item(list, "rose", -1);
form.add_list_item(list, "smith", 0);
int ok=form.create_button("OK");
int cancel=form.create_button("E&xit");
while(true)
{
form.monitor();
delay(5);
update_game_window();
if(form.is_pressed(ok))
{
selections=form.get_list_selections(list);
for(int counter=0; counter<selections.length(); counter++)
{
text+=selections[counter];
if(counter==(selections.length()-1))
{
text+=".";
}
else
{
text+=", ";
}
}
alert("Information", text);
exit();
}
if(form.is_pressed(cancel))
{
exit();
}
}
}
```