# custom_menu

custom_menu object


This adds the list to the menu.

# bool add_list(string i, string ref, bool multi)

## Parameters

Variable| Description
---|---
i | The specified item.
ref | The reference name for the item.
multi | an optional parameter, to set the status of the list multiselection. default is false, meaning the list will not be multiple.

## Return Value

True on success, false on failure.

## Remarks

This function adds the list into the menu. Make sure that the reference names are not the same as each other, as this will make the references unusable. The reference will be returned with the value after the menu is run (e.g., result == "back").

lists with multiselection enabled will allow the user to check many items they want.
