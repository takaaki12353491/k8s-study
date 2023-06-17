# k8s-study
リソースを作成
`kubectl apply -f <file>`
podを取得
`kubectl get pod`
podに入る
`kubectl exec -it <name> sh`

コンテナイメージを作成
`docker build -t <name> .`
コンテナを起動
`docker run -it <name> sh` or `docker run -d <name>`
