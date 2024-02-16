# audio_form


this function returns the string with the asked input. you don't need to be declared, as it uses the already declared object named `form`. note, this is not function in `form` object inside.

# string input(string title,string text,string dt,string pm,int ml,bool r,bool m,string button1, string button2,bool button1auto,bool button2auto)

## parameters
variable | description
---|---
title | the title of the form.
text | the text of the input field.
dt | the default text that should be inserted. leave it empty If you don't want to insert any.
pm | an optional parameter to set the password mask, such as bullet, hidden, star and so on.
ml | the maximum length that the text can be typed. default is 0, meaning unlimited.
r | an optional bool parameter to toggle the read only mode. default is false.
m | an optional parameter to toggle the use of multiline. default is false.
button1 | the text for the ok button. default is ok.
button2 | the text for the cancel button. default is &cancel, meaning the cancel button can be activated by pressing alt+c key.
button1auto | toggle whether the ok button has the ability to be activated automatically If the shortcut key was pressed (If any). default is false.
button2auto | toggle whether the cancel button has the ability to be activated automatically If the shortcut key was pressed (If any). default is false.

## return value

a string with the input data.

## remarks

this function returns the string with the asked input. you don't need to be declared, as it uses the already declared object named `form`

## example
```
#include"form.ngt"
void main()
{
alert("ok",input("name","type your name, maximum 30","","",30,false,false)); //also multiline is off.
}
```