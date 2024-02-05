# functions

alert

  


This function displays a message box on the user's screen with a title and text.  


# bool alert(string title, string text, string button_text)

## Parameters

||| variable| description  
---|---  
title | The title of the window.  
text | The text that is to be shown.  
button_text | the text of the button. default is ok  
  
## Return value

true on success, false on failure.

## Remarks

This function is useful for displaying information to the user such as error messages and other important alerts. The script execution will pause until the user clicks on the OK button.

## Example


```
void main()
{
alert("Information", "This is an alert box");
}

```
