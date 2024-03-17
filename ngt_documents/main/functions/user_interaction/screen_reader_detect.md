# functions

screen_reader_detect

this method will return a string defineing the current running screen reader.

# string screen_reader_detect()

## return value

a string of the currently running screen reader on success, an empty string on failure.

## example

```
void main()
{
string s=screen_reader_detect();
if(s.is_empty())
{
alert("information","your operating system is not using any screen reader, ok");
}
else
{
alert("information","your screen reader is detected. "+s,"quit");
}
}
```