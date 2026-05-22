# HC to Requisition Creation Workflow

This workflow represents the corrected business process for how headcount approval leads to requisition creation and assignment within TA.

---

## Workflow Diagram (Text-Based)

Manager Identifies HC Need  
        ↓  
Manager Submits HC Request  
        ↓  
HRBP Review → Finance Review  
        ↓  
HC Approved  
        ↓  
Hiring Manager Notifies TAM  
        ↓  
TAM Creates Requisition  
        ↓  
TAM Assigns Req to TAS  
        ↓  
TAS Begins Sourcing Workflow  

---

## Workflow Notes

- HC approval **must** occur before any requisition is created  
- HRBP and Finance act as the approval gate  
- Hiring Manager does **not** create the requisition  
- TAM owns req creation and setup  
- TAS owns sourcing and candidate movement  
- This workflow prevents shortcut drift and ensures compliance with business logic
```mermaid
flowchart TD
    %% STYLES
    classDef manager fill:#f9c74f,stroke:#b8860b,stroke-width:1px,color:#000;
    classDef hr fill:#90be6d,stroke:#2d6a4f,stroke-width:1px,color:#000;
    classDef ta fill:#4d9de0,stroke:#1d3557,stroke-width:1px,color:#fff;
    classDef decision fill:#9d4edd,stroke:#5a189a,stroke-width:1px,color:#fff;

    %% NODES
    A[Manager Identifies HC Need]:::manager --> B[Manager Submits HC Request]:::manager
    B --> C[HRBP Review]:::hr
    B --> D[Finance Review]:::hr
    C --> E{HC Approved?}:::decision
    D --> E
    E -->|Yes| F[Hiring Manager Notifies TAM]:::manager
    F --> G[TAM Creates Requisition]:::ta
    G --> H[TAM Assigns Req to TAS]:::ta
    H --> I[TAS Begins Sourcing Workflow]:::ta
```
