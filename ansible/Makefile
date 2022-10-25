.PHONY: cluster
cluster:
	ansible-playbook cluster.yml

.PHONY: test
test:
	ansible all -m ping

prepare:
	ansible-playbook prepare.yml 

prepare-container:
	ansible-playbook cluster.yml --tags "container-node-common"

prepare-nodes:
	ansible-playbook cluster.yml --tags "kube-node-common"

pki-gen:
	ansible-playbook cluster.yml --tags "pki-generate"

pki-config:
	ansible-playbook cluster.yml --tags "pki-config"
	
vmware-config:
	ansible-playbook cluster.yml --tags "vmware-cloud-config"

etcd:
	ansible-playbook cluster.yml --tags "etcd"

kubernetes:
	ansible-playbook cluster.yml --tags "kube-control-plane,kube-worker"