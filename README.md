# python-steamid
### The python port of node-steamid (created by McKay)

## What is python-steamid?
Python steamid is a library, directed at parsing steam IDs, and returning information about them. One of the great things about it,
is that it will parse *any* steamid, without you having to specify what it is. Another benefit is it not using the internet. 
Meaning you can run this program offline, without any problems.

## How to install
As stated above, this library uses no other moduals, that don't come with atleast python3.6 and above (re and math, although it 
doesn't use math, but I forgot to remove it). You just have to do
```
pip install steamid
```
And your done! You can now import it.

## How to use

The library comes with a class called `SteamID`, that takes any steam ID as input, must be a string.
```py
from steamid import SteamID
my_id = SteamID('76561198269569899') 
#This is a steam64 ID. However, other IDs are usable, like steam2, and steam3 IDs
```

## Properties

### AccountIDMask
 * Class variable: *0xFFFFFFFF*
  
### AccountInstanceFlags
 * Class variable: *0x000FFFFF*
 
### ChatInstanceFlags
 * Class variable: (dict)

### Instance
 * Class variable: (dict)
 
### Type
 * Class variable: (dict)
 
### TypeChars
 * Class variable: (dict)
 
### Universe 
 * Class variable: (dict)
 
### accountid
 * Object variable: (int): *Will onlly exist if the ID is a user*
 
### instance
 * Object variable: (int)
 
### type
 * Object variable: (int)
 
### universe
 * Object variable: (int)
 
## Functions

### fromIndividualAccountID
`Returns a SteamID object, based on the account ID.`
 * Static Method
 * Input: accountid (int)
 * Output: SteamID object (SteamID)
 
### steam2 & getSteam2RenderedID
`Creates a steam2 ID from the current SteamID object`
 * Object Method
 * Input: newerFormat
 * Output: steam2id (str)
 
### steam3 & getSteam3RenderedID
`Creates a steam3 ID from the current SteamID object`
 * Object Method
 * Input: -
 * Output: steam3id (str)
 
### __str__ & getSteamID64
`Creates a steam64 ID from the current SteamID object`
 * Object Method
 * Input: -
 * Output: steam64id (str)
 
### isValid
`Checks the SteamID object, to make sure it's a valid steam id.`
 * Object Method
 * Input: -
 * Output: True / False (bool)
