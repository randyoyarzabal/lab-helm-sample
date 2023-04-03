# Example Helm Chart 

This Helm chart deploys an nginx LB demo based on the "docker.io/nginxdemos/hello" image.  By default, it deploys the `plain-text` version, but can be overriden to the GUI version by defining `latest` in `Values.image.tag`.

Tha app shows the node it is running on each time you refresh so it is best to deploy `n` replicas for `n` worker nodes.

Default values are defined in the `values.yaml`

*Be sure to define the proper `Values.route.host` for your setup.*

## Usage Example

### Installation
`helm install nginx-lb helm-lb-txt --create-namespace --namespace helm-nginx-demo`

### Upgrade/Changes
`helm upgrade nginx-lb helm-lb-txt`

### Un-installation
`helm uninstall nginx-lb`
