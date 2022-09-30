### Task 7kyu:

You might know some pretty large perfect squares. But what about the NEXT one?
Complete the findNextSquare method that finds the next integral perfect square after the one passed as a parameter. 
Recall that an integral perfect square is an integer n such that sqrt(n) is also an integer.
If the parameter is itself not a perfect square then -1 should be returned. You may assume the parameter is non-negative.

[Task link](https://www.codewars.com/kata/56269eb78ad2e4ced1000013/train/java)

#### Solution:
```
public class NumberFun {
  public static long findNextSquare(long sq) {
      long result; 
      double d = Math.sqrt(sq);
      if ( d % 1  == 0) result = (long) Math.pow(++d, 2);
      else result = -1;
      return result;
  }
}
```

#### Fav solution:
```
public class NumberFun {
  public static long findNextSquare(long sq) {
      return Math.sqrt(sq) % 1 != 0 ? -1 : (long)Math.pow(Math.sqrt(sq)+1,2);
  }
}
```

#### Comment:
The best design solution, which is different from mine.


### Task 8 kyu:

Complete the function that calculates the area of the red square, when the length of the circular arc A is given as the input. 
Return the result rounded to two decimals.

[Task link](https://www.codewars.com/kata/5748838ce2fab90b86001b1a)

### My solution:

```
public class Geometry{
  public static double squareArea(double A){
    double B = 2* A / Math.PI;
    B *= B;
    String formattDouble = String.format("%.2f", B);
    B = Double.parseDouble(formattDouble);
    return B;
  }
}
```

### Fav solution:

```
public class Geometry{
  public static double squareArea(double A) {
    return Math.round(400 * A * A / 3.141592 / 3.141592) / 100.;
  }
}
```

#### Comment:
The person did not try to solve through Math.Pi, but simply wrote.
