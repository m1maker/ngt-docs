# datetime

datetime object

  


The date time object is used for date and time calculations and works as a calendar.

# datetime()

## Parameters

None.

## Remarks

When the date object is created, the date and time will be set to the current date and time according to the system's date. From then on, you can change the date and time later with their respective methods.

## Example


```
// Displays the date and time.
datetime d;
void main()
{
alert("hello", d.get_year() + ", " + d.get_month() + ", " + d.get_day() + ", " + d.get_hour() + ", " + d.get_minute() + ", and " + d.get_second());
}

```
