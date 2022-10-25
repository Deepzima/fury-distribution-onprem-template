ca.%:
	kubeadm init phase certs ca --cert-dir ${PWD}

sa.%:
	kubeadm init phase certs sa --cert-dir ${PWD}

etcd/etcd-ca.%:
	mkdir -p etcd
	kubeadm init phase certs etcd-ca --cert-dir ${PWD}

front-proxy-ca.%:
	kubeadm init phase certs front-proxy-ca --cert-dir ${PWD}