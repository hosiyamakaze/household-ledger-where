仕様メモ
・条件の種類（CODE, LIKE, BETWEEN）
　CODE:コード値の=比較のみ。ただし複数のコード値はIN (...)に置き換える
　LIKE:%～%を使ったLIKE
　日付・金額はfrom以上～To以下、From,toが与えられたらBETWEENに置き換える
・AND / OR フォルダは多段階に入れ子可能
　閉じたフォルダは、SQL生成対象外
・列名は家計簿.DB3の支出テーブルの項目をCODE,LIKE,BETWEENに振り分ける
・CODE条件は、候補リスト
・LIKE,BETWEEN条件は手入力
・生成結果はSQL文字列
・バリデーション（型不一致）は検査しない
・操作対象は最後に選択されたNode、黄色でバックグランド表示される。
・実行は”SELECT * FROM 支出 WHERE “+生成結果SQL文字列
※生成結果SQLは家計簿.sqbproのSQL実行タブに貼り付けて利用することもできる

USE WITH  household-ledger-search//家計簿DB3data/
