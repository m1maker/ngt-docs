# dictionary

dictionary object

  


This method will retrieve a list of all the keys that are present in the dictionary.

# string[] get_keys()

## Parameters

None.

## Return value

An array with all the keys on success, or an empty array on failure.

## Remarks

none

## Example
    
    
    dictionary game_board; // Declare our dictionary.
    void main()
    {
    // Add a bunch of keys to the dictionary.
    for(uint i = 0; i < 20; i++)
    {
    game_board.set("key_" + (i + 1), 0);
    }
    
    // Assemble a string with a list of all the keys and display it in an alert box.
    string output;
    string[] keys = game_board.get_keys();
    for(uint i = 0; i < keys.length(); i++)
    {
    if(output == "")
    output += keys[i];
    else
    output += "\n" + keys[i];
    }
    alert("Keys", output);
    }
    
