both **false positives** and **false negatives** are very common concepts in Quality Assurance, software testing, security testing, machine learning, medical systems, and many other fields.

----
# Simple Definition

## False Positive

The system says **something is wrong**, but actually **everything is fine**.

Example:
- Your fraud detection system blocks a valid restaurant withdrawal request.
- Antivirus flags a safe file as malicious.
- A test case fails because of a bad test script, not because of a real bug.

Meaning:
> “Detected a problem that does not really exist.”

---

## False Negative

The system says **everything is fine**, but actually **there is a real problem**.

Example:
- A hacker attack passes undetected.
- A restaurant withdraws more money than allowed and the system accepts it.
- A buggy feature passes testing even though it is broken.

Meaning:
> “Missed a real problem.”

---
# Quick Memory Trick

| Result           | Reality        | Type           |
| ---------------- | -------------- | -------------- |
| "Problem exists" | No problem     | False Positive |
| "No problem"     | Problem exists | False Negative |
Or simpler:
- **False Positive = fake alarm**
- **False Negative = missed alarm**

