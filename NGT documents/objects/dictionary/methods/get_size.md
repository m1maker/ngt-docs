# dictionary

dictionary object

  


This method returns the number of elements in the dictionary.

# uint get_size()

## Parameters

None.

## Return value

The number of elements present in the dictionary, or 0 if the dictionary is empty or if an error occurs.

## Remarks

This method returns the number of key/value pairs in the dictionary. Therefore, if the dictionary had a value named "value" linked to a key named "key", the size would return 1.

## Example
    
    
    // Create a dictionary and display its size.
    
    void main()
    {
    int value = -1;
    dictionary names;
    names.set("Damien", 0);
    names.set("Philip", 1);
    names.set("Percival", 2);
    names.set("Byron", 3);
    names.set("Humphrey", 4);
    alert("Count", "The dictionary contains " + names.get_size() + " entries.");
    string[] keys = names.get_keys();
    for(int counter = 0; counter < keys.get_size(); counter++)
    {
    names.get(keys[counter], value);
    alert("Names", keys[counter] + " contains the value " + value + ".");
    }
    }
    
