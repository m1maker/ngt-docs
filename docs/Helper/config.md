## Enums

### SaveDataTypes
- **SAVEDATA_DEF = 0**: Default save type.
- **SAVEDATA_INI**: INI file format save type.

## Class: save_data

### Members

- `private string key`: Encryption key used for data encryption/decryption.
- `private string filename`: The name of the file where data will be saved and loaded from.
- `private dictionary dataDictionary`: Stores the data in a dictionary structure.
- `private int saveType = SAVEDATA_DEF`: The type of save format to use.

### Methods

#### Constructor
- Initializes the `filename`, `key`, and `saveType` with provided values. The `encryptionKey` is optional and defaults to an empty string if not provided.

#### get_type() property
- Returns the current save type.

#### load()
- Opens the file and reads its contents. If successful, it loads the data into `dataDictionary` using the appropriate parser based on the save type.

#### save()
- Opens the file in write mode and saves the current state of `dataDictionary` to the file using the appropriate serializer based on the save type.

#### add(const string&in name, double value)
- Adds or updates a numeric value in the dictionary with the given key.

#### readNumber(const string&in name)
- Reads a numeric value from the dictionary. If the save type is INI, it first reads the string and converts it to a number.

#### add(const string&in name, const string&in value)
- Adds or updates a string in the dictionary with the given key.

#### read(const string&in name)
- Reads a string from the dictionary.

#### get_keys() property
- Returns an array of keys in `dataDictionary`.

#### exists(string key)
- Checks if a key exists in the dictionary.

#### clear()
- Clears all data from the dictionary.

### Private Helper Methods

- `private dictionary loadDictionary(string data)`: Parses the loaded data based on the save type and encryption key.
- `private string saveDictionary(dictionary @d)`: Serializes the dictionary into a string format based on the save type and encryption key.
- `private dictionary parseIniData(const string&in data)`: Parses INI formatted data into a dictionary.
- `private string convertToIniFormat(dictionary @d)`: Converts a dictionary into an INI formatted string.

## Usage

To use this class, you would typically create an instance of `save_data`, and then call methods to load, save, add, and read data. Here is an example:

``` angelscript
// Create an instance of save_data with a specific file name
save_data saver("game_progress.dat", "my_encryption_key");

// Save some data
saver.add("player_level", 10);
saver.add("health_points", 100);
saver.save();

// Load the saved data
saver.load();

// Read and print the saved data
double level = saver.readNumber("player_level");
string health = saver.read("health_points");

print("Player Level: " + level.to_string() + "\nHealth Points: " + health + "\n");
```

This example demonstrates how to save and load player progress data, including reading numeric and string values.
