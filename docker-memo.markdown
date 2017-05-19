# Dockerに関するメモ

### imageを全削除するコマンド


```

docker rmi $(docker images | awk '/^<none>/ { print $3 }')

```


### コンテナを全削除するコマンド


```

docker ps -a | awk '{print $1}' | tail -n +2 | xargs docker rm

```