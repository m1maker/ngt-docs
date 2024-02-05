# timer

timer object

  


This function forces the time by microseconds.

# void force_micros(uint64 micros)

## Parameters

variable| description  
---|---  
micros | The microseconds to set the time.  
  
## Return Value

None

## Remarks

This method forces the time to set to a specified number of microseconds.

## Example
    
    
    void main()
    {
    timer c;
    c.force_micros(2000); // Forced the time to 2000 microseconds. Thus, the timer will move to 2000 microseconds.
    }
    
