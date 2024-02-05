# functions

clipboard_copy_text

  


This function copies text to the clipboard.  


# bool clipboard_copy_text(string text)

## Parameters

||| variable| description  
---|---  
text | The text that should be copied.  
  
## Return value

true on success, false on failure.

## Remarks

This function will copy the specified text to the Windows clipboard, overwriting whatever is already there.

## Example


```
void main()
{
clipboard_copy_text("Hello");
}

```
