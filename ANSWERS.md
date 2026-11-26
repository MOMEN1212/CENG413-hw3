# HW-3 Answers

## 1. What is the difference between readiness and liveness probes?

A readiness probe checks if the application is ready to receive requests. A liveness probe checks if the application is still working. If readiness fails, Kubernetes stops sending traffic to the pod, while a liveness failure can cause the container to restart.

## 2. Why is a Secret not the same as encryption?

A Kubernetes Secret stores sensitive information, but it is not automatically encrypted just because it is called a Secret. Its data is normally base64-encoded, which is easy to decode. Proper encryption and access permissions are needed to protect real passwords.

## 3. What happens when a container crosses its memory limit?

If a container uses more memory than its limit, Kubernetes may terminate it with an OOMKilled error. The container can then restart depending on its restart policy. This can cause the application to become temporarily unavailable.