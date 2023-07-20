---
title: "Java CheatSheet"
date: 2021-06-24T16:33:52-05:00
draft: false
tags: ["Java","Programming"]
categories: ["Programming Language"]
slug: "java-cheatsheet"
subtitle: "Common used Java code"
description: "Common used Java code"
keywords: 
- Java
- Programming
- Gramma
---

# Some Java to know

## Matrix

    int m = nums.length;
    int n = nums[0].length;

    // Reshape matrix
    for (int x = 0; x < m * n; ++x) {
        ans[x / c][x % c] = nums[x / n][x % n];
    }

## Collections

    Collections.swap(vector, 0, 4);
    Collections.reverse(row);   // row is ArrayList<>()

## Stack

    Stack<Integer> s1 = new Stack<Integer>();
    Stack<ListNode> stack = new Stack<ListNode>();
    stack.pop().val;
    stack.push(temp);
    stack.isEmpty();
    stack.peek();
    stack.size();

## Queue

    Queue<Integer> Q = new LinkedList<Integer>();
    Q.size();
    Q.poll();
    Q.offer();
    Q.peek();


## Dequeue

Queue in Java: https://dumbitdude.com/queue-in-java/

Deque: https://www.geeksforgeeks.org/deque-interface-java-example/

Double ended queue, allows LIFO and FIFO

    Deque<String> dq = new LinkedList<>();
    dq.addLast(); = dq.add(); = dq.offer();
    dq.addFirst(); = dq.push(); = dq.offerFirst();
    dq.removeFirst();
    dq.removeLast();
    dq.peekFirst();
    dq.peekLast();

## Heap

https://blog.csdn.net/xiaolinnulidushu/article/details/104629479

MinHeap

    PriorityQueue<Integer> heap = new PriorityQueue<>();
    heap.offer(num);
    heap.poll();
    heap.peek();


MaxHeap

    PriorityQueue<Integer> pQueue = new PriorityQueue<Integer>(Collections.reverseOrder());
    // 默认是小根堆，实现大根堆需要重写一下比较器。
    Queue<Integer> pq = new PriorityQueue<>((v1, v2) -> (v2 - v1));
    Queue<Integer> B = new PriorityQueue<>((x, y) -> (y - x));

## Integer

    Integer.MAX_VALUE
    Integer.MIN_VALUE

Parse string to integer

    Integer.parseInt(s);

## long

    long pre = Long.MIN_VALUE;

## LinkedLIst

    ListNode[] A = new ListNode[100];
    ListNode cur = head;

    ListNode cur = new ListNode();
    ListNode res = cur;
    //用cur操作, return res;

    同理
    ListNode cur = head;
    用cur操作
    return head;

    // Initialzie 一个linkedlist需要 list type
    String [] a = new String[] { "A", "B", "C", "D" };
    List<String> list = Arrays.asList(a);

Dummy: // dummy --> head --> node1 --> node2 --> null

    ListNode dummy = new ListNode(0); dummy.next = head;      // 新List，头部为0，指向head
    //或者 ListNode dummy = new ListNode(0,head);

    ListNode tmp = dummy;   // 复制了一份，为了操作，return的时候return dummy.next，因为dummy仍然在头部

    //Use tmp to iterate      // 进行操作

    return dummy.next;      // dummy的value是0，.next则是答案


    ListNode()
          Creates a completely blank ListNode
    ListNode(java.lang.Object data)
          Creates a new ListNode containing the specified data type.
    ListNode(java.lang.Object data, ListNode next)
          Creates a new ListNode object containing specified data and next references.


    LinkedList tmp = new LinkedList<>();
    tmp.addLast(node.val);
    tmp.addFirst(node.val);
    tmp.getLast();
    tmp.add(0, val);

## ArrayList

    List<List<Integer>> res = new ArrayList<>();
    List<Integer> arr = new ArrayList<>();

    arr.set(loc,value); // Insert value
    arr.add(x); // Append value
    arr.addAll(x) // ON
    arr.remove(3); // Remove by index
    arr.contains(5);

    // convert to List<Integer>
    Integer [] myarr = new Integer [];
    Arrays.asList(myarr);

    int[] numbers = {10 20, 30, 40};
    int[] arr = new int[size];
    Arrays.fill(arr, 0);
    int[][] numMatrix = { {1, 2, 3, 4}, {5, 6, 7, 8}};

    // Convert hashset to ararylist
    return new ArrayList<>(myset);

Convert arraylist/linkedlist to array

    1D:
    LinkedList<Integer> list = new LinkedList<Integer>();
    int[] a = list.toArray();

    toArray <---> asList

    2D:
    List<int[]> res = new ArrayList<>();
    int [][] array = res.toArray(new int[res.size()][]);

Convert Set to array // set --> String[]

    HashSet<String> ans = new HashSet<String>();
    ans.toArray(new String[0]);

## Arraylist vs Linkedlist

```
        ArrayList               LinkedList
        dynamic array           doubly linked list
        slow                    fast
        act as a list           act as a list and queue

```

### ArrayList Operations:

    arr.set();
    arr.add();
    arr.get();
    arr.size();

## Array

```
Initialization:
int[] myIntArray = new int[3];
int[] myIntArray = {1, 2, 3};
int[] myIntArray = new int[]{1, 2, 3};
String[] myStringArray = new String[3];
String[] myStringArray = {"a", "b", "c"};
String[] myStringArray = new String[]{"a", "b", "c"};
myStringArray = new String[]{"a", "b", "c"};

Copy: Can also use .clone();
    int[] a = new int[]{1,2,3,4,5};
    int[] b = a.clone();
    Arrays.copyOfRange(intersection, 0, index);
    copyofrange其实是复制从 0 至 index-1个elements     （arr, inclusive, exclusive）

Sort:
    Arrays.sort(arr);
    Arrays.sort(arr, (a,b) -> Integer.compare(a[0], b[0]));      // 2D: int[][] arr;
    Arrays.sort(a, Collections.reverseOrder()); // reverse order


Return:
return new int[]{1,2};
return new String(result);  // char[] result = {'a','b'};

Return null array:
return new int[0]; or return new int[]{};

// 2d return null
return new int[0][]

```

New:
The elements in the array allocated by new will automatically be initialized to zero (for numeric types), false (for boolean), or null (for reference types)

## Math

    Math.max(1,2);
    Returns the highest value
    Math.pow(10,2);
    returns double
    Round up
    Math.ceil(125.9)=126.0
    Math.ceil(0.4873)=1.0
    Math.ceil(-0.65)=-0.0

    Generate random number
    https://stackoverflow.com/questions/5887709/getting-random-numbers-in-java

    import java.util.Random;

    Random rand = new Random();    
    int n = rand.nextInt(50); // Obtain a number between [0 - 49].

    double random = Math.random() * 49 + 1;
    // or
    int random = (int )(Math.random() * 50 + 1);

    random() method returns a random number between 0.0 and 0.9..., you multiply it by 50, so upper limit becomes 0.0 to 49.999... when you add 1, it becomes 1.0 to 50.999..., now when you truncate to int, you get 1 to 50. 

# String

```
public String reverseWords(String s) {
String[] splited = s.trim().split("\\s+"); // split by whitespace
Collections.reverse(Arrays.asList(words));
return String.join(" ", words);

Substring
    s.substring(lo, lo + maxLen);

eg.
    String s1="javatpoint";
    System.out.println(s1.substring(2,4));//returns va   (invlusive, exclusive)
    System.out.println(s1.substring(2));//returns vatpoint

// Comparsion
    s.equals("happy");
    Can't use s == "happy"

Check char in string:
    str.charAt(index);

Convert：convert char[] to a string
char[] mychararr = s.toCharArray(); // [a,b,c,d]
1. mystr = String.valueOf(mychararr);  // CAN NOT just use mystr = mychararr.toString();
2. return new String(mychararr)
--> "abcd"

// to convert char[] to string Array Use toString
Arrays.toString(mychararr);
--> "[a, b, c, d]"


Indexof
System.out.println("FOO".indexOf("")); // outputs 0 wtf!!!
System.out.println("FOO".indexOf("bar")); // outputs -1 as expected
System.out.println("FOO".indexOf("F")); // outputs 0 as expected
System.out.println("".indexOf("")); // outputs 0 as expected, I think

```

# Character

Convert char to int

    int a = '15' - '0';
    int a = Integer.parseInt(String.valueOf('15'));

    Character.isDigit(c); // boolean

### StringBuilder

    StringBuilder mystr;
    mystr.append("a");
    mystr.append(4); appends the string representation of the int argument to this sequence
    mystr.deleteCharAt(10);
    sb.reverse().toString();

## length

    .length: // returns length of an array
    .length(): // returns length of a STRING

## loop traversal

To traverse a string, we can use:

```
for(String car: cars)
{expressions}
```

## Hashset declaration

    Set<Pair<Integer, Integer>> visited = new HashSet();
    HashSet<Integer> myset = new HashSet<Integer>();
    mySet.add ("First");
    myset.remove(x);
    myset.contains(y);

    for(int obj : set)
        if(obj.equals(2))
            return obj;


    Convert Haset set to array:
        int[] y = new int[set.size()];
        int c = 0;
        for(int x : set) y[c++] = x;

## HashMap

    Hashtable<Integer,String>; myTable= new Hashtable<Integer,String>();
    myTable.put(1, "John");

    if (map.containsKey("vishal"))
    Integer a = map.get("vishal");

    // Init
    HashMap<Integer, Integer> [] rows = new HashMap[9];
    for (int i = 0; i < 9; i++) {
      rows[i] = new HashMap<Integer, Integer>();

    Character:
    HashMap<Character,Integer> mymap = new HashMap<Character,Integer>();
    HashMap<Integer,String> myMap= new HashMap<Integer,String>();
    myMap.put(1, "First");

    常用：
    for(int num : nums1)
        mymap.put(num,mymap.getOrDefault(num,0) + 1);

    for (Integer a : map.keySet()) {
        if(map.get(a) == 1) return a;
        }

Common Use

    int count = map.getOrDefault(num, 0);  // returns valuce at pos num, or return 0

Return map as arraylist

    return new ArrayList<>(mymap.values());

Map.Entry is a key and its value combined into one class. This allows you to iterate over Map.entrySet() instead of having to iterate over Map.keySet(), then getting the value for each key. A better way to write what you have is:

```
for (Map.Entry<String, JButton> entry : listbouton.entrySet())
{
  String key = entry.getKey();
  JButton value = entry.getValue();

  this.add(value);
}
```

Initiazliation

```
// this works for up to 10 elements:
Map<String, String> test1 = Map.of(
    "a", "b",
    "c", "d"
);

// this works for any number of elements:
import static java.util.Map.entry;
Map<String, String> test2 = Map.ofEntries(
    entry("a", "b"),
    entry("c", "d")
);
```

## TreeSet (basically a sorted hashset)

```
TreeSet<Long> set = new TreeSet<Long>();
set.ceiling(x);
The ceiling() method of java.util.TreeSet<E> class is used to return the least element in this set greater than or equal to the given element, or null if there is no such element.
set.remove(x);
```

## TreeMap

Internally, for every element, the keys are compared and sorted in the ascending order.
tree_map = new TreeMap<Integer, String>();

## Final

    final int myNum = 10; // Means myNum cannot be changed

## (? :)

    int score = 80;
    int reward = (store >= 80) ? 100 : 50;

## Method/Function

```
public class Student {
    String name;
    public Student() {
        name = "Samuel";
    }
    public static void main(String[] args) {
        Student student  = new Student();
        System.out.println(student.name);
    }
}
```

**Difference** between a method and a funtion is: A method is associated with an **object**, while a function is **not**

eg.

    myMethod(); // Function or method (means the same)
    var newstr = str.toUpperCase() // .toUpperCase() is the method

## Try Catch Finally

```
public static void main(String[] args) {
**Finally** block will **ALWAYS** execute when the try block exits

    try {
        System.out.println(0/1);
        int[] array = new int[]{1, 2};
        System.out.println(array[3]);
    } catch (Exception e) {
        System.out.println("An exception occurs.");
    } finally {
        System.out.println("After try...catch block");
    }
}
```

---

# Others

## Data types

```
byte	1 byte	Stores whole numbers from -128 to 127

short	2 bytes	Stores whole numbers from -32,768 to 32,767

int	    4 bytes	Stores whole numbers from -2,147,483,648 to 2,147,483,647

long	8 bytes	Stores whole numbers from -9,223,372,036,854,775,808 to -

float	4 bytes	Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits

double	8 bytes	Stores fractional numbers. Sufficient for storing 15 decimal digits

boolean	1 bit	Stores true or false values

char	2 bytes	Stores a single character/letter or ASCII values
```

## Build environment for the first time

### Download JDK

Typically, for **Mac** users: JDK will be stored under path:

```
/Library/Java/JavaVirtualMachines/jdk-10.jdk/Contents/Home
```

Follow steps below to add JAVA_HOME to your PATH in order to run Java under any path:

1. Login and open a Terminal or command line window
2. Open the ~/.bash_profile using vi or another command-line editor such as Pico. For example enter vi ~/.bash_profile.
3. Set your PATH to include the JDK sub-folder named java. For example:

```
export PATH=$PATH:/usr/java/jdk1.6.0_10/bin
```

4. Save the changes and either logout and then back in, or, to active the new settings enter source ~/.bash_profile

---

# To be reviewd

[Encapsulation/Inheritance/Polymorphism](https://turingplanet.org/2020/01/15/%e7%bb%a7%e6%89%bf%e5%92%8c%e6%8e%a5%e5%8f%a3%e3%80%90java%e5%85%a5%e9%97%a8%e6%95%99%e7%a8%8b6%e3%80%91/)
