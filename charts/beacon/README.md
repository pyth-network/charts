# beacon

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v1.0.0](https://img.shields.io/badge/AppVersion-v1.0.0-informational?style=flat-square)

Highly available Wormhole RPC

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| beacon.heartbeatInterval | int | `5` | Heartbeat interval in seconds. The liveness probe will fail if the latency between the VAAs and the current time    is greater than the heartbeat interval. Must be set. |
| beacon.logLevel | string | `"warn"` | Beacon log level. Valid values are: trace, debug, info, warn, error |
| beacon.natsStream | string | `nil` | NATS stream name. Must be set. Example: mainnet-vaas |
| beacon.natsUrl | string | `nil` | NATS server URL. Must be set. Example: 1.2.3.4:4222 |
| beacon.wormholeBootstrapAddrs | string | `"/dns4/wormhole-mainnet-v2-bootstrap.certus.one/udp/8999/quic/p2p/12D3KooWQp644DK27fd3d4Km3jr7gHiuJJ5ZGmy8hH4py7fP4FP7,/dns4/wormhole-v2-mainnet-bootstrap.xlabs.xyz/udp/8999/quic/p2p/12D3KooWNQ9tVrcb64tw6bNs2CaNrUGPM7yRrKvBBheQ5yCyPHKC"` | Wormhole bootstrap addresses |
| beacon.wormholeNetworkId | string | `"/wormhole/mainnet/2"` | Wormhole network id |
| beacon.writerBatchSize | int | `1000` | Batch size for the writer. When the batch size is reached, the writer will flush the batch to the NATS stream. |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"public.ecr.aws/pyth-network/beacon"` |  |
| image.tag | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext.fsGroup | int | `10001` |  |
| podSecurityContext.runAsGroup | int | `10001` |  |
| podSecurityContext.runAsNonRoot | bool | `true` |  |
| podSecurityContext.runAsUser | int | `10001` |  |
| replicaCount | int | `3` | Number of Beacon replicas |
| resources.limits | object | `{}` |  |
| resources.requests.cpu | int | `1` |  |
| resources.requests.memory | string | `"1Gi"` |  |
| securityContext.allowPrivilegeEscalation | bool | `false` |  |
| securityContext.capabilities.drop[0] | string | `"ALL"` |  |
| securityContext.readOnlyRootFilesystem | bool | `true` |  |
| service.grpcPort | int | `8080` |  |
| service.metricsPort | int | `8081` |  |
| service.type | string | `"ClusterIP"` |  |
| service.wormholeListenPort | int | `8999` |  |
| tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.3](https://github.com/norwoodj/helm-docs/releases/v1.11.3)