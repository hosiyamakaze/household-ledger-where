
##USE WITH<br>
 household-ledger-search/家計簿DB3data/<br>

##仕様メモ<br>
・条件の種類（CODE, LIKE, BETWEEN）<br>
　CODE:コード値の=比較のみ。ただし複数のコード値はIN (...)に置き換える<br>
　LIKE:%～%を使ったLIKE<br>
　日付・金額はfrom以上～To以下、From,toが与えられたらBETWEENに置き換える<br>
・AND / OR フォルダは多段階に入れ子可能。フォルダコメントを設定しファイル名とする <br>
　閉じたフォルダは、SQL生成対象外<br>
・列名は家計簿.DB3の支出テーブルの項目をCODE,LIKE,BETWEENに振り分ける<br>
・CODE条件は、候補リスト<br>
・LIKE,BETWEEN条件は手入力<br>
・生成結果はSQL文字列<br>
・バリデーション（型不一致）は検査しない<br>
・操作対象は最後に選択されたNode、黄色でバックグランド表示される。<br>
・実行は”SELECT * FROM 支出 WHERE “+生成結果SQL文字列<br>
※生成結果SQLは家計簿.sqbproのSQL実行タブに貼り付けて利用することもできる<br>

