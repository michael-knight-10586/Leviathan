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
  Leviathan["Leviathan"]
  Leviathan --> Pequod["Pequod"]
  Pequod --> Ocean["Ocean"]
  Ocean --> Armory["Armory"]

  subgraph Pequod
    Chartroom["Chartroom"]
    Maps["Maps"]
    Logbook["Logbook"]
  end

  subgraph Ocean
    England_1["England_1"]
    England_2["England_2"]
  end

  subgraph Armory
    Gam["Gam"]
    subgraph Armory_England1["England_1 (Armory)"]
      Spouter_inn["Spouter_inn"]
      Crows_nest["Crows_nest"]
      Whaleboat["Whaleboat"]
      Tackle["Tackle"]
    end
  end
```