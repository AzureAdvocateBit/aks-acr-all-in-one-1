# Azure Kubernetes Service and Azure Container Service Creation Script

This is a simple bash script that allows you to provide a few variables to create both an [Azure Kuberntes Service Cluster](https://docs.microsoft.com/azure/aks/?WT.mc_id=code-github-jagord) and an [Azure Container Registry](https://docs.microsoft.com/azure/container-registry/?WT.mc_id=code-github-jagord) in a few minutes.

## Installation and Use

_REQUIRED_

Install [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest&WT.mc_id=code-github-jagord)

or

Use [Azure Cloud Shell](https://docs.microsoft.com/azure/cloud-shell/overview?WT.mc_id=code-github-jagord) to execute the bash script.

# Installation

Just clone this repo, open with your favorite editor and provide the following variables:

```
export GROUPNAME = " "
export LOCATION = " "
export AKSNAME = " "
export ACRNAME = " " # must be globally unique
export k8sversion = " "
```
The `k8sversion` variable can be determined based on your location and the current versions available.  Check the docs on ["Supported Kubernetes versions in Azure Kubernetes Service"](https://docs.microsoft.com/azure/aks/supported-kubernetes-versions?WT.mc_id=code-github-jagord)

Additionally, you can run the following from `az cli` :

```
az aks get-versions --location $LOCATION --output table
```

Once done, save the file and execute the bash script:

```
bash aks-acr.sh
```
