# array

array object

This method will remove the final value in the array.

# void remove_last()

## Parameters

None.

## Return value

None.

## Remarks

On the outside, this method simply does the equivalent of array.resize(array.length()-1).

## Example
    
    
    string[] names(2);
    
    void main()
    {
    names[0]="harry";
    names[1]="ngt";
    names.remove_last();
    for(uint counter=0; counter
    
    
