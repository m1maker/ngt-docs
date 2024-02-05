# instance

instance object

  


The instance object is used to check whether a given program is already running.

# instance(string application_name)

## Parameters

||| variable| description  
---|---  
application_name | An optional unique name that is used internally for the program.  
  
## Remarks

This object is useful if you wish to prevent multiple instances of the same program from being opened at the same time.

If the application_name argument is specified, it should not be more than 100 characters in length. If it is not specified, it will default to a hash of the program executable and hence will not work if trying to prevent an older version of a program from running alongside an updated copy.

This class does not have many functions, as this is simple.

## Example


```
/*
Write a script that checks for another instance of itself. To make this script work effectively you must run it at least twice within twenty seconds of the first instance being started.
*/

void main()
{
instance myapp("instancetester");
if(myapp.is_running())
{
alert("Error", "This script is already running, hence, failed to execute!");
quit();
}
wait(20000);
}

```
