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

## 083 B : 無限ループになってしまう、失敗例

```java
import java.util.*;

public class Main{
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int n = sc.nextInt();
    int a = sc.nextInt();
    int b = sc.nextInt();
    int tmp = 0;
    int num = 0;
    int o = 0;
      
    for(int i = 1; i <= n; i++) {
      o = i;
      while(0 < i) {
        tmp += (i % 10);
        i = (i / 10);
      }
      if(a <= tmp && tmp <= b) {
      num += o;
      }
      
    }
    System.out.println(num);
  }
}
```

## 083 B : メソッド定義、各桁の和の求め方

```java
import java.util.*;

public class Main{
  // 各桁の和を求めるメソッドを作る
  public static int someSum(int num) {
    int tmp = 0;
    while(0 < num) {
      tmp += num % 10;
      num /= 10;
    }
    return tmp;
  }
  
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int n = sc.nextInt();
    int a = sc.nextInt();
    int b = sc.nextInt();
    int nums = 0;
    
    for(int i = 1; i <= n; i++) { // n回繰り返す
      int tmp = someSum(i); // someSumメソッドのnumに i を代入してif文判定に使用
      if(a <= tmp && tmp <= b) {
      nums += i;
      }
    }
    System.out.println(nums);
  }
}
```


## 088 B : 配列並べ替え Integer型 ラッパークラス

```java
import java.util.*;

public class Main{
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int n = sc.nextInt();
    Integer[] a = new Integer[n]; // int型から、Integer型に変更
    int alice = 0;
    int bob = 0;
    for(int i = 0; i < n; i++) {
      a[i] = sc.nextInt();
    }
    
    Arrays.sort(a, Collections.reverseOrder()); // 昇順なら ,(コンマ)以降必要なし
    // 降順はint型はダメらしいので、Integer型に変更
    for(int i = 0; i < n; i++) {
      if(i % 2 == 0) {
        alice += a[i];
      } else {
        bob += a[i];
      }
    }
    System.out.println(alice - bob);
  }
}
```

## 085 B : 配列の重複

```java
// import java.util.*;
import java.util.Scanner;
import java.util.HashSet;
import java.util.Arrays;

public class Main{
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int N = sc.nextInt();
    int[] d = new int[N];
    for(int i = 0; i < N; i++) {
      d[i] = sc.nextInt();
    }
    
    HashSet hs = new HashSet(); //重複を排除して要素を格納するクラス
    int count = 0;
    for(int i = 0; i < N; i++) {
      hs.add(d[i]);
      // count++; 重複は弾けるがカウントされる
    }
    // System.out.println(Arrays.toString(d));
    // System.out.println(hs.length); // .length では要素数を取得できない、なぜ？
    System.out.println(hs.size());
  }
}
```

## 207 A : 

```java
// import java.util.*;
import java.util.Scanner;
// import java.util.HashSet;
import java.util.Arrays;

public class Main{
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int[] num = new int[3];
    for(int i = 0; i < 3; i++) {
      num[i] = sc.nextInt();
    }
    Arrays.sort(num);
    System.out.println(num[1] + num[2]);
  }
}
```

## 001 B : 

```java

```

## 001 B : 

```java

```
