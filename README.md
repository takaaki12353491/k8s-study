# k8s-study
podを取得
`kubectl get pod`
podに入る
`kubectl exec -it <name> sh`

# debug pod
`docker build -t debug .`
`docker run -it debug sh`
`kubectl apply -f debug-pod.yml`