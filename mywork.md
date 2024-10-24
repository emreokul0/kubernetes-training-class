# Kubectl Commands

## 1. minikube start

**Output:**

```bash
😄  minikube v1.34.0 on Ubuntu 20.04 (docker/amd64)
✨  Using the docker driver based on existing profile
👍  Starting "minikube" primary control-plane node in "minikube" cluster
🚜  Pulling base image v0.0.45 ...
🔄  Restarting existing docker container for "minikube" ...
🐳  Preparing Kubernetes v1.31.0 on Docker 27.2.0 ...
🔎  Verifying Kubernetes components...
    ▪ Using image gcr.io/k8s-minikube/storage-provisioner:v5
    ▪ Using image docker.io/kubernetesui/dashboard:v2.7.0
    ▪ Using image docker.io/kubernetesui/metrics-scraper:v1.0.8
💡  Some dashboard features require the metrics-server addon. To enable all features please run:

        minikube addons enable metrics-server

🌟  Enabled addons: storage-provisioner, default-storageclass, dashboard
🏄  Done! kubectl is now configured to use "minikube" cluster and "default" namespace by default
```

## 2. minikube status

**Output:**

```bash
minikube
type: Control Plane
host: Running
kubelet: Running
apiserver: Running
kubeconfig: Configured

```

## 3. kubectl get pods -A

**Output:**

```bash
NAMESPACE              NAME                                        READY   STATUS    RESTARTS      AGE
default                my-pod                                      1/1     Running   1 (38s ago)   12d
kube-system            coredns-6f6b679f8f-hp9vb                    0/1     Running   3 (38s ago)   12d
kube-system            etcd-minikube                               1/1     Running   3 (38s ago)   12d
kube-system            kube-apiserver-minikube                     1/1     Running   3 (38s ago)   12d
kube-system            kube-controller-manager-minikube            1/1     Running   3 (38s ago)   12d
kube-system            kube-proxy-bc2wv                            1/1     Running   3 (38s ago)   12d
kube-system            kube-scheduler-minikube                     1/1     Running   3 (38s ago)   12d
kube-system            storage-provisioner                         1/1     Running   7 (38s ago)   12d
kubernetes-dashboard   dashboard-metrics-scraper-c5db448b4-2ts27   1/1     Running   2 (38s ago)   12d
kubernetes-dashboard   kubernetes-dashboard-695b96c756-fvn88       1/1     Running   3 (38s ago)   12d
```
