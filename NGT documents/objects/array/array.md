# array

array object

  


The array object is used to store multiple values of the same type.

# array(int number_of_elements)

## Parameters

variable| description  
---|---  
number_of_elements | An optional parameter that specifies the number of elements to create.  
  
## Remarks

The array object is unique to any other object, since it is declared as and behaves like a variable containing a single value. When you wish to declare an array, you simply put the type of variable that the array will hold, followed by an empty set of square brackets. Then when you wish to access one of its values, you put the element number in a set of square brackets (see the examples and language tutorial for a more in-depth explanation of the workings of arrays). 

Please note that if an error occurs while working with arrays, the NGT engine will terminate with a runtime error rather than silently setting an error code. Therefore it is essential that you take great care when working with arrays. 

## Example
    
    
    // Declare an array and display its values.
    
    void main()
    {
    string[] names(2);
    names[0] = "ngt";
    names[1] = "harry";
    for(uint counter = 0; counter < names.length(); counter++)
    {
    alert("Names", "Element " + counter + " contains the name " + names[counter] + ".");
    }
    }
    
