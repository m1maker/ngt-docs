# string

string object

  


This function returns a new string with the trimmed data.

# string substr(uint start = 0, int count = -1)

## Parameters

||| variable| description  
---|---  
start | The position in which the string should start trim.  
count | This specifies the number of characters to trim. By default, -1 is specified, indicating all characters will be returned from the start position that is specified through the "start" variable.  
  
## Return Value

A string with the data starting from the "start" variable till the "count" variable on success, an empty string on failure.

## Remarks

This function returns a new string with the trimmed data.

## Example


```
// Trims a string to another string.
void main()
{
string first = "hello, world!";
string trim = first.substr(7, 5);
// Here, we use 7 to return "world" and length is 5. The 'w' is starting from 7, not 8, as the start position is 0 based.
alert("final", trim);

// Let's do a more complicated one.
string a = "welcome to New Game Toolkit, and thank you for using the easiest language!";
string what = "New Game Toolkit";
string f = "welcome to ";
string trim2 = a.substr(f.length() - 1, what.length());
// What have we done here? We declared the "a" variable to store the text, "what" variable to the text we wish to be trimmed, and "f" variable to specify the start position. Because we use f.length() - 1 to retrieve the position to start, and what.length() to set how many characters should be trimmed.
alert("final2",trim2);
}

```
