# functions

get_master_volume

  


This function gets the master volume for the sound mixer.  


# float get_master_volume()

## Parameters

None.

## Return value

The master volume between 1 and 0. Default is 1.

## Remarks

The master volume works similar to the master fader on a mixing desk. It controls every sound that is played during the game and works independently of a sound object's volume control. This means that you can continue treating the volume of individual sound objects exactly the same as before, where 1 is always the maximum based on the current master volume. This can be useful if your game uses quiet TTS output and has a rather loud or busy soundscape.

Please note that these functions do not apply to the Windows volume control, only sounds that are played from within the game itself.

## Example
    
    
    // Set the master volume to 0.35 and retrieve the new value.
    void main()
    {
    set_master_volume(0.35);
    alert("Sound master volume", "The sound master volume is " + get_master_volume() + ".");
    }
    
