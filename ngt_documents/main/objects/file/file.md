# file

file object


The file object is used to read and write files stored on the hard disk.

# file()

## Parameters

None.

## Remarks

When the file object is first created, it will not be active. To activate it you must call the open method with the filename that is to be associated with, and the mode to open. You can call the open method at any time to associate it with a new file. The process is that you can reuse the same file object over and over, if you desire so.

## Example

```
file f;
void main()
{
f.open("hello.txt","w");
f.write("Hello world!");
f.close();
}
```