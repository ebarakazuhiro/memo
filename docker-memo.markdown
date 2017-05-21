# Dockerに関するメモ

### imageを全削除するコマンド


```

sudo docker rmi $(sudo docker images -q)

```


### コンテナを全削除するコマンド


```

docker ps -a | awk '{print $1}' | tail -n +2 | xargs docker rm

```