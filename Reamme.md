


kubectl get nodes

kubectl get nodes -o wide

kubectl run nginx --image=nginx  // run pod

kubectl get pods

kubectl describe pod nginx

kubectl delete pod nginx

kubectl create -f replicaset-def.yml
kubectl get replicase
kubectl get pods

Scale Replica:
//update replica yml- replica count : 6
kubectl replace -f replicaset-def.yml
kubectl scale --replicas=6 -f replicaset-def.yml
kubectl scale --replicas=6 replicaset myapp-replicaset ( metadata/name)

kubectl describe replicaset replicaset-def.yaml

// Deployments
kubectl create -f deployment-def.yaml
kubectl create -f deployment-def.yaml --record //record the cmd
kubectl get deployments
kubectl get all
kubectl describe deploy name
kubectl edit -f deployment-def.yaml --record
kubectl edit deploy dep-name
kubectl delete deployment deployment-def.yaml
kubectl create deployment --help
kubectl apply -f deployment-def.yml // update the deployment
// Roll out
kubectl rollout status deployment/myapp-deployment
kubectl rollout history deployment/myapp-deployment
kubectl set image deployment/deployment-def.yml nginx=nginx:1.9.1 // --record


// Services
kubectl describe service
kubectk get services
 
