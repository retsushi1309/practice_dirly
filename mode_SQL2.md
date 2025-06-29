# 学習した内容

# DISTINT 重複する内容を省いたカラムデータ
    SELECT DISTINCT(name)
    FROM purchases;

# 四則演算で消費税を含んだ価格の取り出し
    SELECT name , price, price*1.08
    FROM purchases;    

# SUM関数　カラムの合計でーたを出す
    SELECT SUM(price)
    FROM purchases;

# AVG関数　カラムの平均データを出す
    SELECT  AVG(price)
    FROM purchases;

# COUNT関数 カラムデータの合計の数
    SELECT COUNT(name)　// nullのデータが入っていないのは省いて数える
    FROM purchases;
    
    SELECT COUNT(*) //入っていないデータも数える

#　MAX、MIN関数　最大値と最小値を取得
    SELECT MAX(price)
    FROM purchases;
    
    SELECT MIN(price)
    FROM purchases;

#　GRUOUP BY グループの合計を取得
    SELECT COUNT(price)
    purchased_at
    FROM purchases
    GROUP BY purchased_at;

# 複数のグループ
    SELECT SUM(price),purchased_at,character_name
    FROM purchases
    GROUP BY purchased_at,character_name;

# 複数のグループのデータを取得しグループ化
    SELECT SUM(price), purchased_at
    FROM purchases
    WHERE character_name ="にんじゃわんこ"
    GROUP BY purchased_at, price,purchased_at;

# 複数のデータのうち２０００超えるデータだ取得
    SELECT SUM(price), purchased_at
    FROM purchases
    GROUP BY purchased_at
    HAVING SUM(price) > 2000;
