# functions

speak

  


This function speaks some text using a screen reader which is determined automatically.  


# void speak(string text, bool stop = true);

## Parameters

||| variable| description  
---|---  
text | The text that is to be spoken.  
stop | Toggle whether the previously speaking speech should be stopped. (Default: true)  
  
## Return value

None

## Remarks

This function speaks some text using a screen reader which is determined automatically.

## Example


```
void main()
{
init_engine();
speak("I am a screen reader");
}

```
