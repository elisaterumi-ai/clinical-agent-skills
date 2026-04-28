---
name: clinical-coding-icd
description: Maps clinical text to standardized diagnosis codes (e.g., ICD-10) based on explicitly mentioned conditions. Use when extracting or assigning diagnostic codes from medical records, clinical notes, or patient summaries.
---

When mapping clinical text to ICD codes, follow these steps:

## 1. Identify codable conditions

Extract only diagnoses or conditions that are:

- Explicitly stated in the text  
- Clinically meaningful and codable  

Do not infer diagnoses from symptoms alone.

---

## 2. Normalize the diagnosis

- Interpret the clinical term as written  
- Map it to the closest standard diagnostic concept  
- Preserve specificity when possible (e.g., type, location, severity)

---

## 3. Assign ICD code

- Map each diagnosis to the most appropriate ICD code  
- Prefer the most specific code available  
- If specificity is insufficient, use a more general code  

Do not fabricate or guess codes.

---

## 4. Handle multiple diagnoses

- Extract and code each diagnosis independently  
- Avoid duplication  
- Maintain clear mapping between diagnosis and code  

---

## 5. Output format

Return the result as JSON:

```json
{
  "codes": [
    {
      "diagnosis": "...",
      "icd_code": "...",
      "description": "..."
    }
  ]
}
```

## 6. Constraints

- Only code explicitly mentioned diagnoses
- Do not infer diagnoses from symptoms
- Do not hallucinate ICD codes
- If uncertain, prefer a higher-level (less specific) code
- Do not include explanations outside the JSON output
