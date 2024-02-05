# string

string object

  


This method is used to determine whether the given string is empty. That is to say, contains no characters.

# bool is_empty()

## Parameters

None.

## Return Value

True if the string is empty, false otherwise.

## Remarks

None.

## Example


```
// Declare a string and check if it is empty.
void main()
{
string example = "good job!";
if (example.is_empty())
{
alert("empty", "The string seems to be empty");
quit();
}
alert("Information", "The string is nicely full of data.");
}

```
