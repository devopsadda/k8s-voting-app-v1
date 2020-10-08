# k8s-voting-app-v1

Deploy a simple voting application in your local Kubernetes setup [ Minikube ]

Execute below commands after you are ready with the definition files:

kubectl get svc

kubectl create -f voting-app-deploy.yaml
kubectl create -f voting-app-service.yaml
kubectl get pods,svc,deploy
minikube service voting-service --url

kubectl create -f redis-deploy.yaml
kubectl create -f redis-service.yaml
kubectl get pods,svc,deploy

kubectl create -f postgres-deploy.yaml
kubectl create -f postgres-service.yaml
kubectl get pods,svc,deploy

kubectl create -f worker-app-deploy.yaml
kubectl get pods,svc,deploy

kubectl create -f result-app-deploy.yaml
kubectl create -f result-app-service.yaml
kubectl get pods,svc,deploy
minikube service result-service --url
