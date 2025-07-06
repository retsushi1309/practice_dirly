# Templateにいついて
    01のアプリケーションの作成まで



# 1.テンプレートフォルダの中にフォルダの作成
    フォルダを作成てその中にindex.html入れる

# 2.テンプレートを表示する処理
    views.pyに
    def index(request):
        return render(request, 'index.html')

# 3.urlを設定する
    フォルダにurls.pyを追加
    from django.urls import path
    from . import views

    app_name = 'template_app'

    urlpatterns = [
        path ('', views.index, name='index')
    ]

# テンプレートのファイルの配置のセッティング
    settings.pyの16行　付近変更
    from pathlib import Path
    import os
    # Build paths inside the project like this: BASE_DIR / 'subdir'.
    BASE_DIR = Path(__file__).resolve().parent.parent
    TEMPLATE_DIR = os.path.join(BASE_DIR, 'templates')

    優先的にファイルを見るようになる
    TEMPLATES = [
        'DIRS': [TEMPLATE_DIR],
    ]

# viewからテンプレートに値を埋め込む
    viewを書き替える
    def index(request):
    value = "Good bye"
    return render(request, 'TemplateApp/index.html', context={"value": value})

    
