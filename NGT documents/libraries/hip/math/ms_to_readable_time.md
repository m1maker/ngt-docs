# functions

this method will return a given milliseconds into human readable format.

# string ms_to_readable_time(double ms)
## parameters
variable | description
---|---
ms | the number of milliseconds.

## return value

a string containing a human readable format.

## remarks

this method will return a given milliseconds into human readable format. it is probably used to display status of the current player's playtime, etc.

## example

```
#include"hip.ngt"
void main()
{
double playtime=120000;
alert("playtime","you've been playing for "+ms_to_readable_time(playtime)); //output should be 2 minutes.
}
```