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
*因為 class A implements Comparable<B>，所以 要 insert 的 method 要丟進去的參數要是形態B的東西*



