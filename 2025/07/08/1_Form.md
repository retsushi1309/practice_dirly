# Formのプロジェクとの作成
1.django-admin startproject FromProject

2.python3 manage.py startapp FormApp

# セッティング
  'FormApp'の追加

# 表示のテンプレートの追加
1
from pathlib import Path
import os
　# Build paths inside the project like this: BASE_DIR / 'subdir'.
BASE_DIR = Path(__file__).resolve().parent.parent
TEMPLATE_DIR = os.path.join(BASE_DIR, 'templates')
２
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [TEMPLATE_DIR],
        ]

# FormProject/templates フォルダの作成
index.html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <titile>HOME</title>
    </head>
    <body>
        <h1>ホームページ</h1>
    </body>
</html>
form_page.html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <titile>Form</title>
    </head>
    <body>
       
    </body>
</html>
