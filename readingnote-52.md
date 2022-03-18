# Reading 30 - Hash Tables

## Intro to Hash Tables

**hash** - result of some algorithm taking an incoming string and converint it into a value that is used for security.

**buckets** - waht is contained in each index o the array of the hastable.

**collisions** - when a key gets hashed to the same location of hashtable.

**hashtable** - data structures taht utilized key value pairs.

**hash** - ability to encode the key taht will eventually map to a specific location.

-retreiving hash code and reading an array at that index is in constant time to the hash map has O(1) read access.

### Structure

hash is created from an *array*

### Collisions

-occurs when more than one key hashes to the same index in an array. 

-perfect hash will never have any collisions.

-these occurences are solved when you change the state of buckets.
-intialize a Linked List in each one.

**Hash maps** store values by:
-accepting a key
-calculate the hash of the key
-using modulus to convert hash into an array index.
-storye key with value by appending both to the end of a linked list.

Hash map read values by:
-accepting a key
-calculate has of key
-use modulus to convert has hinto an array index.
-use array index to access short Linked List represent a bucket.
-search through bucket looking for nodes with key/value pair that matches key you were given.

### Internal Methods

**Add()** - send the key to the GetHash method.
-when you determine the index of where it should be placed, go to that index.
-add key/value pair only when something doesn't exist at the index.

**Find()** - take a key
-get hash
-got to the index location specified.
-algorithm interates through the bucket to determine if key exists and then returns the value.

**Contains()** - accept a key, return boolean if that key exists inside the hashtable.
-get the contains to call the GetHash and check hashtable if key exists in the table given the index returned.

**GetHash()** - accept key as a string
-conduct hash
-return index of array when key value should be placed.

[<==BACK](README.md)