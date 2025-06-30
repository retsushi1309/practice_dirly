#今日の学習内容

# フォルダの移動
    cd 新しいフォルダの場所
    git clone https://github.com/ユーザー名/リポジトリ名.git

#　クローンが見えたら成功
    cd practice_dirly
    ls    

#　新しくフォルダの作成とpushまでの流れ
    作るたいフォルダの親まで移動
    cd

    新しくフォルダを作る
    mkdir new_folder

    フォルダのファイルも作成
    touch new_folder/README.md

    ファイルができたかの確認
    ls new_folder

    Gitに追加してcommitする
    git add .
    git commit -m "今日の学習内容"

    GitHubにpushする
    git push origin main

