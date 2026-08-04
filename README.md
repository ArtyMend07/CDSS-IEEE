# CDSS-BR: Apoio à Decisão Clínica para o SUS

Este repositório concentra a documentação, propostas de investigação e especificações técnicas de um Sistema de Apoio à Decisão Clínica (CDSS) voltado à triagem e avaliação de risco em agravos de interesse à saúde pública brasileira, utilizando bases de dados secundárias do Sistema Único de Saúde (SUS).

## Objetivos da Investigação

O projeto visa pesquisar, modelar e validar metodologias analíticas capazes de identificar precocemente pacientes com risco atípico ou probabilidade de agravamento clínico em unidades de atendimento. A plataforma atua unicamente como suporte computacional probabilístico e explicável, preservando a autoridade médica e sem emissão de laudos diagnósticos autônomos.

## Estrutura do Repositório

```text
CDSS-IEEE/
├── docs/
│   ├── research/
│   │   ├── datasets_sus.md              # Mapeamento de fontes de dados abertos (OpenDataSUS, SIH/SUS)
│   │   ├── clinical_problem.md          # Levantamento de subproblemas e justificativas epidemiológicas
│   │   ├── matriz_esforco_impacto.md    # Matriz Esforço x Impacto e enquadramento na RAS
│   │   └── analise_tecnica_datasets.md  # Dicionário verificado de variáveis, features e target
│   ├── requirements/
│   │   └── moscow.md                    # Priorização de requisitos da pesquisa e conformidade ética
│   └── sprints/
│       ├── semana_01.md                 # Relatório de atividades e artefatos da Semana 01
│       └── semana_02.md                 # Relatório de atividades e artefatos da Semana 02
└── README.md                            # Apresentação geral do projeto
```

## Diretrizes de Uso dos Dados

A investigação apoia-se exclusivamente em registros administrativos e epidemiológicos desidentificados disponibilizados pelo Ministério da Saúde, respeitando integralmente as normas de privacidade civil e ética em pesquisa médica.

| Versão | Descrição | Autor(es) | Data | Revisor(es) | Data de Revisão |
|---|---|---|---|---|---|
| 1.1 | Atualização da estrutura do repositório incluindo documentação de sprints e análises técnicas | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-03 | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-03 |
