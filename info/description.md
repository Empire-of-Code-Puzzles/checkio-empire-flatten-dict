We'll begin by storing dictionaries in their on board memory. 
Dictionaries are a convenient data type to store and process configurations.
They allow you to store data by keys to create nested structures.
You are given a dictionary where the keys are strings and the values are strings or dictionaries.
The goal is flatten the dictionary, but save the structures in the keys.
The result should be the a dictionary without the nested dictionaries.
The keys should contain paths that contain the parent keys from the original dictionary.
The keys in the path are separated by a "/". If a value is an empty dictionary,
then it should be replaced by an empty string (""). Let's look at an example:

```
{
    "name": {
        "first": "One",
        "last": "Drone"
    },
    "job": "scout",
    "recent": {},
    "additional": {
        "place": {
            "zone": "1",
            "cell": "2"}
    }
}
```

The result will be:

```
{"name/first": "One",           #one parent
 "name/last": "Drone",
 "job": "scout",                #root key
 "recent": "",                  #empty dict
 "additional/place/zone": "1",  #third level
 "additional/place/cell": "2"}
```

Our master server has already written the code for this task, but it has a bug in it.

**You need to find and fix this bug.**
