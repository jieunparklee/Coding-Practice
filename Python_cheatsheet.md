# Python Cheatsheet 

## [ List ]

### Reverse
`l = l[::-1]` *# [start:stop:step]*  
`l.reverse()` *# in-place*  

### Sort
`l = sorted(l)`  
`l.sort()` *# in-place*  
`l.sort(key=len, reverse=True)` *# sort by length, reverse (longer strings come first)*  
**key can be any function that returns a comparable value** 

### Add element 
`l = l + [1]` 
`l.append(1)` *# in-place*  

### Matrix 
`[[0 for _ in range(b)] for _ in range(a)]` *# a by b matrix*  

## [ String ]  

`str = str.lower()`  `str = str.upper()`  
`str = str.replace(" ", "")`    
`str = str[::-1]`  

`sorted_str = "".join(sorted(str))`  

`list_chars = list(str)` *# str &rarr; list of chars*
