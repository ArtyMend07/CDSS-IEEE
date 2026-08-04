# Matriz Esforço x Impacto e Enquadramento na RAS

A escolha do subproblema clínico para o desenvolvimento do Sistema de Apoio à Decisão Clínica (CDSS) no âmbito do Sistema Único de Saúde (SUS) deve ponderar a relevância epidemiológica para a saúde pública (Impacto) e a viabilidade computacional de extração, limpeza e modelagem dos microdados secundários (Esforço).

## 1. Matriz de Avaliação Comparativa

A tabela abaixo compila a classificação das quatro propostas clínicas formuladas para a pesquisa:

| Tema Proposto | Impacto à Saúde Pública | Esforço de Tratamento (ETL) | Nível na RAS | Viabilidade Geral |
|---|---|---|---|---|
| Predição de Agravamento em Dengue | Alto | Médio | Atenção Primária / Urgência | Alta |
| Risco Cardiovascular na APS | Alto | Alto | Atenção Primária à Saúde | Média |
| Readmissão Hospitalar (SIH/SUS) | Alto | Médio-Alto | Média / Alta Complexidade | Alta |
| Risco e Mortalidade Materno-Infantil | Muito Alto | Baixo-Médio | Primária e Hospitalar | Muito Alta |

## 2. Análise de Esforço Computacional e Impacto Clínico

### Predição de Agravamento em Casos de Dengue
- **Impacto (Alto):** A epidemia sazonal de dengue causa superlotação em Unidades de Pronto Atendimento (UPAs). A antecipação de casos que evoluem para hemorragia ou choque viabiliza a alocação imediata em leitos de observação.
- **Esforço (Médio):** A ficha de notificação compulsória do SINAN (OpenDataSUS) é padronizada no país. O esforço técnica restringe-se à limpeza de valores faltantes em variáveis como prova do laço e contagem de plaquetas.

### Estratificação de Risco Cardiovascular na Atenção Primária
- **Impacto (Alto):** As cardiopatias lideram a mortalidade no Brasil. Rastrear descompensações previne internações de urgência.
- **Esforço (Alto):** As bases longitudinais abertas do e-SUS APS são disponibilizadas no portal SISAB primariamente na forma de relatórios agregados por município ou equipe de saúde. A obtenção de microdados abertos em nível de indivíduo exige convênio ou uso de recortes secundários, elevando expressivamente o esforço de engenharia de dados.

### Readmissão Hospitalar na Média e Alta Complexidade
- **Impacto (Alto):** Readmissões hospitalares em menos de trinta dias indicam falhas no planejamento de alta ou infecções hospitalares, onerando os leitos do SUS.
- **Esforço (Médio-Alto):** Os dados públicos de internação do SIH/SUS são compactados no formato proprietário `.dbc`, exigindo o uso da biblioteca `PySUS` para descompactação. A identificação de readmissões depende da ordenação temporal de Autorizações de Internação Hospitalar (AIH) usando identificadores pseudonimizados.

### Vigilância de Risco e Mortalidade Materno-Infantil
- **Impacto (Muito Alto):** Reduzir a mortalidade infantil e materna é um dos compromissos centrais da vigilância em saúde no país.
- **Esforço (Baixo-Médio):** Os sistemas SINASC (Nascidos Vivos) e SIM (Mortalidade) possuem a documentação mais estruturada e os dicionários mais completos do DATASUS, apresentando baixo índice de inconsistência estrutural.

## 3. Enquadramento na Rede de Atenção à Saúde (RAS)

O funcionamento de um CDSS no SUS depende do ponto de atendimento onde a ferramenta preditiva será executada:

- **Atenção Primária à Saúde (APS - Unidades Básicas de Saúde):**
  - *Aplicações:* Triagem inicial de sinais febris em epidemias de Dengue, acompanhamento pré-natal gestacional (SINASC) e rastreamento de hipertensos e diabéticos.
- **Atenção de Urgência e Emergência (UPAs):**
  - *Aplicações:* Classificação de risco em tempo real para tomada de decisão entre hidratação ambulatorial ou transferência para internação em dengue grave.
- **Atenção Hospitalar de Média e Alta Complexidade:**
  - *Aplicações:* Monitoramento de internações e análise preditiva no momento da alta hospitalar (SIH/SUS) para prever o risco de readmissão nas semanas subsequentes.

| Versão | Descrição | Autor(es) | Data | Revisor(es) | Data de Revisão |
|---|---|---|---|---|---|
| 1.0 | Elaboração do documento independente da Matriz Esforço x Impacto e enquadramento na RAS | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-03 | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-03 |
