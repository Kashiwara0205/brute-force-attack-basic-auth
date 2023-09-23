FROM nginx:1.24.0

RUN apt update

# パスワードを生成するために使う
RUN apt-get install -y apache2-utils

# クラッキング用ツール
RUN apt-get install -y libssl-dev libssh-dev libidn11-dev libpcre3-dev libgtk2.0-dev libpq-dev libsvn-dev firebird-dev
RUN apt-get install -y hydra
