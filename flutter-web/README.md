dockerでFlutter web serverを立ち上げる

## Usage
```
# docker imageを作成
$ docker build . -t flutter

# docker containerを起動
$ docker run -itd --network=host flutter

# 接続を確認
$ curl http://localhost:3000
```

