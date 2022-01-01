## Java Overview (no longer updated)

Math Functions:<br>
``` Math.pow(a,b); // returns a double, so make sure to type cast to int (int) ```<br>
Sort an array<br>
```Arrays.sort(nameOfArray);```

Arrays<br>
int array<br>
``` int a[] = new int[5] ```

List is an interface in Java. You need to instantiate the actual implementation, be it ArrayList or LinkedList, to use a List.<br>
``` List<String> myList = new ArrayList<String>(); ```<br>
``` myList.get(0); // Access first element ```<br>
``` myList.add(5); // Add five as an element ```<br>
``` myList.remove(0); // Remove first element ```<br>
``` myList.size(); // Gets the Length ```<br>

2D Arrays<br>
``` List<List<Integer>> list = new ArrayList<List<Integer>>(); ```<br>
Then add rows when necessary<br>
``` list.add(new ArrayList<Integer>()); ```<br>


Sets:<br>
``` Set<Integer> set = new HashSet<Integer>(); ``` <br>
associated functions: contains(value);

Maps<br>
``` Map<String, Integer> myHashMap = new HashMap<String, Integer>(); // key value pairs```
