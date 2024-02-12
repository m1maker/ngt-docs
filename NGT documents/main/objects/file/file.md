# file

file object


The file object is used to read and write files stored on the hard disk.

# file()

## Parameters

None.

## Remarks

when the file object is first created, it will not be active. to activate it you must call the open method with the filename that is to be associated with, and the mode to open. you can call the open method at any time to associate it with a new file. the process is that you can reuse the same file object over and over, If you desire so.

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