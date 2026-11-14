
# What is Software Testing?
A good answer should mention:
- Verification
- Validation
- Requirements
- Quality
- Risk reduction
- Defect detection

Software testing is a **systematic process** of evaluating a software product to ==verify that it meets functional and non-functional requirements==, validate that it fulfills business and user expectations, identify defects, and reduce the risk of failures in production.

When answering, try to naturally include these ideas:
- Verify requirements.
- Validate user needs.
- Find defects.
- Reduce risks.
- Improve quality.
- Build confidence in the release.

---

# What are the Objectives of Software Testing?

## 1. Find Defects
The most obvious objective.
Testing helps discover defects before customers do.

## 2. Verify Requirements
Verify the software has been built according to the documented requirements.
Ask yourself: 
> "Did we build the product correctly?"

## 3. Validate Business & User Needs
Even if all requirements are implemented correctly, the software must still solve the user's problem.
Ask yourself:
> "Did we build the right product?"

## 4. Reduce Business Risks
QA identifies issues that could negatively affect the business.

## 5. Improve Software Quality
Quality includes:
- Reliability
- Performance
- Security
- Usability
- Compatibility
- Stability

## 6. Build Confidence
Testing provides stakeholders with confidence before release.

## 7. Prevent Future Defects
QA isn't only about detecting problems.
Examples:
- Reviewing requirements
- Reviewing designs
- Improving development processes
- Suggesting better validation
- Improving test coverage

---

# What types of testing do you know?
## Answer:
I know several testing types including:
- Functional Testing
- Regression Testing
- Smoke Testing
- Sanity العقلانية Testing
- API Testing
- Integration Testing
- System Testing
- Acceptance Testing
- Performance Testing
- Security Testing
- UI/UX Testing
- Compatibility Testing
- Exploratory Testing

---

# What is the difference between SDLC and STLC?
## Quick Answer
- **SDLC (Software Development Life Cycle):** The complete process of building and maintaining software.
- **STLC (Software Testing Life Cycle):** The testing process within the software development lifecycle.
### SDLC Phases
1. Requirements
2. Design
3. Development
4. Testing
5. Deployment
6. Maintenance

### STLC Phases
1. Requirement Analysis
2. Test Planning
3. Test Case Design
4. Test Environment Setup
5. Test Execution
6. Test Closure

## Strong Interview Answer
> “SDLC covers the entire process of developing software, from requirements to maintenance. STLC focuses specifically on testing activities, from analyzing requirements and planning tests to executing tests and closing the testing process. STLC is part of the overall SDLC.”

---

# What is the difference between Static Testing and Dynamic Testing?

## Quick Answer
- **Static Testing:** Testing **without executing** the software.
- **Dynamic Testing:** Testing by **executing** the software.

### Examples
**Static Testing:**
- Requirement reviews
- Design reviews
- Code reviews
- Inspections
**Dynamic Testing:**
- Executing test cases
- API testing
- Functional testing
- Regression testing

## Strong Interview Answer
> “Static testing evaluates software artifacts without executing the application, such as reviewing requirements or code. Dynamic testing involves executing the software and verifying its actual behavior against expected results.”

### 🧠 Easy Memory Trick
> **Static = Don't Run**  
> **Dynamic = Run**

---

# What is the difference between Error, Defect, Bug, and Failure?

## Quick Answer
- **Error:** A human mistake.  
    _Example: A developer misunderstands a requirement._
- **Defect:** A problem in a software artifact caused by an error.  
    _Example: The code calculates the total incorrectly._
- **Bug:** Common informal term for a defect found in software.
- **Failure:** When the software behaves incorrectly during execution because of a defect.  
    _Example: The user sees the wrong total._


---

# What is the difference between Smoke, Sanity, Retesting, and Regression Testing?

## Quick Answer
- **Smoke Testing:** Checks whether a new build is stable enough for detailed testing.
- **Sanity Testing:** Checks whether a specific change or fix works correctly.
- **Retesting:** Tests a **specific failed test/bug again** after it has been fixed.
- **Regression Testing:** Checks that new changes **didn't break existing functionality**.

### Example
A developer fixes a login bug:
1. **Smoke** → Is the application generally working?
2. **Retesting** → Does the login bug now work correctly?
3. **Sanity** → Does the related login functionality still behave correctly?
4. **Regression** → Did the login fix break registration, logout, password reset, etc.?

### 🧠 Easy Memory Trick
> **Smoke = Build**  
> **Sanity = Change**  
> **Retesting = Fix**  
> **Regression = Existing features**

---
# Verification vs Validation ? 

## Verification

### Definition
Verification ensures that each phase of development complies with the specified requirements and design.
It is mainly a **static activity** (no need to run the software).
### Examples
- Requirement review
- Design review
- Code review
- Document review

### Example
Requirement:
> Password must contain at least 8 characters.


## 2. Validation

### Definition
Validation ensures the final software behaves as users and the business expect.
It is mainly a **dynamic activity** because the software is executed.

### Examples
- Functional testing
- System testing
- User **Acceptance Testing** (UAT)

### Example
You actually enter:
```
Password: 12345678
```
The system accepts it.
Then enter:
```
1234567
```
The system rejects it.


## Which Happens First?
```less
Requirements
     ↓
Verification
     ↓
Development
     ↓
Validation
     ↓
Release
```


## EASY Memory Trick
- **Verification** → **Requirements & Reviews** → _"Are we building the product right?"_
- **Validation** → **Running & Testing** → _"Are we building the right product?"_
- **Authentication** → **Identity** → _"Who are you?"_

---
# You are testing a login page. What would you test?

## Answer:
==I would divide testing into multiple areas.==

### Functional Testing
- Valid login
- Invalid credentials
- Empty fields
- Remember me
- Logout flow

### Validation Testing
- Email format
- Password length
- Special characters
- Spaces handling

### Security Testing
- SQL injection attempts
- Brute force handling
- Password masking
- Session expiration

### UI/UX Testing
- Error message clarity
- Button states
- Keyboard support
- Responsive layout

### Edge Cases
- Slow internet
- Multiple rapid clicks
- App background/foreground handling

---

# What is the difference between **Re-testing** and **Regression Testing**?

| Aspect                  | Re-testing                                                    | Regression Testing                                                      |
| ----------------------- | ------------------------------------------------------------- | ----------------------------------------------------------------------- |
| **Purpose**             | Verify that a specific bug has been fixed.                    | Verify that **recent changes** have not broken existing functionality.  |
| **Focus**               | The **failed** functionality only.                            | The entire affected area (or application).                              |
| **When it's performed** | After a developer fixes a reported defect.                    | After code changes, bug fixes, enhancements, or new features are added. |
| **Test Cases**          | Executes the same test case(s) that previously failed.        | Executes previously passed test cases related to impacted areas.        |
| **Scope**               | Narrow.                                                       | Broad.                                                                  |
| **Automation**          | Can be manual or automated, but often manual for a few tests. | Frequently automated because it involves many test cases.               |
| **Objective**           | Confirm the defect is fixed.                                  | Ensure nothing else is broken by the change.                            |

## Example
Suppose an e-commerce website has a bug:
**Bug:** Users cannot add a product to the cart.
The developer fixes the issue.

## Step 1: Re-testing
You run the **"Add to Cart"** test case again.
- Add a product.
- Click **Add to Cart**.
- Verify the product appears in the cart.
✅ If it works, the defect is fixed.

## Step 2: Regression Testing
Now you verify that the fix didn't affect other features:
- Login
- Search products
- **Remove from cart**
- **Update quantity**
- **Apply coupons**
- **Checkout**
- Payment
- **Order history**
If all still work correctly, the regression test passes.

## Easy way to remember
- **Re-testing = "Did we fix the bug?"**
- **Regression Testing = "Did the fix break anything else?"**


## Interview Answer (30 seconds)
> **Re-testing** is performed to verify that a reported defect has been fixed by executing the failed test case again.  
> **Regression testing** is performed to ensure that code changes, such as bug fixes or new features, have not introduced defects into existing functionality. 
> Re-testing focuses on a specific defect, while regression testing covers all affected areas of the application.


---

# What are the testing levels?

## Answer
"There are four main testing levels, each focusing on a different scope of the application."

## 1. Unit Testing
- Tests individual functions, methods, or classes.
- Usually performed by developers.
- Fast and isolated.
**Example**  
Testing a function that calculates restaurant commission عمولة.

## 2. Integration Testing
- Verifies communication between two or more modules.
**Example**  
Testing that the **Withdrawal Service** correctly updates the Wallet Service and **Notification Service** after approval.

## 3. System Testing
- Tests the complete application as a whole.
- Usually performed by QA.
**Example**  
Testing the complete withdrawal workflow:  
Restaurant → Request → Admin Approval → Balance Update → Notification.

## 4. User Acceptance Testing (UAT)
- Performed by customers or business users.
- Verifies that the application meets business requirements.
**Example**  
Restaurant managers verify that the withdrawal process matches their operational needs.


---

# Who performs each testing level?

| Testing Level       | Usually Performed By                       |
| ------------------- | ------------------------------------------ |
| Unit Testing        | Developers                                 |
| Integration Testing | Developers / QA                            |
| System Testing      | QA Engineers                               |
| Acceptance Testing  | Customers / Product Owner / Business Users |

---

# What is Black Box Testing?

## Answer
Black Box Testing means testing the application without knowing or considering its internal code or implementation. 
The tester focuses only on inputs, outputs, and expected behavior based on requirements.

## Example:
Login page:
- Enter valid credentials
- Verify successful login
The tester does not care how the authentication is implemented internally.


---

# What is White Box Testing?

## Answer
White Box Testing is performed with knowledge of the internal code, logic, and implementation. 
It focuses on testing code paths, conditions, loops, and branches.

Usually performed by ==developers== or automation engineers.

## Example: 
Testing all branches of an `if-else` statement inside the authentication logic.

---

# What is Gray Box Testing?

## Answer
Gray Box Testing combines both approaches. 
The tester has partial knowledge of the system's internal design while testing it from the user's perspective.

## Example: 
Knowing the **database schema** or **API endpoints** while performing end-to-end testing.

---

# What is Boundary Value Analysis (BVA)?

## Answer
==Boundary Value Analysis is a test design technique where defects are often found at the edges of valid input ranges. ==
Instead of testing only typical values, we focus on values at and around the boundaries.

## Example (Age field)
Allowed:  18–60
Test values:
- 17 ❌
- 18 ✅
- 19 ✅
- 59 ✅
- 60 ✅
- 61 ❌
Because bugs frequently occur at minimum and maximum limits.


---


## What is Equivalence Partitioning?

## Answer
"Equivalence Partitioning divides input values into groups where all values are expected to behave similarly. We test one representative value from each group instead of every possible value."

## Example
Age:  18–60

Partitions:
Invalid: Less than 18
Valid: 18–60
Invalid: Greater than 60

Representative tests:
- 15
- 30
- 70


---

# What is Decision Table Testing?

## Answer
"Decision Table Testing is useful when the application's behavior depends on multiple conditions. We create a table of conditions and expected outcomes to ensure all important combinations are tested."

## Example
Conditions:
- User is logged in
- User has admin role

| Logged In | Admin | Expected |
| --------- | ----- | -------- |
| No        | No    | Denied   |
| Yes       | No    | Denied   |
| Yes       | Yes   | Allowed  |


---

# What is State Transition Testing?

## Answer
"State Transition Testing verifies how a system behaves as it moves between different states after events or actions."

## Example
Account states:
```less
Active
↓
Three failed login attempts
↓
Locked
↓
Admin unlocks account
↓
Active
```
QA verifies each transition occurs correctly and invalid transitions are prevented.


---

# What is Error Guessing?

## Answer
"Error Guessing is an ==experience-based testing technique== where the tester anticipates يتوقع likely defects based on previous projects, domain knowledge, and intuition."

Examples:
- Double-clicking the Submit button
- Entering extremely long text
- Refreshing during payment
- Losing internet connection during checkout
- Using emojis or special characters in text fields


---

# Which **test design** techniques have you used?
## Answer
I would combine several techniques

I commonly use:
- Boundary Value Analysis
- Equivalence Partitioning
- Decision Table Testing
- State Transition Testing
- Error Guessing
- Exploratory Testing
I choose the technique depend **How would you test a password field?**

## Boundary Value Analysis
If the allowed length is 8–20 characters:
- 7 ❌
- 8 ✅
- 9 ✅
- 19 ✅
- 20 ✅
- 21 ❌

## Equivalence Partitioning
- Too short
- Valid length
- Too long

## Functional Testing
- Valid password
- Invalid password
- Empty password

## Security Testing
- SQL injection attempts
- XSS attempts (if applicable)
- Password masking
- Copy/paste behavior (if restricted)
- Rate limiting after repeated failures

## UI/UX Testing
- Show/hide password
- Clear error messages
- Caps Lock indicator (if available)

## Edge Cases
- Leading/trailing spaces
- Unicode characters
- Emojis (if not supported)
- Very long pasted strings"ing on the feature. For example, I use Boundary Value Analysis for input fields, Decision Tables for business rules, and State Transition Testing for workflows like login, order status, or account locking.

---








