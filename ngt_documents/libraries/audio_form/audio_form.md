# audio_form

audio_form object


this object allows you to get the same virtual controls as the windows, with multiple advance controls.

# audio_form()

## parameters

none

## remarks

this is the same to the windows virtual controls. this contains such as, lists, sliders, inputs, and buttons.

it can be useful to display your options, with checkbox, list, slider, and input and more.

an audio form object can hold up to 300 controls by default. however, changing it is not generally advised.

## example

```
//note. you can use form as default, since the object global is declared as form If you don't want to declare yourself.
#include"form.ngt"
void main()
{
form.create_window("test form");
int a=form.create_button("&ok;",true,false);
int b=form.create_button("&cancel;",false,true);
while(true)
{
delay(5);
update_game_window();
form.monitor();
if(form.is_pressed(a))
{
alert("ok","you pressed ok");
exit();
}
else if(form.is_pressed(b))
{
alert("final","you pressed cancel, or escape is detected");
exit();
}
}
}
```