# functions

input_box

This function promts an input box to the user.

`string input_box(string title, string text, string default_text = "", bool secure = false);`

## Parameters

| Variable| Description |
|---|---|
| title | The title of the window. |
| text | The text of the input field. |
| default_text | An optional parameter to set default text. |
| secure | Toggles whether input is a secure field or not, default is false. |

## Return value

string : The input data.