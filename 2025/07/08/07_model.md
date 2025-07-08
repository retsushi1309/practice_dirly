# Modelについて
初めにフォルダを作成して
1.プロジェクトフォルダの作成
django-admin startproject ModelProject
2.アプリケーションフォルダの作成
 python3 manage.py startapp ModelApp 
3.マイグレーションしてテーブル作成
python3 manage.py migrate

settings.pyに追加
INSTALLED_APPS = [
    'ModelApp'
]

models.pyに定義first_nameとlast_nameのテーブルを作成
class Person(models.Model):
    first_name = models.CharField(max_length=30)
    last_name = models.CharField(max_length=30)

マイグレーション０００１モデルの手記作成
python3 manage.py makemigrations ModelApp

