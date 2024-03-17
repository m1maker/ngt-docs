# text_input

text_input object

  


The text input object allows the user to ask to type text.

# text_input()

## Parameters

None

## Remarks

This object allows you to type text on the screen. This is not the main API input, but the external one, meaning we can change the abilities to whatever we want, without having to modify the engine into development.

## Example
    
    
    // Use the text_input object.
    #include "text_input.ngt"
    
    text_input input;
    
    void main()
    {
    alert("final",input.input("type your username"));
    }
    
