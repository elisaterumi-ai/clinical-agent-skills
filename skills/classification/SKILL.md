---
name: clinical-classification
description: Classifies clinical text into predefined categories such as severity, urgency, or clinical type based on patient information. Use when assigning labels for triage, prioritization, or categorization of medical cases.
---

When classifying clinical text, follow these steps:

## 1. Understand the classification task

- Identify the classification dimension from the context (e.g., severity, urgency, type)  
- Use only the categories provided or implied  

## 2. Extract relevant signals

Identify information that supports classification:

- Symptoms and their severity  
- Clinical findings  
- Diagnoses  
- Risk indicators  
- Temporal aspects (acute vs chronic)  

Only use explicitly stated information.

## 3. Assign a label

Classify the case into one of the predefined categories.

Examples (depending on context):

- Severity: MILD / MODERATE / SEVERE  
- Urgency: LOW / MEDIUM / HIGH  
- Type: ACUTE / CHRONIC  

Do not create new categories.

## 4. Justify the classification

Provide a short rationale based on:

- Key symptoms or findings  
- Clinical indicators present in the text  

Keep justification concise and grounded.

## 5. Handle uncertainty

- If information is insufficient, state uncertainty  
- Do not guess or assume missing data  

## 6. Output format

Return the result as structured text:

```text
Label: ...

Rationale:
- ...
- ...
```

## 7. Constraints
   
- Only use categories defined in the context
- Do not hallucinate clinical information
- Do not infer missing data
- Do not introduce external knowledge
Do not provide medical advice or recommendations
