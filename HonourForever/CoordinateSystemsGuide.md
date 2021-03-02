# Stantons coordinates

## Coordinates for Planetoids

Using the star map in game the approximate orbits can be defined

The current implementation restricts this method at a granularity of 1 kkm or 1000 km.
Becausse of this a different system has to be used for planetoids.

Distances [Mkm] | HUR | CRU | ARC | MIC
--- | --- | --- | --- | ---
Stanton | 12.85 | 19.148 | 28.916 | 43.441
HUR | - | 31.924 | 22.881 | 38.408
CRU | 31.924 | - | 42.312 | 57.469 
ARC | 22.881 | 42.312 | - | 59.462
MIC | 38.408 | 57.469 | 59.462 | - 

With this data a representation of the System can be constructed, through which collected coordiantes can be put into terms of travel instructions.


## Coordinates for Planetoid-surfaces
Through obvious granularity/accuracy problems of the method used for [planets and mining claims](#Coordinates-for-Planetoids) a different system has to be used for unmarked POI on planetoids.

As all POI's on Planetoids until now are on a 2D surface (although curved it is still 2D) a usage of three different points can be utilized.

**For each POI** different distance markers can be used, although it is recommended that the three smallest number should be used and the usage of Orbital markers should be avoided in general. (It is currently unclear to the author if OM-X markers are Surface locked or in relation to the main Star or relative to the geometric poles of the planet)

An example for a POI in planetoid coordinated:
> Aberdeen HDMS-Noragaard 100 HDMS-Anderson 224 HDMS-Dobbs 40
note that this example does not ammount to a real location

## Alternative coordinates (Honourian Pathtracing System HoPaSy)

Alternatively coordinates can be packed up in a descriptive way.

- The starting location is written first.
- Then the character "|" is put.
there are two possibilites now
> X|
> 
this signals that on the way from start to end, travel X km in the direction and then stop

> |X

this signals that on the way from start to end, travel so far that the distance X is between you and the end

X has a special formatting

The base unit for X is km, which makes it a nice intermediary for any distance
Instead of the "Comma" or "Decimalpoint" write the order of magnitude:

Order of Magnitude | HoPaSy Symbol | Meaning/Usage
--- | --- | ---|
Mega | M | 1M1 = 1 100 000 km
Kilo | K | 2K1/2k1 = 2 100 km
Unit | u | 3U1/3u1 = 3.1 km
milli | m | 3m1 = 0.0031 km / 3.1 m 

- At last the travel direction is put as the second part


Example:
> PO |1M1 Hurston | 30M MicroTech

> HDMS-Noragaard 20| HDMS-Dobbs


