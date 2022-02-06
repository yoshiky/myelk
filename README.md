# how to work

## 事前準備
- `./data/log/httpd/accesslog/web01`などにApacheログファイルを格納する

## コンテナ作成
```
% docker-compose up -d
```

## logstash起動
個別起動しているが、docker作成時にconf読み込みするようにすればいいかも（なってる？）
```
% docker-compose run --rm logstash /usr/share/logstash/bin/logstash -f ./pipeline/logstash-apache.conf
```
