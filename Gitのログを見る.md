## Gitのログを見る
### ログの見方
#### commit 4b2f7ff43e3e212ef404d71974b3252025c5ae9f   ←    コミットにつくID  
#### Author: anpan <anpan@tst.com>   ←   コミットした人、連絡先
#### Date:   Wed Jul 31 10:00:00 2019 +0900   ←   コミットした時刻

#### test   ←   記入したコメント
### git log --ooneline と記入すると一行で表示される
#### 4b2f7ff test   ←   コミットにつくID　コメント
### git log -p と乳に浴すると変更点が詳しく閲覧できる
#### commit 4b2f7ff43e3e212ef404d71974b3252025c5ae9f   ←    コミットにつくID  
#### Author: anpan <anpan@tst.com>   ←   コミットした人、連絡先
#### Date:   Wed Jul 31 10:00:00 2019 +0900   ←   コミットした時刻

#### test   ←   記入したコメント

#### --- a/index.html   ←  変更前のファイル
#### +++ b/index.html   ←  変更後のファイル
#### @@ -1 +1,2 @@   ←   変更のあった行数
####  line 1
#### +line 2   ←   変更のあった内容
### git log --stat でどのファイルに何の変更があったか確認できる
