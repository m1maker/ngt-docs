# timer

timer object

  


This function forces the time by nano seconds.

# void force_nanos(uint64 nanos)

## Parameters

variable| description  
---|---  
nanos | The nano seconds to set the time.  
  
## Return Value

None

## Remarks

This method forces the time to set to a specified number of nano seconds.

## Example
    
    
    void main()
    {
    timer c;
    c.force_nanos(2000); // Forced the time to 2000 nano seconds. Thus, the timer will move to 2000 nano seconds.
    }
    
