# Internal Knowledge Assistant — Test Results

## 1. Test Overview

The Internal Knowledge Assistant was tested against three required knowledge-coverage scenarios:

1. Fully Covered
2. Partially Covered
3. Uncovered

The tests verify that the GPT answers strictly from the uploaded internal documentation and does not hallucinate or use unsupported external information.

---

## 2. Test 1 — Fully Covered

### Question

> What is the company's annual leave entitlement?

### Expected Behavior

The assistant should provide the documented annual leave entitlement and include a bold source reference.

### Actual Result

The assistant responded:

> Full-time employees are entitled to **24 days of annual leave per calendar year**.

It provided the following source references:

**Source: Employee Leave Policy — Annual Leave Entitlement**

**Source: Employee FAQ & Leave Process Guide — Frequently Asked Questions (Q1)**

### Result

**PASS**

### Validation

- Correct information provided: ✅
- Information supported by uploaded documents: ✅
- No unsupported information added: ✅
- Bold source references provided: ✅

---

## 3. Test 2 — Partially Covered

### Question

> How many sick leave days am I entitled to, and how do I apply for sick leave?

### Expected Behavior

The assistant should not invent a sick leave entitlement or application procedure. It should explain that the requested information is not covered by the available documentation.

### Actual Result

The assistant responded:

> The available internal documentation does **not specify a sick leave entitlement**, so I cannot provide a number of sick leave days.
>
> It also does not document a separate sick-leave application procedure.

It provided the following source references:

**Source: Employee Leave Policy — Information Not Covered by This Policy**

**Source: Employee FAQ & Leave Process Guide — Topics Not Covered in This Guide**

### Result

**PASS**

### Validation

- No sick leave entitlement invented: ✅
- No unsupported application procedure invented: ✅
- Documentation limitation clearly explained: ✅
- Bold source references provided: ✅

---

## 4. Test 3 — Uncovered

### Question

> What is the company's remote work policy?

### Expected Behavior

The assistant should politely state that the information is not available in the uploaded internal documentation and should not provide external or speculative information.

### Actual Result

The assistant responded:

> The available internal documentation does **not contain a remote work policy**. I therefore can’t provide details about remote-work eligibility, schedules, approvals, or requirements without information from the company’s internal documentation.

It provided the following source references:

**Source: Employee Leave Policy — Information Not Covered by This Policy**

**Source: Employee FAQ & Leave Process Guide — Topics Not Covered in This Guide**

### Result

**PASS**

### Validation

- No remote-work policy invented: ✅
- No external information used: ✅
- Refusal was clear and professional: ✅
- Bold source references provided: ✅

---

## 5. Overall Test Summary

| Test | Coverage Scenario | Result |
|---|---|---|
| Test 1 | Fully Covered | **PASS** |
| Test 2 | Partially Covered | **PASS** |
| Test 3 | Uncovered | **PASS** |

### Overall Result

**3/3 Tests Passed**

The Internal Knowledge Assistant successfully demonstrated:

- Strict document-based answering
- Hallucination prevention
- Proper handling of partially covered questions
- Proper refusal of uncovered questions
- Bold source references
- No external knowledge usage

---

## 6. Assessment Conclusion

The tested GPT configuration meets the defined Topic 11 knowledge-grounding requirements for the three required coverage scenarios.