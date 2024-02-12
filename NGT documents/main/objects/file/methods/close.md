# file

file object


This method will close the current object associations.

# int close()

## Parameters

none

## return value

0 on success, -1 on failure.

## Remarks

this method will close the associated file on the object.

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