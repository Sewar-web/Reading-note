# Hash


* Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.



* Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.



* Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.





**Structure**

* Hashing
Basically, a hash code turns a key into an integer. It’s very important that hash codes are deterministic: their output is determined only by their input. Hash codes should never have randomness to them. The same key should always produce the same hash code.

* Creating a Hash
A hashtable traditionally is created from an array. I always like the size 1024. this is important for index placement. After you have created your array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value. Here is a possible suggestion:

* Add or multiply all the ASCII values together.
Multiply it by a prime number such as 599.
Use modulo to get the remainder of the result, when divided by the total size of the array.
Insert into the array at that index.
Example:


```
Key = "Cat"
Value = "Josie"

67 + 97 + 116 = 280

280 * 599 = 69648

69648 % 1024 = 16

Key gets placed in index of 16. 


```

Collisions
A collision occurs when more than one key hashes to the same index in an array. As mentioned earlier, a “perfect hash” will never have any collisions. To put this into perspective, the worst possible hash is one that hashes every single key to the same exact index of an array. The more keys you have hashed to a specific index, the more key/value pair combos you can potentially have.

What would happen if two different keys resolved to be the same index of the array? This is called a collision. The hash map needs to be able to handle two keys resolving to the same index.

If two keys ever ultimately resolved to the same index, then two calls to .Add(key, val) with different keys would overwrite each other.

Collisions are solved by changing the initial state of the buckets. Instead of starting them all as null we can initialize a LinkedList in each one! Now if two keys resolve to the same index in the array then their key/value pairs can be stored as a node in a linked list. Each index in the array is called a “bucket” because it can store multiple key/value pairs.

Since different keys can lead to the same bucket it’s important to store the entire key/value pair in the bucket, not just the value. The key must be stored with the value! If only values were stored in buckets then it would be impossible to determine which value to return when a key led you to a bucket.

This is similar to the original neighborhood names stored in an array with their zip codes shown earlier.

Here’s an actual example of just one bucket in a real hash map. In this example the two different keys "Pioneer Square" and "Alki Beach" happen to ultimately resolve to the same bucket. When we look at the bucket we see a representation of the Linked List that exists there. Pioneer Square was added first, so it’s at the front of the list. Then there’s Alki Beach as the second element in the linked list. Notice that both of them store the entire key/value pair.

hashMap.Add("Pioneer Square", 98104);
hashMap.Add("Alki Beach", 98116);
Bucket 92: [{Pioneer Square: 98104} --> {Alki Beach: 98116}]
If we didn’t store the key, the bucket would look like this. Accessing .get("Pioneer Square") or .get("Alki Beach") would hash the keys and still lead to bucket 92, but it would be impossible to tell which of the zip code values there to return.

Bucket 92: [{98104} --> {98116}]
Hash maps do this to store values:

accept a key
calculate the hash of the key
use modulus to convert the hash into an array index
store the key with the value by appending both to the end of a linked list
Hash maps do this to read value:

accept a key
calculate the hash of the key
use modulus to convert the hash into an array index
use the array index to access the short LinkedList representing a bucket
search through the bucket looking for a node with a key/value pair that matches the key you were given
Hashmap Example:
Hash Code Examples
Consider these