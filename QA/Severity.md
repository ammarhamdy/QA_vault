
In QA/testing, **severity** refers to **how badly a defect impacts the system**. 

A **Severity-1 issue** (sometimes called _critical_) is the **highest level** — it means the defect:
- **Blocks the system or a critical feature from working**
- Has **no workaround**    
- Prevents users from continuing their work


### Quick Severity Levels (common scale)

- **Severity 1 (Critical)** → System down / critical functionality blocked
    
- **Severity 2 (High)** → Major functionality broken but with some workaround
    
- **Severity 3 (Medium)** → Minor functionality issue, does not block main flow
    
- **Severity 4 (Low)** → Cosmetic issues (typos, UI alignment, etc.)


# Examples of Severity-1 Issues

- Application crashes on startup
    
- Login not working (no user can access the system)
    
- Payment transactions failing completely
    
- Data loss or corruption when saving
    
- Security breach allowing unauthorized access


So in a **test plan**, when we say:  
**Exit Criteria: "No open Severity-1 issues"** → it means the product cannot be released until all **critical/blocker bugs** are fixed.


# Severity vs. Priority

**Severity = How bad it is**
**Priority = How fast it should be fixed**

## **Severity** = _Impact on the system_
**How badly the defect affects the functionality.**
Decided mainly by the **QA team**.
Example:
- Login button doesn’t work → **High severity** (users can’t log in).
- Misspelled label on a settings page → **Low severity**.

## **Priority** = _Urgency of fixing the defect_
**How soon the defect should be fixed.**
Decided by **Product Owner / Project Manager / Dev lead**, often based on business needs.
Example:
- ==Misspelled company name on homepage== → **Low severity but High priority** (because it affects brand image, needs urgent fix).
- ==Rare crash in an admin-only report== → **High severity but Low priority** (few users impacted, can wait).

## Comparison Table

| Aspect     | **Severity**                                     | **Priority**                                                                     |
| ---------- | ------------------------------------------------ | -------------------------------------------------------------------------------- |
| Definition | How serious the bug is                           | How urgently the bug needs fixing <br>(ما مدى إلحاح الحاجة إلى إصلاح هذا الخلل؟) |
| Focus      | Technical impact                                 | Business impact                                                                  |
| Decided by | QA/Testers                                       | Product Owner / Manager                                                          |
| Example 1  | App crashes on login → **High severity**         | Must fix immediately → **High priority**                                         |
| Example 2  | Typo in About page → **Low severity**            | Needs urgent correction before launch → **High priority**                        |
| Example 3  | Rare crash in unused feature → **High severity** | Can be fixed later → **Low priority**                                            |
