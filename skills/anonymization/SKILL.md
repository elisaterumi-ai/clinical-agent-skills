---
name: clinical-anonymization
description: Anonymizes clinical text by removing or replacing PHI such as names, dates, locations, and identifiers. Use when handling patient data, clinical notes, or any sensitive medical text.
---

When anonymizing clinical text:

1. Identify all personally identifiable information (PHI), including:
   - Names (patients, doctors)
   - Dates
   - Locations
   - Identification numbers
   - Contact details

2. Replace each entity with a consistent placeholder:
   - [PATIENT_1], [DATE_1], [LOCATION_1], [ID_1]

3. Preserve clinical meaning:
   - Do NOT remove symptoms, diagnoses, or treatments
   - Do NOT change medical context

4. Ensure consistency:
   - Same entity → same placeholder

5. Output only the anonymized text.
