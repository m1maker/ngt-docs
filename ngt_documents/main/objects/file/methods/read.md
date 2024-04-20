# file

file object


This method will read the file currently associated.

# string read(uint count)

## Parameters

variable | description
---|---
count | The count that is to be read.

## return value

A string containing the data on success, an empty string otherwise.

## Remarks

This method will read the data of a file. The file has to be opened in read mode in order to read.

You can use the `get_size()` method to read all contents.

## Example

```
file f;
void main()
{
f.open("hello.txt","r");
string r=f.read(f.get_size());
f.close();
alert("The file contents",r);
}
```