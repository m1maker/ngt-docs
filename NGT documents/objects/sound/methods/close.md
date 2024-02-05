# sound

sound object

  


This method will close any sound associated with the object.

# bool close()

## Parameters

None.

## Return value

true on success, false on failure.

## Remarks

Closing a sound releases the current sound memory associated with the object, saving resources while keeping the object available for future use. It's automatically executed when a sound object is destroyed, eliminating the need to manually call it for cleanup, for instance, at the script's end. This method also executes if "load" or "stream" is called on an object already associated with a sound. 

## Example


```
// Load a sound into memory, play it and close it.
void main()
{
init_engine();
sound test;
test.load("c:\\windows\\media\\ding.wav");
test.play_wait();
test.close();
}

```
