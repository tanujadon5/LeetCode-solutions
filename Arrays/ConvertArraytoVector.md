## using Range Based Constructor

#### In C++. vector class provides a constructor which accepts a range i.e.(start, end). It creates a vector from all the element in the given range i.e. from start to end-1.
#### To create a vector from all elements in an array, pass the array elements as range i.e. arr and arr + N, where N is the number of elements in array. 
```c int arr[] = {1, 3, 4, 7, 8, 9};
    // Create a vector from array
    vector<int> numbers(arr, arr + sizeof(arr) / sizeof(int));
    // Print all elements of vector on console
    for(const auto & elem: numbers) {
        cout<<elem<< ", ";
    }
 ```
