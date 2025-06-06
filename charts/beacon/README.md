# beacon

> **:exclamation: This Helm Chart is deprecated!**

![Version: 1.1.1](https://img.shields.io/badge/Version-1.1.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v1.1.3](https://img.shields.io/badge/AppVersion-v1.1.3-informational?style=flat-square)

Highly available Wormhole RPC

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| beacon.heartbeatInterval | int | `5` | Heartbeat interval in seconds. The liveness probe will fail if the latency between the VAAs and the current time    is greater than the heartbeat interval. Must be set. |
| beacon.logLevel | string | `"warn"` | Beacon log level. Valid values are: trace, debug, info, warn, error |
| beacon.natsStream | string | `nil` | NATS stream name. Must be set. Example: mainnet-vaas |
| beacon.natsUrl | string | `nil` | NATS server URL. Must be set. Example: 1.2.3.4:4222 |
| beacon.wormholeBootstrapAddrs | string | `"/dns4/wormhole-v2-mainnet-bootstrap.xlabs.xyz/udp/8999/quic/p2p/12D3KooWNQ9tVrcb64tw6bNs2CaNrUGPM7yRrKvBBheQ5yCyPHKC,/dns4/wormhole.mcf.rocks/udp/8999/quic/p2p/12D3KooWDZVv7BhZ8yFLkarNdaSWaB43D6UbQwExJ8nnGAEmfHcU,/dns4/wormhole-v2-mainnet-bootstrap.staking.fund/udp/8999/quic/p2p/12D3KooWG8obDX9DNi1KUwZNu9xkGwfKqTp2GFwuuHpWZ3nQruS1"` | Wormhole bootstrap addresses |
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
| probes.liveness.enabled | bool | `true` |  |
| probes.startup.enabled | bool | `true` |  |
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
Autogenerated from chart metadata using [helm-docs v1.13.1](https://github.com/norwoodj/helm-docs/releases/v1.13.1)
