# Phase 1 - Upgrading CP4BA and CP4I

- [Phase 0: Install Existing Environment](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-0.md)
- [**Phase 1: Upgrading CP4BA and CP4I**](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-1.md)
  - [Step 1: Upgrade CPFS to 3.7.x](#upgrade-cloud-pak-foundational-services-to-37x)
  - [Step 2: Upgrade CP4BA to 21.0.1](#cp4ba-2003-to-2101)
  - [Step 3: Upgrade CP4BA to 21.0.2](#cp4ba-2101-to-2102)
  - [Step 4: Upgrade CPFS to 3.19.x](#upgrade-cloud-pak-foundational-services-to-319x-lts)
  - [Step 5: Upgrade CP4BA to 21.0.3 iFix 14](#cp4ba-2102-to-2103)
  - [Step 6: Upgrade CP4I to 2021.4 (Optional)](#cp4i-202041-to-20214-optional)
- [Phase 2: Upgrading OpenShift (4.6-4.10)](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-2.md)
- [Phase 3: Upgrading CP4I (2022.2)](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-3.md)
- [Phase 4: Upgrading CP4BA (22.0.1)](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-4.md)
- [Phase 5: Upgrading OpenShift (4.10-4.12)](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-5.md)

## Upgrade Cloud Pak Foundational Services to 3.7.x

- [Documentation for CPFS 3.7.x](https://www.ibm.com/docs/en/cloud-paks/1.0?topic=online-upgrading-foundational-services-from-operator-release#upgrade-36x-37)
- [Updating the installer catalog source image tag](https://www.ibm.com/docs/en/cloud-paks/1.0?topic=online-upgrading-foundational-services-from-operator-release#image_tag)
  - Images for specifying catalog source:
    - [icr.io/ibmcom/ibm-common-service-catalog:3.7](icr.io/ibmcom/ibm-common-service-catalog:3.7)
    - [cr.icr.io/ibmcom/ibm-common-service-catalog:3.7](cr.icr.io/ibmcom/ibm-common-service-catalog:3.7)
- [Upgrading from a Helm release](https://www.ibm.com/docs/en/cloud-paks/1.0?topic=online-upgrading-foundational-services-from-helm-release)

### Uninstall Common Services Metering

- [Documentation for Uninstalling](https://www.ibm.com/docs/en/cloud-paks/1.0?topic=online-uninstalling-metering-service)

## CP4BA 20.0.3 to 21.0.1

- [Repo for CASE Package 21.0.1](https://github.com/icp4a/cert-kubernetes/tree/21.0.1)
- [Source to Download CASE Package](https://github.com/IBM/cloud-pak/raw/master/repo/case/ibm-cp-automation-3.0.1.tgz)
- [Upgrading Dependencies](https://www.ibm.com/docs/en/cloud-paks/cp-biz-automation/21.0.x?topic=containers-upgrading-dependencies)
  - This is also covered in the previous step "Upgrade Cloud Pak Foundational Services to 3.7.x"
- [Upgrading Operator](https://www.ibm.com/docs/en/cloud-paks/cp-biz-automation/21.0.x?topic=containers-upgrading-operator)
- [Upgrading ODM](https://www.ibm.com/docs/en/cloud-paks/cp-biz-automation/21.0.x?topic=upgrade-upgrading-operational-decision-manager)
- [Applying Updated Custom Resource](https://www.ibm.com/docs/en/cloud-paks/cp-biz-automation/21.0.x?topic=containers-applying-upgraded-custom-resource)
- [Post-Update Tasks](https://www.ibm.com/docs/en/cloud-paks/cp-biz-automation/21.0.x?topic=containers-completing-post-upgrade-tasks)
- [Migrating data from ODM](https://www.ibm.com/docs/en/cloud-paks/cp-biz-automation/21.0.x?topic=data-migrating-from-operational-decision-manager)

<!-- ### TODO -->

## CP4BA 21.0.1 to 21.0.2

- [Documentation for Upgrade to 21.0.2](https://www.ibm.com/docs/en/cloud-paks/cp-biz-automation/21.0.x?topic=operator-upgrading-in-hub)
- [Updating Custom Resource](https://www.ibm.com/docs/en/cloud-paks/cp-biz-automation/21.0.x?topic=upgrade-checking-version-deployment-type-license)
- [Upgrading ODM](https://www.ibm.com/docs/en/cloud-paks/cp-biz-automation/21.0.x?topic=upgrade-upgrading-operational-decision-manager)
- [Applying Updated Custom Resource](https://www.ibm.com/docs/en/cloud-paks/cp-biz-automation/21.0.x?topic=containers-applying-upgraded-custom-resource)
- [Post-Update Tasks](https://www.ibm.com/docs/en/cloud-paks/cp-biz-automation/21.0.x?topic=containers-completing-post-upgrade-tasks)
- [Migrating data from ODM](https://www.ibm.com/docs/en/cloud-paks/cp-biz-automation/21.0.x?topic=data-migrating-from-operational-decision-manager)

<!-- ### TODO -->

## Upgrade Cloud Pak Foundational Services to 3.19.x (LTS)

- Note: When upgrading Cloud Pak foundational services from 3.6 to 3.19, if you have the IBM API Connect operator installed, you must change the subscription of the IBM API Connect operator to the v2.1.7-eus channel at the same time, otherwise the upgrade will not start. The 2.1.11 version of the API Connect operator (which is associated with the v2.1.7-eus channel), is the only version that is compatible with Cloud Pak foundational services 3.19.
- [Documentation for APIC Operator Upgrade](https://www.ibm.com/docs/en/cloud-paks/cp-integration/2022.2?topic=upgrading-from-20204)
- [Source for CPFS 3.19.x](https://www.ibm.com/docs/en/cloud-paks/1.0?topic=online-upgrading-foundational-services-from-operator-release#upgrade-38x)

<!-- ### TODO -->

## CP4BA 21.0.2 to 21.0.3

- [Documentation for CP4BA 21.0.3](https://www.ibm.com/docs/en/cloud-paks/cp-biz-automation/21.0.3?topic=containers-upgrading-non-air-gapped-environment-from-2102)
- [Documentation for 21.0.3 iFix014](https://www.ibm.com/support/pages/node/6827587)
- [Source for CASE Package](https://github.com/IBM/cloud-pak/raw/master/repo/case/ibm-cp-automation/3.2.14/ibm-cp-automation-3.2.14.tgz)

<!-- ### TODO -->

## CP4I 2020.4.1 to 2021.4 (Optional)

- [Upgrade documentation for 2021.4](https://www.ibm.com/docs/en/cloud-paks/cp-integration/2021.4?topic=upgrading)
- Note: This is labeled as Optional because the latest iFix of 2020.4.1 is already compatible with OpenShift 4.10. We did take this step in our upgrade procedure.

<!-- ### TODO -->
