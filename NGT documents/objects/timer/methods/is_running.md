# timer

timer object

  


This method checks whether the timer is currently running.

# bool is_running()

## Parameters

variable| description  
---|---  
none | No parameters for this method.  
  
## Return Value

true if the timer is currently running, or false if the timer is paused.

## Remarks

None

## Example
    
    
    void main()
    {
    timer c;
    if(c.is_running())
    {
    alert("yes", "The timer is nicely running!");
    }
    else
    {
    alert("error", "The timer is not running. This could mean either the timer is paused.");
    }
    }
    
