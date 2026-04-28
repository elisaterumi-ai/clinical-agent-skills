---
name: clinical-anonymization
description: Anonymizes clinical text by removing or replacing personally identifiable information (PHI/PII) such as names, dates, locations, identifiers, and contact details. Use when processing clinical notes, patient records, or any sensitive healthcare data.
---

When anonymizing clinical text, follow these steps:

## 1. Identify sensitive information

Detect and classify all Personally Identifiable Information (PII/PHI), including:

- Names (patients, doctors, relatives)
- Dates (birth, admission, discharge, events)
- Locations (cities, hospitals, addresses)
- Identification numbers (CPF, RG, SSN, medical record numbers)
- Contact information (phone numbers, emails)
- Organization names (clinics, hospitals, employers)
- Geographic details smaller than a state level
- Any unique identifiers that can re-identify a person

## 2. Apply anonymization

Replace each entity with a consistent placeholder:

- [PATIENT_1], [DOCTOR_1]
- [DATE_1]
- [LOCATION_1]
- [ID_1]
- [CONTACT_1]
- [ORG_1]

Rules:

- Maintain consistency: the same entity must always map to the same placeholder
- Do not invent or infer missing data
- Do not remove clinical meaning
- Use consistent indexed placeholders per entity type. If multiple entities of the same type exist, assign incremental IDs (e.g., [PATIENT_1], [PATIENT_2]).

## 3. Preserve clinical utility

- Keep all medical information intact:
  - symptoms
  - diagnoses
  - medications
  - procedures
- Maintain sentence structure and readability
- Avoid over-anonymization that removes useful context

## 4. Generalization (when needed)

If exact anonymization is not possible, generalize:

- Exact age → age range (e.g., "84 years" → "80+ years")
- Specific date → month/year or relative time ("March 2023" → "[DATE_1]")
- Precise location → broader region

## 5. Validate output

Before returning the result:

- Ensure no PII/PHI remains
- Ensure consistency of placeholders
- Ensure medical meaning is preserved

## 6. Output format

Return only the anonymized text.

Do not include explanations.
Do not include metadata unless explicitly requested.
