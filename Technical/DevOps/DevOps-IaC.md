# Technical | DevOps | Infrastructure As a Code

## Introduction

TODO: Explain whch infrastructure prerequisites are needed to run your project. Explain which coding tools are going to be used to deploy your infrastrucure (Ansilbe, Terraform, Bicep, ARM, CludCode, etc.).


## Process

TODO: Explain process of developing and deploying infrastrucure code (recomended editors, recomended DevOps tools). Link pipeline documents used to explain deployment process


### Sequence diagram example
---

```mermaid
sequenceDiagram;
 % autonumber;
 participant D as Infrastructure Engineer
 participant Ops as Approver
 participant DOP as Azure DevOps
 participant Snd as Sandbox;
 participant Dev as Dev;
 participant Tst as Test;
 participant Stg as Staging;
 participant Prd as Production;

 Note over Dev, Stg: Dev branch
 Note over Prd: Main branch

%%rect rgba(0, 0, 255)
  D->>+DOP: Pull Reguest on Azure DevOps

  DOP->>+Snd: Automatic deployment to Sandbox environment;
  Snd->>+Snd: Infrastructure testing;
  Snd-->>-D: Fix bugs
  Snd->>+Snd: Resource purging;

  DOP->>+Dev: Automatic deployment to Dev environment;

  DOP->>+Stg: Automatic deployment to Staging;
  Stg->>+Stg: Manual security and networking tests;
  Stg-->-D: Fix Bugs


  Ops->>+Prd: Automatic deployment to Production with manual approval;

%%end
```
