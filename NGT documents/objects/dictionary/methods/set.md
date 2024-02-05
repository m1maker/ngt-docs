# dictionary

dictionary object

  


This method will set a value referred to by the key.

# void set(string key, ? value)

## Parameters

variable| description  
---|---  
key | The key to use.  
value | A variable of any type whose value you wish to associate with the specified key.  
  
## Return value

None.

## Remarks

If a particular key already exists in the dictionary, its value will be automatically overwritten.

## Example
    
    
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
    
