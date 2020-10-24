# 参考ページ
https://reffect.co.jp/laravel/finally-understand-laravel-on-docker

https://www.youtube.com/watch?v=fN8h4lfXhDQ


# 使い方

git clone
```
git clone https://github.com/ksm-mnyk/docker-laravel.git

cd docker-laravel/
```

### コンテナ作成・起動
```
docker-compose up -d
```

### composerを使用して、laravelプロジェクト作成(初回のみ必要）
```
docker run --rm -v `pwd`/src:/app composer create-project --prefer-dist laravel/laravel .
```
※ 数分かかる

-vオプションで、ローカルPCのディレクトリとcomposerコンテナ上の/appディレクトリを紐づけ。そのため上記のコマンドを実行すると./srcディレクトリの下にLaravelに関連するディレクトリ、ファイルが保存される。


### 開発サーバー起動
```
docker exec -it php php artisan serve --host=0.0.0.0 --port=8000
```

### アクセス
ブラウザで localhot:8000 へアクセス

### ソース改造
```
cd src
code .
```
srcディレクトリ配下をvisual stadio code で開く

### コンテナ停止
```
docker-compose down
```





