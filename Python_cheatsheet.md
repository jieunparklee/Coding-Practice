# Python Cheatsheet 

## [ List ]

### Reverse
`l = l[::-1]` *# [start:stop:step]*  
`l.reverse()` *# in-place*  

### Sort
`l = sorted(l)`  
`l.sort()` *# in-place*  
`l.sort(key=len, reverse=True)` *# sort by length, reverse (longer strings come first)*  
`l.sort(key=lambda e: len(e), reverse=True)` *same functionality as above*           
**key can be any function that returns a comparable value** 

### Add element 
`l = l + [1]`   
`l.append(1)` *# in-place*  

### Matrix 
`[[0 for _ in range(b)] for _ in range(a)]` *# a by b matrix*  

### Count
`l.count(1)` *# count the number of 1s in list l*              
**works for string as well**   

### Index
`l.index(1,k)` *# return the first occurence of 1 after index k (inclusive) in l*           
**works for string as well**     

`l = [0,1,2]`  
`l[5]` *# IndexError: list index out of range*    
`l[5:]` &rarr; `[]` *# Slicing out of range works*   
`l[:5]` &rarr; `[0,1,2]`   

### Tree representation
node : i     
left child : 2i+1    
right child : 2i+2     

## [ String ]  
*str is immutable*

`str = str.lower()`  `str = str.upper()`  
`str = str.replace(" ", "")`    
`str = str[::-1]`  

`sorted_list = sorted(str)` *# str &rarr; list of sorted chars*    
`sorted_str = "".join(sorted(str))`  

`list_chars = list(str)` *# str &rarr; list of chars*

`str_list = str.split()` *# split str by space : "   hello   world  !" &rarr; ['hello', 'world', '!']*

## [ Dictionary ]  

### Sort  
```
best_item = sorted(dic.items(), key=lambda item: item[1])[0]  
best_key = best_item[0]  
best_value = best_item[1]  
```