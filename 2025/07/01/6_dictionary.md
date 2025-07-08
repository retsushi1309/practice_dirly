# 辞書型の書き方
                キー :きーの中身,
    fruits = {'apple': 100, 'banana': 120}
    peint(fruits)

キーの中身の取り出し方
    print(fruit['apple']) //100が出力される

# キーの中身の書き換え方
    fruits['banana'] = 150
    print(fruits) //{'apple':100,'banana':150}と書き換えられる

# キーの追加
    fruits['peach'] = 180
    print(fruits) //{'apple':100,'banana':150,'peach':180}となる
    リストではエラーになるがキー辞書型では存在しないキーに対してvalueを設定すると
    新しくキーとvalueが追加される

# メソッド
    dict_keys 全てのKeyが格納されたリスト

    for value in fruits.values(): ()の意味はvalueの値を全部取りだす　keys()だったらkeyを全部取り出す
        print(value)

    items　keyとvalueの両方を取り出せるメソッド