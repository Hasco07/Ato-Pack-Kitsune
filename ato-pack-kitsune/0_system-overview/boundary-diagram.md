# Boundary Diagram (Mermaid)

> Fictional boundary diagram to show what is **in-scope** vs **out-of-scope** for Kitsune.

```mermaid
flowchart LR
  classDef blocked fill:#f7d7d7,stroke:#b55,stroke-width:1px,color:#000;

  subgraph LAN["Kitsune LAN - Air-gapped / Offline"]
    direction LR

    subgraph UZ["User Zone"]
      DevWS["Developer Workstations"]
    end

    subgraph AZ["Admin Zone"]
      AdminWS["Admin Workstations"]
    end

    subgraph SZ["Server Zone"]
      IdP["Directory Services / IdP"]
      Git["Source Control Server"]
      CI["Build / CI Server"]
      Art["Artifact Repository"]
      Test["Test Harness / Simulator"]
    end

    subgraph ST["Security Tooling"]
      SIEM["Central Logging / SIEM"]
      Scanner["Vulnerability Scanner"]
    end

    DevWS --> IdP
    AdminWS --> IdP

    DevWS --> Git
    CI --> Git
    CI --> Art
    CI --> Test

    Git --> SIEM
    CI --> SIEM
    Art --> SIEM
    Test --> SIEM
    IdP --> SIEM

    Scanner --> DevWS
    Scanner --> Git
    Scanner --> CI
    Scanner --> Art
    Scanner --> Test
  end

  Media["Controlled Media Transfer Point (Fictional)"]
  Ext["External Networks / Internet"]:::blocked

  Media -. "Approved import/export only" .-> LAN
  LAN -. "No direct connectivity" .-> Ext
