#Crossplane custom Configuration for bootstrapping clusters

The custom configuration install various xrds that can be used to bootstrap clusters in an opinioated fashion.

# Install 

## Crossplane
    - Ensure crossplaine is installed please follow instcutions at (crossplane)[https://crossplane.github.io/docs/v1.0/getting-started/install-configure.html]#
    - Ensure the crossplane helm provider is isntalled   (crossplane-helm)[https://github.com/crossplane-contrib/provider-helm]

## Install configuration
   Applying the following configuraion will install the configuration into your cluster

```
    apiVersion: pkg.crossplane.io/v1
    kind: Configuration
    metadata:
      name: platfrom-bootstrap
    spec:
      package: kanzifucius/platfrom-bootstrap:master
      packagePullPolicy: Always
      revisionActivationPolicy: Automatic
      revisionHistoryLimit: 1
  ```

# Usage
  See manifests in bootstrap-examples [bootstrap-examples]


  