# tts_voice

tts_voice object

This method will speak a given string.

# bool speak(string text)

## Parameters

variable | description
---|---
text | The text to speak.

## Return value

true on success, false on failure.

## Remarks

If Sapi is already speaking the text will be placed in the buffer queue and is the last string spoken, unless the buffer is cleared beforehand with either the stop, speak_interrupt or speak_interrupt_wait methods.

## Example

```
tts_voice speech;
void main()
{
speech.speak("hello");
}
```