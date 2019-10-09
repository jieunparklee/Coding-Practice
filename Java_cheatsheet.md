# Java Cheatsheet 

## [ Array ]

### Initialize
`int[] data = new int[5];`         
or            
`int[] data = {0, 1, 2, 3, 4, 5};`         


### Reverse
`Collections.reverse(Arrays.asList(a));` *reversing an array*  

```
char[] inputArray = input.toCharArray(); 
Collections.reverse(Arrays.asList(inputArray));
```
*reversing a string*

### Sort
`import java.util.Arrays;`       
`Arrays.sort(arr);` *in-place*                 
`Arrays.sort(arr, 1, 5);` *# only sort from index 1 to 4*     f

### Length 
`arr.length` *For string it is `str.length()`*    

### Subarray
`int[] ints1 = Arrays.copyOfRange(ints, start, end+1);` 

## [ ArrayList ]

### Accessing elements 
```
lst.add(el);
lst.get(idx);
```

### Sort 
```
Collections.sort(letterList, (o1, o2) -> {
            String[] s1 = o1.split(" ");
            String[] s2 = o2.split(" ");
            for (int i=1; i<Math.min(s1.length, s2.length); i++) {
                if (!s1[i].equals(s2[i])) {
                    return s1[i].compareTo(s2[i]);
                }
            }
            return s1[0].compareTo(s2[0]);
        }); 
```         

*Arrays.sort() works for Arrays with primitive data types, Collections.sort() works for objects, Collections like ArrayList, LinkedList* 

### Length
`lst.size()`          
                

## [ Loops ]
```
for (int i = 0; i < 5; i++) {
  System.out.println(i);
}
```

```
int i = 5;
while i != 0 {
  System.out.println(i);
  i--;
}
```

## [ HashMap ]
```
import java.util.HashMap; 

Map<String, Integer> map = new HashMap<>(); 
map.put("apple", 10); 
map.put("banana", 5);

if (map.containsKey("apple")) {
	System.out.println(map.get("apple");
}

```

## [ String ]
```
String str = "Hello World !";
String[] strArr = str.split(" ");
```                                    
*strArr: {"Hello", "World", "!"}*

```
char[] chars = {'a','p','p','l','e'};
String str = new String(chars); 
```      

`ch = str.charAt(0); `      

```
str1.equals(str2);
str1.compareTo(str2);
```           


## [ Stack ]
```
Stack<Integer> st = new Stack<Integer>();
st.push(new Integer(1));
Integer a = (Integer) st.pop();
```

## [ Casting ]
```
Integer.toString(int1);
Double.parseDouble(strD);
Integer.parseInt(strI);
```



