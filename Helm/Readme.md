# HELM CHARTS
 - Helm Overview
	1. Package manager for Kubernetes applications
	2. Simplifies deployment, scaling, and management of applications on Kubernetes
	3. Consists of Charts, Templates, and Releases
	
 - Helm Architecture:
<br>Client-Server Model:
	<br>Helm CLI interacts with Tiller (deprecated) or Helm 3 uses direct Kubernetes API calls

 - Helm Concepts:
   - Charts:
	 - Package of pre-configured Kubernetes resources
	 - Consists of templates, values, and metadata
	 - Organized into a directory structure
 - Templates:
	 -  Define Kubernetes resources using Go templating language
	 - Allow dynamic configuration through values.yaml
 - Values:
	- Customizable parameters for charts
	- Stored in values.yaml file
 - Release:
	- Deployed instance of a chart
  - Can be upgraded, rolled back, or deleted

## Public Repo of Helm Chart - [ArtifactHub](https://artifacthub.io/)

## LIST OF COMMANDS

1. Installing a Chart:
`helm install <RELEASE_NAME> <CHART_NAME> `

2. Upgrading a Release:
`helm upgrade <RELEASE_NAME> <CHART_NAME>` 

3. Rolling Back a Release:
	`helm rollback <RELEASE_NAME> <REVISION_NUMBER>`

4. Uninstalling a Release:
`helm uninstall <RELEASE_NAME>`

5. List Helm releases:
   `helm list`
6. Inspect a release
   `helm status <RELEASE_NAME>`

7. Show Helm Release History:
`helm history <RELEASE_NAME>`

8. Lint a Helm Chart:
`helm lint <CHART_PATH>`

9. Dry Run a Helm Release:
`helm install --dry-run --debug <RELEASE_NAME> <CHART_NAME>`

10. View Helm Values for a Release:
`helm get values <RELEASE_NAME>`
