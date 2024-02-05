# functions

get_sound_storage

  


This function gets the location of the path in which the engine will look for sound files loaded through the sound object.  


# string get_sound_storage()

## Parameters

None.

## Return value

The path on success, or an empty string on failure.

## Remarks

Note that both \ and / can be used to specify paths.

If an empty string is returned by this function, it means that the engine will not look for sounds in a specified path, but will attempt to locate requested files on disk instead. This is the default behavior.

## Example
    
    
    // Tell the engine to look for sound files in a folder called sounds, and then print this.
    void main()
    {
    set_sound_storage("sounds");
    alert("Sound storage", "The sound storage is " + get_sound_storage() + ".");
    }
    
