# custom_menu

custom_menu object

# error codes

* cme_none : success
* cme_faildelexist : bad request: trying to remove the item that does not exist
* cme_no_special : the operation cannot be done because of containing special characters used to determine the menu items
* cme_run_title_empty : the menu could not run. bad request: the title for the menu is empty
* cme_canceled : user choose to cancel
* cme_alreadyactive : the menu cannot run. bad request: not allowed overrun
* cme_outrange : 1 or more parameters are out of range
* cme_invalid_length : the items and the references length are not same each other, thus it is invalid for the menu to show up
* cme_invalid_type : the type is invalid.