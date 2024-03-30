# functions

this method will return whether the coordinates are in range, by giving current coordinates x y z, minimum and maximum ranged coordinates.

# bool inrange(double x, double y, double z, double minx, double maxx, double miny, double maxy, double minz, double maxz)

## parameters

variable | description
---|---
x | the current x coordinate.
y | the current y coordinate.
z | the current z coordinate.
minx | the minimum x coordinate for the range.
maxx | the maximum x coordinate for the range.
miny | the minimum y coordinate for the range.
maxy | the maximum y coordinate for the range.
minz | the minimum z coordinate for the range.
maxz | the maximum z coordinate for the range.

## return value

true on If in range, false on out of range.

## remarks

this method will return whether the coordinates are in range, by giving current coordinates x y z, minimum and maximum ranged coordinates.

this method is overloaded, meaning you can use the default, or by vectors to minimum and maximum coordinates, or by vectors for all.

* `bool inrange(double x, double y, double z, double minx, double maxx, double miny, double maxy, double minz, double maxz)` : default.
* `bool inrange(double x, double y, double z, vector@ min, vector@ max)` : give 3 current coordinates as variables, vectors for minimum and maximum coordinate range.
* `bool inrange(vector@ current, vector@ min, vector@ max)` : use vectors for all the variables, thus you will declare the 3 vectors to use this one.

## example

```
#include"hip.ngt"
void main()
{
//manual
bool manual=inrange(2,3,1,0,50,0,50,0,50);
print(manual);
manual=inrange(2,3,500,0,50,0,50,0,50);
print(manual);

//use vectors for min and max;
vector min,max;
min.x=0;
min.y=0;
min.z=0;
max.x=100;
max.y=50;
max.z=10;
bool v=inrange(10,10,0,min,max);
print(v);
v=inrange(500,200,10,min,max);
print(v);

//use all as vectors.
vector user;
min.x=0;
min.y=0;
min.z=0;
max.x=100;
max.y=50;
max.z=10;
user.x=10;
user.y=30;
user.z=10;
bool us=inrange(user,min,max);
print(us);
user.z=10000;
us=inrange(user,min,max);
print(us);
}
void print(bool what)
{
if(what) alert("yes","in range");
else alert("no","out of range");
}
```