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
| Armory/England_1/ | England_1 | League-specific transforms |  |
| Armory/England_1/Blubber_room/ | Blubber_room | Head-to-head & tables |  |
| Armory/England_1/Crows_nest/ | Crows_nest | Rolling-form metrics |  |
| Armory/England_1/Whaleboat/ | Whaleboat | Expected-points models |  |
| Armory/England_1/Tackle/ | Tackle | Composite rankings |  |
| Armory/England_1/Line/ | Line | Line analytics |  |
| Armory/England_1/Harpoon/ | Harpoon | Harpoon analytics |  |
| Awhalin/ | Awhalin | Model staging |  |
| Awhalin/Gam/ | Gam |  |  |
| Awhalin/England_1/ | England_1 |  |  |
| Awhalin/England_1/Mapple/ | Mapple |  |  |
| Awhalin/England_1/Peleg/ | Peleg |  |  |
| Awhalin/England_1/Bildad/ | Bildad |  |  |
| Awhalin/England_1/Flask/ | Flask |  |  |
| Awhalin/England_1/Stubb/ | Stubb |  |  |
| Awhalin/England_1/Fedallah/ | Fedallah |  |  |
| Awhalin/England_1/Tashtego/ | Tashtego |  |  |
| Awhalin/England_1/Daggoo/ | Daggoo |  |  |
| Awhalin/England_1/Elijah/ | Elijah |  |  |
| Awhalin/England_1/Ahab/ | Ahab |  |  |
| Awhalin/England_1/Starbuck/ | Starbuck |  |  |
| Awhalin/England_1/Ishmael/ | Ishmael |  |  |
| Awhalin/England_1/Queequeg/ | Queequeg |  |  |
| Awhalin/England_1/Rachel/ | Rachel |  |  |

## Diagram

```mermaid
flowchart TB
  classDef default fill:#3BA17B,stroke:#3BA17B,color:gold;
  Leviathan:::default
  Leviathan --> Pequod
  Leviathan --> Ocean
  Leviathan --> Armory
  Leviathan --> Awhalin
  subgraph Pequod [Pequod]
    Pequod --> Chartroom
    Pequod --> Maps
    Pequod --> Logbook
  end
  subgraph Ocean [Ocean]
    Ocean --> England_1
    Ocean --> England_2
  end
  subgraph Armory [Armory]
    Armory --> Gam
    Armory --> England_1
  subgraph England_1 [England_1]
    England_1 --> Blubber_room
    England_1 --> Crows_nest
    England_1 --> Whaleboat
    England_1 --> Tackle
    England_1 --> Line
    England_1 --> Harpoon
  end
  end
  subgraph Awhalin [Awhalin]
    Awhalin --> Gam
    Awhalin --> England_1
  subgraph England_1 [England_1]
    England_1 --> Mapple
    England_1 --> Peleg
    England_1 --> Bildad
    England_1 --> Flask
    England_1 --> Stubb
    England_1 --> Fedallah
    England_1 --> Tashtego
    England_1 --> Daggoo
    England_1 --> Elijah
    England_1 --> Ahab
    England_1 --> Starbuck
    England_1 --> Ishmael
    England_1 --> Queequeg
    England_1 --> Rachel
  end
  end
```