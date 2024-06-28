# dictionary

dictionary

  


The dictionary object is used to store pairs of keys and values, with the key being a string with which one can look up a value of any type.

  


# dictionary()

## Parameters:

None.

## Remarks:

The dictionary object proves useful when storing an arbitrary number of variables with different types. While setting a new value, a unique string key must be used to refer to the value subsequently. Deletion of a value at any time does not affect the others.

In technical terms, the dictionary functions akin to a hash map. Upon insertion of a new key/data pair, a hash is generated from the key, making later lookup operations significantly faster than a linear search of all the keys.

## Example:
    
    
    dictionary game_board; // Declare our dictionary.
    
    void main()
    {
    int value; // Declare a variable for retrieving values from a dictionary.
    
    // Set our values.
    game_board.set("1", 2); // Sets the value 2 to a key called 1.
    game_board.set("2", 4); // Sets the value 4 to a key called 2.
    game_board.get("1", value); // Retrieve value for 1.
    alert("Dictionary example", "current value=" + value);
    game_board.get("2", value); // Retrieve value for 2.
    alert("Dictionary example", "current value=" + value);
    game_board.delete_all(); // Delete all the values.
    }
    
