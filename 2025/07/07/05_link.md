#　動的にリンクの生成書き方
    <a href="{% url 'template_app:home' %}">Home</a>

# static　静的コンテンツ

# リンクの作成書き方
    {% load static %}//必須

    <img src="{% static  'sample.jpg' %}">

# settings.py で設定も変えることできる
    # Static files (CSS, JavaScript, Images)
    # https://docs.djangoproject.com/en/5.2/howto/static-files/

    STATIC_URL = 'static/'

# 一番上のフォルダを見る設定
    settings.py
    BASE_DIR = Path(__file__).resolve().parent.parent
    TEMPLATE_DIR = os.path.join(BASE_DIR, 'templates')
追加 STATIC_DIR = os.path.join(BASE_DIR, 'static')

    一番上にフォルダを策定した後
    settings.pyの一番下に追加
    STATICFILES_DIRS = [
    STATIC_DIR,
    ]

# cssのファイル作成
    sample.htmlに<link relを追加
    {% load static %}
    <link rel="stylesheet" href="{% static 'sample.css%'%}">
