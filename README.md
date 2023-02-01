# OpenShift / CP4BA / CP4I Upgrade Documentation

## Index

0. [Overview](#overview)
1. [Compatibility Matrix](#compatibility-matrix)
   - [CP4BA](#cp4ba)
   - [CP4I](#cp4i)
2. [Upgrade Proposal](#upgrade-proposal)
3. [Upgrade Execution](#upgrade-execution)
4. [Upgrade Phases](#upgrade-phases)

## Overview

| Component | Current Version | Proposed Target Version | Long Term Support Release |
| --------- | --------------- | ----------------------- | ------------------------- |
| OpenShift | 4.6.60          | 4.10                    | 4.10                      |
| CP4BA     | 20.0.3          | 22.0.1 IF002            | 21.0.3 IF014              |
| CP4I      | 2020.4.1        | 2022.2.1                | 2022.2                    |

## Compatibility Matrix

The following are the compatibility charts for the Cloud Paks.

### CP4BA

The CP4BA CASE package name is `ibm-cp-automation`

| OpenShift     | CP4BA        | IAF    | CPFS   |
| ------------- | ------------ | ------ | ------ |
| 4.6, 4.7, 4.8 | 20.0.3       |        | 3.5    |
| 4.6, 4.7, 4.8 | 20.0.3.2     |        | 3.6.5  |
| 4.6, 4.8      | 21.0.1       |        | 3.5    |
| 4.6, 4.7, 4.8 | 21.0.2       | 1.0    | 3.5    |
| 4.6, 4.7, 4.8 | 21.0.2 IF012 | 1.3.7  | 3.19   |
| 4.6, 4.8, 4.9 | 21.0.3       | 1.0    | 3.13   |
| 4.6, 4.8, 4.9 | 21.0.3 IF014 | 1.3.11 | 3.19.5 |
| 4.8, 4.10     | 22.0.1       | 1.3.7  | 3.19   |

### CP4I

The CP4I CASE package name is `ibm-cp-integration`

| OpenShift           | CP4I       | IAF           | CPFS         | CASE  |
| ------------------- | ---------- | ------------- | ------------ | ----- |
| 4.6.8               | 2020.4.1-0 |               | 3.6.X        | 2.1.0 |
|                     | 2020.4.1-1 |               |              | 2.1.1 |
|                     | 2020.4.1-1 |               |              | 2.1.2 |
|                     | 2020.4.1-2 |               |              | 2.1.3 |
|                     | 2020.4.1   |               |              | 2.1.4 |
|                     | 2020.4.1   |               |              | 2.1.5 |
|                     | 2020.4.1   |               |              | 2.1.6 |
|                     | 2020.4.1   |               |              | 2.1.7 |
| 4.6.8+, 4.7.x       | 2021.1.1-0 |               | 3.7.2+       | 2.2.0 |
| 4.6.8+, 4.7.x       | 2021.1.1-0 |               | 3.7.2+       | 2.2.1 |
| 4.6.8+, 4.7.x       | 2021.1.1-0 |               | 3.7.2+       | 2.2.2 |
| 4.6.8+, 4.7.x       | 2021.2.1   | 1.0.X, 1.1.X  | 3.7.2+       | 2.3.0 |
| 4.6.8+, 4.7.x, 4.8+ | 2021.3.1   | 1.1.x, 1.2.X  | 3.8.0+       | 2.4.0 |
| 4.6, 4.7, 4.8, 4.10 | 2021.4.1   | 1.1, 1.2, 1.3 | 3.8.0 - 3.19 | 2.5.0 |
|                     | 2021.4.1-1 |               |              | 3.0.0 |
|                     | 2021.4.1-2 |               |              | 3.0.1 |
| 4.10.x              | 2022.2.1   |               | 3.19.x       | 4.0.0 |

## Upgrade Proposal

### The proposed upgrade process would be the following:

> #### 1. Upgrade both Cloud Paks
>
> - CP4BA 20.0.X to 21.0.1 to 21.0.2 to 21.0.3 IF7 or later
> - CP4I 2020.4.1 to to 2021.4
>
> #### 2. Upgrade OpenShift
>
> - 4.6 to 4.7 to 4.8
>
> #### 3. Upgrade the CP4BA
>
> - CP4BA to 22.0.1
>
> #### 4. Upgrade OpenShift
>
> - 4.8 to 4.9 to 4.10
>
> #### 5. Upgrade the CP4I
>
> - CP4I to 2022.2

## Upgrade Execution

### The upgrade process was executed as follows:

> #### 1. Upgrade both Cloud Paks
>
> - CP4BA 20.0.X to 21.0.1 to 21.0.2 to 21.0.3 IF014 (LTS)
> - CP4I 2020.4.1 to to 2021.4
>
> #### 2. Upgrade OpenShift 4.6 to 4.10
>
> - OpenShift 4.6 to 4.7 to 4.8 to 4.9 to 4.10
>
> #### 3. Upgrade CP4I (LTS)
>
> - CP4I to 2022.2
>
> #### 4. Upgrade CP4BA
>
> - CP4BA to 22.0.1
>
> #### 5. Upgrade Openshift
>
> - OpenShift 4.10 to 4.11 to 4.12

## Upgrade Phases

### Phase 0: Install Existing Environment

- [Step 1: Install OpenShift 4.6.60 (Work in progress)](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-0.md#openshift-4660)
- [Step 2: Install CP4BA 20.0.3](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-0.md#cp4ba-2003)
- [Step 3: Install CP4I 2020.4.1](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-0.md#cp4i-202041)

### Phase 1: Upgrading CP4BA and CP4I

- [Step 1: Upgrade CPFS to 3.7.x](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-1.md#upgrade-cloud-pak-foundational-services-to-37x)
- [Step 2: Upgrade CP4BA to 21.0.1](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-1.md#cp4ba-2003-to-2101)
- [Step 3: Upgrade CP4BA to 21.0.2](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-1.md#cp4ba-2101-to-2102)
- [Step 4: Upgrade CPFS to 3.19.x](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-1.md#upgrade-cloud-pak-foundational-services-to-319x-lts)
- [Step 5: Upgrade CP4BA to 21.0.3 iFix 14](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-1.md#cp4ba-2102-to-2103)
- [Step 6: Upgrade CP4I to 2021.4 (Optional)](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-1.md#cp4i-202041-to-20214-optional)

### Phase 2: Upgrading OpenShift (4.6-4.10)

- [Step 1: Upgrade OpenShift to 4.7](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-2.md#upgrade-openshift-46-to-47)
- [Step 2: Upgrade OpenShift to 4.8](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-2.md#upgrade-openshift-47-to-48)
- [Step 3: Upgrade OpenShift to 4.9](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-2.md#upgrade-openshift-48-to-49)
- [Step 4: Upgrade OpenShift to 4.10](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-2.md#upgrade-openshift-49-to-410)

### Phase 3: Upgrading CP4I (2022.2)

- [Step 1: Upgrade CP4I to 2022.2](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-3.md#upgrade-cp4i-to-20222)

### Phase 4: Upgrading CP4BA (22.0.1)

- [Step 1: Upgrade CP4BA to 22.0.1](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-4.md#upgrade-cp4ba-to-2201)

### Phase 5: Upgrading OpenShift (4.10-4.12)

- [Step 1: Upgrade OpenShift to 4.11](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-5.md#upgrade-openshift-410-to-411)
- [Step 2: Upgrade OpenShift to 4.12](https://github.com/gabrielhicksibm/upgrade-documentation/blob/main/phases/phase-5.md#upgrade-openshift-411-to-412)
