# functions

screen_reader_detect

This method will return a string defineing the current running screen reader.

# string screen_reader_detect()

## Return value

A string of the currently running screen reader on success, an empty string on failure.

## Example

```
void main()
{
string s=screen_reader_detect();
if(s.is_empty())
{
alert("Information","Your operating system is not using any screen reader, ok");
}
else
{
alert("Information","Your screen reader is detected. "+s,"Quit");
}
}
```