# ADR 0001: Arquitetura MLOps-First

## Status
Aceito

## Contexto
O desenvolvimento isolado em *Jupyter Notebooks* focado apenas em métricas estatísticas frequentemente resulta em classificadores sem utilidade prática hospitalar, um fenômeno conhecido na indústria como falha na transição para produção. Projetos sem uma base sólida de engenharia de dados perdem a rastreabilidade do experimento e exigem reescrita sistêmica quando o volume de dados aumenta.

## Decisão
O projeto será fundamentado na arquitetura **MLOps-First** (*Infrastructure-First Machine Learning*). Antes da redação de código analítico de Ciência de Dados, o ambiente de desenvolvimento deve conter infraestrutura madura de testes automáticos, versionamento estrito (ex: integração com Git e DVC) e definição de contrato da API. Essa abordagem "deslocada para a esquerda" (*Shift-Left MLOps*) exige que questões operacionais sejam sanadas na concepção do projeto.

## Consequências
*   **Positivas:** Reproducibilidade rigorosa, facilidade de auditoria e segurança contra falhas na ingestão de novos lotes do DATASUS.
*   **Negativas:** Requer um investimento de tempo inicial mais alto na configuração de *pipelines* e repositórios antes da obtenção dos primeiros *insights* clínicos do algoritmo.

| Versão | Descrição | Autor(es) | Data | Revisor(es) | Data de Revisão |
|---|---|---|---|---|---|
| 1.0 | Registro inicial de decisão arquitetural MLOps-First | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-18 | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-18 |
