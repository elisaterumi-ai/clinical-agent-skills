---
name: diagnostic-support
description: Generates possible diagnostic hypotheses based on clinical text, including symptoms, findings, and test results. Use when analyzing patient data to assist clinical reasoning and suggest differential diagnoses.
---

When generating diagnostic hypotheses, follow these steps:

## 1. Extract relevant clinical information

Identify key elements from the input:

- Symptoms and complaints  
- Clinical signs and findings  
- Medical history  
- Laboratory and exam results  

Only use explicitly stated information.

## 2. Generate differential diagnoses

- Propose a list of possible diagnoses based on the available data  
- Include multiple hypotheses when appropriate  
- Consider common and plausible conditions  

Do not assume missing information.

## 3. Justify each hypothesis

For each suggested diagnosis, provide a brief justification based on:

- Symptoms  
- Findings  
- Clinical context  

Keep justifications concise and grounded in the input.

## 4. Rank by likelihood

- Order hypotheses from most to least likely  
- Base ranking only on the provided information  

Do not overstate certainty.

## 5. Express uncertainty clearly

- Use cautious language (e.g., “possible”, “suggestive of”)  
- Do not present any diagnosis as definitive  

## 6. Output format

Return the result as structured text:

```text
Possible Diagnoses:

1. Diagnosis name  
   - Justification: ...

2. Diagnosis name  
   - Justification: ...
```

## 7. Constraints

- This is assistive support, not a medical diagnosis
- Do not provide treatment recommendations
- Do not hallucinate clinical data
- Do not infer information not present in the input
- Do not express certainty beyond the available evidence
