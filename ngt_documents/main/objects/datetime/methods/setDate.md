# datetime

datetime object

  


The setDate method is used within the datetime object, and sets the current year, month, and day of the current date object.

# bool setDate(uint year, uint month, uint day)

## Parameters

Variable| Description  
---|---  
year | The year to set.  
month | The month to set.  
day | The day to set.  
  
## Return value

true on success, false on failure.

## Remarks

This method sets the current date.

## Example
    
    
    datetime d;
    void main()
    {
    d.setDate(2023, 12, 1);
    alert("hello", d.get_day() + ", " + d.get_month() + ", " + d.get_day() + ", " + d.get_hour() + ", " + d.get_minute() + ", and " + d.get_second());
    }
    
