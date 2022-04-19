# 第一回　アルゴリズム検定

## A 2 倍チェック　例外処理

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

## B 　増減管理　配列の使い方

```java
import java.util.*;

public class Main {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int N = sc.nextInt(); // 何日分のデータを受け取るか決める
    int[] A = new int[N]; // 日数分の配列Aを作る
    for(int i = 0; i < N; i++) {
      A[i] = sc.nextInt(); // i を 0 で初期化したので最初の配列が入る
    }

    // int i = 0;
    // while(i <= A.length) {
    for(int i = 0; i < A.length - 1; i++) {
      int tmp = A[i + 1] - A[i]; // [i + 1] にすることで前日のデータと比較できる

      if(tmp == 0) { // 比較結果が一緒の場合、売上が変わらないので、stayを出力
        System.out.println("stay");
      } else if(tmp < 0) { // 比較結果が0より小さい場合、売上が下がったことになるので、downを出力
        System.out.println("down " + Math.abs(tmp)); // 絶対数に変換
      } else {
        System.out.println("up " + tmp);
      }
    // i++;
    }
  }
}
```

## C 　 3 番目　配列並び替え

```java
import java.util.Scanner;
import java.util.Arrays;

public class Main {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int[] array = new int[6];
      for(int i = 0; i < array.length; i++) {
      array[i] = sc.nextInt();
      }

    Arrays.sort(array); //昇順に並び替え
    System.out.println(array[3]);

  }
}
```

## D 重複検査

```java

```

## D 重複検査

```java

```
