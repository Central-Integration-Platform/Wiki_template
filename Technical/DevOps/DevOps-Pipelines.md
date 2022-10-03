# Technical | DevOps | Pipelines

## Introcuction

TODO: Explain overall pipeline tooling and  process for both Infrastructure as code regular development/testing used in project

## DevOps pipeline

TODO: Add links to tool documentation explaing use and sintax for developing pipelines

### Pipeline process

TODO: Explain process for different stages (Build, Deploy, Test, Release). Link your pipeline code. Examples:

- **Build** - implemented within `azure-pipelines-ansible-pr.yml` file
- **Deploy** - implemented within `azure-pipelines-ansible.yml` file

#### Build pipeline

TODO: Detail explaination of phases of each stage of the pipeline. Example:

Build process is integral part of the [Pull request](DevOps-Pull-Requests.md)  process. Every time changes in working branch (`feature-xx/task-xx/smal-description`) have been submitted the **Build** process starts.

***Phases:***

- **Build** - IaC code is deployed to Sandbox *environment* and resources created
- **Test** - resources are tested that they are up and running and configured correctly
- **Purge** - resources are purged from Sandbox *environment*

#### Flow chart example:

``` mermaid
graph TD
    A((Pull request)) -->|Build| B(Create Sandbox resources)
    B --> C{Creation successful?}
    C -->|Yes| D[Test Resources]
    C -->|No| E((Exit-Failure))
    D --> F{Test successful?}
    F -->|Yes| G(Purge Resources)
    F -->|No| E
    G -->H((Exit-Success))
```

#### Deploy pipeline

Deployment is being divided in tree stages:

- Deployment to **dev** *environment*- performs only if **Pull request** has been successfully merged to ***dev*** branch
- Deployment to **staging** *environment* - performs only if deployment to **dev** *environment*has been successful 
- Deployment to **prod** *environment* - performs only if **Pull request** that merges ***dev*** branch to ***main*** has been approved and successfully merged

***Branches used: ***

- ***dev*** - for deployment to **dev** *environment* and **staging** *environment*
- ***main*** - for deployment to **prod** *environment* 


#### Flow chart:

``` mermaid
graph TD
    A((Merge to Dev)) -->|Deploy| B(Create Dev resources)
    B --> C{Creation successful?}
    C -->|Yes| D(Create Staging Resources)
    C -->|No| E((Exit-Failure))
    D --> F{Creation successful?}
    F -->|Yes| G[Skip production]
    F -->|No| E
    G -->H((Exit-Success))
```

``` mermaid
graph TD
    A((Merge Dev->Main)) -->|Skip| B(Create Dev resources)
    B --> |Skip| C(Create Staging resources)
    C --> |Deploy| D(Create Prod resources)
    D --> E{Creation successful?}
    E -->|Yes| F((Exit-Success))
    E -->|No| G((Exit-Failure))
```
