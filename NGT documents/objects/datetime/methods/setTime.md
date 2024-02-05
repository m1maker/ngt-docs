# datetime

datetime object

  


The setTime method is used within the datetime object, and sets the current hour, minute, and second of the current date object.

# bool setTime(uint hour, uint minute, uint second)

## Parameters

||| Variable| Description  
---|---  
hour | The hour to set.  
minute | The minute to set.  
second | The second to set.  
  
## Return value

true on success, false on failure.

## Remarks

This method sets the current time. note, all the hour is 24, meaning 0 to 23.

## Example


```
datetime d;
void main()
{
d.setTime(0, 0, 0);
alert("hello", d.get_second() + ", " + d.get_minute() + ", " + d.get_second() + ", " + d.get_hour() + ", " + d.get_minute() + ", and " + d.get_second());
}

```
