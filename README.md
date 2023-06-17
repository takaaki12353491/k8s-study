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
###### 