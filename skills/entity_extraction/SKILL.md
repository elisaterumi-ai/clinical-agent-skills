---
name: clinical-entity-extraction
description: Extracts structured clinical entities such as diseases, symptoms, medications, procedures, and lab results from clinical text. Use when analyzing medical notes, patient records, or extracting structured information from unstructured healthcare data.
---

When extracting clinical entities, follow these steps:

## 1. Identify relevant entities

Extract clinically meaningful entities, including:

- Diseases and diagnoses  
- Symptoms and signs  
- Medications (including dosage if available)  
- Procedures and treatments  
- Laboratory tests and results  

Only extract entities that are explicitly mentioned in the text.

Do not infer or hallucinate information.

## 2. Classify each entity

Assign each entity one of the following types:

- DISEASE  
- SYMPTOM  
- MEDICATION  
- PROCEDURE  
- LAB_RESULT  

If an entity does not clearly belong to one of these categories, do not include it.

## 3. Preserve original text spans

- Extract entities exactly as they appear in the text  
- Do not normalize, translate, or modify wording  
- Maintain original casing and phrasing  

## 4. Avoid duplication

- If the same entity appears multiple times, extract it once  
- Preserve distinct entities separately  

## 5. Output format

Return the result as a JSON object:

```json
{
  "entities": [
    {
      "text": "...",
      "type": "..."
    }
  ]
}
```
 
## 6. Constraints

- Do not include explanations  
- Do not include entities outside the defined categories  
- Do not infer missing clinical information  
