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
 #### To calculate the number of elements (N) in array, we divided the size of array by the size of the type of elements in array. Then we passed the range arr & arr + N in the vector constructor to create a vector from the array.
 
 
## using – begin() / end()

#### std::begin(arr) -> Return an iterator pointing to the first element of the array.
#### std::end(arr) -> Return an iterator pointing to the one after the last element of the array.
#### Get the the start & end of an array using begin() and end(). Then pass that to the vector constructor to create a vector from an array.
```c
// Create a vector from array
    vector<int> numbers(begin(arr), end(arr));
```

## Create an empty vector in C++ and add array elements to it

#### In vector, the insert() function accepts a position of the vector and a range (start, end) as arguments. Then inserts all the elements from the range into the vector at given position.
```c
// Create an empty vector
    vector<int> numbers;
    // Add array elements to vector
    numbers.insert(numbers.begin(), begin(arr), end(arr));
```

## using copy() algorithm

#### Create an empty vector. Then pass the array elements as range (start, end) to the copy() function as initial two argument and as the third argument pass the back_insert_iterator of the vector. It will copy all the elements of array into the vector. 
```c
// Create an empty vector
    vector<int> numbers;
    // Iterate over array elements and copy 
    // them to vector
    copy(   begin(arr),
            end(arr),
            back_inserter(numbers));
```


