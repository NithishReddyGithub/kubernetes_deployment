# Deploy Containerized Application to AKS  

## 📋 Task  
Deploy the containerized application to **Azure Kubernetes Service (AKS)** using a Kubernetes Deployment YAML file.  
Include **readiness** and **liveness** probes for application health monitoring.  

---

## 📂 Outcome  
- `deployment.yaml` (Kubernetes deployment manifest)  
- `deployment-logs.txt` (Logs of deployment execution)  
- `kubectl-get-pods.txt` (Output of `kubectl get pods`)  
- `kubectl-describe-pod.txt` (Output of `kubectl describe pod <pod_name>`)  
- Screenshots of pod status and description  

---

## ⚙️ Deployment Steps  

1. **Apply Deployment YAML**  
   ```bash
   kubectl apply -f deployment.yaml | tee deployment-logs.txt
   ```

---

## Verify Pods  

```bash
kubectl get pods -n <namespace> | tee kubectl-get-pods.txt
```

---

## Describe Pod for Details  

```bash
kubectl describe pod <pod_name> -n <namespace> | tee kubectl-describe-pod.txt
```

---

## 🔍 Health Probes  

The `deployment.yaml` includes:  

- **Liveness Probe** → Ensures the container is restarted if it becomes unhealthy.  
- **Readiness Probe** → Ensures traffic is routed only when the pod is ready.

---

## 📂 Logs & 📸 Screenshots  
  
- **kubectl get pods Output**: [kubectl-get-pods.txt](https://github.com/NithishReddyGithub/kubernetes_deployment/blob/main/get-pods.txt)  
- **kubectl describe pod Output**: [kubectl-describe-pod.txt](https://github.com/NithishReddyGithub/kubernetes_deployment/blob/main/pod-describe.txt)  

### 📸 Screenshots (Placeholders)  
- Screenshot: ![Successful `kubectl get pods` output](./get-pods.png) 
- Screenshot: ![Pod details from `kubectl describe pod`](./describe-pods.png)
- Screenshot:  ![Application running successfully in AKS](./my-profile.png)
