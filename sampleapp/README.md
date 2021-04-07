コンテナ起動時にFlutterプロジェクトをビルドして，生成されたソースを使ってPythonでWebサーバーを起動する．

## Usage
```
$ docker build -t pyflutter .

$ docker run -itd -p 80:80 -v $(pwd):/code pyflutter

$ curl http://localhost:80
```
ホスト側のポート番号は任意

