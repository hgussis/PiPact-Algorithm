# PiPact-Algorithm
This algorithm seeks to predict if two Raspberry Pi devices are within 6 feet of eachother for more than 15 minutes. The Main Method file opens up the data log and creates arrays based on that log and the obstructions present. The other files contain data that is pertinent to those specific obstructions, and they are accessed via the Main Method file.

In order to use this algorithm, a list of the barriers must be inputted by the user:

The barrier list contains the time stamps and type of interaction the devices had (ex. ([1,3,"no obs],[3,9,"wall"]) means that from minutes 1-3 during the current hour there were no obstructions and from minutes 3 to 9 there was a wall between the devices

Valid obstruction types: "no obs","wall","door","pockets","doorxpocket", "pocketxhumanxwall","2humans","humanxwall","sockxwall","sockxhuman","human"

Exceptions:
- There must be atleast two tuples in the barrier_list or an error will be raised
