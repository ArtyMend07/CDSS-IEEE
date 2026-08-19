# ADR 0002: Versionamento Semântico para Modelos (SemVer)

## Status
Aceito

## Contexto
Diferente da Engenharia de Software convencional, sistemas de Inteligência Artificial dependem de três pilares flutuantes: código, dados e hiperparâmetros. Sem um controle metodológico das versões empacotadas do modelo preditivo, é impossível investigar falhas de desempenho (*drift*) ou garantir a recuperação do estado exato da ferramenta de apoio à decisão clínica.

## Decisão
Aplicar-se-á o controle formal do **Semantic Versioning (SemVer)** adaptado para todo artefato preditivo:
*   **`MAJOR` (X.0.0):** Atualizado em caso de mudanças drásticas (quebra de contrato de API), como a alteração do algoritmo primário ou mudança nos campos exigidos na triagem hospitalar.
*   **`MINOR` (x.Y.0):** Atualizado quando o classificador é **retreinado** com uma nova massa de dados (ex: nova carga de Declarações de Nascido Vivo), mantendo o desempenho anterior retrocompatível.
*   **`PATCH` (x.y.Z):** Atualizado para mitigar vulnerabilidades no código de inferência e de pré-processamento que não afetam a lógica matemática intrínseca do preditor.

## Consequências
*   **Positivas:** Viabiliza o registro limpo da linhagem do modelo, informando aos desenvolvedores clínicos se uma atualização afetará a integração via API.
*   **Negativas:** Exige aderência rigorosa a plataformas de controle, como MLflow ou painéis dedicados, inibindo experimentos isolados não documentados.

| Versão | Descrição | Autor(es) | Data | Revisor(es) | Data de Revisão |
|---|---|---|---|---|---|
| 1.0 | Adoção de Versionamento Semântico para ML | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-18 | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-18 |
