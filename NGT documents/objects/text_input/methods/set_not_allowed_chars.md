# text_input

text_input object

  


This method sets the characters that should not be allowed to type.

# bool set_not_allowed_chars(string ch, string des)

## Parameters

Variable| Description  
---|---  
ch | One or more characters.  
des | The description for the tooltip.  
  
## Return Value

True on success, false on failure.

## Remarks

none

## Example
    
    
    // Include the text_input
    #include "text_input.ngt"
    
    text_input t;
    
    void main()
    {
    // Set not allowed characters and description.
    bool success = t.set_not_allowed_chars("0123456789", "Numbers not allowed");
    
    if (success)
    {
    // Not allowed characters set successfully.
    }
    }
    
