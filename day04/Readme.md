**Arrays**
Elements in array are stored in continous locations.

`Arrays in golang are of fixed length. once size is declared we cannot change it.`
`Elements should be of same datatype`
`Array have property called length and capacity. Length denoted no. of elements in the array and capacity denotes how much elements can an array contain.`
```
synatax:
var <array_name> [<size_array>] <data_type>
var grades [5] int
```

```
Array initialization:
var grades [3]int = [3] int{10,20,30}
------------------------------
grades := [3] int {10,20,30}
------------------------------
grades := [...] int {10,20,30}
```

***Functions on array:***
`len() -> The length of the array refers to the number of elements stored in the array, take array as input and returns the size of an array.`
```
Indexes in array :
1st index : 0
last index : length-1 
arr[0], arr[2]

for i:=0; i<=len(grades); i++ {
    fmt.Println(grades[i])
}

Looping through an array:
 for index, element := `range` grades {
     fmt.Println(index, "=>", element )
 } 
 
range keyword is mainly used for iterating all the elements in an array, slice or map.
For arrays, range set the scope of iteration upto the length of the array.
 ```
-------------------------------------------------------------------------
SLICE:
` Slice is defined as a continious segment of underlying array and it provides access to numbered sequence of elements from that area.`
1. Slice provides to a part of array in sequential order.
2. They are more flexible and powerful than array since array have limitations of being fixed size.
3. We can add or remove elements from slice
4. More flexible.

Declaring and initializing a slice
`<slice_name> := []<data_type>{<values>}`
`grades := []int{10, 20, 30}`
