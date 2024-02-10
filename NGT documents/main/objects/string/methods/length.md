# string

string object

  


This method returns the length of the string.

# uint length()

## Parameters

None

## Return Value

The length of the string, or 0 if the string is empty or if an error occurs.

## Remarks

Please note that the value returned is the length of the string rather than the index of the last character in the string. Therefore, when using the length method as a basis for a loop, it is important to check that any counting variable accessing individual characters in the string stops when the counter reaches the length mark, not beyond it. This is because the index is 0 based. In other words, with a string containing 3 entries, you may access elements 0, 1, and 2.

## Example
    
    
    // Declare a string and display its characters.
    void main()
    {
    string hello;
    hello = "Hello";
    alert("String", "The string " + hello + " contains " + hello.length() + " characters.");
    for (int counter = 0; counter < hello.length(); counter++)
    {
    alert("String", "Character " + counter + " is " + hello[counter] + ".");
    }
    }
    
