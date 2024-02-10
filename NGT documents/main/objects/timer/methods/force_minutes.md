# timer

timer object

  


This function forces the time by minutes.

# void force_minutes(uint64 minutes)

## Parameters

variable| description  
---|---  
minutes | The minutes to set the time.  
  
## Return Value

None

## Remarks

This method forces the time to set to a specified number of minutes.

## Example
    
    
    void main()
    {
    timer c;
    c.force_minutes(2000); // Forced the time to 2000 minutes. Thus, the timer will move to 2000 minutes.
    }
    
