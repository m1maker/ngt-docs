# array

array object

  


This method will remove an existing value at a specified position in an array.  


# void remove_at(int position)

## Parameters

variable| description  
---|---  
position | The index of the element to remove.  
  
## Return value

None.

## Remarks

Once the value has been removed, the array will be automatically resized to reflect the change.

## Example
    
    
    string[] names(2);
    
    void main()
    {
    names[0]="harry";
    names[1]="ngt";
    names.remove_at(1);
    for(uint counter=0; counter
    
    
    
    
    
