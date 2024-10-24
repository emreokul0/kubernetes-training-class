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

## 4. kubectl get pods

**Output:**

```bash
NAME     READY   STATUS    RESTARTS      AGE
my-pod   1/1     Running   1 (43s ago)   12d
```

## 5. kubectl get namespaces

**Output:**

```bash
NAME                   STATUS   AGE
default                Active   12d
kube-node-lease        Active   12d
kube-public            Active   12d
kube-system            Active   12d
kubernetes-dashboard   Active   12d
```

## 6. kubectl get pods -n kube-

**Output:**

```bash
NAME                               READY   STATUS    RESTARTS      AGE
coredns-6f6b679f8f-hp9vb           1/1     Running   3 (14m ago)   12d
etcd-minikube                      1/1     Running   3 (14m ago)   12d
kube-apiserver-minikube            1/1     Running   3 (14m ago)   12d
kube-controller-manager-minikube   1/1     Running   3 (14m ago)   12d
kube-proxy-bc2wv                   1/1     Running   3 (14m ago)   12d
kube-scheduler-minikube            1/1     Running   3 (14m ago)   12d
storage-provisioner                1/1     Running   8 (13m ago)   12d
```

## 7. kubectl get pods -n default

**Output:**

```bash
NAME     READY   STATUS    RESTARTS      AGE
my-pod   1/1     Running   1 (15m ago)   12d
```

## 8. kubectl get pods -o wide -A

**Output:**

```bash
NAMESPACE              NAME                                        READY   STATUS    RESTARTS      AGE   IP             NODE       NOMINATED NODE   READINESS GATES
default                my-pod                                      1/1     Running   1 (16m ago)   12d   10.244.0.11    minikube   <none>           <none>
kube-system            coredns-6f6b679f8f-hp9vb                    1/1     Running   3 (16m ago)   12d   10.244.0.13    minikube   <none>           <none>
kube-system            etcd-minikube                               1/1     Running   3 (16m ago)   12d   192.168.49.2   minikube   <none>           <none>
kube-system            kube-apiserver-minikube                     1/1     Running   3 (16m ago)   12d   192.168.49.2   minikube   <none>           <none>
kube-system            kube-controller-manager-minikube            1/1     Running   3 (16m ago)   12d   192.168.49.2   minikube   <none>           <none>
kube-system            kube-proxy-bc2wv                            1/1     Running   3 (16m ago)   12d   192.168.49.2   minikube   <none>           <none>
kube-system            kube-scheduler-minikube                     1/1     Running   3 (16m ago)   12d   192.168.49.2   minikube   <none>           <none>
kube-system            storage-provisioner                         1/1     Running   8 (16m ago)   12d   192.168.49.2   minikube   <none>           <none>
kubernetes-dashboard   dashboard-metrics-scraper-c5db448b4-2ts27   1/1     Running   2 (16m ago)   12d   10.244.0.14    minikube   <none>           <none>
kubernetes-dashboard   kubernetes-dashboard-695b96c756-fvn88       1/1     Running   4 (16m ago)   12d   10.244.0.12    minikube   <none>           <none>
```

## 9. kubectl get pods -o wide -n kube-system

**Output:**

```bash
NAME                               READY   STATUS    RESTARTS      AGE   IP             NODE       NOMINATED NODE   READINESS GATES
coredns-6f6b679f8f-hp9vb           1/1     Running   3 (17m ago)   12d   10.244.0.13    minikube   <none>           <none>
etcd-minikube                      1/1     Running   3 (17m ago)   12d   192.168.49.2   minikube   <none>           <none>
kube-apiserver-minikube            1/1     Running   3 (17m ago)   12d   192.168.49.2   minikube   <none>           <none>
kube-controller-manager-minikube   1/1     Running   3 (17m ago)   12d   192.168.49.2   minikube   <none>           <none>
kube-proxy-bc2wv                   1/1     Running   3 (17m ago)   12d   192.168.49.2   minikube   <none>           <none>
kube-scheduler-minikube            1/1     Running   3 (17m ago)   12d   192.168.49.2   minikube   <none>           <none>
storage-provisioner                1/1     Running   8 (16m ago)   12d   192.168.49.2   minikube   <none>           <none>
```

## 10. kubectl get pods -n kube-system | less

**Output:**

```bash
NAME                               READY   STATUS    RESTARTS      AGE
coredns-6f6b679f8f-hp9vb           1/1     Running   3 (57m ago)   13d
etcd-minikube                      1/1     Running   3 (57m ago)   13d
kube-apiserver-minikube            1/1     Running   3 (57m ago)   13d
kube-controller-manager-minikube   1/1     Running   3 (57m ago)   13d
kube-proxy-bc2wv                   1/1     Running   3 (57m ago)   13d
kube-scheduler-minikube            1/1     Running   3 (57m ago)   13d
storage-provisioner                1/1     Running   8 (56m ago)   13d
(END)
```

## 11. kubectl get pods -n sbm-dev

sbm-dev namespace'inde yer alan podları listeler.

**Output:**

```bash
No resources found in sbm-dev namespace.
```

sbm-dev namespace'inde hiç pod yer almadığını gösteriyor.
