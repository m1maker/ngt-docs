# vector

vector object


The vector object is used within the map, corresponding to coordinates x, y, and z, see remarks.

# vector()

## Parameters

None

## Remarks

The vector object is used within the map, corresponding to coordinates x, y, and z. It can be useful for map coordination, probably used within 2 or 3-dimensional grids. A list of properties will be provided below. This document will not create a separate documentation for vector object properties, as there are not many properties.

Property| Description
---|---
x| The x-coordinate of the vector.
y| The y-coordinate of the vector.
z| The z-coordinate of the vector.

## Example

```
void main()
{
vector v;
v.x = 0;
v.y = 0;
v.z = 0;
alert("vector", v.x + ", " + v.y + ", " + v.z);
}
```