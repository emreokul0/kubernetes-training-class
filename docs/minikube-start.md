# Minikube Start

## Steps to Install Minikube

1. **Update and Upgrade the System**:
   Before proceeding, it's good practice to update the package lists and upgrade installed packages:

   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

   ![Apt Update Result](./images/apt-update-result.png)

   ![Apt Upgrade Result](./images/apt-upgrade-result.png)

2. **Start Minikube with Docker Driver**:
   To start Minikube using Docker as the driver, run the following command:

   ```bash
   minikube start --driver=docker
   ```

   ![Minikube Start With Docker Driver](./images/minikube-start-with-docker-driver.png)

3. **Check Minikube Status**:
   Verify that Minikube is running correctly:

   ```bash
   minikube status
   ```

   ![Minikube Status Check](./images/minikube-status-check.png)

4. **Access the Minikube Dashboard (Optional)**:
   Minikube provides a dashboard for visual management. To launch it, run:

   ```bash
   minikube dashboard
   ```

   ![Minikube Dashboard Access](./images/minikube-dashboard-access.png)

5. **Using kubectl with Minikube**:
   You can now use `kubectl` to manage your Minikube cluster. For example, check the nodes in your cluster with:

   ```bash
   kubectl get nodes
   ```
