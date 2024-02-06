# functions

floor




This function returns the largest integral value that is not greater than x.

# double floor(double x)

## Parameters

Variable| Description
---|---
x | The number to round.

## Return Value

The largest integral value not greater than x.

## Remarks

This function will always decrease x, except where x is already an integer. For example, the floor of 9.2 will be 9, but the floor of -11.6 will be -12.

## Example

```
void main()
{
double a = floor(8);
double b = floor(9.2);
double c = floor(-11.6);
alert("ok", a + ", " + b + ", " + c);
}
```
