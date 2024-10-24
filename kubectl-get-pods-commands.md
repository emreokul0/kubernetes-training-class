# Kubectl Get Pods Commands

Here is a table of common `kubectl get pods` commands and their descriptions for Kubernetes:

| **Command**                                   | **Description**                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| `kubectl get pods`                            | Lists all pods in the current namespace.                                        |
| `kubectl get pods --all-namespaces`           | Lists all pods across all namespaces.                                           |
| `kubectl get pods -o wide`                    | Lists all pods with additional information, including node and IP addresses.    |
| `kubectl get pods -n <namespace>`             | Lists all pods in the specified namespace.                                      |
| `kubectl get pods --field-selector status.phase=Running` | Lists all pods that are currently in the `Running` phase.                      |
| `kubectl get pods -o json`                    | Lists all pods in JSON format.                                                  |
| `kubectl get pods -o yaml`                    | Lists all pods in YAML format.                                                  |
| `kubectl get pods --sort-by=.metadata.name`   | Lists all pods sorted by pod name.                                              |
| `kubectl get pods --selector=<label-key>=<label-value>` | Lists all pods with the specified label.                                 |
| `kubectl get pods -l app=<app-name>`          | Lists all pods with a specific label (`app=<app-name>`).                        |
| `kubectl get pod <pod-name> -o yaml`          | Displays detailed information about a specific pod in YAML format.              |
| `kubectl get pods --watch`                    | Watches for changes in the status of pods and displays updates in real-time.    |
| `kubectl get pods --no-headers`               | Lists all pods without headers (useful for scripting).                          |
| `kubectl get pods --output=custom-columns=<spec>` | Customizes the columns displayed when listing pods.                           |
| `kubectl describe pod <pod-name>`             | Shows detailed information about a specific pod.                                |

This table provides a variety of `kubectl get pods` commands, from simple listings to more advanced options such as filtering by labels and output formats.
