# Properties

### lfolder
- **Type**: string (Read/Write)
- **Description**: The languages folder, default is "lang".

### base_lang
- **Type**: string (Read/Write)
- **Description**: The base language, default is "English".

### base_lang_flag
- **Type**: string (Read/Write)
- **Description**: The flag for the base language, default is "🇺🇸" (USA Flag).

### base_lang_code
- **Type**: string (Read/Write)
- **Description**: The ISO code for the base language, default is "Eng".

### lex
- **Type**: string (Read/Write)
- **Description**: The language extension, default is ".lng".

## Methods

### get_langname() Property
- **Returns**: string
- **Description**: Returns the current language name.

### refresh(string&in l, string&in folder = "", string&in ex = "")
- **Parameters**:
  - `l`: string (Language code to load, default is the current language).
  - `folder`: string (Optional, custom languages folder path).
  - `ex`: string (Optional, custom language file extension).
- **Description**: Refreshes the translation data for a specified language.

### translate(const string&in l, string&in text, const string&in firstr = "", const string&in secondr = "")
- **Parameters**:
  - `l`: string (Language code to use for translation, default is the current language).
  - `text`: string (Text to be translated).
  - `firstr`: string (Optional, first string to replace).
  - `secondr`: string (Optional, second string to replace).
- **Returns**: string
- **Description**: Translates the input text into the specified language. Optionally replaces specific strings.

### get_flag(string&in l = "")
- **Parameters**:
  - `l`: string (Language code to fetch flag for, default is the current language).
- **Returns**: string
- **Description**: Returns the flag associated with the specified language or the base language if not found.

### get_flag() Property
- **Returns**: string
- **Description**: Returns the flag associated with the current language.

### get_code(string&in l = "")
- **Parameters**:
  - `l`: string (Language code to fetch ISO code for, default is the current language).
- **Returns**: string
- **Description**: Returns the ISO code associated with the specified language or the base language if not found.

### get_code() Property
- **Returns**: string
- **Description**: Returns the ISO code associated with the current language.

### load_language_file(const string l)
- **Parameters**:
  - `l`: string (Language code to load).
- **Returns**: array<string>
- **Description**: Loads and returns the lines from a language file for the specified language. If the file is not found, an empty array is returned.

## Usage Example

```angelscript
translator trans;
trans.refresh("Spanish");
string translated_text = trans.translate("Spanish", "Welcome to the game!");
println(translated_text); // Output: Bienvenido al juego!
```

This example demonstrates how to refresh translation data for Spanish and translate a text string into Spanish.
