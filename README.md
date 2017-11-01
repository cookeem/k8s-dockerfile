Running kubeadm without an internet connection

All of the control plane components run in Pods started by the kubelet and the following images are required for the cluster works will be automatically pulled by the kubelet if they don’t exist locally while kubeadm init is initializing your master:
```
Image Name	v1.7 release branch version	v1.8 release branch version
gcr.io/google_containers/kube-apiserver-${ARCH}	v1.7.x	v1.8.x
gcr.io/google_containers/kube-controller-manager-${ARCH}	v1.7.x	v1.8.x
gcr.io/google_containers/kube-scheduler-${ARCH}	v1.7.x	v1.8.x
gcr.io/google_containers/kube-proxy-${ARCH}	v1.7.x	v1.8.x
gcr.io/google_containers/etcd-${ARCH}	3.0.17	3.0.17
gcr.io/google_containers/pause-${ARCH}	3.0	3.0
gcr.io/google_containers/k8s-dns-sidecar-${ARCH}	1.14.4	1.14.4
gcr.io/google_containers/k8s-dns-kube-dns-${ARCH}	1.14.4	1.14.4
gcr.io/google_containers/k8s-dns-dnsmasq-nanny-${ARCH}	1.14.4	1.14.4
```
