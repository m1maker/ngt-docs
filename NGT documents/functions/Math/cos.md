# functions

cos

  


This function returns the cosine of an angle of x radians.

# double cos(double x)

## Parameters

Variable| Description  
---|---  
x | A value representing an angle expressed in radians that will be calculated.  
  
## Return Value

The cosine of x.

## Remarks

None.

## Example
    
    
    void main()
    {
    double param = 60.0;
    double result = cos(param * 3.14159 / 180);
    alert("cos test", "The cos of " + param + " is " + result + ".");
    }
    
