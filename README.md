First i have created a directory with name "kind-cluster" 
Under this, i have created config.yaml file
vim config.yaml
# two node (one worker) cluster config
kind: Cluster
apiVersion: kind.x-k8s.io/v1alpha4
nodes:
- role: control-plane
- role: worker
After this i run the command: kind create cluster --config=config.yaml
Cluster was created, but nodes were not running, then i fixed that issue
But now pods are not running (Status - ContainerCreating)
Error Warning  FailedCreatePodSandBox  kubelet 
Failed to create pod sandbox: rpc error: code = Unknown desc = failed to setup network for sandbox "7cead98505d1ff8037591afb80fec8bbfa72d92deb9dff0a0da0795c44cf1184": open /run/flannel/subnet.env: no such file or directory
