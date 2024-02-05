# functions

string_to_number

  


This method returns the number out of a string.

# double string_to_number(string text, uint&out; byte)

## Parameters

Variable| Description  
---|---  
text | The text that is to be converted.  
byte | An optional variable to place how many numbers have been converted. This variable will be set to, not read from.  
  
## Return Value

The converted numbers on success, 0 otherwise.

## Remarks

This method converts a given text to the numbers. It is useful to get only numbers from an input string.

## Example
    
    
    void main()
    {
    string a = "200";
    string b = "599.23";
    uint ab, bb;
    int a1 = string_to_number(a, ab);
    double b1 = string_to_number(b, bb);
    alert("numbers", "The first string was converted to " + a1 + ", and the length is " + ab + ". Second variable was converted to " + b1 + ", and length is " + bb);
    }
    
