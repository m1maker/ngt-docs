# string

string object

This method is used to determine whether the given string is lowercase.

# bool is_lower()

## Parameters

None.

## Return Value

True if the string is lowercase, false otherwise.

## Remarks

None.

## Example

```
// Declare a string and check if it is lowercase.
void main()
{
string example = "Good job!";
if (example.is_lower())
{
alert("lowercase", "The string seems to be lowercase");
exit();
}
alert("Information", "The string is not lowercase");
}
```
