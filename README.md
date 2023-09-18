# capi-diagrams

This repository contains the draw.io files that I personally created to understand the detailed implementation of [cluster-api](https://github.com/kubernetes-sigs/cluster-api/tree/main).

You are welcome to freely reference the diagrams managed in this repository, keeping in mind the following:

* The updates to this repository are primarily intended to enhance my personal understanding. It's not guaranteed to cover every aspect of the internal implementation.
* This repository does not assure conformance with the latest code.
* There's a possibility that diagrams within this repository might contain inaccuracies. I disclaim any liability arising from its use.


It is recommended to consult the actual source code for a more accurate understanding.  
If you notice any errors, I would greatly appreciate comments or pull requests."


### Version

Now, I am targetting the version of cluster-api is v1.5.1 and cluster-api openstack provider is v0.7.3.

### Change Log

* 2023/09/18 Create repository and add first contents.  
  - Sequence diagram ('sequence-diagram' sheet) between [cluster-api](https://github.com/kubernetes-sigs/cluster-api/tree/v1.5.1) and [cluster-api openstack provider](https://github.com/kubernetes-sigs/cluster-api-provider-openstack/tree/v0.7.3) when creating workload k8s cluster.
    - KubeadmControlPlane creation sequence (NOW EDTTING)
  - Relationship between each controller and CR.
    - 'capo-controllers' sheet contains following Controller/CR relationship and deployed as 'capo-controller-manager' pod.
      - Controller/Reconciler
        - OpenStackClusterReconciler
        - OpenStackMachineReconciler
      - CustomResource
        - cluster-api-provider-openstack/api/v1alpha6
          - OpenStackCluster
          - OpenStackMachine
        - cluster-api/api/v1beta1
          - Cluster
          - Machine
    - 'capi-control-plane-controllers' sheet contains following Controller/CR relationship and deployed as 'capi-kubeadm-control-plane-controller-manager' pod.
      - Controller/Reconciler
        - KubeadmControlPlaneReconciler
      - CustromResource
        - cluster-api/controlplane/kubeadm/api/v1beta1
          - KubeadmControlPlane
        - cluster-api/api/v1beta1
          - Cluster
          - Machine
    - 'capi-controllers' sheet contains following Controller/CR relationship and deployed as 'capi-controller-manager' pod.
      - Controller/Reconciler
        - ClusterReconciler
        - MachineReconciler
      - CustromResource
        - cluster-api/api/v1beta1
          - Cluster
          - Machine
    - 'capi-kubeadm-bootstrap-controllers'p sheet contains following Controller/CR relationship and deployed as 'capi-kubeadm-bootstrap-controller-manager' pod.
      - Controller/Reconciler
        - KubeadmConfigReconciler
      - CustromResource
        - cluster-api/bootstrap/kubeadm/api/v1beta1
          - KubeadmConfig
        - cluster-api/api/v1beta1
          - Cluster
          - Machine

