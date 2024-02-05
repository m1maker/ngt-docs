# functions

clipboard_read_text

  


This function reads text from the clipboard.  


# string clipboard_read_text()

## Parameters

None

## Return value

The text stored in the clipboard on success, or an empty string on failure.

## Remarks

None

## Example


```
void main()
{
clipboard_copy_text("Hello");
alert("Clipboard text", clipboard_read_text());
}

```
