# bool 比較演算子
    
    =を使った時の否定系 ！

    inを使った時の否定系　not
　　
    a = 3
    print(2 < a <= 10)

# データ型の調べ方
    a = 2
    type(a) //int
    変数にはどんなデータ型か確認する

    型変換
    three = 3
    print(three, type(three)) //3 (int)
    
    int から　str の文字列に変換
    three_str = str(three)
    print(three_str, type(three_str)) //3 (str)

    str から int の文字列に変換
    three_int = int(three)
    ptint(three_int, type(three_int)) //3(int)

   文字列数値型に変換
    price = '1,980円'
    price = int(price.replace(',''').replace('円','')) 
    print(price, type(peice)) // 1980 (int)


