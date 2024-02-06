# functions

tan




This function returns the tangent of an angle of x radians.

# double tan(double x)

## Parameters

Variable| Description
---|---
x | A value representing an angle expressed in radians that will be calculated.

## Return Value

The tangent of x.

## Remarks

None.

## Example

```
void main()
{
double param = 45.0;
double result = tan(param * 3.14159 / 180);
alert("tan test", "The tan of " + param + " is " + result + ".");
}
```
