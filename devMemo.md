## environment
* redis
  * NoSQLデータベースの一つ
* redisとMySQLを両方使用している
  * redisのようなNoSQLはアクセス速度が高速なので、セッション情報やキャッシュ情報などの頻繁に使用する情報の管理を行っている
* MySQLではrootユーザーのパスワードをランダムで生成している
  * 生成されたパスワードはログに表示される
* volumesではマイグレーションの設定を行っている。
  * マイグレーションはデータ移行という意味で、レガシーからモダンなシステムへ移行する再などに使用される
* 実行ログは各Dockerファイル内の自動的に指定された場所にJSON形式で記述される


## エイリアス設定
* alias startforcas='cd ~/source/forcas/environment && docker compose up -d && cd ../forcas-front && yarn dev'
