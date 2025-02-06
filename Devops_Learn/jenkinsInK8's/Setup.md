# Option1: Using deploy & service manifest
Jenkins install using the deployment and service manifest - https://www.jenkins.io/doc/book/installing/kubernetes/
https://github.com/jenkinsci/helm-charts/blob/main/charts/jenkins/README.md

Create a Namespace
Create a service account with Kubernetes admin permissions.
Create local persistent volume for persistent Jenkins data on Pod restarts.
Create a deployment YAML and deploy it.
Create a service YAML and deploy it.


# Option2: install using helm chart
$ curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
$ chmod 700 get_helm.sh
$ ./get_helm.sh

helm repo add jenkinsci https://charts.jenkins.io
helm repo update

# The helm charts in the Jenkins repo can be listed with the command:
helm search repo jenkinsci

## Jenkins Kubernetes Manifest Files
All the Jenkins Kubernetes manifest files used here are hosted on GitHub. Please clone the repository if you have trouble copying the manifest from the document.

git clone https://github.com/scriptcamp/kubernetes-jenkins

