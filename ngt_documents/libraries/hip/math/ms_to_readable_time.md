# functions

this method will return a given milliseconds into human readable format and round wherever is available.

# string ms_to_readable_time(double ms, int round_year_to, int round_month_to, int round_week_to, int round_day_to, int round_hour_to, int round_minute_to, int round_second_to)

## parameters

variable | description
---|---
ms | the number of milliseconds.
round_year_to | an optional parameter specifies the number to round year, 0 is default.
round_month_to | an optional parameter specifies the number to round month, 0 is default.
round_week_to | an optional parameter specifies the number to round week, 0 is default.
round_day_to | an optional parameter specifies the number to round day, 0 is default.
round_hour_to | an optional parameter specifies the number to round hour, 0 is default.
round_minute_to | an optional parameter specifies the number to round minute, 0 is default.
round_second_to | an optional parameter specifies the number to round second, 0 is default.

## return value

a string containing a human readable format.

## remarks

this method will return a given milliseconds into human readable format. it is probably used to display status of the current player's playtime, etc.

## example

```
#include"hip.ngt"
void main()
{
double playtime=120000;
alert("playtime","you've been playing for "+ms_to_readable_time(playtime)); //output should be 2 minutes.
}
```