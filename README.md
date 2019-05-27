# my-first-blog

このリポジトリは未来電子プログラミングカリキュラムPart3の課題提出用ブログです。

やること:

$ git clone https://github.com/Mateheath/my-first-blog.git
$ cd my-first-blog
$ docker-compose up -d
$ docker-compose exec web ./manage.py migrate
$ docker-compose exec web ./manage.py createsuperuser

admin siteにログインします。
http://127.0.0.1:8000/admin

アクセス http://127.0.0.1:8000/post/1

理由：
1.クローンしただけでは、ソースコードを移行しただけであって、データベースの内容は移行できていない。つまり、クローン時点でこちらのPCにはデータベースの情報は無い。厳密には、migrate前のデータベースの情報があるのみ。すなわち、migrateを実行する必要がある。
2.アプリケーションの仕様上、ユーザがログインをしていなければ、実行できない（？）。そのため、まずsuperuserを作成する必要があるのではないか。

