# HELM CHARTS
![image](https://github.com/imprateeksh/knowledge-center/assets/78964991/6d4ae1ed-13da-485c-b265-a89003f4151e)

 - Helm history
   - Originally created by DeisLabs and donated to CNCF
   - Goal is to help manage k8s manifests in an easier fashion
   - Helm supports Kubernetes natively
   - Release history/versioning (like version control in GitHub)
   - Started in 2016 (Helm2) and Helm3 was released in 2019

 - Helm Overview
	1. Package manager for Kubernetes applications
	2. Simplifies deployment, scaling, and management of applications on Kubernetes
	3. Consists of Charts, Templates, and Releases
        4. Manages multiple applications in one place
        5. Without using Helm, managing and organizing the configuration can become challenging and result in a large and disorganized set of configuration files.
        6. Helm provides a more organized and streamlined approach to application deployment and configuration management
	
 - Helm Architecture:
<br>Client-Server Model:
	<br>Helm CLI interacts with Tiller (deprecated) or Helm 3 uses direct Kubernetes API calls
## Helm2 Vs Helm3
 - Mainly removal of Tiller
   ![image](https://github.com/imprateeksh/knowledge-center/assets/78964991/30386b4f-2ef8-4888-af56-d2fc58493cac)


## Helm Chart Architecture:
![image](https://github.com/imprateeksh/knowledge-center/assets/78964991/1c854bda-7c60-4d29-bd9b-42c571c2e7e4)

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

## Chart Lifecycle and Management
![image](https://github.com/imprateeksh/knowledge-center/assets/78964991/6c859115-9229-4dd2-9a61-fe9a4dd85a0f)


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

## Best Practices
### Value Files
 - Lower case names are preferred
 - Words should be in camelCase.
 - Split values into separate files for different environments (e.g., values-prod.yaml, values-dev.yaml).
### General Conventions
 - Proper Chart Names: Use lowercase letters and dashes for chart names (e.g., my-app)
 - Use of Hyphens
 - Dots(.) play an important role
 - Use the functions whenever required.
 - Follow standard helm directory structure
 - Use Semantic Versioning (SemVer) for chart versioning.
 - Documentation- Include a well documented Readme.md with details on usage, values and dependencies.
 - Leverage Helm templates to generate Kubernetes manifests.
 - Keep templates simple; avoid complex logic. Use helper functions for clarity.
 - Use conditionals for optional dependencies based on user choices
 - Include RBAC resources in your chart for proper security.
 - Use helm lint to catch common issues in your chart.
 - Host your charts in a repository for easy distribution.
 - Implement tests using helm test to validate the functionality of your chart.
