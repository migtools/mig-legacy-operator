# Crane Legacy Operator
[![Publish Image](https://github.com/konveyor/mig-legacy-operator/actions/workflows/publish.yml/badge.svg)](https://github.com/konveyor/mig-legacy-operator/actions/workflows/publish.yml)
[![Molecule](https://github.com/konveyor/mig-legacy-operator/actions/workflows/molecule.yml/badge.svg)](https://github.com/konveyor/mig-legacy-operator/actions/workflows/molecule.yml)

Crane Legacy Operator (mig-legacy-operator) performs an install of basic components for enabling migrations from old versions of OpenShift.

This operator should be used for versions older than 4.6.

For newer versions and documentation see [Crane Operator](https://github.com/konveyor/mig-operator)

# Installation
OpenShift 3.9 to 4.5:
```
oc create -f https://raw.githubusercontent.com/konveyor/mig-legacy-operator/main/deploy/operator.yml
oc create -f https://raw.githubusercontent.com/konveyor/mig-legacy-operator/main/deploy/controller.yml
```

OpenShift 3.7:
```
oc create -f https://raw.githubusercontent.com/konveyor/mig-legacy-operator/main/deploy/operator-3.7.yml
oc create -f https://raw.githubusercontent.com/konveyor/mig-legacy-operator/main/deploy/controller.yml
```
