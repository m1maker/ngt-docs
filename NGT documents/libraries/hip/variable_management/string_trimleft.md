# functions

this method will trim the left side of the string.

# string string_trimleft(string str, uint count)
## parameters
variable | description
---|---
str | the base string to return from.
count | the number of characters to trim.

## return value

a string with the data trimmed from the very left side of the base string on success, an empty string on failure.

## remarks

this method returns a trimmed string from the left side of the base string.

## example

```
#include"hip.ngt"
void main()
{
alert("hello",string_trimleft("hello world",6));
//output should be world.
}
```