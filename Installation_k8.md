### Install Kubernetes on Windows 
1. Donwnload the latest file
```sh
curl.exe -LO "https://dl.k8s.io/release/v1.29.2/bin/windows/amd64/kubectl.exe"
```
2. Validate the binary (Optional)
```sh
curl.exe -LO "https://dl.k8s.io/v1.29.2/bin/windows/amd64/kubectl.exe.sha256"
```
3. again validate some file
```sh
CertUtil -hashfile kubectl.exe SHA256
type kubectl.exe.sha256
```
4. check the version installed 
```sh
kubectl version --client
```
or 
```sh
kubectl version --client --output=yaml
```
### Install on Windows using Chocolatey, Scoop, or winget
1. Winget package working in windows 
```sh
winget install -e --id Kubernetes.kubectl
```
2. Test to ensure the version you installed is up-to-date:
```sh
kubectl version --client
```
3. Navigate to your home directory:
```sh
cd ~
```
4. Create the .kube directory
```sh
mkdir .kube
```
5. go inside the directory

---Pending-------
