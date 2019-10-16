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

`l.rfind(1)` *# return the last occurence of 1*                    

### Assign
`l = [1,2,3]`        
`l[:] = [2,3,1]` *# in-place reassignment to existing variable l*          
`l = [2,3,1]` *# make variable l point to a new array object*             

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
`str.isdigit()` *check whether str is digit*               

## [ Dictionary ]  

### Sort  
```
best_item = sorted(dict.items(), key=lambda item: item[1])[0]  
best_key = best_item[0]  
best_value = best_item[1]  
```

`best_item = sorted(dict.items(), key=lambda item: (item[1], item[0]))[0]` *# tie-breaker with key value (item[0])*        

```
heap = [(-freq, word) for word, freq in count.items()]
heapq.heapify(heap)
top_k_freq = [heapq.heappop(heap)[1] for _ in range(k)]
```

### Ordered Dictionary 
*From Python 3.7 insertion order is guaranteed for ordinary dictionary as well*           
```
self.dic = collections.OrderedDict()
val = self.dic.pop(key) 
self.dic.popitem(last=False) 
self.dic.move_to_end(key)
```       


## [ Set ]   
`s = set([])`     
`s.add(1)` *# in-place*      
`s.remove(1)`               
`s = s | {1}` *# union, using or functionality*        

`set([1,2,3]) & set([2,3])` &rarr; `set([2,3])` *# get intersection*       

`set([1,2,3]) - set([2,3])` &rarr; `set([1])` *# get difference*       
`set([1,2]) - set([1,2,3])` &rarr; `set([])`                       
`set([1,2]) ^ set([1,2,3])` &rarr; `set([3])` *# get symmetric difference*       



## [ Function ]
### Nested functions
```
def main() :
  x = 1
  def add(y) :
	nonlocal x # make x accessible (read/write)
	x+=y
  add(2)
  print(x) # 3 
``` 

```
def main() :
  x = []
  def add(y) :
	x.append(y) # iterables can be accessed without the nonlocal keyword 
	add(2)
  print(x) # [2] 
``` 

## [ Heap ]
```
import heapq

heap = []
heapq.heappush(heap, e)
heapq.heappop(heap)
```
*descending by default*          
