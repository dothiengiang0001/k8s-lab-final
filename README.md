- Cách lệnh chạy:

kubectl apply -f nginx-proxy/nginx-proxy-deployment.yaml
kubectl apply -f nginx-proxy/nginx-proxy-service.yaml

kubectl apply -f web1/web1-deployment.yaml
kubectl apply -f web1/web1-service.yaml

kubectl apply -f web2/web2-deployment.yaml
kubectl apply -f web2/web2-service.yaml

- Chọn worker node cụ thể khi triển khai tài nguyên:

kubectl apply -f <your-resource-file.yaml> --node="node-name"

- Chọn worker node dựa trên các điều kiện hoặc labels:

kubectl apply -f <your-resource-file.yaml> --selector="label-key"="label-value"
