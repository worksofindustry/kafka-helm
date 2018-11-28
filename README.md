# Confluent Open Source Helm Chart

## Documentation

The Confluent Helm Chart documentation is located at [docs.confluent.io](https://docs.confluent.io/current/quickstart/cp-helm-charts/docs/index.html).

## Thanks

Huge thanks to:

- [Kafka helm chart](https://github.com/kubernetes/charts/tree/master/incubator/kafka)
- [ZooKeeper helm chart](https://github.com/kubernetes/charts/tree/master/incubator/zookeeper)
- [Schema Registry helm chart](https://github.com/kubernetes/charts/tree/master/incubator/schema-registry)
- [kubernetes-kafka](https://github.com/Yolean/kubernetes-kafka)
- [docker-kafka](https://github.com/solsson/dockerfiles)
- [Hydromax USA](https://www.hydromaxusa.com)

## Installation Help

The documentation out there is limited, so here are some tips that'll help you with your install. To use this repo you'll need a working Kubernetes Cluster, Helm and Tiller installed.

- To install to local repo: git clone https://github.com/worksofindustry/kafka-helm.git
- After adding in your own value.yaml file rebuild the repo running: helm package kafka-helm from on the 
  top level of the directory. 
- After making any changes its best practice to recreate the index.yaml file by going inside of the repo
  and running helm repo index .
- Run a dry-run to verify no bugs ex. helm install --dry-run --debug -f ./kafka-helm/charts/cp-kafka/my-values.yaml ./cp-helm-charts >      debug.txt 
- Keep deployments and release names shorter than 64 char due to DNS naming limitations. 

