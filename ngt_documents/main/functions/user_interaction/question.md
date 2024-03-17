# functions

question


This function displays a message box on the user's screen with a title and text, as well as a yes and a no button.


# int question(string title, string text)

## Parameters

variable| description
---|---
title | The title of the window.
text | The text that is to be shown.

## Return value

1 for yes, 2 for no

## Remarks

This function is useful when you want to ask the user a simple question. The script execution will pause until the user clicks on either the yes or the no button.

## Example

```
void main()
{
int a=question("ngt engine","do you enjoy with NGT engine?");
if(a==1)
{
alert("thanks","thanks for using NGT!");
}
else if(a==2)
{
alert("well","If you do not use NGT, you shouldn't even run this");
}
else
{
alert("woops","something happened to cause failure");
}
}
```