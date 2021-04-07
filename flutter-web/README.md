dockerでFlutter web serverを立ち上げる

`--network=host`は[LINUX限定](https://docs.docker.com/network/host/)

## Usage
```
# docker imageを作成
$ docker build . -t flutter

# docker containerを起動
$ docker run -itd --network=host flutter

# 接続を確認
$ curl http://localhost:3000
```

