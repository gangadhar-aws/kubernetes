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
