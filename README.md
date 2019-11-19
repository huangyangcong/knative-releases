knative-releases

#### 下载
```
wget https://github.com/knative/serving/releases/download/v0.10.0/serving.yaml
wget https://github.com/knative/eventing/releases/download/v0.10.1/release.yaml
wget https://github.com/knative/serving/releases/download/v0.10.0/monitoring.yaml
```
#### 替换
```
find ./ -name "*.yaml"|xargs sed -i 's/@sha256\S*/:v0.10.0/g' 
```
#### 执行
```
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-activator:v0.10.0
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-autoscaler:v0.10.0
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-autoscaler-hpa:v0.10.0
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-queue:v0.10.0
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-controller:v0.10.0
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-webhook:v0.10.0
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-networking:v0.10.0
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-broker-ingress:v0.10.1
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-broker-filter:v0.10.1
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-controller:v0.10.1
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-cronjob_receive_adapter:v0.10.1
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-apiserver_receive_adapter:v0.10.1
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-sources_controller:v0.10.0
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-webhook:v0.10.0
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-in_memory-channel_controller:v0.10.0
docker pull registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-in_memory-channel_dispatcher:v0.10.0


docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-activator:v0.10.0 gcr.io/knative-releases/knative.dev/serving/cmd/activator:v0.10.0
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-autoscaler:v0.10.0 gcr.io/knative-releases/knative.dev/serving/cmd/autoscaler:v0.10.0
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-autoscaler-hpa:v0.10.0 gcr.io/knative-releases/knative.dev/serving/cmd/autoscaler-hpa:v0.10.0
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-queue:v0.10.0 gcr.io/knative-releases/knative.dev/serving/cmd/queue:v0.10.0
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-controller:v0.10.0 gcr.io/knative-releases/knative.dev/serving/cmd/controller:v0.10.0
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-webhook:v0.10.0 gcr.io/knative-releases/knative.dev/serving/cmd/webhook:v0.10.0
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-networking:v0.10.0 gcr.io/knative-releases/knative.dev/serving/cmd/networking/istio:v0.10.0
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-broker-ingress:v0.10.1 gcr.io/knative-releases/knative.dev/eventing/cmd/broker/ingress:v0.10.1
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-broker-filter:v0.10.1 gcr.io/knative-releases/knative.dev/eventing/cmd/broker/filter:v0.10.1
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-controller:v0.10.1 gcr.io/knative-releases/knative.dev/eventing/cmd/controller:v0.10.1
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-cronjob_receive_adapter:v0.10.1 gcr.io/knative-releases/knative.dev/eventing/cmd/cronjob_receive_adapter:v0.10.1
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-apiserver_receive_adapter:v0.10.1 gcr.io/knative-releases/knative.dev/eventing/cmd/apiserver_receive_adapter:v0.10.1
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-sources_controller:v0.10.0 gcr.io/knative-releases/knative.dev/eventing/cmd/sources_controller:v0.10.0
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-webhook:v0.10.0 gcr.io/knative-releases/knative.dev/eventing/cmd/webhook:v0.10.0
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-in_memory-channel_controller:v0.10.0 gcr.io/knative-releases/knative.dev/eventing/cmd/in_memory/channel_controller:v0.10.0
docker tag registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-in_memory-channel_dispatcher:v0.10.0 gcr.io/knative-releases/knative.dev/eventing/cmd/in_memory/channel_dispatcher:v0.10.0

docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-activator:v0.10.0
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-autoscaler:v0.10.0
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-autoscaler-hpa:v0.10.0
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-queue:v0.10.0
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-controller:v0.10.0
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-webhook:v0.10.0
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/serving-networking:v0.10.0
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-broker-ingress:v0.10.1
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-broker-filter:v0.10.1
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-controller:v0.10.1
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-cronjob_receive_adapter:v0.10.1
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-apiserver_receive_adapter:v0.10.1
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-sources_controller:v0.10.0
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-webhook:v0.10.0
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-in_memory-channel_controller:v0.10.0
docker rmi registry.cn-hangzhou.aliyuncs.com/knative-mirrors/eventing-in_memory-channel_dispatcher:v0.10.0
```
