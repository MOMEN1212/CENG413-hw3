# CENG413 HW-3: Kubernetes

This project runs my HW-2 Flask application with Redis using Kubernetes.

## 1. Deploy the Application

```bash
kubectl apply -f k8s/
```

## 2. Check Pods and Services

```bash
kubectl get pods
kubectl get services
```

## 3. Test the Application

```bash
kubectl port-forward service/app-service 8080:8080
```

In another terminal, run:

```bash
curl http://localhost:8080/health
curl -X POST http://localhost:8080/count/increment
curl http://localhost:8080/count
```

## 4. Observations

The Flask and Redis pods started successfully. The application was tested, and the counter worked correctly with Redis.