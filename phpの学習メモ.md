# phpの学習メモ
* " "　の間でも認識される "　　\"  
* tabを挿入する　　\t  
* なおかつ　　&&  and  
* もしくは　　||  or  
* ～ではない　　?? !

switchで条件分岐する際、用意した case 以外を選択する場合は
case ではなく default を利用する  
例

```php
for ($a = 1; $a <= 300; $a++) {
    switch ($a) {
        case ($a % 15 == 0):
            echo "fizzbuzz" . "\t";
            break;
        case ($a % 5 == 0):
            echo "buzz" . "\t";
            break;
        case ($a % 3 == 0):
            echo "fizz" . "\t";
            break;
        default:
            echo $a . "\t";
            break;
    }
}
```

条件分岐でループをスキップし回したい場合は　　continue
条件分岐でループを破棄して戻りたい場合は　　 break　　を使用する
改行は PHP_EOL でおこなう

function  を使用することで処理を一つのまとまりにすることができる  
例

```php

function showAd($test)
{
  echo "=============" . PHP_EOL;
  echo "====" . $test . "====" . PHP_EOL;
  echo "=============" . PHP_EOL;
}

showAd(anpn);
echo 'Tom is great!' . PHP_EOL;
echo 'Bob is great!' . PHP_EOL;
showAd(bikn);
echo 'Steve is great!' . PHP_EOL;
echo 'Bob is great!' . PHP_EOL;
showAd();
```

return  は値を返す、また　return  の後ろは読まれなくなる  
関数外の変数は関数で利用することができない、利用するには  global  とつけるか　変数内で定義する必要がある。  
関数内だけで有効な変数の範囲をローカルスコープ  
関数外で有効な変数の範囲をグローバルスコープと呼ぶ

変数を値として利用することができる。これを無名関数、クロージャーと呼ぶ  
例

```php

function sum($a, $b, $c)
{
  return $a + $b + $c;
}

$sum = function ($a, $b, $c) {
  return $a + $b + $c;
};

echo $sum(100, 900, 200) . PHP_EOL;
```

条件演算子を活用することで条件分岐を短くすることができる場合がある
例

```php

function sum($a, $b, $c) 
{
  $hi = $a + $b + $c;
  return $hi < 0 ? 0 : $hi;   ←　　return 条件　？　真の場合　：　偽の場合；
}

echo sum(100,100,100) . PHP_EOL;
echo sum(-500,100,100) . PHP_EOL;
```

引数は型を指定することができる。指定する場合は引数の前にデータ型を入力すればよい。  
指定された方以外のデータが入力されるとエラーが吐き出される。 
より重い制限をかけたい場合は  declare(strict_types=1);　を入力しておく。

配列の内容を確認したい場合は　var_dump($配列名);  もしくは　print_r(配列名);  
配列のすべての要素に処理を行う場合は　foreach  を利用する  
配列内で配列を利用したい場合は入力した配列名の前に　... をつける。  
