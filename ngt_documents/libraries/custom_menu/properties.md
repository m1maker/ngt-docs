# custom_menu

custom_menu object

# properties

variable| description  
---|---  
wrap | bool parameter, which toggles the wrapping. when on, the menu will wrap back to first and last item as soon as the index ends.  
sidescrolling | bool parameter, which toggles the sidescrolling. default is false. If the sidescrolling is enabled, you use left and right arrow keys to navigate. otherwise, the normal up and down arrows are used.  
clicksound | the sound to play once clicked.  
edgesound | the sound to play once the menu reaches to the edge.  
wrapsound | the sound to play once the menu is wrapped.  
opensound | the sound to play once the menu is displaied, or another word, When the menu is shown.  
movesound | the sound to play once the menu item is navigated.
ttkey | set or get the key that is used to press to repeat the title of the menu. If set to -1, the title will not repeat since there is no key to press. default is `SDLK_TAB`
running | return true or false, whether the menu is running. this cannot be modified from the script.
position | returns the current position of the menu. this is set to -1 on failure. this cannot be modified from the script.
item_length | returns the length of total items. this is set to -1 on failure or no menu items. this property cannot be modified from the script.
error | returns the error code of a previously called action. this is set to 0 on normal. this cannot be modified from the script.
error_info | returns a string with the error information that occurs previously. this is an empty string on normal. this cannot be modified from the script.
click | returns a string of the reference of the current clicked item. this is set to empty on no item is being clicked.