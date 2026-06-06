# Evidence Correlation Flow

```mermaid
flowchart LR
    graph["Microsoft Graph"] --> engine["Correlation Engine"]
    teams["Teams"] --> engine
    gitlab["GitLab"] --> engine
    support["Support Records"] --> engine
    sla["SLA Versions"] --> engine
    releases["Release History"] --> engine

    engine --> timeline["Timeline Reconstruction"]
    timeline --> package["Evidence Package"]
    package --> report["Audit Report"]
```
