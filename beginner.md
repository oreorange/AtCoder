#ABC

## B-1 21 : 平方数かどうかを判定
```java
import java.util.*; // スキャナー使うため

public class Main {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    String a = sc.next();
    String b = sc.next();
    String jj = a + b; // aとbを横並びにするためにString

    int ab = Integer.parseInt(jj); // abを整数型に変更
    double heihokon = Math.sqrt(ab); // 平方根を求める
    
    if(heihokon % 1 == 0) { // 1で割ってあまりが出なければ整数
      System.out.println("Yes");
    } else {
      System.out.println("No");
    }
  }
}
```
