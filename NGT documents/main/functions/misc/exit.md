# functions

exit




This function quits the program.


# void exit()

## Parameters

None

## Return value

None

## Remarks

It is safe to call this function from anywhere within your script. All memory and resources that have been allocated for your game will be automatically released back to Windows. This also happens whenever a script finishes executing, so it is not necessary to call this function at the end of your code.

## Example

```
// Display a message box and then quit.
void main()
{
alert("quitting program", "Thanks for playing!");
exit();
}
```
