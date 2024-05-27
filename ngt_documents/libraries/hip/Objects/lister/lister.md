# lister

lister object

The lister object allows you to join any array in a given seperater, and returns as a string.

# lister()

## Remarks

There is 1 main function, `convert`, which converts an array into string.

## Example

```
#include"hip.ngt"
void main()
{
string[] names={"Jaims","Sophia","Jack","Rose"};
lister l;
alert("Information",l.convert(names));
}
```