# 第一回　アルゴリズム検定

## A
2倍チェック　例外処理
```java
import java.util.Scanner;
 
public class Main {
  public static void main(String[] args) {
  Scanner sc = new Scanner(System.in);
  String sNum = sc.next();
    try {
      int num = Integer.parseInt(sNum);
      System.out.println(num * 2);
    } catch (Exception e) {
      System.out.println("error");
    }
  }
}
```
