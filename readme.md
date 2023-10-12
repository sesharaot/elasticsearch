# 1st install below CRD

#### Install custom resource definitions:

kubectl create -f https://download.elastic.co/downloads/eck/2.9.0/crds.yaml

The following Elastic resources have been created:

customresourcedefinition.apiextensions.k8s.io/agents.agent.k8s.elastic.co created
customresourcedefinition.apiextensions.k8s.io/apmservers.apm.k8s.elastic.co created
customresourcedefinition.apiextensions.k8s.io/beats.beat.k8s.elastic.co created
customresourcedefinition.apiextensions.k8s.io/elasticmapsservers.maps.k8s.elastic.co created
customresourcedefinition.apiextensions.k8s.io/elasticsearches.elasticsearch.k8s.elastic.co created
customresourcedefinition.apiextensions.k8s.io/enterprisesearches.enterprisesearch.k8s.elastic.co created
customresourcedefinition.apiextensions.k8s.io/kibanas.kibana.k8s.elastic.co created
customresourcedefinition.apiextensions.k8s.io/logstashes.logstash.k8s.elastic.co created




#### Install the operator with its RBAC rules:

kubectl apply -f https://download.elastic.co/downloads/eck/2.9.0/operator.yaml


#### Monitor the operator logs:

kubectl -n elastic-system logs -f statefulset.apps/elastic-operator