# BASH Scripts for WCP interactions
---
* `enable-wcp.sh` - Enable WCP on a AVI/NSX based setup

1. Modify the bash script `enable-wcp.sh` by editing the following entries per your env. - 
```
DEPLOYMENT_TYPE='NSX'

VCENTER_VERSION=8
VCENTER_HOSTNAME=192.168.100.50
VCENTER_USERNAME=administrator@vsphere.local
VCENTER_PASSWORD='VMware1!'
K8S_SUP_CLUSTER=Cluster
K8S_CONTENT_LIBRARY=utkg
K8S_STORAGE_POLICY=tanzu
K8S_MGMT_PORTGROUP='DVPG-Management-network'
K8S_WKD0_PORTGROUP='Workload0-VDS-PG'
K8S_WKD1_PORTGROUP='Workload1-VDS-PG'

export DNS_SERVER='192.168.100.1'
export NTP_SERVER='129.6.15.28'
export DNS_SEARCHDOMAIN='env1.lab.test'

export MGMT_STARTING_IP='192.168.100.60'
export MGMT_GATEWAY_IP='192.168.100.1'
export MGMT_SUBNETMASK='255.255.254.0'

#### AVI specific details
export AVI_CLOUD='domain-c9'
export AVI_HOSTNAME=192.168.100.58
export AVI_USERNAME=admin
export AVI_PASSWORD='VMware1!'

#### NSX specifc details
export NSX_MANAGER=192.168.100.59
export NSX_USERNAME='admin'
export NSX_PASSWORD='VMware1!VMware1!'
export NSX_EDGE_CLUSTER='sup-edge-cluster'
export NSX_T0_GATEWAY='sup-t0-gw'
export NSX_DVS_PORTGROUP='Pacific-VDS'
export NSX_INGRESS_CIDR='172.16.0.0/28'
export NSX_EGRESS_CIDR='172.16.0.16/28'
export NSX_NAMESPACE_NETWORK='10.244.0.0/20'
```

2. Execute `enable-wcp.sh`
---
