# string

string object

  


This method is used to determine whether the given string is uppercase.

# bool is_upper()

## Parameters

None.

## Return Value

True if the string is uppercase, false otherwise.

## Remarks

None.

## Example


```
// Declare a string and check if it is uppercase.
void main()
{
string example = "Good job!";
if (example.is_upper())
{
alert("uppercase", "The string seems to be uppercase");
quit();
}
alert("Information", "The string is not uppercase");
}

```
