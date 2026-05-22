# UAT Cycle 1 — Requisition Creation & Approval Routing (Corrected)

## Objective
Validate that a requisition is created only after headcount approval and that the TA workflow reflects the correct business process.

---

## PHASE 1 — Preconditions

- Manager has submitted a headcount (HC) request
- HRBP and Finance have approved the HC request
- Hiring Manager has notified the Talent Acquisition Manager (TAM)
- TAM has access to create requisitions
- No known defects blocking requisition creation

---

## PHASE 2 — Test Script

### Test Case ID
UAT-REQ-001

### Scenario
TAM creates a requisition after HC approval and assigns it to TAS.

### Test Steps
1. Confirm HC approval is visible/validated (HRBP + Finance)
2. TAM navigates to **Create Requisition**
3. TAM selects job profile: **Talent Acquisition Specialist**
4. TAM enters required fields:
   - Department: HR  
   - Location: Orlando  
   - Hiring Manager: John Smith  
   - Recruiter: Helen White (TAS)  
5. TAM adds compensation range
6. TAM submits requisition for creation
7. TAM assigns requisition to TAS for sourcing

---

## Expected Results

- System generates a **Req ID**
- No approval routing is triggered
