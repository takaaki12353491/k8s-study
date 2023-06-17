# k8s
###### リソースを作成
`kubectl apply -f <file>`
###### リソースを取得
`kubectl get <resource>`
###### リソースを削除
`kubectl delete <resource> <name>`
###### podに入る
`kubectl exec -it <name> sh`
###### 名前解決
`ping <pod>.<HeadlessService>`

# docker
###### コンテナイメージを作成
`docker build -t <name> .`
###### コンテナを起動
`docker run -it <name> sh` or `docker run -d <name>`

# db
###### keyfile作成
`openssl rand -base64 1024 | tr -d '\r\n' | cut -c 1-1024 > keyfile`
###### secret作成
```
kubectl create secret generic mongo-secret \
--from-literal=root_username=<username> \
--from-literal=root_password=<password> \
--from-file=./keyfile
```
###### 初期化
```
rs.initiate({
  _id: "rs0",
  members: [
    { _id: 0, host: "mongo-0.db-svc:27017" },
    { _id: 1, host: "mongo-1.db-svc:27017" },
    { _id: 2, host: "mongo-2.db-svc:27017" },
  ]
})
```