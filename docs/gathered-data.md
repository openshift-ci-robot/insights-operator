This document is auto-generated by `make docs`

## CRD

collects the specified Custom Resource Definitions.

The following CRDs are gathered:
- volumesnapshots.snapshot.storage.k8s.io (10745 bytes)
- volumesnapshotcontents.snapshot.storage.k8s.io (13149 bytes)

The CRD sizes above are in the raw (uncompressed) state.

* Location in archive: config/crd/
* Id in config: crds


## CertificateSigningRequests

collects anonymized CertificateSigningRequests.
Collects CSRs which werent Verified, or when Now < ValidBefore or Now > ValidAfter

The Kubernetes api:
    https://github.com/kubernetes/client-go/blob/master/kubernetes/typed/certificates/v1beta1/certificatesigningrequest.go#L78
Response see:
    https://docs.openshift.com/container-platform/4.3/rest_api/index.html#certificatesigningrequestlist-v1beta1certificates

* Location in archive: config/certificatesigningrequests/
* Id in config: certificate_signing_requests
* Since versions:
  * 4.3.25+
  * 4.4.12+
  * 4.5+


## ClusterAuthentication

fetches the cluster Authentication - the Authentication with name cluster.

The Kubernetes api https://github.com/openshift/client-go/blob/master/config/clientset/versioned/typed/config/v1/authentication.go#L50
Response see https://docs.openshift.com/container-platform/4.3/rest_api/index.html#authentication-v1operator-openshift-io

* Location in archive: config/authentication/
* See: docs/insights-archive-sample/config/authentication
* Id in config: authentication


## ClusterFeatureGates

fetches the cluster FeatureGate - the FeatureGate with name cluster.

The Kubernetes api https://github.com/openshift/client-go/blob/master/config/clientset/versioned/typed/config/v1/featuregate.go#L50
Response see https://docs.openshift.com/container-platform/4.3/rest_api/index.html#featuregate-v1-config-openshift-io

* Location in archive: config/featuregate/
* See: docs/insights-archive-sample/config/featuregate
* Id in config: feature_gates


## ClusterImagePruner

fetches the image pruner configuration

* Location in archive: config/clusteroperator/imageregistry.operator.openshift.io/imagepruner/cluster.json
* Id in config: image_pruners


## ClusterImageRegistry

fetches the cluster Image Registry configuration

**Conditional data**: If the Image Registry configuration uses any PersistentVolumeClaim for the storage, the corresponding
PersistentVolume definition is gathered

* Location in archive: config/clusteroperator/imageregistry.operator.openshift.io/config/cluster.json
* Id in config: image_registries
* Since versions:
  * 4.3.40+
  * 4.4.12+
  * 4.5+
* PV definition since versions:
  * 4.6.20+
  * 4.7+


## ClusterInfrastructure

fetches the cluster Infrastructure - the Infrastructure with name cluster.

The Kubernetes api https://github.com/openshift/client-go/blob/master/config/clientset/versioned/typed/config/v1/infrastructure.go#L50
Response see https://docs.openshift.com/container-platform/4.3/rest_api/index.html#infrastructure-v1-config-openshift-io

* Location in archive: config/infrastructure/
* See: docs/insights-archive-sample/config/infrastructure
* Id in config: infrastructures


## ClusterIngress

fetches the cluster Ingress - the Ingress with name cluster.

The Kubernetes api https://github.com/openshift/client-go/blob/master/config/clientset/versioned/typed/config/v1/ingress.go#L50
Response see https://docs.openshift.com/container-platform/4.3/rest_api/index.html#ingress-v1-config-openshift-io

* Location in archive: config/ingress/
* See: docs/insights-archive-sample/config/ingress
* Id in config: ingress


## ClusterNetwork

fetches the cluster Network - the Network with name cluster.

The Kubernetes api https://github.com/openshift/client-go/blob/master/config/clientset/versioned/typed/config/v1/network.go#L50
Response see https://docs.openshift.com/container-platform/4.3/rest_api/index.html#network-v1-config-openshift-io

* Location in archive: config/network/
* See: docs/insights-archive-sample/config/network
* Id in config: networks


## ClusterOAuth

fetches the cluster OAuth - the OAuth with name cluster.

The Kubernetes api https://github.com/openshift/client-go/blob/master/config/clientset/versioned/typed/config/v1/oauth.go#L50
Response see https://docs.openshift.com/container-platform/4.3/rest_api/index.html#oauth-v1-config-openshift-io

* Location in archive: config/oauth/
* See: docs/insights-archive-sample/config/oauth
* Id in config: oauths


## ClusterOperatorPodsAndEvents

collects information about all pods
and events from namespaces of degraded cluster operators. The collected
information includes:

- Pod definitions
- Previous and current logs of pod containers (when available)
- Namespace events

* Location of pod definitions: config/pod/{namespace}/{pod}.json
* Location of pod container current logs:
  config/pod/{namespace}/logs/{pod}/{container}_current.log
* Location of pod container previous logs:
  config/pod/{namespace}/logs/{pod}/{container}_previous.log
* Location of events in archive: events/
* Id in config: operators_pods_and_events
* Spec config for CO resources since versions:
  * 4.6.16+
  * 4.7+


## ClusterOperators

collects all the ClusterOperators definitions and their resources.

The Kubernetes api https://github.com/openshift/client-go/blob/master/config/clientset/versioned/typed/config/v1/clusteroperator.go#L62
Response see https://docs.openshift.com/container-platform/4.3/rest_api/index.html#clusteroperatorlist-v1config-openshift-io

* Location of operators in archive: config/clusteroperator/
* See: docs/insights-archive-sample/config/clusteroperator
* Id in config: operators
* Spec config for CO resources since versions:
  * 4.6.16+
  * 4.7+


## ClusterProxy

fetches the cluster Proxy - the Proxy with name cluster.

The Kubernetes api https://github.com/openshift/client-go/blob/master/config/clientset/versioned/typed/config/v1/proxy.go#L30
Response see https://docs.openshift.com/container-platform/4.3/rest_api/index.html#proxy-v1-config-openshift-io

* Location in archive: config/proxy/
* See: docs/insights-archive-sample/config/proxy
* Id in config: proxies


## ClusterVersion

fetches the ClusterVersion (including the cluster ID) with the name 'version' and its resources.

The Kubernetes api https://github.com/openshift/client-go/blob/master/config/clientset/versioned/typed/config/v1/clusterversion.go#L50
Response see https://docs.openshift.com/container-platform/4.3/rest_api/index.html#clusterversion-v1config-openshift-io

* Location in archive: config/version/
* See: docs/insights-archive-sample/config/version
* Location of pods in archive: config/pod/
* Location of events in archive: events/
* Location of cluster ID: config/id
* See: docs/insights-archive-sample/config/id
* Id in config: version


## ConfigMaps

fetches the ConfigMaps from namespace openshift-config
and tries to fetch "cluster-monitoring-config" ConfigMap from openshift-monitoring namespace.

Anonymization: If the content of ConfigMap contains a parseable PEM structure (like certificate) it removes the inside of PEM blocks.
For ConfigMap of type BinaryData it is encoded as standard base64.
In the archive under configmaps we store name of the namespace, name of the ConfigMap and then each ConfigMap Key.
For example config/configmaps/NAMESPACENAME/CONFIGMAPNAME/CONFIGMAPKEY1

The Kubernetes api https://github.com/kubernetes/client-go/blob/master/kubernetes/typed/core/v1/configmap.go#L80
Response see https://docs.openshift.com/container-platform/4.3/rest_api/index.html#configmaplist-v1core

* Location in archive: config/configmaps/{namespace-name}/{configmap-name}/
* See: docs/insights-archive-sample/config/configmaps
* Id in config: config_maps
* Since versions:
  * 4.3.25+
  * 4.4.6+
  * 4.5+
* "cluster-monitoring-config" ConfigMap data since versions:
  * 4.6.22+
  * 4.7+


## ContainerImages

collects essential information about running containers.
Specifically, the age of pods, the set of running images and the container names are collected.

* Location in archive: config/running_containers.json
* Id in config: container_images
* Since versions:
  * 4.5.33+
  * 4.6.16+
  * 4.7+


## ContainerRuntimeConfig

collects ContainerRuntimeConfig  information

The Kubernetes api:
   https://github.com/openshift/machine-config-operator/blob/master/pkg/apis/machineconfiguration.openshift.io/v1/types.go#L402
Response see:
   https://docs.okd.io/latest/rest_api/machine_apis/containerruntimeconfig-machineconfiguration-openshift-io-v1.html

* Location in archive: config/containerruntimeconfigs/
* Id in config: container_runtime_configs
* Since versions:
  * 4.6.18+
  * 4.7+


## HostSubnet

collects HostSubnet information

The Kubernetes api https://github.com/openshift/client-go/blob/master/network/clientset/versioned/typed/network/v1/hostsubnet.go
Response see https://docs.openshift.com/container-platform/4.3/rest_api/index.html#hostsubnet-v1-network-openshift-io

* Location in archive: config/hostsubnet/
* Id in config: host_subnets
* Since versions:
  * 4.4.29+
  * 4.5.15+
  * 4.6+


## InstallPlans

collects Top x InstallPlans from all openshift namespaces.
Because InstallPlans have unique generated names, it groups them by namespace and the "template"
for name generation from field generateName.
It also collects Total number of all installplans and all non-unique installplans.

The Operators-Framework api https://github.com/operator-framework/api/blob/master/pkg/operators/v1alpha1/installplan_types.go#L26

* Location in archive: config/installplans/
* Id in config: install_plans
* Since versions:
  * 4.5.33+
  * 4.6.16+
  * 4.7+


## MachineAutoscalers

collects MachineAutoscalers definition

The Kubernetes api:
      https://github.com/openshift/cluster-autoscaler-operator/blob/master/pkg/apis/autoscaling/v1beta1/machineautoscaler_types.go
Response see:
      https://docs.openshift.com/container-platform/4.7/rest_api/autoscale_apis/machineautoscaler-autoscaling-openshift-io-v1beta1.html#machineautoscaler-autoscaling-openshift-io-v1beta1

* Location in archive: config/machineautoscalers/{namespace}/{machineautoscaler-name}.json
* Id in config: machine_autoscalers
* Since versions:
  * 4.8+


## MachineConfigPool

collects MachineConfigPool information

The Kubernetes api:
    https://github.com/openshift/machine-config-operator/blob/master/pkg/apis/machineconfiguration.openshift.io/v1/types.go#L197
Response see:
    https://docs.okd.io/latest/rest_api/machine_apis/machineconfigpool-machineconfiguration-openshift-io-v1.html

* Location in archive: config/machineconfigpools/
* Id in config: machine_config_pools
* Since versions:
  * 4.5.33+
  * 4.6+


## MachineHealthCheck

collects MachineHealthCheck information

The Kubernetes api:
      https://github.com/openshift/machine-api-operator/blob/master/pkg/generated/clientset/versioned/typed/machine/v1beta1/machinehealthcheck.go
Response see:
      https://docs.openshift.com/container-platform/4.3/rest_api/index.html#machinehealthcheck-v1beta1-machine-openshift-io

* Location in archive: config/machinehealthchecks
* Id in config: machine_healthchecks
* Since versions:
  * 4.8+


## MachineSet

collects MachineSet information

The Kubernetes api:
      https://github.com/openshift/machine-api-operator/blob/master/pkg/generated/clientset/versioned/typed/machine/v1beta1/machineset.go
Response see:
      https://docs.openshift.com/container-platform/4.3/rest_api/index.html#machineset-v1beta1-machine-openshift-io

* Location in archive: machinesets/
* Id in config: machine_sets
* Since versions:
  * 4.4.29+
  * 4.5.15+
  * 4.6+


## MostRecentMetrics

gathers cluster Federated Monitoring metrics.

The GET REST query to URL /federate
Gathered metrics:
	 virt_platform
  etcd_object_counts
  cluster_installer
  vsphere_node_hw_version_total
  namespace CPU and memory usage
  followed by at most 1000 lines of ALERTS metric

* Location in archive: config/metrics/
* See: docs/insights-archive-sample/config/metrics
* Id in config: metrics


## NetNamespace

collects NetNamespaces networking information

The Kubernetes api https://github.com/openshift/client-go/blob/master/network/clientset/versioned/typed/network/v1/netnamespace.go
Response is an array of netNamespaces. Netnamespace contains Name, EgressIPs and NetID attributes.

* Location in archive: config/netnamespaces
* Id in config: netnamespaces
* Since versions:
  * 4.6.20+
  * 4.7+


## Nodes

collects all Nodes.

The Kubernetes api https://github.com/kubernetes/client-go/blob/master/kubernetes/typed/core/v1/node.go#L78
Response see https://docs.openshift.com/container-platform/4.3/rest_api/index.html#nodelist-v1core

* Location in archive: config/node/
* Id in config: nodes


## OLMOperators

collects list of installed OLM operators.
Each OLM operator (in the list) contains following data:
- OLM operator name
- OLM operator version
- related ClusterServiceVersion conditions

* See: docs/insights-archive-sample/config/olm_operators
* Location of in archive: config/olm_operators
* Id in config: olm_operators
* Since versions:
  * 4.7+


## OpenShiftAPIServerOperatorLogs

collects logs from openshift-apiserver-operator with following substrings:
  - "the server has received too many requests and has asked us"
  - "because serving request timed out and response had been started"

The Kubernetes API:
      https://github.com/kubernetes/client-go/blob/master/kubernetes/typed/core/v1/pod_expansion.go#L48
Response see:
      https://docs.openshift.com/container-platform/4.6/rest_api/workloads_apis/pod-core-v1.html#apiv1namespacesnamespacepodsnamelog

* Location in archive: config/pod/{namespace-name}/logs/{pod-name}/errors.log


## OpenshiftAuthenticationLogs

collects logs from pods in openshift-authentication namespace with following substring:
  - "AuthenticationError: invalid resource name"

The Kubernetes API:
        https://github.com/kubernetes/client-go/blob/master/kubernetes/typed/core/v1/pod_expansion.go#L48
Response see:
        https://docs.openshift.com/container-platform/4.6/rest_api/workloads_apis/pod-core-v1.html#apiv1namespacesnamespacepodsnamelog

* Location in archive: config/pod/openshift-authentication/logs/{pod-name}/errors.log
* Since versions:
  * 4.7+


## OpenshiftSDNControllerLogs

collects logs from sdn-controller pod in openshift-sdn namespace with following substrings:
  - "Node %s is not Ready": A node has been set offline for egress IPs because it is reported not ready at API
  - "Node %s may be offline... retrying": An egress node has failed the egress IP health check once,
      so it has big chances to be marked as offline soon or, at the very least, there has been a connectivity glitch.
  - "Node %s is offline": An egress node has failed enough probes to have been marked offline for egress IPs.
      If it has egress CIDRs assigned, its egress IPs have been moved to other nodes.
      Indicates issues at either the node or the network between the master and the node.
  - "Node %s is back online": This indicates that a node has recovered from the condition described
      at the previous message, by starting succeeding the egress IP health checks.
      Useful just in case that previous “Node %s is offline” messages are lost,
      so that we have a clue that there was failure previously.

The Kubernetes API:
       https://github.com/kubernetes/client-go/blob/master/kubernetes/typed/core/v1/pod_expansion.go#L48
Response see:
       https://docs.openshift.com/container-platform/4.6/rest_api/workloads_apis/pod-core-v1.html#apiv1namespacesnamespacepodsnamelog

* Location in archive: config/pod/openshift-sdn/logs/{pod-name}/errors.log
* Since versions:
  * 4.6.21+
  * 4.7+


## OpenshiftSDNLogs

collects logs from pods in openshift-sdn namespace with following substrings:
  - "Got OnEndpointsUpdate for unknown Endpoints",
  - "Got OnEndpointsDelete for unknown Endpoints",
  - "Unable to update proxy firewall for policy",
  - "Failed to update proxy firewall for policy",

The Kubernetes API:
         https://github.com/kubernetes/client-go/blob/master/kubernetes/typed/core/v1/pod_expansion.go#L48
Response see:
         https://docs.openshift.com/container-platform/4.6/rest_api/workloads_apis/pod-core-v1.html#apiv1namespacesnamespacepodsnamelog

* Location in archive: config/pod/openshift-sdn/logs/{pod-name}/errors.log
* Since versions:
  * 4.6.19+
  * 4.7+


## PNCC

collects a summary of failed PodNetworkConnectivityChecks.
Time of the most recently failed check with each reason and message is recorded.
The checks are requested via a dynamic client and
then unmarshaled into the appropriate structure.

Resource API: podnetworkconnectivitychecks.controlplane.operator.openshift.io/v1alpha1
Docs for relevant types: https://pkg.go.dev/github.com/openshift/api/operatorcontrolplane/v1alpha1

* Location in archive: config/podnetworkconnectivitychecks.json
* Id in config: pod_network_connectivity_checks
* Since versions:
  * 4.8+


## PodDisruptionBudgets

gathers the cluster's PodDisruptionBudgets.

The Kubernetes api https://github.com/kubernetes/client-go/blob/v11.0.0/kubernetes/typed/policy/v1beta1/poddisruptionbudget.go#L80
Response see https://docs.okd.io/latest/rest_api/policy_apis/poddisruptionbudget-policy-v1beta1.html

* Location in archive: config/pdbs/
* See: docs/insights-archive-sample/config/pdbs
* Id in config: pdbs
* Since versions:
  * 4.4.30+
  * 4.5.34+
  * 4.6+


## SAPConfig

collects selected security context constraints
and cluster role bindings from clusters running a SAP payload.

**Conditional data**: This data is collected only if the "installers.datahub.sap.com" resource is found in the cluster.

Relevant OpenShift API docs:
  - https://pkg.go.dev/github.com/openshift/client-go/authorization/clientset/versioned/typed/authorization/v1
  - https://pkg.go.dev/github.com/openshift/client-go/security/clientset/versioned/typed/security/v1

* Location in archive: config/securitycontentconstraint/, config/clusterrolebinding/
* Since versions:
  * 4.6.20+
  * 4.7+


## SAPDatahubs

collects `datahubs.installers.datahub.sap.com` resources from SAP/SDI clusters.

* Location in archive: customresources/installers.datahub.sap.com/datahubs/<namespace>/<name>.json
* Since versions:
  * 4.7.5+
  * 4.8+


## SAPMachineConfigs

collects a subset of MachineConfigs related to SDI by applying a set of filtering rules.

Gathered MachineConfigs at the time of implementation of the gatherer:
* `75-worker-sap-data-intelligence`
* `75-master-sap-data-intelligence`
* `99-sdi-generated-containerruntime`

Response see https://docs.openshift.com/container-platform/4.7/rest_api/machine_apis/machineconfig-machineconfiguration-openshift-io-v1.html

* Location in archive: config/machineconfigs/<name>.json
* Id in config: sap_machine_configs
* Since versions:
  * 4.8+

## SAPPods

collects information about pods running in SAP/SDI namespaces.
Only pods with a failing status are collected.
Failed pods belonging to a job that has later succeeded are ignored.

**Conditional data**: This data is collected only if the "installers.datahub.sap.com" resource is found in the cluster.

Relevant Kubernetes API docs:
  - https://pkg.go.dev/k8s.io/client-go/kubernetes/typed/core/v1
  - https://pkg.go.dev/k8s.io/client-go/kubernetes/typed/batch/v1
  - https://pkg.go.dev/k8s.io/client-go/dynamic

* Location in archive: config/pod/{namespace}/{pod-name}.json
* Since versions:
  * 4.6.24+
  * 4.7.5+
  * 4.8+


## SAPVsystemIptablesLogs

collects logs from SAP vsystem-iptables containers
including one from license management pods with the following substring:
  - "can't initialize iptables table",

**Conditional data**: This data is collected only if the "installers.datahub.sap.com" resource is found in the cluster.

The Kubernetes API:
       https://github.com/kubernetes/client-go/blob/master/kubernetes/typed/core/v1/pod_expansion.go#L48
Response see:
       https://docs.openshift.com/container-platform/4.6/rest_api/workloads_apis/pod-core-v1.html#apiv1namespacesnamespacepodsnamelog

* Location in archive: config/pod/{namespace}/logs/{pod-name}/errors.log
* Since versions:
  * 4.6.25+
  * 4.7.5+
  * 4.8+


## ServiceAccounts

collects ServiceAccount stats
from kubernetes default and namespaces starting with openshift.

The Kubernetes api https://github.com/kubernetes/client-go/blob/master/kubernetes/typed/core/v1/serviceaccount.go#L83
Response see https://docs.openshift.com/container-platform/4.3/rest_api/index.html#serviceaccount-v1-core

* Location of serviceaccounts in archive: config/serviceaccounts
* See: docs/insights-archive-sample/config/serviceaccounts
* Id in config: service_accounts
* Since versions:
  * 4.5.34+
  * 4.6.20+
  * 4.7+


## WorkloadInfo

collects summarized info about the workloads on a cluster
in a generic fashion

* Location in archive: config/workload_info
* Id in config: workload_info
* Since versions:
  * 4.8+


