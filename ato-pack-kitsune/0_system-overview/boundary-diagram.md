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

    DevWS -->|auth| IdP
    AdminWS -->|auth| IdP

    DevWS -->|commit/fetch| Git
    CI -->|pull| Git
    CI -->|store| Art
    CI -->|test| Test

    Git -->|logs| SIEM
    CI -->|logs| SIEM
    Art -->|logs| SIEM
    Test -->|logs| SIEM
    IdP -->|audit| SIEM

    Scanner -->|scan| DevWS
    Scanner -->|scan| Git
    Scanner -->|scan| CI
    Scanner -->|scan| Art
    Scanner -->|scan| Test
  end

  Media["Controlled Media Transfer Point (Fictional)"]
  Ext["External Networks / Internet"]:::blocked

  Media -. "approved transfer" .-> LAN
  LAN -. "no connectivity" .-> Ext
