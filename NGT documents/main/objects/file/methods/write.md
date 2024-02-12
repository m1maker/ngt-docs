# file

file object


This method will write to the file currently associated.

# int write(string content)

## Parameters
variable | description
---|---
content | the content that is to be written.

## return value

0 on success, -1 on failure.

## Remarks

this method will put contents to the file, depending on how the file is opened. If opened in append mode then the contents will be inserted at the end of the file. or If opened write mode then all the contents will be overwritten with the new contents.

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