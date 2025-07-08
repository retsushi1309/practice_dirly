# Formの定義
  FormApp/forms.pyのフォルダ作成
    from django import forms

    class UseInfo(forms.Form):
    name =forms.CharField()
    age = forms.IntegerField()
    mail = forms.EmailField()

# Formの処理
    from .import forms
    # Create your views here.
    indexの処理
    def index(request):
      return render(request, 'index.html')

    form_pageの処理
      def form_page(request):
    form = forms.UserInfo()
    return render(
        request, 'formpage.html', context={
        'form' : form
        }
    )
