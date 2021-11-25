### Hashing is a method for representing dictionaries for large datasets.

It allows lookups, updating and retrieval operation to occur in a constant time i.e. O(1).

After storing a large amount of data, we need to perform various operations on these data.

Linear search and binary search perform lookups/search with time complexity of O(n) and O(log n) respectively. As the size of the dataset increases, these complexities also become significantly high which is not acceptable.Hashing allows lookups to occur in constant time i.e. O(1).
 
The Hash table data structure stores elements in key-value pairs where
Key- unique integer that is used for indexing the values
Value - data that are associated with keys.

In a hash table, a new index is processed using the keys. And, the element corresponding to that key is stored in the index. This process is called hashing.
![alt-text](https://cdn.programiz.com/sites/tutorial2program/files/Hash-2_0.png)


Let k be a key and h(x) be a hash function.

Here, h(k) will give us a new index to store the element linked with k.

