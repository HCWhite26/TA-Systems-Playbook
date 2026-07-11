# End-to-End Recruiting Workflow — v1

## Purpose
This workflow represents the full recruiting lifecycle from role kickoff through offer acceptance and pre‑boarding. It serves as the anchor workflow for all sub‑workflows in the TA Systems Playbook. The Intake Workflow (Workflow 1.1) occurs immediately before HM1 and provides the detailed structure for role calibration, success profile definition, and interview plan alignment.

## Workflow Notes
- Covers the entire lifecycle from kickoff → sourcing → interviewing → offer → pre‑boarding  
- Defines ownership across 7 functional lanes  
- Establishes consistent handoffs and decision points  
- Intake is a required sub‑workflow that occurs immediately before HM1 (Kickoff). The detailed Intake Workflow is documented in Workflow 1.1.  
- Serves as the parent workflow for Intake, Sourcing, Interviewing, and Offer sub‑workflows  
- Ensures alignment across TA, HRBP, Finance, and People Ops  

## Sub‑Workflow Mapping
- Workflow 1.1 — Intake Workflow (occurs immediately before HM1)  
- Workflow 1.2 — Sourcing Workflow  
- Workflow 1.3 — Interview Workflow  
- Workflow 1.4 — Offer Workflow  
- Workflow 1.5 — Pre‑Boarding Workflow

## Diagram
```mermaid
flowchart LR

classDef hm fill:#f9c74f,stroke:#8b860b,stroke-width:1px,color:#000;
classDef hrbp fill:#90be6d,stroke:#2d6a4f,stroke-width:1px,color:#000;
classDef tam fill:#4d9de0,stroke:#1d3557,stroke-width:1px,color:#fff;
classDef tas fill:#4d9de0,stroke:#1d3557,stroke-width:1px,color:#fff;
classDef interview fill:#577590,stroke:#1d3557,stroke-width:1px,color:#fff;
classDef comp fill:#f9844a,stroke:#7f4f24,stroke-width:1px,color:#000;
classDef hr fill:#43aa8b,stroke:#2d6a4f,stroke-width:1px,color:#000;

subgraph Hiring_Manager
direction TB
HM1[Kickoff: Define Role Requirements]:::hm
HM2[Approve JD & Interview Plan]:::hm
HM3[Participate in Interviews]:::hm
HM4[Final Candidate Selection]:::hm
HM5[Approve Offer Details]:::hm
end

subgraph HR_Business_Partner_HRBP
direction TB
HRBP1[Validate Role Need & Org Alignment]:::hrbp
HRBP2[Support JD Finalization]:::hrbp
HRBP3[Participate in Debrief If Applicable]:::hrbp
HRBP4[Support Offer Strategy]:::hrbp
end

subgraph Talent_Acquisition_Manager_TAM
direction TB
TAM1[Launch Requisition]:::tam
TAM2[Define Sourcing Strategy]:::tam
TAM3[Oversee Interview Plan Setup]:::tam
TAM4[Partner on Final Candidate Decision]:::tam
TAM5[Initiate Offer Process]:::tam
end

subgraph Talent_Acquisition_Specialist_TAS
direction TB
TAS1[Market Calibration & Pipeline Build]:::tas
TAS2[Outbound + Inbound Sourcing]:::tas
TAS3[Initial Screening & Qualification]:::tas
TAS4[Candidate Management Through Loop]:::tas
TAS5[Prepare Offer Packet]:::tas
end

subgraph Interview_Team
direction TB
INT1[Conduct Structured Interviews]:::interview
INT2[Submit Scorecards]:::interview
INT3[Participate in Debrief]:::interview
end

subgraph Compensation_Finance
direction TB
COMP1[Comp Review & Approval]:::comp
end

subgraph HR_People_Ops
direction TB
HR1[Pre‑Boarding Handoff]:::hr
HR2[Initiate Onboarding Workflow]:::hr
end

%% Phase 1 — Role Kickoff & Requisition Launch
HM1 --> HRBP1 --> TAM1
HRBP1 --> HM2
TAM1 --> TAM3
TAM3 --> HM2

%% Phase 2 — Sourcing & Pipeline Development
TAM2 --> TAS1 --> TAS2 --> TAS3
TAS3 --> HM3

%% Phase 3 — Interviewing & Evaluation
HM3 --> INT1 --> INT2 --> INT3
INT3 --> HRBP3
INT3 --> TAM4
TAM4 --> HM4

%% Phase 4 — Offer, Close & Pre‑Boarding
HM4 --> TAM5 --> TAS5 --> COMP1 --> HM5
HM5 --> HR1 --> HR2
