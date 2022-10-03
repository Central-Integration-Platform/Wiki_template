# Technical | DevOps | Deployment

## Deployment Workflow

TODO: Explain deplyment workflow and link addtional documents like contribution, pipelines, etc.

### Sequence diagram example
---

``` mermaid
sequenceDiagram;
 % autonumber;
 participant D as Developer
 participant Ops as Approver 
 participant DOP as Azure DevOps
 participant Dev as Dev;
 participant Tst as Test;
 participant Stg as Staging;
 participant Prd as Production;

 Note over Dev, Stg: Dev branch
 Note over Prd: Main branch

%%rect rgba(0, 0, 255)
  D->>+DOP: Pull Reguest on Azure DevOps

  DOP->>+Dev: Automatic deployment to Development;
  Dev->>+Dev: Automatic Unit tests;
  Dev-->>-D: Fix bugs

  DOP->>+Stg: Automatic deployment to Staging;
  Stg->>+Stg: Automatic Integration tests;
  Stg-->-D: Fix Bugs


  Ops->>+Prd: Automatic deployment to Production with manual approval;

%%end

```
