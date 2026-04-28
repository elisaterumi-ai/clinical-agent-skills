---
name: clinical-risk-prediction
description: Assesses patient risk level (e.g., low, medium, high) based on clinical information such as symptoms, history, and findings. Use when evaluating potential severity, complications, or need for prioritization in clinical contexts.
---

When assessing clinical risk, follow these steps:

## 1. Extract relevant risk factors

Identify information that may influence risk, including:

- Symptoms (severity, duration)
- Vital signs and clinical findings
- Medical history (e.g., chronic conditions)
- Age or vulnerability indicators
- Laboratory or exam results

Only use explicitly stated information.

## 2. Identify risk indicators

Determine whether the case includes signs of:

- Clinical deterioration
- Severity or acute conditions
- Comorbidities that increase risk
- Abnormal findings or critical values

Do not assume missing data.

## 3. Assign risk level

Classify the case into one of the following:

- LOW  
- MODERATE  
- HIGH  

Base the classification strictly on the available information.

## 4. Justify the classification

Provide a brief explanation including:

- Key risk factors identified  
- Why they increase or decrease risk  

Keep justification concise and grounded in the input.

## 5. Express uncertainty

- If information is incomplete, state uncertainty  
- Avoid overconfidence  

## 6. Output format

Return the result as structured text:

```text
Risk Level: HIGH

Rationale:
- ...
- ...
```

## 7. Constraints

- This is assistive risk assessment, not a medical diagnosis
- Do not provide treatment recommendations
- Do not hallucinate clinical information
- Do not infer missing data
- Do not express certainty beyond the available evidence
