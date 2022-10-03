> **GitHub NOTE** 
>  - All changes to wiki documents should be merged to **master** branch. This branch is only recoginzed by *GitHub Wiki* system.
>  - Two origins have to be added to the project:
> ``` git remote add origin https://github.com/sysco-middleware/Wiki_template.git ``` 
> ``` git remote add wiki https://github.com/sysco-middleware/Wiki_template.wiki.git ```
>  - Documentation changes should be pushed to both origins:
> ``` git push origin mastar ``` - master branch used for Pull Request merges
> ``` git push wiki master ``` - master branch used for updatating Wiki pages in GitHub



# Introduction

| Target release           |   1.0                                                                                       |
| :----------------------- |:--------------------------------------------------------------------------------------------|
| **Epic**                 | [issue-1](Link/to/the/issue)                                                                |
| **Document status**      | **APPROVAL PENDING**                                                                        |
| **Document owner**       | [@Ola Nordman](mailto:ola.nordman@cegal.com)                                                |
| **Project Stakeholders** | [@Little Boss](mailto:little.boss@cegal.com),[@Big Boss](mailto:big.boss@cegal.com)         |
| **Project Approver**     | [@Big Boss](mailto:big.boss@cegal.com)                                                      |
| **Project Contributors** | [@Ola Nordman](mailto:ola.nordman@cegal.com), [@Kari Nordman](mailto:kari.nordman@cegal.com)|

TODO: Extended project description with the list of Stakeholders and their contacts. Explain type of user/clients that this project is aimed to.

# Requirements

## Functional requirements

Functional requirements description if it can be helpful for developers, testers or other architects

## Acceptance criteria

Table showing functional acceptance criteria. These are also very useful in the design of tests.

| No.| Description                           | Comment                               |
| :--|:--------------------------------------|:--------------------------------------|
| 1. | First acceptance criteria description | Additional criteria comments          |

## Non-functional requirements

Table with any non-functional requirements. Can be things like performance, security, availability, gdpr, etc.

| No.| Description                            | Comment                               |
| :--|:---------------------------------------|:--------------------------------------|
| 1. | First requiremnnt criteria description | Additional criteria comments          |

## Open questions

Table of any open question in connection with the solution design. Can be closed during the design work or still be open when you have started development.

| Date-Time  | Created by             | Description            | Responsible            | Answer / Solution      |
| :----------|:-----------------------|:-----------------------|:-----------------------|:-----------------------|
| 01.08.2022 | [@Little Boss](mailto:little.boss@cegal.com) | Question explanation | [@Ola Nordman](mailto:ola.nordman@cegal.com) |

# Architecture
TODO: Here you can add small architecture intro (which modeling language has been used to describe architecture, etc.) links to Architecture section of Wiki hyerachy:

1. [High Level Design](Technical/Architecture/Design/Design-High%20Level.md)
2. [Business Process Design](Technical/Architecture/Design/Design-Business%20Process.md)
3. [Data Modeling](Technical/Architecture/Design/Desing-Data%20Model.md)
4. [Data Flow](Technical/Architecture/Design/Design-Data%20Flow.md)
5. [API](Technical/Architecture/Design/Design-API.md)
6. [UI Design](Technical/Architecture/Design/Design-UI.md)

## Governance

TODO: Short explanation of governance process (security concerns) for on-prem and/or cloud installation. Link detailed Wiki documents:

[Governance](Technical/Architecture/Governance/Governance.md)
1. [Naming Standards](Technical/Architecture/Governance/Governance-Naming.md)
2. [Tagging](Technical/Architecture/Governance/Governance-Tagging.md)
3. [Cloud Subscriptions](Technical/Architecture/Governance/Governance-Subscriptions.md)
4. [Security](Technical/Architecture/Governance/Governance-Security.md)
   1. [Rolles](Technical/Architecture/Governance/Governance-Rolles.md)
   2. [Mappings](Technical/Architecture/Governance/Governance-Principalities.md)

# Dev-Ops

TODO: Short explain which DevOps practicess/tools have been used on the project for code deploymnet, testing and contributing. Link detailed Wiki documents


[Contribute](Technical/DevOps/DevOps-Contribute.md)
[Pull Request Process](Technical/DevOps/DevOps-Pull-Requests.md)
[Test Your Code](Technical/DevOps/DevOps-Test.md)
[Deployment Process](Technical/DevOps/DevOps-Deployment.md)
[Ci-Cd Pipeline Process](Technical/DevOps/DevOps-Pipelines.md)
[Infrastructure as a Code](Technical/DevOps/DevOps-IaC.md)

# Management and Monitoring

TODO: Short explanation of platform/tools used for application management and monitoring. Link do detailed Wiki documents

[Administration](Administration/Administration.md)
1. [Daily operations](Administration/Administration-Operational.md)
2. [Maintenance and upgrade](Administration/Administration-Maintenance.md)
3. [Monitoring](Administration/Administration-Monitoring.md)
