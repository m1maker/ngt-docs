# timer

timer object

  


This function forces the time by hours.

# void force_hours(uint64 hours)

## Parameters

||| variable| description  
---|---  
hours | The hours to set the time.  
  
## Return Value

None

## Remarks

This method forces the time to set to a specified number of hours.

## Example


```
void main()
{
timer c;
c.force_hours(2000); // Forced the time to 2000 hours. Thus, the timer will move to 2000 hours.
}

```
