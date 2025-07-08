# URLの設定
FormApp/urls.pyのフォルダを作成
# FormApp/urls.py
from django.urls import path
from . import views

app_name = 'form_app'

urlpatterns =[
    path('',views.index,name='index'),
    path('form_page/', views.form_page, name='form_page'),
]
# FormProjectに追加
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('form_page/', include('FormApp.urls')),

#　画面上に表示の確認
def form_page(request):
    form = forms.UserInfo()
    print("form: ", form)
    return render(
        request, 'formpage.html', context={
        'form' : form
        }
    )
# form_page.html
  <body>
    {{ form }}追加
  </body>
  
  # index.html
    <body>
        <h1>ホームページ</h1>
        <a href="{% url 'form_:form_page' %}">ホーム画面へ</a>追加
    </body>












    
