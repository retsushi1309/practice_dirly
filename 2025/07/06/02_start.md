# URLディスパッチ
    動的なページの作成

# 1.first_app/views.py
    動的な値としてユーザーネームをとって画面上に表示
    def user_page(request, user_name):
    return HttpResponse(f'<h1>{user_name} Page</h1>')

# 2.first_app/urls.pyの変更
    URL上のどのパラメータURLのパラメータの値を参照しているのか
    path('page/<str:user_name>', views.user_page, name='user_page'),

# 3. first/views.py 追加
    def と　return　の間
    print(type(user_name), user_name)