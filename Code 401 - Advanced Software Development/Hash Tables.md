# Hash Tables
### What is a Hashtable?
* Hash : A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array ( A data structure that is used to store keys/value pairs)

* Buckets : A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

* Collisions : A collision is what happens when more than one key gets hashed to the same location of the hashtable.


### Why do we use them?
* Hold unique values
* Dictionary
* Library
### What Are they?
Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.

# Review, Research, and Discussion (Links to an external site.)
### General 
  * We use hash tables to hold unique values, as away to store and search for things
  * The main idea of a hash table is that it has the ability to store a key into this data structure and quickly retrieve the value. Both are done through hashing.
  * The hash function takes a key and returns an interger
  * Ability to have a consistent O(1) read and write access

# Creating a hash 
A hashtable traditionally is created from an array. I always like the size 1024. this is important for index placement. After you have created your array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value. Here is a possible suggestion:
* Add or multiply all the ASCII values together.
* Multiply it by a prime number such as 599.
* Use modulo to get the remainder of the result, when divided by the total size of the array.
* Insert into the array at that index.




