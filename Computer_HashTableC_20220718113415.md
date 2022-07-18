## Hash table theory
### Definitions
- Associative array : AKA Map, Symbol Table or Dictionary. Implements three main methods : search; insert; delete
- Hash table :AKA hash map, map,dictionary. Associative array making use of hash function 
### Characteristics 
- Hash table is a really fast way to store and retrieve data
- It is made of *buckets*; which stores a key-value pair. The location of this bucket is defined using a hash function
- The bucket position is therefore linked to an integer
- To retrieve the position of a bucket ; we pass the integer to the hash function which give us the index
- This permits to have an array indexing complexity; which is only O(1) complexity
## Hash function
- Function that takes a string as input; return a number between 0 and m (m the array length)
- This is done by computing a big integer on string characteristics and then reducing its size using modulus

instance of computing hash integer: `hash += (a ** (string_len - (i+1))) * char_code(string[i])`; where a is a prime number and i variable between 0 and string length
- The issue with hash is the **pathological set**. It is a set that always return the same hash value for differents inputs.
- Perfect hash function does not have pathological set; but such function does not exist
- The pathological set introduce a new complexity O(n) which can be used for DOS attacks schemes
### Handling collisions
- The input of a hash function is infinite but the output is finite; collision therefore exists
- To handle this issue; we need a technique : **double hashing**
- This is given by : `index = hash_a(string) + i * hash_b(string) % num_buckets` where i is the number of collision
### Resizing
- We need to dynamically handle the array size for performance reasons
- The array size must be a prime; thereforce we must handle that too
