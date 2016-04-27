# Test 
## HW7 30423005 ##

### Q1 ###
    class A implements Comparable<B> {
    private int x,y;
    public A(int x, int y) {
    this.x = x;
    this.y = y;
    }
    public int getX() {return x;}
    public int getY() {return y;}
    public String toString() {
    return x+ “, “, +y;
    }
    // insert your codes
    }

Which code should be inserted to compile the program?
- A. public int compareTo(Object o) { /* contents of the method */}
- B. public int compareTo(A a) { /* contents of the method */}
- C. public int compareTo(B b) { /* contents of the method */}
- D. public int compareTo(Object o, B b) { /* contents of the method */}
 
*Ans*
`C. public int compareTo(B b) { /* contents of the method */}`
* 因為 class A implements Comparable<B>，所以 要 insert 的 method 丟進去的參數要是形態B的東西 *


### Q2 ###
    import java.util.*;
    class Execute{
    public static void main(String[] args) {
    ArrayList list = new ArrayList();
    list.add(“a”);
    list.add(1);
    list.add(“b”);
    list.add(2);
    Collections.sort(list);
    System.out.println(list);
    }
    }

What is the outcome of the program?
- A. compile time error
- B. run time exception
- C. [1, 2, a, b]
- D. [a, 1, b, 2]
 
*Ans*
`B. run time exception`
* 會錯在 `Collections.sort(list);` 這一行，因為他要sort的時候就要先比較大小，但是list裡面有 `Integer` 與 `String` 這兩種型態，在型態不同卻想要比較的情況下，就要先強制轉換其中一個的類型變成跟另一個類型相同，可是這樣就會出錯，所以後面要比較的時候根本也不能比。*
* 實際使用IDE執行的時候錯誤訊息也顯示*
    Exception in thread "main" java.lang.ClassCastException: java.lang.String cannot be cast to java.lang.Integer
	at java.lang.Integer.compareTo(Integer.java:52)
	at java.util.ComparableTimSort.countRunAndMakeAscending(ComparableTimSort.java:320)
	at java.util.ComparableTimSort.sort(ComparableTimSort.java:188)
	at java.util.Arrays.sort(Arrays.java:1312)
	at java.util.Arrays.sort(Arrays.java:1506)
	at java.util.ArrayList.sort(ArrayList.java:1454)
	at java.util.Collections.sort(Collections.java:141)
	at homeworks.A.main(A.java:22)
    Java Result: 1

