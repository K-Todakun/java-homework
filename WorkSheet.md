author: Kanta Toda
summary: WorkSheet
id: WorkSheet
categories: codelab,markdown
environments: Web
status: Published
feedback link: 
# Javaプログラミング

## 授業の復習-課題1

### 課題1

以下の仕様をもとにコードを書いてみよう。

2つの32ビット整数を入力し、足し算を行いなさい。
足し算を行うクラスを用意し、コンストラクタで初期化しなさい。
Mainクラスで2つの値を入力し、足し算クラスに渡して、戻り値で、結果を取得し表示しなさい。

以下はこの問題を解くにあたっての解説です。

> 値を入れるための箱＝2つの32ビット整数

これは、変数を用意するということです。
Javaでは、フィールド変数といいます。
つまり、32ビット整数型のフィールド変数を2つ用意します。

足し算をするクラスをCalcAddクラスとします。
その中に32ビット整数型のフィールド変数を2つ用意するとこのようになります。

```CalcAdd.java
public class CalcAdd {
    private int a;
    private int b;    
}
```

> コンストラクタで初期化しなさい。

コンストラクタで初期化するということは、以下のようなコードになります。

```
public class CalcAdd {
    private int a;
    private int b;

    public CalcAdd(int a, int b) {
        this.a = a;
        this.b = b;
    }
}
```

> Mainクラスで2つの値を入力

入力するために、Scannerをインスタンス化すること。入力された値を保持するための変数を用意することを行わなければいけません。
コードでは以下のようになります。

```
public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("足し算したい値を入力してください。");
        System.out.print("1つ目：");
        int a = input.nextInt();
        System.out.print("2つ目：");
        int b = input.nextInt();
    }
}
```

> CalcAddの足し算をするメソッド

```
public class CalcAdd {
    private int a;
    private int b;
    public CalcAdd(int a, int b) {
        this.a = a;
        this.b = b;
    }
    public int add(){
        return a+b;
    }
}
```

> CalacAddクラスに渡して、戻り値で、結果を取得し表示しなさい。

Mainクラスで、CalcAddクラスをインスタンス化し、入力した値を渡します。
そして、CalcAddクラスの足し算メソッドを呼び出します。戻り値で結果が帰ってくるので、その値を入れる変数を用意します。
最後に、その値を表示します。

```
public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("足し算したい値を入力してください。");
        System.out.print("1つ目：");
        int a = input.nextInt();
        System.out.print("2つ目：");
        int b = input.nextInt();
        CalcAdd calcadd = new CalcAdd(a,b);
        int sum = CalcAdd.add();
        System.out.println("合計は" + sum + "です。");
    }
}
```

以上で、おしまいです。

## 授業の復習-課題2

### 課題2

課題1を参考に、以下の仕様通りにプログラムを作成しなさい。

2つの32ビット整数を入力し、掛け算を行いなさい。
掛け算を行うクラスを用意し、コンストラクタで初期化しなさい。
Mainクラスで2つの値を入力し、掛け算クラスに渡して、戻り値で、結果を取得し表示しなさい。

## 授業の復習-課題3

### 課題3

![BMIのクラス図](WorkSheet/img/BMI.png) 

## 授業の復習-課題4

### 課題4

![Squareのクラス図](WorkSheet/img/Square.png) 



