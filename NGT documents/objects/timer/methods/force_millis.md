# timer

timer object

  


This function forces the time by milliseconds.

# void force_millis(uint64 millis)

## Parameters

||| variable| description  
---|---  
millis | The milliseconds to set the time.  
  
## Return Value

None

## Remarks

This method forces the time to set to a specified number of milliseconds.

## Example


```
void main()
{
timer c;
c.force_millis(2000); // Forced the time to 2000 milliseconds. Thus, the timer will move to 2000 milliseconds.
}

```
