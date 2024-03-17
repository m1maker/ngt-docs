# timer

timer object

  


This function forces the time by seconds.

# void force_seconds(uint64 seconds)

## Parameters

variable| description  
---|---  
seconds | The seconds to set the time.  
  
## Return Value

None

## Remarks

This method forces the time to set to a specified number of seconds.

## Example
    
    
    void main()
    {
    timer c;
    c.force_seconds(2000); // Forced the time to 2000 seconds. Thus, the timer will move to 2000 seconds.
    }
    
