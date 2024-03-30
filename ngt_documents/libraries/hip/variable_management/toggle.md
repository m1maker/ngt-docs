# functions

this method will change the value of the value, respectively.

# toggle(value)

## parameters

variable | description
---|---
value | the value you want to change, see remarks.

## return value

the value changed from the default value depending on the type, see remarks.

## remarks

the following types are supported

* int
* bool

## example

```
#include"hip.ngt"
void main()
{
int a=0;
a=toggle(a);
alert("ok","while default is 0, the a variable was changed value to "+a);
}
```