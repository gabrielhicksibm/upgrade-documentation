# Phase 2

- [Phase 0: Install Existing Environment](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-0.md)
- [Phase 1: Upgrading CP4BA and CP4I](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-1.md)
- [**Phase 2: Upgrading OpenShift (4.6-4.10)**](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-2.md)
  - [Step 1: Upgrade OpenShift to 4.7](#upgrade-openshift-46-to-47)
  - [Step 2: Upgrade OpenShift to 4.8](#upgrade-openshift-47-to-48)
  - [Step 3: Upgrade OpenShift to 4.9](#upgrade-openshift-48-to-49)
  - [Step 4: Upgrade OpenShift to 4.10](#upgrade-openshift-49-to-410)
- [Phase 3: Upgrading CP4I (2022.2)](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-3.md)
- [Phase 4: Upgrading CP4BA (22.0.1)](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-4.md)
- [Phase 5: Upgrading OpenShift (4.10-4.12)](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-5.md)

## Upgrade OpenShift 4.6 to 4.7

- [Source for Upgrading 4.6 to 4.7](https://docs.openshift.com/container-platform/4.7/updating/updating-cluster-within-minor.html)

<!-- ### TODO -->

## Upgrade OpenShift 4.7 to 4.8

- [Source for Upgrading 4.7 to 4.8](https://docs.openshift.com/container-platform/4.8/updating/updating-cluster-within-minor.html)

<!-- ### TODO -->

## Upgrade OpenShift 4.8 to 4.9

- [Source for Upgrading 4.8 to 4.9](https://docs.openshift.com/container-platform/4.9/updating/updating-cluster-within-minor.html)

### Extra Step: Manual approval to upgrade

- [Kubernetes API Change Explained](https://access.redhat.com/articles/6955985)
- [4.9 Upgrade Prep](https://access.redhat.com/articles/6329921)
  - To acknowledge the change and proceed with the installation, you will need the following command:
  - `oc -n openshift-config patch cm admin-acks --patch '{"data":{"ack-4.8-kube-1.22-api-removals-in-4.9":"true"}}' --type=merge`

## Upgrade OpenShift 4.9 to 4.10

- [Source for Upgrading 4.9 to 4.10](https://docs.openshift.com/container-platform/4.10/updating/updating-cluster-within-minor.html)

<!-- ### TODO -->
