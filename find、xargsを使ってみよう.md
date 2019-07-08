## find、xargsを使ってみよう
### find コマンド
#### ファイルを検索することができる
### find /etc -name "hello"   ←   find 検索の起点となるフォルダ名 -name "探したい文字列"
#### 読み取りが許可されていないファイルはエラーが出る
#### -type f を末尾に着けるとディレクトリを除きファイルのみを表示することも可能
### find /etc -name "hello" -type f   ←   find 検索の起点となるフォルダ名 -name "探したい文字列" -type f
#### 抜き出したファイルにコマンドを使用することも可能
### find /etc -name "hello" -type f -exec wc -l {} +   ←   find 検索の起点となるフォルダ名 -name "探したい文字列" -type f -exec 使用するコマンド {} + 
### xargs
#### 複数のコマンドを結果の流し込める
### find /etc -name "hello" -type f | xargs wc -l {} +   ←   find 検索の起点となるフォルダ名 -name "探したい文字列" -type f | xargs 使用するコマンド {} + 
