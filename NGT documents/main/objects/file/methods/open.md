# file

file object


This method will open a file for reading or writing.

# int open(string filename, string open_mode)

## Parameters
variable | description
---|---
filename | the name of the file to open. This can be either an absolute path, a relative path or the file name on its own.
open_mode | the mode to open, see remarks.

## return value

0 on success, -1 on failure.

## Remarks

both the slash(`/`), and the backslash(`\`) can be used to specify the filename.

the following is a list of valid open modes.

* `a` : append.
* `w` : write.
* `r` : read.

the file will be created If the file does not exist If opened in write or append mode. otherwise, when opened in read mode, the filename or the path of the filename must exist in order to be successful.

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