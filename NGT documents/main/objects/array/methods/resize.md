# array

array object

This method resizes an array object.

# void resize(uint new_length)

## Parameters

variable| description  
---|---  
new_length | The new length of the array. A value of 0 means the array is reset completely.  
  
## Return value

None.

## Remarks

If the new_length parameter is greater than the current length, the relevant number of empty values will be added to the array. If the value is less, the array is truncated from right to left. 

## Example
    
    
    // Declare an array and display its values.
    
    void main()
    {
    string[] names(5);
    names[0]="a";
    names[1]="b";
    names[2]="c";
    names[3]="d";
    names[4]="e";
    names.resize(names.length()+1);
    names[5]="f";
    for(uint counter=0; counter
    
    
