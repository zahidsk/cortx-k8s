# cortx

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.0.0-803](https://img.shields.io/badge/AppVersion-2.0.0--803-informational?style=flat-square)

CORTX is a distributed object storage system designed for great efficiency, massive capacity, and high HDD-utilization.

**Homepage:** <https://github.com/Seagate/cortx-k8s/tree/integration/charts/cortx>

## Source Code

* <https://github.com/Seagate/cortx>
* <https://github.com/Seagate/cortx-k8s>

## Requirements

Kubernetes: `>=1.22.0-0`

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | kafka | 16.2.7 |
| https://helm.releases.hashicorp.com | consul | 0.42.0 |

## Installation

### Downloading the Chart

Locally download the Chart files:

```bash
git clone https://github.com/Seagate/cortx-k8s.git
```

Install Chart dependencies:

```bash
helm repo add hashicorp https://helm.releases.hashicorp.com
helm repo add bitnami https://charts.bitnami.com/bitnami
helm dependency build cortx-k8s/charts/cortx
```

### Installing the Chart

To install the chart with the release name `cortx` and a configuration specified by the `myvalues.yaml` file:

```bash
helm install cortx cortx-k8s/charts/cortx -f myvalues.yaml
```

See the [Parameters](#parameters) section for details about all of the options available for configuration.

### Uninstalling the Chart

To uninstall the `cortx` release:

```bash
helm uninstall cortx
```

## Parameters

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| configmap.clusterId | string | `""` |  |
| configmap.clusterName | string | `"cortx-cluster"` |  |
| configmap.clusterStorageSets | object | `{}` |  |
| configmap.clusterStorageVolumes | object | `{}` |  |
| configmap.cortxControl.agent.resources.limits.cpu | string | `"500m"` |  |
| configmap.cortxControl.agent.resources.limits.memory | string | `"256Mi"` |  |
| configmap.cortxControl.agent.resources.requests.cpu | string | `"250m"` |  |
| configmap.cortxControl.agent.resources.requests.memory | string | `"128Mi"` |  |
| configmap.cortxControl.enabled | bool | `true` |  |
| configmap.cortxHa.enabled | bool | `true` |  |
| configmap.cortxHa.fault_tolerance.resources.limits.cpu | string | `"500m"` |  |
| configmap.cortxHa.fault_tolerance.resources.limits.memory | string | `"1Gi"` |  |
| configmap.cortxHa.fault_tolerance.resources.requests.cpu | string | `"250m"` |  |
| configmap.cortxHa.fault_tolerance.resources.requests.memory | string | `"128Mi"` |  |
| configmap.cortxHa.health_monitor.resources.limits.cpu | string | `"500m"` |  |
| configmap.cortxHa.health_monitor.resources.limits.memory | string | `"1Gi"` |  |
| configmap.cortxHa.health_monitor.resources.requests.cpu | string | `"250m"` |  |
| configmap.cortxHa.health_monitor.resources.requests.memory | string | `"128Mi"` |  |
| configmap.cortxHa.k8s_monitor.resources.limits.cpu | string | `"500m"` |  |
| configmap.cortxHa.k8s_monitor.resources.limits.memory | string | `"1Gi"` |  |
| configmap.cortxHa.k8s_monitor.resources.requests.cpu | string | `"250m"` |  |
| configmap.cortxHa.k8s_monitor.resources.requests.memory | string | `"128Mi"` |  |
| configmap.cortxHare.hax.resources.limits.cpu | string | `"1000m"` |  |
| configmap.cortxHare.hax.resources.limits.memory | string | `"2Gi"` |  |
| configmap.cortxHare.hax.resources.requests.cpu | string | `"250m"` |  |
| configmap.cortxHare.hax.resources.requests.memory | string | `"128Mi"` |  |
| configmap.cortxHare.haxClientEndpoints | list | `[]` |  |
| configmap.cortxHare.haxDataEndpoints | list | `[]` |  |
| configmap.cortxHare.haxServerEndpoints | list | `[]` |  |
| configmap.cortxIoService.name | string | `"cortx-io-svc-0"` |  |
| configmap.cortxIoService.ports.http | string | `""` |  |
| configmap.cortxIoService.ports.https | string | `""` |  |
| configmap.cortxMotr.clientEndpoints | list | `[]` |  |
| configmap.cortxMotr.clientInstanceCount | int | `0` |  |
| configmap.cortxMotr.confd.resources.limits.cpu | string | `"500m"` |  |
| configmap.cortxMotr.confd.resources.limits.memory | string | `"512Mi"` |  |
| configmap.cortxMotr.confd.resources.requests.cpu | string | `"250m"` |  |
| configmap.cortxMotr.confd.resources.requests.memory | string | `"128Mi"` |  |
| configmap.cortxMotr.confdEndpoints | list | `[]` |  |
| configmap.cortxMotr.extraConfiguration | string | `""` |  |
| configmap.cortxMotr.iosEndpoints | list | `[]` |  |
| configmap.cortxMotr.motr.resources.limits.cpu | string | `"1000m"` |  |
| configmap.cortxMotr.motr.resources.limits.memory | string | `"2Gi"` |  |
| configmap.cortxMotr.motr.resources.requests.cpu | string | `"250m"` |  |
| configmap.cortxMotr.motr.resources.requests.memory | string | `"1Gi"` |  |
| configmap.cortxMotr.rgwEndpoints | list | `[]` |  |
| configmap.cortxRgw.authAdmin | string | `"cortx-admin"` |  |
| configmap.cortxRgw.authSecret | string | `"s3_auth_admin_secret"` |  |
| configmap.cortxRgw.authUser | string | `"cortx-user"` |  |
| configmap.cortxRgw.enabled | bool | `true` |  |
| configmap.cortxRgw.extraConfiguration | string | `""` |  |
| configmap.cortxRgw.maxStartTimeout | int | `240` |  |
| configmap.cortxRgw.rgw.resources.limits.cpu | string | `"2000m"` |  |
| configmap.cortxRgw.rgw.resources.limits.memory | string | `"2Gi"` |  |
| configmap.cortxRgw.rgw.resources.requests.cpu | string | `"250m"` |  |
| configmap.cortxRgw.rgw.resources.requests.memory | string | `"128Mi"` |  |
| configmap.cortxSecretName | string | `"cortx-secret"` |  |
| configmap.cortxSecretValues | object | `{}` |  |
| configmap.cortxStoragePaths.config | string | `"/etc/cortx"` |  |
| configmap.cortxStoragePaths.local | string | `"/etc/cortx"` |  |
| configmap.cortxStoragePaths.log | string | `"/etc/cortx/log"` |  |
| configmap.cortxVersion | string | `"unknown"` |  |
| consul.client.containerSecurityContext.client.allowPrivilegeEscalation | bool | `false` | Allow extra privileges in Consul client agent containers |
| consul.enabled | bool | `true` | Enable installation of the Consul chart |
| consul.server.containerSecurityContext.server.allowPrivilegeEscalation | bool | `false` | Allow extra privileges in Consul server agent containers |
| consul.ui.enabled | bool | `false` | Enable the Consul UI |
| externalConsul.adminSecretName | string | `"consul_admin_secret"` |  |
| externalConsul.adminUser | string | `"admin"` |  |
| externalConsul.endpoints | list | `[]` |  |
| externalKafka.adminSecretName | string | `"kafka_admin_secret"` |  |
| externalKafka.adminUser | string | `"admin"` |  |
| externalKafka.endpoints | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| kafka.containerSecurityContext.allowPrivilegeEscalation | bool | `false` | Allow extra privileges in Kafka containers |
| kafka.deleteTopicEnable | bool | `true` | Enable topic deletion |
| kafka.enabled | bool | `true` | Enable installation of the Kafka chart |
| kafka.serviceAccount.automountServiceAccountToken | bool | `false` | Allow auto mounting of the service account token |
| kafka.serviceAccount.create | bool | `true` | Enable the creation of a ServiceAccount for Kafka pods |
| kafka.transactionStateLogMinIsr | int | `2` | Overridden min.insync.replicas config for the transaction topic |
| kafka.zookeeper.containerSecurityContext.allowPrivilegeEscalation | bool | `false` | Allow extra privileges in Zookeeper containers |
| kafka.zookeeper.enabled | bool | `true` | Enable installation of the Zookeeper chart |
| kafka.zookeeper.serviceAccount.automountServiceAccountToken | bool | `false` | Allow auto mounting of the service account token |
| kafka.zookeeper.serviceAccount.create | bool | `true` | Enable the creation of a ServiceAccount for Zookeeper pods |
| nameOverride | string | `""` |  |
| platform.networkPolicy.cortxControl.podAppLabel | string | `"cortx-control-pod"` |  |
| platform.networkPolicy.cortxData.podNameLabel | string | `"cortx-data"` |  |
| platform.networkPolicy.create | bool | `false` |  |
| platform.podSecurityPolicy.create | bool | `false` |  |
| platform.rbacRole.create | bool | `true` |  |
| platform.rbacRoleBinding.create | bool | `true` |  |
| platform.services.hax.port | int | `22003` |  |
| platform.services.hax.protocol | string | `"https"` |  |
| platform.services.hax.type | string | `"ClusterIP"` |  |
| platform.services.io.count | int | `1` |  |
| platform.services.io.name | string | `"cortx-io-svc"` |  |
| platform.services.io.nodePorts.http | string | `""` |  |
| platform.services.io.nodePorts.https | string | `""` |  |
| platform.services.io.ports.http | int | `80` |  |
| platform.services.io.ports.https | int | `443` |  |
| platform.services.io.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` | Custom annotations for the CORTX ServiceAccount |
| serviceAccount.automountServiceAccountToken | bool | `false` | Allow auto mounting of the service account token |
| serviceAccount.create | bool | `true` | Enable the creation of a ServiceAccount for CORTX pods |
| serviceAccount.name | string | `""` | The name of the service account to use. If not set and `create` is true, a name is generated using the fullname template |
