# Technical | Integrations | Integration Name | Architecture | Data flow

TODO: Show and explain data flow (sequence) that your integration is going to use/implement.

## Sequence diagram example

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

[Link to examples](https://github.com/mermaid-js/mermaid/blob/develop/docs/sequenceDiagram.md)