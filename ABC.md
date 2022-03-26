# ABC

## 086
B - 1 21 : 平方数かどうかを判定
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

## 087
A : お買い物、お釣り計算
```java
import java.util.Scanner; // スキャナーだけ

public class Main {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int x = sc.nextInt(); // 所持金
    int a = sc.nextInt(); // a値段
    int b = sc.nextInt(); // b値段
    
    System.out.println((x - a) % b); // aは1つ購入、bは買えるだけ購入、余った金額がお釣り
  }
}
```
