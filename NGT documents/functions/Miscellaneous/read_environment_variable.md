# functions

read_environment_variable

  


This function reads the value of a user specific or system-wide environment variable.

# string read_environment_variable(string name)

## Parameters

||| variable| description  
---|---  
name | The name of the environment variable to read.  
  
## Return Value

A string containing the retrieved value on success, or an empty string on failure.

## Remarks

Environment variables are pieces of information that are either related to the operating system or to the current user. This function can retrieve both types.

The environment variable names are not case sensitive.

## Example


```
// Try to retrieve some information about the username.
void main()
{
string value = read_environment_variable("USERNAME");
if (value == "")
{
alert("Error", "An empty string is retrieved");
quit();
}
alert("Value", value);
}

```
