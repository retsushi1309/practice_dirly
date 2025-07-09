# settngs.py　にURLの設定追加
MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')

# views.pyにファイルを保存するオブジェクト追加
def upload_sample(request):
    if request.method == 'POST' and request.FILES['upload_file']:
        upload_file = request.FILES['upload_file']
        fs = FileSystemStoronge() 
        
#一番上にインポート追加
from django.core.files.storage import FileSystemStorage

def upload_sample(request):
    if request.method == 'POST' and request.FILES['upload_file']:
        upload_file = request.FILES['upload_file']
        fs = FileSystemStoronge() 
        //ここから追加//
        file_path = os.path.join('upload', upload_file.name)
        print(file_path)
        
#一番上にosインポート追加
from os

#ファイルの保存
def upload_sample(request):
    if request.method == 'POST' and request.FILES['upload_file']:
        upload_file = request.FILES['upload_file']
        fs = FileSystemStoronge() 
        file_path = os.path.join('upload', upload_file.name)
        print(file_path)
        //ここから追加//
        file = fs.save(file_path, upload_file)
        uplode_file_url = fs.url(file)#ファルを保存するURL
        return render(request, 'formapp/upload_file.html',
            context ={
            'uploade_file_url': uploaded_file_url,
            })
     return render(request, 'formapp/upload_file.html')
