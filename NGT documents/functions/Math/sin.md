# functions

sin

  


This function returns the sine of an angle of x radians.

# double sin(double x)

## Parameters

Variable| Description  
---|---  
x | A value representing an angle expressed in radians that will be calculated.  
  
## Return Value

The sine of x.

## Remarks

None.

## Example
    
    
    void main()
    {
    double param = 30.0;
    double result = sin(param * 3.14159 / 180);
    alert("sin test", "The sin of " + param + " is " + result + ".");
    }
    
