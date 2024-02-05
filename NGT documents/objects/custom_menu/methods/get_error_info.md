# custom_menu

custom_menu object

  


This function returns the error that previously occurred.

# string get_error_info()

## Parameters

None

## Return Value

A string containing the previous error information.

## Remarks

This function returns information about the previous error. As the custom menu object has its own error handling, its own set of error functions will need to be present.

## Example


```
// Make a simple menu.
#include "custom_menu.ngt"
void main()
{
show_game_window("menu test");
custom_menu c;
string errorInfo = c.get_error_info();
if (!errorInfo.is_empty())
{
// Handle the error information.
}
}

```
