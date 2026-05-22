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
    A[Manager Identifies HC Need] --> B[Manager Submits HC Request]
    B --> C[HRBP Review]
    B --> D[Finance Review]
    C --> E{HC Approved?}
    D --> E
    E -->|Yes| F[Hiring Manager Notifies TAM]
    F --> G[TAM Creates Requisition]
    G --> H[TAM Assigns Req to TAS]
    H --> I[TAS Begins Sourcing Workflow]
