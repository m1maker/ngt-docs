# functions

join


This function returns a string joined from array based on the seperater

# string join(string[] array, string sep)

## Parameters

Variable| Description
---|---
array | An array to base
sep | The seperater, such as `\r\n` for new line

## return value

A string with the joined data on success, an empty string on failure.

## Remarks

None

## example

```
void main()
{
string[] a={"hello","world"};
string final=join(a, " ");
alert("final",final); //output should be hello world
}
```
