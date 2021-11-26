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


### HASH TABLE and MAP are the types of containers which store data with key-value combination. It means that particular data will have an special key and the value associated (mapped value) with this key. <key, value>

The implementation of HASH TABLE on C++ is unordered_map<> and the implementation of map on C++ is map<>.

Unordered_map<> and map<> work almost on the same principle, many similar functions but they have one main difference.

In unordered_map<> keys are not sorted and insertion of particular key takes O(1).
In map<> keys are in sorted order and the insertion of particular key will take O(logn).
This means that if you need keys to be in sorted order then it is better to use map<>, otherwise use unordered_map<>.

```cpp
unordered_map<int, int> q;
q[3]=7;

For map:
map<int, int> q;
q[3]=7;
```

we created <3, 7> combination and this means that in our q the key=3 will have the value=7 associated with it and if we want to print that:

```cpp
cout<<q[3]<<endl;

Output:7
```


