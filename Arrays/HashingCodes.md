Key and value will have particular types and we can construct many combinations like that:

unordered_map<int, int> q1;
unordered_map<int, vector<int>> q2;
unordered_map<int, vector<vector<string>>> q3;
unordered_map<char, pair<int, char>> q4;
unordered_map<string, int> q5;
  
 ### insert other key and with its associated value:
  
  ```cpp
  unordered_map<int, int> q;

//1st way:
q.insert(make_pair(3, 7));

//2nd way:
q[3]=7;

//3rd way:
q.emplace(3, 7);
  ```
  
  ```cpp
  unordered_map<int, int> q;
q[3]=7;
cout<<q[3]<<endl;

q[3]=10;
cout<<q[3]<<endl;

Output: 7
        10
  ```
  
### To check does the particular key exists or not:

```cpp
unordered_map<int, int> q;
int ourkey=3;

//1st way:
q.count(ourkey)>0;

//2nd way:
unordered_map<int, int>:: iterator z;
z=q.find(ourkey);  
if(z == q.end()){
   cout<<"This key does not exists"<<endl; 
}
else{
    cout<<z->first<<" "<<z->second<<endl;
}

//and if you want to delete and remove that key with its value from q you can use:

//1st way:
q.erase(ourkey);   // deletion by key

//2nd way:
q.erase(z);      // deletion by iterator
```
 ## Find() 
#### find function in C++ is used to search for a specific key in an unordered map.
####   unordered_map.find(key);
#### Parameters: It takes the key as a parameter.

#### Return values: If the given key exists in unordered_map it returns an iterator to that element otherwise it returns the end of the map iterator.
  
  ## Count()
####  count() is a builtin method in C++ which is used to count the number of elements present in an unordered_map with a given key.
####  Parameters: This function accepts a single parameter key which is needed to be checked in the given unordered_map container.
####  Return Value: This function returns 1 if there exists a value in the map with the given key, otherwise it returns 0.
  ```cpp
   // Check if element with key 1 is present using 
    // count() function
    if(umap.count(key))
    {
        cout<<"Element Found"<<endl;
    }
    else
    {
        cout<<"Element Not Found"<<endl;    
    }
  ```
  
##  Traverse unordered_map<>:
```cpp
unordered_map<int, int> q;
for(int i=1;i<=3;i++){
	 q[i]=i+1;                                    // construct pairs, I mean key-value combinations
}

for(auto z=q.begin();z!=q.end();z++){   //traversing from beginning till end
     cout<<"key is "<<z->first<<" and the value is "<<z->second<<endl; 
}

for(auto z=q.rbegin();z!=q.rend();z++){   //traversing from end till beginning
     cout<<"key is "<<z->first<<" and the value is "<<z->second<<endl; 
}
	```
  ## Insert keys as vector elements and value as the count of elements present in vector
  
  ```cpp
  unordered_map<int, int> q;
        for(int i=0;i<nums.size();i++){
            if(q.count(nums[i])>0){
                q.at(nums[i])=q.at(nums[i])+1;         //my value is the frequncy of key
            }
            else{
                q.insert(make_pair(nums[i], 1));// insert nums[i] as key and 1 as value
             }
        }
 ```
  other way
  ```cpp
  for(int i=0;i<nums.size();i++){
		      q[nums[i]]++;           //q[nums[i]] as key is inserted and by default value was 0 but with++ value became 1
        }
  ```
 
                                  
