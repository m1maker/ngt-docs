# functions

set_sound_storage

  


This function sets the location of the path in which the engine will look for sound files loaded through the sound object.  


# void set_sound_storage(string path)

## Parameters

||| variable| description  
---|---  
path | The path to use. This can be either an absolute path or a relative path.  
  
## Return value

None.

## Remarks

Note that both \ and / can be used to specify paths.

If an empty string is passed to this function, the engine will not look for sounds in a pack file but will attempt to locate requested files on disk instead. This is the default behavior.

It is perfectly legal to call this function more than once in your game. Sounds that are already loaded will not be affected; any changes are only seen the next time you attempt to load a sound.

## Example


```
// Tell the engine to look for sound files in a folder called sounds.
void main()
{
set_sound_storage("sounds");
}

```
