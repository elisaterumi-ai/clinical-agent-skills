🌍 Language:
[English](README.md) | [Português](README.pt-BR.md) | [Español](README.es.md)

# Clinical Agent Skills

![Clinical AI Skills](./assets/clinical-ai-skills.png)

Una colección curada de **skills reutilizables para agentes de IA aplicados al ámbito clínico y de la salud**.

Este repositorio proporciona bloques modulares diseñados para soportar flujos de trabajo clínicos reales utilizando Large Language Models (LLMs), combinados con lógica estructurada, validación y conocimiento específico del dominio.

En lugar de prompts aislados, cada skill está diseñada como una **unidad confiable y componible de comportamiento**, permitiendo la creación de agentes clínicos robustos.

## Qué encontrarás aquí

- **[Anonimización Clínica](./skills/anonymization/)**  
  Elimina información sensible del paciente (PHI) preservando la utilidad de los datos.

- **[Extracción de Entidades (NER Clínico)](./skills/entity_extraction/)**  
  Identifica enfermedades, medicamentos, síntomas y procedimientos en texto no estructurado.

- **[Sumarización Clínica](./skills/summarization/)**  
  Transforma notas clínicas extensas en resúmenes estructurados (por ejemplo, formato SOAP).

- **[Soporte Diagnóstico (Asistivo)](./skills/diagnostic_support/)**  
  Sugiere posibles hipótesis diagnósticas basadas en los datos del paciente *(uso asistivo, no determinístico)*.

- **[Codificación Clínica (ICD/CID)](./skills/coding_icd/)**  
  Mapea texto clínico a códigos médicos estandarizados.

- **[Predicción de Riesgo](./skills/risk_prediction/)**  
  Evalúa el nivel de riesgo del paciente basado en datos clínicos.

- **[Preguntas y Respuestas Clínicas](./skills/clinical_qa/)**  
  Responde preguntas basadas en registros clínicos.

- **[Extracción de Línea de Tiempo](./skills/timeline_extraction/)**  
  Reconstruye el historial del paciente en orden cronológico.

- **[Generación de Reportes](./skills/report_generation/)**  
  Genera informes clínicos estructurados.

- **[Estructuración de Datos](./skills/data_structuring/)**  
  Convierte notas clínicas en JSON estructurado.

- **[Clasificación Clínica](./skills/classification/)**  
  Clasifica casos clínicos según severidad, urgencia o tipo.

## 🧠 ¿Qué es una "Skill"?

Una **skill** es más que un prompt.

Es un **módulo reutilizable orientado a tareas** que puede incluir:

- Instrucciones para LLM  
- Preprocesamiento y posprocesamiento  
- Reglas de validación  
- Salidas estructuradas (por ejemplo, JSON)  
- Integración opcional con ontologías médicas (como ICD o SNOMED)

Cada skill está diseñada para ser:

- ✔️ Reutilizable  
- ✔️ Componible  
- ✔️ Testeable  

Si deseas profundizar en el concepto de skills para agentes de IA, consulta este repositorio:

👉 https://github.com/elisaterumi-ai/agent-skills-in-practice

## Principios de Diseño

- Confiabilidad por encima de la generación libre  
- Salidas estructuradas en lugar de texto libre  
- IA asistiva, no diagnóstico autónomo  
- Privacidad primero (LGPD/HIPAA)  
- Desarrollo guiado por evaluación  


## Estructura del Repositorio

```
/skills
  /anonymization
  /entity_extraction
  /summarization
  /diagnostic_support
  /coding_icd
  /risk_prediction
  /clinical_qa
  /timeline_extraction
  /report_generation
  /data_structuring
  /classification
```

## Aviso

Este repositorio está destinado **únicamente a investigación y desarrollo**.

Las skills proporcionadas son **herramientas asistivas** y no deben utilizarse como sustituto del juicio, diagnóstico o tratamiento médico profesional.

## Visión

Construir una base práctica para **agentes clínicos seguros, modulares y alineados con las necesidades reales del sector salud**, reduciendo la brecha entre demos experimentales con LLMs y sistemas médicos listos para producción.

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas!

Puedes:
- Añadir nuevas skills clínicas  
- Mejorar prompts y pipelines  
- Contribuir con datasets de evaluación  
- Sugerir métricas y benchmarks  

## 🔗 Conecta conmigo

Comparto contenidos prácticos sobre IA, agentes y aplicaciones reales:

- LinkedIn (Perfil): https://www.linkedin.com/in/elisa-terumi  
- LinkedIn (Página): https://www.linkedin.com/company/exploring-artificial-intelligence  
- Newsletter: https://exploringartificialintelligence.substack.com/  
- Medium: https://medium.com/@elisa-terumi  

## ⭐ Historial de Stars

<a href="https://www.star-history.com/?repos=elisaterumi-ai%2Fagent-skills-in-practice&type=date&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/chart?repos=elisaterumi-ai/agent-skills-in-practice&type=date&theme=dark&legend=top-left" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/chart?repos=elisaterumi-ai/agent-skills-in-practice&type=date&legend=top-left" />
   <img alt="Star History Chart" src="https://api.star-history.com/chart?repos=elisaterumi-ai/agent-skills-in-practice&type=date&legend=top-left" />
 </picture>
</a>
