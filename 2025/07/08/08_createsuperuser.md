# 管理画面の利用
    デフォルトの管理画面の使用方法

# 管理画面のパスの設定
from django.contrib import asmin
urlptterns =[
    path('admin/',admin.site.urls),
]
# 管理画面ログイン用のスーパーユーザーの作成
python manage.py creatsuperuser
# 管理画面で扱うmodelの追加
admin.site.register(Model)

# 1.models.py 
    from django.db import models
from datetime import date, datetime
# Create your models here.
class Person(models.Model):
    first_name = models.CharField(max_length=30)
    last_name = models.CharField(max_length=30)
    birthdy = models.DateField(default=date(1900, 1,1))
    email = models.EmailField(db_index=True)
    salary = models.FloatField(null=True)
    memo = models.URLField()
    web_dite = models.URLField(null=True)
    creat_at = models.DateTimeField(defolt=datetime.now)

# 2 
python3 manage.py makemigrations ModelApp --name add_person

# 3
python3 manage.py migrate                                 

# 4ログインユーザー設定
python3 manage.py createsuperuser

# 5 admin.py追加
from django.contrib import admin
from .models import Person
　# Register your models here.
admin.site.register(Person)

# 6
python3 manage.py runserver