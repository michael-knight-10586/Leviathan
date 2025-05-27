| Path | Metaphor | Intended Role | Notes |
|------|----------|---------------|-------|
| Pequod/ | Pequod | Docs & notebooks hub |  |
| Pequod/Chartroom/ | Chartroom | High-level overviews + config |  |
| Pequod/Maps/ | Maps | Architecture diagrams + specs |  |
| Pequod/Logbook/ | Logbook | Project diary & notes |  |
| Ocean/ | Ocean | Data lake |  |
| Ocean/England_1/ | England_1 | Premier League data |  |
| Ocean/England_2/ | England_2 | Championship data |  |
| Armory/ | Armory | Feature-engineering pipelines |  |
| Armory/Gam/ | Gam | Cross-league utilities |  |
| Armory/England_1/ | England_1 (Armory) | League-specific transforms |  |
| Armory/England_1/Spouter_inn/ | Spouter_inn | Head-to-head & tables |  |
| Armory/England_1/Crows_nest/ | Crows_nest | Rolling-form metrics |  |
| Armory/England_1/Whaleboat/ | Whaleboat | Expected-points models |  |
| Armory/England_1/Tackle/ | Tackle | Composite rankings |  |

```mermaid
flowchart TB
  %% Define a default style for all nodes
  classDef default fill:#014F43,stroke:#014F43,color:gold;

  %% Top-level flow
  Leviathan["Leviathan"]:::default
  Leviathan --> Pequod["Pequod"]:::default
  Pequod --> Ocean["Ocean"]:::default
  Ocean --> Armory["Armory"]:::default

  %% Subgraphs
  subgraph Pequod
    Chartroom["Chartroom"]:::default
    Maps["Maps"]:::default
    Logbook["Logbook"]:::default
  end

  subgraph Ocean
    England_1["England_1"]:::default
    England_2["England_2"]:::default
  end

  subgraph Armory
    Gam["Gam"]:::default
    subgraph Armory_England1["England_1 (Armory)"]
      Spouter_inn["Spouter_inn"]:::default
      Crows_nest["Crows_nest"]:::default
      Whaleboat["Whaleboat"]:::default
      Tackle["Tackle"]:::default
    end
  end
```