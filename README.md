# IBM Helm API Operator

> **Important:** Do not install this operator directly. Only install this operator using the IBM Common Services Operator. For more information about installing this operator and other Common Services operators, see [Installer documentation](http://ibm.biz/cpcs_opinstall). If you are using this operator as part of an IBM Cloud Pak, see the documentation for that IBM Cloud Pak to learn more about how to install and use the operator service. For more information about IBM Cloud Paks, see [IBM Cloud Paks that use Common Services](http://ibm.biz/cpcs_cloudpaks).

Operator used to manager IBM Helm API service. Helm API provides REST endpoints for accessing Helm charts, releases, and repos.

## Supported platforms

### Platforms

- Red Hat OpenShift Container Platform 4.3 and above

### Operating Systems

- Red Hat Enterprise Linux CoreOS

## Operator versions

- 3.6.0

## Prerequisites

1. Red Hat OpenShift Container Plataform 4.x installed
1. Cluster Admin role for installation
1. [IBM Cert Manager Operator](https://github.com/IBM/ibm-cert-manager-operator)
1. [IBM MongoDB Operator](https://github.com/IBM/ibm-mongodb-operator)
1. [IBM IAM Operator](https://github.com/IBM/ibm-iam-operator)
1. [IBM Management Ingress Operator](https://github.com/IBM/ibm-management-ingress-operator)
1. [IBM Platform API Operator](https://github.com/IBM/ibm-platform-api-operator)

## Documentation

For installation and configuration, see [IBM Knowledge Center link].

### Developer guide

Information about building and testing the operator.

#### Cloning the operator repository
```
# git clone git@github.com:IBM/ibm-helm-api-operator.git
# cd ibm-helm-api-operator
```

#### Building the operator image
```
# make build
```

#### Installing the operator 
```
# make install
```

#### Uninstalling the operator
```
# make uninstall
```

#### Debugging the operator

Check the Cluster Service Version (CSV) installation status
```
# oc get csv
# oc describe csv ibm-helm-api-operator.v3.6.0
```

Check the custom resource status
```
# oc describe helmapis helm-api
# oc get helmapis helm-api -o yaml
```

Check the operator status and log
```
# oc describe po -l name=ibm-helm-api-operator
# oc logs -f $(oc get po -l name=ibm-helm-api-operator -o name)
```

#### End-to-End testing using Operand Deployment Lifecycle Manager

See [ODLM guide](https://github.com/IBM/operand-deployment-lifecycle-manager/blob/master/docs/install/common-service-integration.md#end-to-end-test)

# PodSecurityPolicy Requirements

# SecurityContextConstraints Requirements
