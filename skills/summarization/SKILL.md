---
name: clinical-summarization
description: Summarizes clinical text into a structured medical summary using formats such as SOAP (Subjective, Objective, Assessment, Plan). Use when condensing patient records, clinical notes, or medical histories into concise, structured summaries.
---

When summarizing clinical text, follow these steps:

## 1. Identify key clinical information

Extract the most relevant information, including:

- Patient complaints and symptoms  
- Clinical findings and observations  
- Diagnoses or clinical impressions  
- Treatments, medications, and procedures  
- Relevant test results  

Focus only on medically relevant content.

## 2. Structure the summary using SOAP format

Organize the output into:

- **Subjective**: Patient-reported symptoms, complaints, history  
- **Objective**: Clinical findings, exam results, vital signs, labs  
- **Assessment**: Diagnoses or clinical interpretation  
- **Plan**: Treatments, medications, follow-ups, next steps  

If a section has no information, include it with an empty or minimal entry.

## 3. Be concise and precise

- Remove redundant or repetitive information  
- Keep clinically important details  
- Use short, clear sentences  

## 4. Preserve clinical meaning

- Do not alter diagnoses or medical facts  
- Do not introduce new information  
- Do not infer beyond what is stated  

## 5. Handle ambiguity carefully

- If information is unclear, reflect uncertainty without guessing  
- Do not assume missing details  

## 6. Output format

Return the summary in structured text:

```text
Subjective:
...

Objective:
...

Assessment:
...

Plan:
...
```

## 7. Constraints

- Do not include explanations
- Do not hallucinate clinical information
- Do not omit critical medical details
