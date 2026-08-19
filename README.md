# CDSS-BR: Apoio à Decisão Clínica para o SUS

Este repositório concentra a documentação, propostas de investigação e especificações técnicas de um Sistema de Apoio à Decisão Clínica (CDSS) voltado à triagem e avaliação de risco em agravos de interesse à saúde pública brasileira, utilizando bases de dados secundárias do Sistema Único de Saúde (SUS).

## Objetivos da Investigação

O projeto visa pesquisar, modelar e validar metodologias analíticas capazes de identificar precocemente pacientes com risco atípico ou probabilidade de agravamento clínico em unidades de atendimento. A plataforma atua unicamente como suporte computacional probabilístico e explicável, preservando a autoridade médica e sem emissão de laudos diagnósticos autônomos.

## Estrutura do Repositório

```mermaid
graph LR
    A[CDSS-IEEE] --> B[docs]
    A --> C[README.md]
    B --> D[arch/adr]
    B --> E[research]
    B --> F[requirements]
    B --> G[sprints]
    
    D --> D1["0001-arquitetura-mlops-first.md"]
    D --> D2["0002-versionamento-semantico-modelos.md"]
    D --> D3["0003-framework-mlops-lifecycle.md"]
    
    E --> E1["datasets_sus.md"]
    E --> E2["clinical_problem.md"]
    E --> E3["matriz_esforco_impacto.md"]
    E --> E4["analise_tecnica_datasets.md"]
    
    F --> F1["moscow.md"]
    
    G --> G1["semana_01.md"]
    G --> G2["semana_02.md"]
    G --> G3["semana_03.md"]
```

## Diretrizes de Uso dos Dados

A investigação apoia-se exclusivamente em registros administrativos e epidemiológicos desidentificados disponibilizados pelo Ministério da Saúde, respeitando integralmente as normas de privacidade civil e ética em pesquisa médica.

| Versão | Descrição | Autor(es) | Data | Revisor(es) | Data de Revisão |
|---|---|---|---|---|---|
| 1.1 | Atualização da estrutura do repositório incluindo documentação de sprints e análises técnicas | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-03 | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-03 |
| 1.2 | Refatoração estrutural da apresentação visual (Mermaid.js) e adição de governança de ADRs MLOps | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-18 | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-18 |
