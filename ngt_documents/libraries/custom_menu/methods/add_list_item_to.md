# custom_menu

custom_menu object




This adds the list item to the given reference.

# bool add_list_item_to(string ref, string item, string list_ref, int per, bool select)

## Parameters

Variable| Description
---|---
ref | The reference name of the list.
item | the specify list item to be added.
list_ref | the specify list reference to be added. If pass as empty, the item will be set instead.
per | the position in which the item should insert, -1 is default.
select | an optional parameter, to set the status of the list selection. default is false, meaning the list item will not be checked. this will not affect on non multiselection lists.

## Return Value

True on success, false on failure.

## Remarks

This function adds the list item into the menu. Make sure that the reference name exists, and list reference are not same as each other, as this will make the references unusable.
