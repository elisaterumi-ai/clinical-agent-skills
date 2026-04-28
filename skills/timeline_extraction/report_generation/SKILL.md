---
name: clinical-report-generation
description: Generates structured clinical reports (e.g., discharge summaries, medical reports, or clinical notes) based on patient data. Use when transforming clinical information into clear, standardized medical documentation.
---

When generating a clinical report, follow these steps:

## 1. Extract relevant information

Identify key elements from the input:

- Patient context (if available)  
- Symptoms and complaints  
- Clinical findings and observations  
- Diagnoses or impressions  
- Treatments, medications, and procedures  
- Test results  

Use only explicitly stated information.

## 2. Organize the report

Structure the report into clear sections:

- **Patient Summary**  
- **Clinical Findings**  
- **Assessment**  
- **Plan / Recommendations**  

If a section has no information, include it with minimal content.

## 3. Use clear clinical language

- Write in a professional and concise medical style  
- Avoid redundancy  
- Maintain clarity and readability  

## 4. Preserve accuracy

- Do not alter clinical meaning  
- Do not introduce new information  
- Do not infer missing details  

## 5. Maintain coherence

- Ensure logical flow between sections  
- Keep consistency in terminology  
- Avoid contradictions  

## 6. Output format

Return the report as structured text:

```text
Patient Summary:
...

Clinical Findings:
...

Assessment:
...

Plan / Recommendations:
...
```

## 7. Constraints
   
- Do not hallucinate clinical information
- Do not infer missing data
- Do not provide medical advice beyond what is stated
- Keep the report concise and structured
