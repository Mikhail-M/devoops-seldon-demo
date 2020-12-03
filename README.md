# devoops-seldon-demo

1) 
kubectl create namespace seldon-system
kubectl label namespace seldon-system istio-injection=enabled
kubectl create namespace model-namespace
kubectl label namespace model-namespace istio-injection=enabled


устанавливаем seldon operator

~~~
helm install seldon-core seldon-core-operator \
    --repo https://storage.googleapis.com/seldon-charts \
    --set usageMetrics.enabled=true \
    --namespace seldon-system \
    --set istio.enabled=true
~~~


http://34.70.244.125/seldon/model-namespace/mlflow/api/v1.0/doc/#/
http://34.70.244.125/seldon/model-namespace/iris-model/api/v1.0/doc/#

data: 
{ "data": { "ndarray": [[1,2,3,4]] } }

