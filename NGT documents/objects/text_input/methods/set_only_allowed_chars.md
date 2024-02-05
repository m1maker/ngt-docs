# text_input

text_input object

  


This method sets the characters that should only be allowed to type.

# bool set_only_allowed_chars(string ch, string des)

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
    // Set only allowed characters and description.
    bool success = t.set_only_allowed_chars("0123456789", "Numbers only allowed");
    
    if (success)
    {
    // only allowed characters set successfully.
    }
    }
    
