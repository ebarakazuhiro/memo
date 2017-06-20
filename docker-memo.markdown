# Dockerに関するメモ

### Dockerfile リファレンスメモ


Dockerfileのリファレンスのメモは[こちら](http://docs.docker.jp/engine/reference/builder.html#from)から


### docker-compose リファレンスメモ


docker-composeのリファレンスのメモは[こちら](http://docs.docker.jp/compose/compose-file.html)から


### imageを全削除するコマンド


```

sudo docker rmi $(sudo docker images -q)

```


### コンテナを全削除するコマンド


```

docker ps -a | awk '{print $1}' | tail -n +2 | xargs docker rm

```