# Django template language (DTL)

# DTL_1.pythonコードをHTMLに埋め込む書き方
    def home(request):
    my_name = 'Taro Yamada'
    favourite_fruits = ['Appole', 'Grape', 'Lemon']
    my_info = {
        'name' : 'Taro',
        'age' : 18
    }
    return render(request, 'templateApp/home.html', cintext={
        'my_name': my_name,
        'favourite_fruits': favourite_fruits,
        'my_info': my_info,
        })

    urls.pyにurlを受け取るように書き換える
    urlpatterns = [
    path ('', views.index, name='index'),
    path ('home', views.home, name='home'),
    ]
# DTL_2.制御文の書き方
    処理の記述
    {% %}: if,forなどの式
    {{ }}: 値をアウトプットする
    {# #}: コメント文

    for文
    {% for value in myslist %}
     <p>{{ value }}</p>
    {% endfor %}

    if文
    {% if value in mylist %}
     <p>something</p>
    {% elif 式 %}
    {% else %}
        <p>Hmmm</p>
    {% endif %}

    コメント文
    {# コメント文は画面に表示されません #}
