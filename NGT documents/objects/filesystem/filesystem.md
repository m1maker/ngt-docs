# filesystem

filesystem object

  


The filesystem object is used to perform additional actions on files and directories.

# filesystem()

## Parameters

None.

## Remarks

The filesystem object is used to perform additional actions on files and directories. It can be useful for changing paths and other actions.

## Example


```
filesystem f;
void main()
{
alert("hello", "The current located script path is, " + f.get_current_path());
}

```
