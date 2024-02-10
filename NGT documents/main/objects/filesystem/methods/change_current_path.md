# filesystem

filesystem object

  


This function sets the current path.

# bool change_current_path(string path)

## Parameters

variable| description  
---|---  
path | The new path to set as the current path.  
  
## Return Value

true on success, false on failure.

## Remarks

Both slash (/) and backslash (\\) can be used for the path.

## Example
    
    
    void main()
    {
    filesystem f;
    f.change_current_path("D:\\NGT");
    }
    
