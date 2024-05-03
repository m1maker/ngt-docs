# audio_form

audio_form object

This method will setup the form as tab control.

# void setup_tab_page(string title, string label)

## Parameters

variable | description
---|---
title | The title of the tab control.
label | The description for the tab control.

## Remarks

A tab control acts like category in window.

## Example

```
#include "form.ngt"
void main()
{
show_game_window("hello");
form.reset();
form.create_window("test window", false, true);
int c1=form.create_input_box("test input1 outside tab pages");
int c11=form.create_checkbox("test", true);
int c2=form.create_tab_control("options category", "test descryption which I dont know where it used");
audio_form tab1;
tab1.setup_tab_page("jeneral", "jeneral descryption");
int ct1=tab1.create_input_box("user data directory");
int ct2=tab1.create_button("browse");
int ct3=tab1.create_checkbox("i am a good program", false);
audio_form tab2;
tab2.setup_tab_page("connection", "connection descryption");
int ct21=tab2.create_input_box("tab 2 input1");
int ct22=tab2.create_checkbox("checkbox in the tab2", false);
int ct23=tab2.create_slider("volume control", 0, 100);
form.add_tab_page(c2, tab1);
form.add_tab_page(c2, tab2);
int cm1=form.create_button("ok", true);
int cm2=form.create_button("cancel", false, true);
form.focus(c1);
while(true)
{
form.monitor();
delay(5);
update_game_window();
if(form.is_pressed(cm2)) exit();
if(form.is_pressed(cm1))
{
alert("ok",form.get_text(ct1));
alert("ok tab2 box",tab2.get_text(ct21));
exit();
}
}
}
```