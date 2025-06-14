## A-1～A-4: Dart超入門

---
2025年4月22日
### 今日のキーワード： 「やきとり」➡「やきとり」はその名の通り、鳥肉を串焼きにした料理ですが、実は江戸時代では鳥肉が高価で手に入りにくかったため、魚や豆腐、さらにはうなぎの肝を焼いて「やきとり」と呼んでいたそうです。実は「やきとりの日」があります。8月29日が「やきとりの日」とされており、「やき（8）」「にく（29）」の語呂合わせからきています。この日に美味しいやきとりを楽しむのはいかがでしょう？
---

ブラウザ上でDartPadを実行する方法➡
(https://dartpad.dev/)

> DartPadにてプログラミング復習

```dart

void main() {
  print("Helli, world!");
  print("こんにちは。");
  print("私の名前は");
  print("佐藤です。");

  print("1" + "1");
  print(1 + 1);

  print(5 ~/ 2 ); //商
  print(5 / 2 ); //余
  print(5 % 2 ); //余
  print(1 * 1);

  print(1000 > 999999);
  print(999999 > 1000);

  int a;
  int b = 10;

  a = 100;
  b = a;
  a = a + 20;
  b = b + 5;

  print(a + 100);
  print(b);

  print(a ++);
  print(++ a);

  int a = 100;
  if (a % 2 == 0) {
     値がtrueの時の処理
    print("偶数です");
  } else {
     値がfalseの時の処理
    print("奇数です");
  }

  int max = 10;
  int min = 1;
  int sum = 0;

  int count = min;

  while (count <= max) {
     値がtrueの間、実行を繰り返す
    sum += count;
    count ++;
  }

  print(sum);

  List<int> array = [1, 2, 3];

  int a = 2;
  array[a] = 10;

  print(array[0]);
  print(array[1]);
  print(array[2]);
}
```

---
2025年4月23日
### 今日のキーワード： 「からあげ」➡「からあげ」の「から」は「唐（から）」、つまり中国に由来する説があります。しかし、現代の「からあげ」は日本独自の料理であり、鶏肉に片栗粉や小麦粉をまぶして揚げるスタイルは日本ならではです。からあげを美味しく仕上げるポイントは二度揚げです。一度目は低温で火を通し、二度目は高温でカリッと仕上げることで、外はサクサク、中はジューシーになります。
---


```dart

void main() {
  Car Obj = Car(); // インスタンス生成

  print(Obj.speed);
  Obj.accelerate();
  print(Obj.speed);
  Obj.brake();
  print(Obj.speed);
}

class Car {
  int speed = 0;
  int gas = 40;

  void accelerate() {
    speed++;
  }

  void brake() {
    if (speed > 0) {
      speed--;
    }
  }
}

【ガソリンとブレーキの機能の実装】
void main() {
  Car obj = Car(); // インスタンス生成

  print(obj.speed); //0
  obj.accelerate();
  print(obj.speed); //1
  obj.brake();
  print(obj.speed); //0

  print(obj.gas); //39
  for (int i = 0; i < 45; i++) {
    obj.accelerate();
  }
  print(obj.speed); //39
  print(obj.gas); //0

  for (int i = 0; i < 5; i++) {
    obj.brake();
  }
  print(obj.speed); //34
}

class Car {
  int speed = 0;
  int gas = 40;

  void accelerate() {
    //ガソリンの有無によってスピードを出す
    if (gas > 0) {
      speed++;
      gas--;
    } else {
      print('No gas!');
    }
  }

  void brake() {
    //ブレーキ機能
    if (speed > 0) {
      speed--;
    }
  }
}
```