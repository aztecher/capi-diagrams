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

* 2023/11/21 Update KCP creation diagram and add CR-Controller relationship diagram.  
  - About KCP creation diagram
    - Fix mistakes
    - Add sequence after setup KCP resource (after 「kubeadm init」in workload cluster)
  - About CR-Controller relationship diagram
    - Showing which controller is responsible for 'For', 'Owns' and 'Watches' for each Custom Resource.
* 2023/10/09 Complete to write '(first) kcp creation' and 'worker creation' sequences.  
  - 'Complete' means that I was able to write down enough information to fully understand what I wanted to know, not all of the process.
  - If you want to quick review, please refere to the [png](./png) directory.  
  - If you want to see the figures in a different (non-png) format, or to change the contents in your own way, you are free clone this repository and modify it as you wish.
    - Hopefully, we will be happy to send your changes to this repository as a PR and enhance the content of this repository.
* 2023/09/18 Create repository and add first contents.  
  - Sequence diagram ('sequence-diagram' sheet) between [cluster-api](https://github.com/kubernetes-sigs/cluster-api/tree/v1.5.1) and [cluster-api openstack provider](https://github.com/kubernetes-sigs/cluster-api-provider-openstack/tree/v0.7.3) when creating workload k8s cluster.
    - KubeadmControlPlane creation sequence (NOW EDTTING)
  - Relationship between each controller and CR.
