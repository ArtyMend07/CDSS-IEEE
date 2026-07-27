# CDSS-BR: Apoio à Decisão Clínica para o SUS

Este repositório concentra a documentação, propostas de investigação e especificações técnicas de um Sistema de Apoio à Decisão Clínica (CDSS) voltado à triagem e avaliação de risco em agravos de interesse à saúde pública brasileira, utilizando bases de dados secundárias do Sistema Único de Saúde (SUS).

## Objetivos da Investigação

O projeto visa pesquisar, modelar e validar metodologias analíticas capazes de identificar precocemente pacientes com risco atípico ou probabilidade de agravamento clínico em unidades de atendimento. A plataforma atua unicamente como suporte computacional probabilístico e explicável, preservando a autoridade médica e sem emissão de laudos diagnósticos autônomos.

## Estrutura do Repositório

```text
CDSS-IEEE/
├── docs/
│   ├── research/
│   │   ├── datasets_sus.md         # Mapeamento de fontes de dados abertos 
│   │   └── clinical_problem.md     # Levantamento de subproblemas e justificativas epidemiológicas
│   └── requirements/
│       └── moscow.md               # Priorização de requisitos da pesquisa e conformidade ética
└── README.md                       # Apresentação geral do projeto
```

## Diretrizes de Uso dos Dados

A investigação apoia-se exclusivamente em registros administrativos e epidemiológicos desidentificados disponibilizados pelo Ministério da Saúde, com o intuito de respeitar as normas de privacidade civil e ética em pesquisa médica (seguindo LGPD).

| Versão | Descrição | Autor(es) | Data | Revisor(es) | Data de Revisão |
|---|---|---|---|---|---|
| 1.0 | Elaboração inicial da apresentação do repositório | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-07-27 | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-07-27 |
