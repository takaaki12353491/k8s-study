# k8s
###### リソースを作成
`kubectl apply -f <file>`
###### リソースを取得
`kubectl get <resource>`
###### リソースを削除
`kubectl delete <resource> <name>`
###### podに入る
`kubectl exec -it <name> sh`

# docker
###### コンテナイメージを作成
`docker build -t <name> .`
###### コンテナを起動
`docker run -it <name> sh` or `docker run -d <name>`
