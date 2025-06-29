# 学習した内容



#　クエりとは
    SELECT name　❷どのカラムのデータ
    FROM purchases; 　❶どのテーブル

#　 複数のカラムのデータ
    SELET namw, price

# どの横行を取得するか　WHERE
    SELECT *
    FROM purchases
    WHERE category = "食費"

# どの横行を取得するかさらに絞り込み　WHERE
    SELECT *
    FROM purchases
    WHERE price = 1000;

# 比較演算子
    SELECT *
    FROM purchases
    WHERE price >= 1000;

# LIKE演算子　
    SELECT *
    FROM purchases
    WHERE name like "%プリン%"; //プリンが入っている項目全て
                    "プリン%"; //先頭にプリンが入っている
                    "%プリン";　//後方にプリンが入っている

# NOT演算子　入っていないもの
    SELECT *
    FROM purchases
    WHERE NOT character_name = "プリン" ;

# NULLのデータの取得　項目がないデータ
    SELECT *
    FROM purchases
    WHERE price IS NULL;

# AND演算子　違う項目データ
    SELECT *
　FROM purchases
　WHERE category = "食費"
　AND character_name ="ひつじ仙人";

# OR演算子　違う項目データどちらかはいているもの
    SELECT *
    FROM purchases
    WHERE category ="食費"
    OR character_name = "にんじゃわんこ";

# ORDER 並べ替え
    SELECT *
    FROM purchases
    ORDER BY price DESC ;　降順
    ORDER BY price ASC ;　昇順

#　 LIMIT 必要な数だけ
    SELECT *
    FROM purchases
    LIMIT 5;