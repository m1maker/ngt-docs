# file

file object


This method will open a file for reading or writing.

# int open(string filename, string open_mode)

## Parameters

variable | description
---|---
filename | The name of the file to open. This can be either an absolute path, a relative path or the file name on its own.
open_mode | The mode to open, see remarks.

## return value

0 on success, -1 on failure.

## Remarks

Both the slash(`/`), and the backslash(`\`) can be used to specify the filename.

The following is a list of valid open modes.

* `a` : Append.
* `w` : Write.
* `r` : Read.

The file will be created if the file does not exist if opened in write or append mode. Otherwise, when opened in read mode, the filename or the path of the filename must exist in order to be successful.

## Example

```
file f;
void main()
{
f.open("hello.txt","w");
f.write("hello world!");
f.close();
}
```