# Djangoのプロジェクト作成まで
    必ず環境構築はする

# 1.フォルダの作成

# 2..venv のフォルダの作成
    ⌘＋⇧＋p
    インタープリンターの作成
    Enviroment
    venv選択

# 3.pythonとpipの確認
    which python3
    which pip
    同じ場所の確認

# 4.(venv)ではない時
    .venv/binまで移動
    source activate　実行

# 5.pipのインストール
    pip install djanogo実行
    libにdjangoのライブラリができているかの確認

# 6.新しくフォルダの中に必要なファイル作成
    (.venv) pc@jesMacBook-Air 01_URLDispatch % 
    django-admin startproject first_project //実行

# 7.Djangoを立ち上げる
    (.venv) pc@jesMacBook-Air first_project %
    python3 manage.py runserver

# 8.setting で日本語化
    settings.py 106行目あたり
    LUNGUAGE_CODE ='ja'
    TIME_ZONE = 'Asia/Tokyo'

# ターミナルを終わらせる
    Control＋C

# 9.マイグレーションについて
    データベースの指定
    デフォルトでDjangoの管理画面を使うためのテーブルの作成
    (.venv) pc@jesMacBook-Air first_project % 
    python3 manage.py migrate

# 10.アプリケーションの作成
    (.venv) .venvpc@jesMacBook-Air first_project % 
    python3 manage.py startapp first_app
    
    ！忘れがち！
    アプリケーション作成したら
    first_projectのsettings.py で
    INSTALLED_APP =[
        'first_app'　追加する
    ]

# 11_1.viewを用いたページ作成
    first_app /views.py
    from django.http import HttpResponse

    def index(request):
        return HttpResponse('<h1>Good Bye</h1>')

# 11_2.first_app /フォルダの作成urls.py
    from django.urls import path
    from . import views

    app_name ='first_app'

    urlpatterns =[
    path('hell', views.index, name='index'),
    ]

# 11_3.first_project/urls.py
    書き換える
    from django.urls import path, include

    urlpatterns = [
    path('admin/', admin.site.urls),
    path('first_app/', include('first_app.urls')),
    ]

# 12.viewとurlのマッピンングまで
    (.venv) pc@jesMacBook-Air first_project % python3 manage.py runserver