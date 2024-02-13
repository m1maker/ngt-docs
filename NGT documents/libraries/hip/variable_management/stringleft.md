# functions

this method will return from the left side of the string.

# string stringleft(string str, uint count)
## parameters
variable | description
---|---
str | the base string to return from.
count | the number of characters to return.

## return value

a string with the data from the very left side of the base string on success, an empty string on failure.

## remarks

this method returns a string from the left side of the base string.

## example

```
#include"hip.ngt"
void main()
{
alert("hello",stringleft("hello world",5));
//output should be hello.
}
```