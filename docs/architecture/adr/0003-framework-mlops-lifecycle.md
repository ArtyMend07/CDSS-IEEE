# ADR 0003: Framework MLOps Lifecycle

## Status
Aceito

## Contexto
O processo de construção de soluções analíticas preditivas requer diretrizes formais de execução para evitar retrabalhos. O framework clássico CRISP-DM de 1996 moldou historicamente a mineração estruturada de dados, no entanto, para sustentar ecossistemas de produção ininterrupta, é imperativo o uso de um protocolo alinhado aos padrões da Engenharia Contínua.

## Decisão
Fica adotada a metodologia **MLOps Lifecycle** como protocolo condutor do projeto. A fundamentação empírica permanecerá inspirada nos processos clássicos do CRISP-DM (Entendimento Clínico, Limpeza, Modelagem), sendo que a adoção formal transmutará essas etapas na lógica de Integração Contínua (CI), Treinamento Contínuo (CT), Serventia (Deployment) e Observabilidade de Desvios (Drift Monitoring) na rotina do SUS. 

## Consequências
*   **Positivas:** Permite o alinhamento técnico entre engenheiros e cientistas de dados visando esteiras unificadas sem intervenções repetitivas ou acoplamento.
*   **Negativas:** Incrementa a complexidade teórica global do ciclo, uma vez que a avaliação da eficácia transcende as métricas acadêmicas (F1-score) incorporando exigências sistêmicas como monitoramento de deriva conceitual ao longo dos plantões clínicos.

| Versão | Descrição | Autor(es) | Data | Revisor(es) | Data de Revisão |
|---|---|---|---|---|---|
| 1.0 | Padronização metodológica via MLOps Lifecycle com herança CRISP-DM | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-18 | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-18 |
