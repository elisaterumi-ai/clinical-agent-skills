---
name: clinical-timeline-extraction
description: Extracts and organizes clinical events into a chronological timeline based on patient records or medical notes. Use when reconstructing the sequence of symptoms, diagnoses, treatments, or hospital events.
---

When extracting a clinical timeline, follow these steps:

## 1. Identify temporal information

Detect all time-related expressions, including:

- Dates (e.g., 12/03/2023)  
- Relative time (e.g., "2 days ago", "last week")  
- Event order (e.g., "after admission", "prior to surgery")  

## 2. Extract clinical events

Identify relevant events such as:

- Symptom onset  
- Medical visits or admissions  
- Diagnoses  
- Treatments or procedures  
- Medication changes  
- Test results  

Only include explicitly mentioned events.


## 3. Link events to time

- Associate each event with its corresponding time reference  
- If no explicit time is given, mark as `"time": "unknown"`  

Do not infer missing temporal information.

---

## 4. Normalize order

- Arrange events in chronological order  
- Use relative ordering if exact dates are not available  

## 5. Preserve original meaning

- Keep event descriptions close to the original text  
- Do not rewrite or interpret beyond what is stated  

## 6. Output format

Return the result as JSON:

```json
{
  "timeline": [
    {
      "time": "...",
      "event": "..."
    }
  ]
}
```

## 7. Constraints
   
- Only include events present in the text
- Do not hallucinate dates or events
- Do not infer temporal relationships not explicitly stated
- Do not modify clinical meaning
Keep event descriptions concise and factual
