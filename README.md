# Example of how to create and delete TKG clusters, using Github Actions

This is a quick example on how one could create, manage and delete TKG clusters, using Github Actions.
Use a own risk.

## Add Cluster

To create, add "TanzuKubernetesCluster" yaml files in the apply folder and commit.

## Change Cluster

To change a cluster config, simply change to "TanzuKubernetesCluster" files in the apply folder and commit.

## Delete cluster

To delete a cluster, move the "TanzuKubernetesCluster" yaml file to the delete folder and commit.

## Pre req

For this to work, you need to set the following Github secrets :

- TAILSCALE_AUTHKEY
The authkey, used to connect to the Tailscale network
- KUBECTL_VSPHERE_USER
The user with permissions to create and delete clusters
- KUBECTL_VSPHERE_PASSWORD
The password of the above user
- KUBECTL_CONTEXT
The context of where this users has it's rights, and where the TKG clusters, will be created.
- IPADRESS
The management ipadress for the superwizor cluster
