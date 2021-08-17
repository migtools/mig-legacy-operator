# Crane Legacy Operator
Crane Legacy Operator (mig-legacy-operator) performs an install of basic components for enabling migrations from old versions of OpenShift.

This operator should be used for versions older than 4.6.

For newer versions and documentation see [mig-operator](https://github.com/konveyor/mig-operator)

# Installation
```
oc create -f https://raw.githubusercontent.com/konveyor/mig-legacy-operator/main/deploy/operator.yml
oc create -f https://raw.githubusercontent.com/konveyor/mig-legacy-operator/main/deploy/controller.yml
```
