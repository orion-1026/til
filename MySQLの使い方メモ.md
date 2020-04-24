## MySQLのメモ
| コマンド    | 効果               | 書き方                                                              |
|-------------|--------------------|---------------------------------------------------------------------|
| insert      | データを追加する   | insert into テーブル名(項目) values (項目)                          |
| update      | レコードを更新する | update テーブル名 set 更新内容                                      |
| delete      | レコードの削除     | delete from テーブル名                                              |
| where       | 条件               | ～ where 条件                                                       |
| like        | 部分一致           | ～ like %a %a% a% '_'など                                           |
| order by    | 並び替え           | ～ order by 対象　　desc を末尾に追加で昇順                         |
| limit       | 件数制限（上から） | ～ limit 制限したい数                                               |
| offset      | 開始位置           | ～ offset 飛ばしたい数                                              |
| transaction | 処理をまとめる     | start transaction; ～～～　commit;　　末尾を rollback; に変更で破棄 |
| alter table | 索引作成、削除     | alter table テーブル名 add(dropで削除) index 索引名 (対象)          |