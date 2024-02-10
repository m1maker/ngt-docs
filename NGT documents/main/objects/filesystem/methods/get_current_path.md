# filesystem

filesystem object

  


the ge_current_path function returns the current path where the script is executed. 

# string get_current_path()

## Parameters

none

## Return Value

a string of the current path on success, an empty string on failure.

## Remarks

This function returns the current path where the script is executed. You can also change the current path; see the change_current_path method.

## Example
    
    
    filesystem f;
    void main()
    {
    alert("hello", "The current located script path is, " + f.get_current_path());
    }
    
