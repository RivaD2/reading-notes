# What is A Hash Table

![ready](https://media.giphy.com/media/Tjju729rgJPPk8PMYA/giphy.gif)

In a previous [reading](https://rivad2.github.io/reading-notes/401/class-12.html) I spoke about hashing, encryption and encoding amongst other topics. A **hash** is the result of some algorithm taking an incoming string and converting into a value that could be used for security (or used for something else).

**A hash table is a data structure used to store information. This information will have some sort of key and value. It is a way we implement an [associative array](https://brilliant.org/wiki/associative-arrays/)**

- A hash table may also be called a hash, a hash map, unordered map or dictionary)
  
- We can take that associative array and then map keys to value
- Typically we will perform two steps when using hash tables:
    - A key is converted into an integer index by using a hash function
    - This index decides where the key-value pair record belongs

### Let's talk about the hash function:

- This function takes a key and converts it to a number which will be at a particular index (where it is stored)
- When initalizing the hash table we usually create an array containing a fixed number of buckets.
- A **bucket** is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
- After we have our array, we have to somehow turn that special key into a numeric number value. We typically do the following:
     - Add or multiply all the [ASCII](https://www.w3schools.com/charsets/ref_html_ascii.asp) values together
     - Multiple the key by a prime num such as 599
     - Use modulo to get the remainder of the result when divided by total size of array
     - Insert the array AT that index

### What about collisions?

- A collision is, as you might have guesssed, is when more than one key gets hashed to the same location of the hashtable
- Something important to note is that a **perfect hash will never have any collisions.

### Summary: How hash maps store values and read values

**Hash maps do this to store values:**

- Accept a key
- Calculate the hash of the key
- Use modulus to convert the hash into an array index
- Store the key with the value by appending both to the end of a linked list

**Hash maps do this to read value:**

- Accept a key
- Calculate the hash of the key
- Use modulus to convert the hash into an array index
- Use the array index to access the short LinkedList representing a bucket
- Search through the bucket looking for a node with a key/value pair that matches the key you were given
