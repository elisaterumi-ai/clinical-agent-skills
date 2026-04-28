---
name: clinical-data-structuring
description: Converts unstructured clinical text into structured JSON by extracting key medical information such as symptoms, diagnoses, medications, procedures, and temporal data. Use when transforming clinical notes into machine-readable format.
---

When structuring clinical data, follow these steps:

## 1. Extract key information

Identify and extract relevant clinical elements:

- Symptoms and complaints  
- Diagnoses or conditions  
- Medications (include dosage if available)  
- Procedures and treatments  
- Laboratory results  
- Temporal information (dates, durations, sequence of events)  

Only extract explicitly mentioned information.

## 2. Organize into structured fields

Group extracted information into the following categories:

- `symptoms`  
- `diagnoses`  
- `medications`  
- `procedures`  
- `lab_results`  
- `timeline`  

If a category has no data, return an empty list.

## 3. Preserve original text

- Keep extracted values as they appear in the input  
- Do not normalize or translate  
- Do not modify wording  

## 4. Avoid duplication

- Do not repeat the same entity multiple times  
- Keep distinct entries separate  

## 5. Handle temporal data

- Represent events with associated time when available  
- If time is missing, include `"time": "unknown"`  

## 6. Output format

Return the result as JSON:

```json
{
  "symptoms": [],
  "diagnoses": [],
  "medications": [],
  "procedures": [],
  "lab_results": [],
  "timeline": [
    {
      "time": "...",
      "event": "..."
    }
  ]
}
```

## 7. Constraints

- Do not hallucinate information
- Do not infer missing data
- Only include explicitly stated clinical information
- Keep output strictly in JSON format
- Do not include explanations
