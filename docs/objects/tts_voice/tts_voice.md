# tts_voice

tts_voice object

The tts_voice object is used to speak text using the Microsoft Speech API, more commonly known as Sapi.

# tts_voice()

## Remarks

This object will work with any Sapi 5 compatible voices you have installed on your system.

## Example:

```
//Speak some text using Sapi.
tts_voice speech;
void main()
{
speech.speak_wait("hello, this is Microsoft Sapi, talking from the ngt engine");
}
```