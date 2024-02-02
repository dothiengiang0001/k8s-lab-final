- Các lệnh chạy:

kubectl apply -f nginx-proxy/nginx-proxy-deployment.yaml ; \

kubectl apply -f nginx-proxy/nginx-proxy-service.yaml ; \

kubectl apply -f web1/web1-deployment.yaml ; \

kubectl apply -f web1/web1-service.yaml ; \

kubectl apply -f web2/web2-deployment.yaml ; \

kubectl apply -f web2/web2-service.yaml

- Các lệnh chạy trên k3s tại 1 node tên là "workernode":

kubectl apply -f nginx-proxy/nginx-proxy-deployment.yaml --node=workernode ; \

kubectl apply -f nginx-proxy/nginx-proxy-service.yaml --node=workernode ; \

kubectl apply -f web1/web1-deployment.yaml --node=workernode ; \

kubectl apply -f web1/web1-service.yaml --node=workernode ; \

kubectl apply -f web2/web2-deployment.yaml --node=workernode ; \

kubectl apply -f web2/web2-service.yaml --node=workernode

- Chọn worker node cụ thể khi triển khai tài nguyên:

kubectl apply -f <your-resource-file.yaml> --node="node-name"

- Chọn worker node dựa trên các điều kiện hoặc labels:

kubectl apply -f <your-resource-file.yaml> --selector="label-key"="label-value"
