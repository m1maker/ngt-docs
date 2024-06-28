# sound

sound object


This method will seek the sound

# bool seek(double millisecond)

## Parameters

Parameter| Description
---|---
millisecond | The number of milliseconds to move to.

## Return value

true on success, false on failure.

## Remarks

## Example

```
// Load a sound into memory and play it.
void main()
{
sound test;
test.load("c:\\windows\\media\\ding.wav");
test.seek(1000);
test.play_wait();
test.close();
}
```
