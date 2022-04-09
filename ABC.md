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

## PracticeA Welcome to AtCoder

```java
import java.util.*;

public class Main {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int a = sc.nextInt();
    int[] bc = new int[2];
    for(int i = 0; i < 2; i++) {
      bc[i] = sc.nextInt();
    }
    String s = sc.next();
    int tmp = a + bc[0] + bc[1];
    System.out.println(tmp + " " + s);
  }
}
```

## 081 B : while 文と for 文, count, return, % 2 == 1

```java
import java.util.*;

public class Main{
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int N = sc.nextInt();
    int[] nums = new int[N];
    int count = 0;

    for(int i = 0; i < nums.length; i++) {
      nums[i] = sc.nextInt();
    }
    while(true) {
      for(int i = 0; i < N; i++) {
        if(nums[i] % 2 != 0) {
          System.out.println(count);
          return;
        }
      }
      for(int i = 0; i < N; i++) {
        nums[i] /= 2;
      }
      count++;
    }
  }
}
```
