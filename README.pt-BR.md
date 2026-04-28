🌍 Language:
[English](README.md) | [Português](README.pt-BR.md) | [Español](README.es.md)

# Clinical Agent Skills

![Clinical AI Skills](./assets/clinical-ai-skills.png)

Uma coleção curada de **skills reutilizáveis para agentes de IA aplicados à área clínica e da saúde**.

Este repositório fornece blocos modulares projetados para suportar fluxos de trabalho clínicos reais utilizando Large Language Models (LLMs), combinados com lógica estruturada, validação e conhecimento específico do domínio.

Em vez de prompts isolados, cada skill é projetada como uma **unidade confiável e composável de comportamento** — permitindo a criação de agentes clínicos robustos.

## O que você encontrará aqui

- **[Anonimização Clínica](./skills/anonymization/)**  
  Remove informações sensíveis do paciente (PHI) preservando a utilidade dos dados.

- **[Extração de Entidades (NER Clínico)](./skills/entity_extraction/)**  
  Identifica doenças, medicamentos, sintomas e procedimentos em texto não estruturado.

- **[Sumarização Clínica](./skills/summarization/)**  
  Transforma notas clínicas extensas em resumos estruturados (ex: formato SOAP).

- **[Suporte Diagnóstico (Assistivo)](./skills/diagnostic_support/)**  
  Sugere possíveis hipóteses diagnósticas com base nos dados do paciente *(uso assistivo, não determinístico)*.

- **[Codificação Clínica (ICD/CID)](./skills/coding_icd/)**  
  Mapeia texto clínico para códigos médicos padronizados.

- **[Predição de Risco](./skills/risk_prediction/)**  
  Avalia níveis de risco do paciente com base em dados clínicos.

- **[Perguntas e Respostas Clínicas](./skills/clinical_qa/)**  
  Responde perguntas com base em prontuários e registros clínicos.

- **[Extração de Linha do Tempo](./skills/timeline_extraction/)**  
  Reconstrói o histórico do paciente em ordem cronológica.

- **[Geração de Relatórios](./skills/report_generation/)**  
  Gera relatórios clínicos estruturados.

- **[Estruturação de Dados](./skills/data_structuring/)**  
  Converte notas clínicas em JSON estruturado.

- **[Classificação Clínica](./skills/classification/)**  
  Classifica casos clínicos por severidade, urgência ou tipo.

## 🧠 O que é uma "Skill"?

Uma **skill** é mais do que um prompt.

É um **módulo reutilizável orientado a tarefas** que pode incluir:

- Instruções para LLM  
- Pré-processamento e pós-processamento  
- Regras de validação  
- Saídas estruturadas (ex: JSON)  
- Integração opcional com ontologias médicas (ex: ICD, SNOMED)

Cada skill é projetada para ser:

- ✔️ Reutilizável  
- ✔️ Componível  
- ✔️ Testável  

Se quiser se aprofundar no conceito de skills para agentes de IA, veja este repositório:

👉 https://github.com/elisaterumi-ai/agent-skills-in-practice

## Princípios de Design

- Confiabilidade acima de geração livre  
- Saídas estruturadas em vez de texto livre  
- IA assistiva, não diagnóstico autônomo  
- Privacidade em primeiro lugar (LGPD/HIPAA)  
- Desenvolvimento orientado por avaliação  

## Estrutura do Repositório

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

Este repositório é destinado **exclusivamente para pesquisa e desenvolvimento**.

As skills aqui fornecidas são **ferramentas assistivas** e não devem ser utilizadas como substitutas de julgamento, diagnóstico ou tratamento médico profissional.

## Visão

Construir uma base prática para **agentes clínicos seguros, modulares e alinhados com necessidades reais da saúde** — reduzindo a distância entre demos experimentais com LLMs e sistemas médicos prontos para produção.

## 🤝 Contribuindo

Contribuições são bem-vindas!

Você pode:
- Adicionar novas skills clínicas  
- Melhorar prompts e pipelines  
- Contribuir com datasets de avaliação  
- Sugerir métricas e benchmarks  

## 🔗 Conecte-se comigo

Compartilho conteúdos práticos sobre IA, agentes e aplicações reais:

- LinkedIn (Perfil): https://www.linkedin.com/in/elisa-terumi  
- LinkedIn (Página): https://www.linkedin.com/company/exploring-artificial-intelligence  
- Newsletter: https://exploringartificialintelligence.substack.com/  
- Medium: https://medium.com/@elisa-terumi  

## ⭐ Histórico de Stars

<a href="https://www.star-history.com/?repos=elisaterumi-ai%2Fagent-skills-in-practice&type=date&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/chart?repos=elisaterumi-ai/agent-skills-in-practice&type=date&theme=dark&legend=top-left" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/chart?repos=elisaterumi-ai/agent-skills-in-practice&type=date&legend=top-left" />
   <img alt="Star History Chart" src="https://api.star-history.com/chart?repos=elisaterumi-ai/agent-skills-in-practice&type=date&legend=top-left" />
 </picture>
</a>
