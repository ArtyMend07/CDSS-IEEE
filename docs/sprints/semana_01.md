# Relatório de Sprint: Semana 01

**Período de Referência:** 20/07/2026 a 26/07/2026  
**Fase do Projeto:** Concepção Epidemiológica e Estruturação de Repositório

## 1. Objetivos da Semana

A primeira semana de atividades concentrou-se na fundamentação metodológica do Sistema de Apoio à Decisão Clínica (CDSS) aplicado ao Sistema Único de Saúde (SUS), no mapeamento de fontes públicas de dados clínicos e na organização estrutural de controle de versão.

Os compromissos planejados no backlog foram:
- Investigar o embasamento clínico e técnico de um CDSS no contexto da saúde pública brasileira.
- Avaliar bases abertas (OpenDataSUS, SIH/SUS e repositórios científicos) para delimitar subproblemas médicos aplicáveis.
- Inicializar e padronizar o repositório institucional para documentação e futuros pipelines de dados.

## 2. Atividades Executadas e Artefatos de Pesquisa

As tarefas da semana foram executadas e detalhadas nos respectivos documentos técnicos do projeto:

- **Conceituação de CDSS no Brasil:** A fundamentação epidemiológica, restrições éticas (não emissão de diagnóstico determinístico) e formulação de quatro vertentes de investigação médica encontram-se documentadas em [clinical_problem.md](../research/clinical_problem.md).
- **Levantamento de Bases de Dados do SUS:** A compilação dos portais abertos do Ministério da Saúde (SINAN via OpenDataSUS, SIH/SUS via TABNET e pacotes Python como `PySUS`) está detalhada em [datasets_sus.md](../research/datasets_sus.md).
- **Priorização de Requisitos (MoSCoW):** A definição das prioridades metodológicas e científicas do estudo encontra-se em [moscow.md](../requirements/moscow.md).
- **Estruturação do Repositório:** A arquitetura do repositório modular e o plano geral de trabalho estão apresentados no [README.md](../../README.md).

## 3. Conclusão do Ciclo

Todas as metas definidas para a semana inicial foram atingidas, consolidando a base conceitual e infraestrutural para análise dos microdados na semana subsequente.

| Versão | Descrição | Autor(es) | Data | Revisor(es) | Data de Revisão |
|---|---|---|---|---|---|
| 1.1 | Refatoração do relatório da Semana 01 para referenciar artefatos via links relativos | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-03 | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-03 |
