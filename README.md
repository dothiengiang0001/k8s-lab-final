- Các lệnh chạy:

kubectl apply -f nginx-proxy/nginx-proxy-deployment.yaml ; \

kubectl apply -f nginx-proxy/nginx-proxy-service.yaml ; \

kubectl apply -f web1/web1-deployment.yaml ; \

kubectl apply -f web1/web1-service.yaml ; \

kubectl apply -f web2/web2-deployment.yaml ; \

kubectl apply -f web2/web2-service.yaml

- Các lệnh chạy trên k3s tại 1 node tên là "workernode":

sudo k3s kubectl apply -f nginx-proxy/nginx-proxy-deployment.yaml \

sudo k3s kubectl apply -f nginx-proxy/nginx-proxy-service.yaml \

sudo k3s kubectl apply -f web1/web1-deployment.yaml \

sudo k3s kubectl apply -f web1/web1-deployment.yaml \

sudo k3s  kubectl apply -f web1/web1-service.yaml \

sudo k3s kubectl apply -f web2/web2-deployment.yaml \

sudo k3s kubectl apply -f web2/web2-service.yaml

- Chọn worker node cụ thể khi triển khai tài nguyên:

kubectl apply -f <your-resource-file.yaml> --node="node-name"

- Chọn worker node dựa trên các điều kiện hoặc labels:

kubectl apply -f <your-resource-file.yaml> --selector="label-key"="label-value"

- Các lệnh thường dùng:
- 
kubectl get pods,service,node -o wide

