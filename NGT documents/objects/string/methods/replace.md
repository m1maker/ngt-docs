# string

string object

  


This method replaces a string with a given text and returns a new string.

# string replace(string from, string to)

## Parameters

variable| description  
---|---  
from | The text that should be replaced.  
to | The text to replace with.  
  
## Return Value

A string with the updated data.

## Remarks

None.

## Example
    
    
    void main()
    {
    string a = "hello dear!";
    string b = a.replace("hello", "welcome");
    alert("final", b); // Output should be "welcome dear!".
    }
    
