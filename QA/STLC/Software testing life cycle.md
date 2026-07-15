
The Software Testing Life Cycle (STLC) is a structured sequence of phases that guide testing activities to ensure software quality and reliability. 

Beginning with **Requirement Analysis**, the STLC identifies what needs to be tested and sets the scope. 

Next, **Test Planning** defines the strategy, resources, and schedule. 

**Test Case Development** produces detailed test scenarios and scripts. 

In **Test Environment Setup**, the necessary hardware, software, and tools are prepared.

**Test Execution** carries out the actual tests, logging results and defects. 

Finally, **Test Closure (إنهاء)** assesses (يقيم) completion criteria, documents lessons learned, and archives test artifacts (القطع الأثرية). 

Together, these phases facilitate early defect detection, efficient test management, and continuous improvement of testing processes.


---

# 1. Requirement Analysis

During Requirement Analysis, testers review and analyze the software requirements to identify testable aspects and ==clarify ambiguities==.

They collaborate with _stakeholders_—including _business analysts_ and _developers_—to ==ensure complete understanding of functional and non-functional requirements==.

This phase yields a **[[Requirement Traceability Matrix (RTM)]]**, mapping each requirement to corresponding test cases, thereby ensuring full coverage and aiding impact analysis when changes occur.


## Key Activities
- **Requirement review meetings** to clarify scope and testability.
- **Creation of RTM** linking requirements to test scenarios.
- **Identification of automation feasibility** for ==regression-prone areas==.


## Entry and Exit Criteria
- **Entry:** Approved requirement documents and stakeholder availability.
- **Exit:** Sign-off on RTM and testable requirement list.


---

# 2. Test Planning

Test Planning defines the overall _approach_, _resources_, _schedule_, and _risk mitigation strategies_ for testing. 

A **Test Plan document** outlines the scope, objectives, resources, roles, test deliverables, and milestones.

## Key Activities
**Establishing test objectives** based on requirements and risk assessment.
**Estimating effort** for test design, execution, and defect management.
**Allocating resources** (testers, tools, environments) and defining entry/exit criteria per phase.

## Entry and Exit Criteria
**Entry:** Completed RTM and initial risk analysis.
**Exit:** Approved Test Plan and resource commitments

---

# 3. Test Case Development

In this phase, testers create detailed **test cases and test scripts** that cover all identified requirements. 

These cases specify input data, execution steps, and expected outcomes to validate functionality and performance

## Key Activities
**Designing test cases** for positive, negative, and edge scenarios.
**Preparing test data** sets, mock services, and stubs.
**Peer review** of test artifacts to ensure clarity and completeness.

## Entry and Exit Criteria
**Entry:** Approved Test Plan and RTM.
**Exit:** Completion of test cases/scripts with peer review sign-off.

---

# 4. Test Environment Setup

The Test Environment Setup phase readies (make them ready) the hardware, software, network configurations, and testing tools needed to execute test cases. 

It mirrors the production environment to uncover environment-specific defects.

## Key Activities
**Configuring test servers**, databases, and middleware.
**Installing test tools** (e.g., defect trackers, automation frameworks).
**Validating environment readiness** through smoke or sanity tests.

## Entry and Exit Criteria
**Entry:** Approved test cases and scripts.
**Exit:** Environment validation report and sign-off

---

# 5. Test Execution

Test Execution involves ==running test cases against the application and logging the actual results==. 

==Defects are reported, tracked, and prioritized for fixes==. 

==Regression tests are also performed== to ensure bug fixes do not introduce new issues.

## Key Activities
**Executing manual or automated tests** per plan.
**Logging defects** with detailed reproducible steps.
**Defect retesting and regression testing** after fixes.

---

# 6. Test Closure

In Test Closure, the test team evaluates completion criteria, compiles metrics, and archives deliverables. 

A **Test Closure Report** summarizes testing activities, defect metrics, coverage, and lessons learned, guiding process improvements for future projects.

