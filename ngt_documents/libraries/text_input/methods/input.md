# text_input

text_input object


This method allows you to get the input, allowing the user to type.

# string input(string ttl, string default_text, bool uses_password, string mask_char, int txtlength)

## Parameters

Variable| Description
---|---
ttl | The title of the input.
default_text | The default text to be inserted. You could leave blank for no default text insertion.
uses_password | Toggle whether the input is a secure/password field. False is the default.
mask_char | The character to speak typing passworded text. You can use anything, for instance, star, bullet, hidden, etc. Note this will only be used if uses_password is true.
txtlength | The maximum length that the text can be inserted. Default is 0, meaning unlimited.

## Return Value

A string with the data.

## Remarks

This method will set the canceled property to true if the user presses the escape key.

## Example

```
// Include the text_input
#include "text_input.ngt"

text_input t;

void main()
{
// Ask the user the maximum of 20 characters username.
alert("username", t.input("Type the username", "", false, "", 20));

// Ask the password with hidden, and bullet.
alert("pass1", t.input("Type password", "", true, "hidden"));
alert("pass2", t.input("Type confirm password", "", true, "bullet"));
}
```
