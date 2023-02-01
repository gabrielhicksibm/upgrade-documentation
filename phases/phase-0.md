# Phase 0

- [**Phase 0: Install Existing Environment**](https://github.ibm.com/Gabriel-Hicks/upgradeDocs/blob/main/phases/phase-0.md)
  - [Step 1: Install OpenShift 4.6.60 (Work in progress)](#openshift-4660)
  - [Step 2: Install CP4BA 20.0.3](#cp4ba-2003)
  - [Step 3: Install CP4I 2020.4.1](#cp4i-202041)
- [Phase 1: Upgrading CP4BA and CP4I](https://github.ibm.com/Gabriel-Hicks/upgradeDocs/blob/main/phases/phase-1.md)
- [Phase 2: Upgrading OpenShift (4.6-4.10)](https://github.ibm.com/Gabriel-Hicks/upgradeDocs/blob/main/phases/phase-2.md)
- [Phase 3: Upgrading CP4I (2022.2)](https://github.ibm.com/Gabriel-Hicks/upgradeDocs/blob/main/phases/phase-3.md)
- [Phase 4: Upgrading CP4BA (22.0.1)](https://github.ibm.com/Gabriel-Hicks/upgradeDocs/blob/main/phases/phase-4.md)
- [Phase 5: Upgrading OpenShift (4.10-4.12)](https://github.ibm.com/Gabriel-Hicks/upgradeDocs/blob/main/phases/phase-5.md)

## Install Existing Environment

| Component | Current Version |
| --------- | --------------- |
| OpenShift | 4.6.60          |
| CP4BA     | 20.0.3          |
| CP4I      | 2020.4.1        |

## OpenShift 4.6.60

- To do.

## CP4BA 20.0.3

- [Source for CASE Package](https://github.com/icp4a/cert-kubernetes/tree/20.0.3.2)
- [Step 1 CP4A + ODM Enterprise Prerequisites](https://community.ibm.com/community/user/automation/blogs/lawrence-louie1/2021/02/09/part-1-set-up-your-ocp-cluster-for-odm-cp4a-enterp)
- [Step 2 CP4A + ODM Enterprise Prerequisites](https://community.ibm.com/community/user/automation/blogs/lawrence-louie1/2021/02/09/part-2-check-the-cluster-is-ready-and-create-a-cr)
- [Step 3 CP4A + ODM Enterprise Prerequisites](https://community.ibm.com/community/user/automation/blogs/lawrence-louie1/2021/02/09/part-3-setup-your-operational-decision-manager-dep)

## CP4I 2020.4.1

- [Operator Documentation](https://www.ibm.com/docs/en/cloud-paks/cp-integration/2020.4?topic=installing-adding-online-catalog-sources-cluster)
- Note: To mirror the existing environment, Cloud Pak Foundational Services should not be upgraded greater than v3.6.5. For more information see the bottom of the operator documentation above.
