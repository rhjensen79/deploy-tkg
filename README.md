# Example of how to create and delete TKG clusters, using Github Actions and Tailscale

This is a quick example on how one could create, manage and delete TKG clusters, using Github Actions with Tailscale.
Use a own risk.

## Add Cluster

To create, add "TanzuKubernetesCluster" yaml files in the apply folder and commit.

## Change Cluster

To change a cluster config, simply change to "TanzuKubernetesCluster" files in the apply folder and commit.

## Delete cluster

To delete a cluster, move the "TanzuKubernetesCluster" yaml file to the delete folder and commit.

## Pre req

This setup assumes, that you have a Tailscale network, with access to a vsphere cluster, already setup with TKG, ready to deploy new clusters.

The following secrets need to be set in Github, for the Github Actions to know, who and how to connect, to the enviroment :

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

Note the kubectl and kubectl-vsphere files, in the root, is taken from my enviroment. You might need to replace them with a combatible version, from your own environment.
