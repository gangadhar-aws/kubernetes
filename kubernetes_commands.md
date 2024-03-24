1. create pod using kubectl command you can use create or apply
```sh
kubectl apply -f my_pod_playbook.yaml
```
 - here -f attribute is yaml file name
2. How to check or get the pods information 
```sh
kubectl get pods
```
3. How can we get more details of our pod?
```sh
kubectl describe pod pod_name
```
4. Create a new pod with the nginx image.
```sh
kubectl run nginx --image=nginx
```
5. Delete the pod
```sh
kubectl delete pod pod_name
```
6. Create a new pod with the name redis and the image redis123
```sh
kubectl run redis --image=redis123
```
7. how can we edit the image name
```sh
kubectl edit pod pod_name
```
8. Create a Replica-set command
```sh
kubectl create -f my_replicaset.yaml
```
9. To see list of replica-set 
```sh
kubectl get replicaset
```
10. Deleting the replica-set
```sh
kubectl delete replicaset rc_name_app
```
 -  also deletes all underlying pods
11. Update/Edit the Yaml file the replica set 
```sh
kubectl replace -f replica_set.yaml
```
12. Scale the Replicas 
```sh
kubectl scale --replicas=6 -f replica_set.yaml
```
```sh
kubectl sclae replicaset myapp_replicaset --replicas=4
```
13. Deleting only single pod 
```sh
kubectl delete pod myapp_pod_name
```
#### Deployments Commands
14. Create Deployments
```sh
kubectl create -f my_deployment_file.yaml
```
15. How to see all the deployments
```sh
kubectl get deployments
```
16. how to see all Details, pods/deployments/replicaset
```sh
kubectl get all
```
### Deployment Rollback Commands
17. update the deployment instances 
```sh
kubectl apply -f deployment_file.yaml
```
18. 2nd way using kubectl set image command:     
```sh
kubectl set image deployment/myapp_name nginx-container=nginx:1.9.1
```
19. How to rollback old version
```sh
kubectl rollout undo deployment/myapp_deployment_name
```
#### Summarize Commands
20. Create Deploymnet using file
```sh
kubectl create -f deploymnet_file.yaml
```
21. Get Deployments 
```sh
kubectl get deployments
```
22. update Deployments
```sh
kubectl apply -f deployment_file.yaml
```
```sh
kubectl set image deploymnet/deployment_name nginx=nginx:1.9.1
```
23. status of deployments
```sh
kubectl rollout status deployment/deploymnet_app
```
```sh
kubectl rollout history deployment/deploymnet_appname
```
24. rollback deployments
```sh
kubectl rollout undo deploymnet/deploymnet_appname
```
