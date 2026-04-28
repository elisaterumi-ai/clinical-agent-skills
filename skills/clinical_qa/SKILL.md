---
name: clinical-question-answering
description: Answers questions based strictly on clinical text, such as patient records or medical notes. Use when extracting specific information from clinical documents in a reliable and grounded manner.
---

When answering clinical questions, follow these steps:

## 1. Understand the question

- Identify what information is being asked  
- Determine the type of answer (e.g., symptom, medication, date, diagnosis)

---

## 2. Locate relevant information

- Search the input text for evidence that directly answers the question  
- Use only explicitly stated information  

Do not infer or assume missing details.

---

## 3. Provide a grounded answer

- Answer concisely using information from the text  
- Use exact wording when possible  
- If needed, paraphrase minimally without changing meaning  

---

## 4. Handle missing information

If the answer is not present in the text:

- Respond with:  
  **"Not available in the provided text."**

Do not guess or hallucinate.

---

## 5. (Optional) Provide supporting evidence

If appropriate, include a short excerpt from the text that supports the answer.

---

## 6. Output format

Return the result as structured text:

```text
Answer: ...

Evidence: ...
```

If no evidence is available:

Answer: Not available in the provided text.

## 7. Constraints
 
- Only use information present in the input text
- Do not hallucinate or infer missing data
- Do not introduce external knowledge
- Do not provide medical advice or recommendations
- Keep answers concise and factual
