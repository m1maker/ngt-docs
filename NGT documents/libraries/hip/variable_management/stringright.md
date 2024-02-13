# functions

this method will return from the right side of the string.

# string stringright(string str, uint count)
## parameters
variable | description
---|---
str | the base string to return from.
count | the number of characters to return.

## return value

a string with the data from the very right side of the base string on success, an empty string on failure.

## remarks

this method returns a string from the right side of the base string.

## example

```
#include"hip.ngt"
void main()
{
alert("hello",stringright("hello world",5));
//output should be world.
}
```