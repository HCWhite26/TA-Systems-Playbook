# UAT Cycle 1 — Requisition Creation & Approval Routing

## Objective
Validate that a requisition can be created successfully and that the approval workflow routes correctly based on business rules.

---

## PHASE 1 — Preconditions

- User is logged in with correct role (Hiring Manager or Recruiter)
- Access to “Create Requisition” is enabled
- Approval chain exists (Manager → HRBP → TA Lead)
- Job profile exists (Talent Acquisition Specialist)
- No known defects blocking requisition creation

---

## PHASE 2 — Test Script

### Test Case ID
UAT-REQ-001

### Scenario
Create a new requisition and validate approval routing.

### Test Steps
1. Navigate to **Create Requisition**
2. Select job profile: **Talent Acquisition Specialist**
3. Enter required fields:
   - Department: HR  
   - Location: Orlando  
   - Hiring Manager: John Smith  
   - Recruiter: Helen White  
4. Add compensation range
5. Submit requisition for approval

---

## Expected Results

- System generates a **Req ID**
- Approval workflow triggers automatically
- Routing follows:
  1. Hiring Manager  
  2. HRBP  
  3. TA Lead  
- Status updates to **Pending Approval**
- No validation errors

---

## PHASE 3 — Analyst Thinking Model

During execution, validate:

- Field prepopulation accuracy  
- Workflow routing logic  
- UI behavior consistency  
- Error handling  
- Timing of workflow triggers  
- Data integrity  

---

## PHASE 4 — Defect Documentation Template

**Defect ID:**  
**Severity:**  
**Module:** Requisition Creation  
**Steps to Reproduce:**  
**Expected Result:**  
**Actual Result:**  
**Impact:**  
**Attachments:**  

---

## PHASE 5 — Retest & Sign-Off

- If workflow functions correctly → **Pass**
- If workflow fails → Log defect and retest after fix
