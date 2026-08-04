# Análise Técnica e Dicionário de Variáveis das Bases DATASUS e OpenDataSUS

Este documento consolida a análise estrutural, os dicionários de dados verificados e a avaliação de viabilidade analítica dos conjuntos de dados públicos do Ministério da Saúde para aplicação em Sistemas de Apoio à Decisão Clínica (CDSS). As informações e descrições foram extraídas diretamente dos manuais oficiais do DATASUS, OpenDataSUS e Plataforma de Ciência de Dados aplicada à Saúde (PCDaS/Fiocruz).

## 1. SINAN - Sistema de Informação de Agravos de Notificação (Dengue)

O SINAN reúne os registros de notificação compulsória de casos suspeitos e confirmados de dengue em todo o território nacional.

- **Repositórios Oficiais:**
  - Portal Dados Abertos SUS: https://dadosabertos.saude.gov.br/dataset?tags=dengue
  - Portal de Serviços SINAN: https://sinan.saude.gov.br/
  - Portal SINAN Net: https://portalsinan.saude.gov.br/
- **Nível na Rede de Atenção à Saúde (RAS):** Atenção Primária à Saúde (APS) e Atenção de Urgência/Emergência (UPAs).
- **Viabilidade para CDSS:** Altíssima. Os dados são estruturados por indivíduo notificado, com alto volume anual e variáveis sintomáticas preenchidas no atendimento de triagem.
- **Variável Alvo (Target):**
  - `CLASSI_FIN` (Classificação Final do Caso): Categórica nominal. Valores: 5 (Dengue), 10 (Dengue com sinais de alarme), 11 (Dengue grave), 12 (Chikungunya), 8 (Inconclusivo).
  - `EVOLUCAO` (Evolução do Caso): Categórica nominal. Valores: 1 (Cura), 2 (Óbito por dengue), 3 (Óbito por outras causas), 4 (Óbito em investigação), 9 (Ignorado).
- **Variáveis Preditivas Principais (Features):**
  - `FEBRE`, `MIALGIA`, `CEFALEIA`, `EXAME_LACO`, `NAUSEA`, `VOMITO`, `DOR_ABDO`: Binárias (1 = Sim, 2 = Não).
  - `PLAQUETAS`: Numérica (contagem plaquetária por milímetro cúbico) ou categórica de faixa clínica.
  - `NU_IDADE_N`: Numérica codificada pelo SINAN (ex: quatro dígitos onde o primeiro indica a unidade de medida e os três últimos indicam a quantidade; 4001 a 4120 representa 1 a 120 anos).
  - `CS_SEXO`: Categórica nominal (M = Masculino, F = Feminino, I = Ignorado).

## 2. SIH/SUS - Sistema de Informações Hospitalares

O SIH/SUS armazena os microdados das Autorizações de Internação Hospitalar (AIH), registrando morbidade hospitalar, procedimentos clínicos e custos na rede pública ou conveniada.

- **Repositórios Oficiais:**
  - FTP do DATASUS (Arquivos compactados .DBC): https://datasus.saude.gov.br/transferencia-de-arquivos/
  - Consulta Tabular TABNET: https://datasus.saude.gov.br/informacoes-de-saude-tabnet/
- **Nível na Rede de Atenção à Saúde (RAS):** Atenção Hospitalar de Média e Alta Complexidade.
- **Viabilidade para CDSS:** Alta para modelagem de risco hospitalar (mortalidade ou readmissão em 30 dias), exigindo a biblioteca Python `PySUS` para descompactação dos arquivos `.dbc`.
- **Variável Alvo (Target):**
  - `MOTIVO_SAI` (Motivo da Saída/Desfecho): Categórica nominal. Valores comuns: 11 (Alta melhorado), 12 (Alta curado), 41 (Óbito com declaração de óbito fornecida pelo médico assistente), 42 (Óbito com declaração fornecida pelo IML).
  - *Readmissão em 30 dias:* Variável derivada através da ordenação temporal das AIHs (`DT_INTER`, `DT_SAIDA`) para um mesmo identificador pseudonimizado.
- **Variáveis Preditivas Principais (Features):**
  - `DIAG_PRINC` (Diagnóstico Principal): Categórica alfanumérica baseada na CID-10 (ex: I21 para Infarto Agudo do Miocárdio, J18 para Pneumonia).
  - `DIAG_SECUN` (Diagnóstico Secundário): Categórica alfanumérica (CID-10 de comorbidade associada).
  - `DIAS_PERM` (Dias de Permanência): Numérica inteira (intervalo observável comum: 1 a 365 dias).
  - `IDADE`: Numérica inteira (anos).
  - `US_TOT`: Numérica contínua (valor total da AIH em moeda de referência do sistema).

## 3. SINASC e SIM - Nascidos Vivos e Mortalidade Materno-Infantil

O SINASC registra as Declarações de Nascido Vivo (DNV) e o SIM registra as Declarações de Óbito (DO), permitindo cruzar variáveis gestacionais e desfechos de mortalidade infantil.

- **Repositórios Oficiais (Links Diretos - Portal Dados Abertos SUS):**
  - SINASC (Nascidos Vivos): https://dadosabertos.saude.gov.br/dataset/sistema-de-informacao-sobre-nascidos-vivos-sinasc
  - SIM (Mortalidade): https://dadosabertos.saude.gov.br/dataset/sistema-de-informacao-sobre-mortalidade-sim
  - PCDaS / Fiocruz (Dicionários Curados): https://pcdas.icict.fiocruz.br/
- **Nível na Rede de Atenção à Saúde (RAS):** Atenção Primária (Acompanhamento Pré-Natal) e Atenção Hospitalar (Maternidades).
- **Viabilidade para CDSS:** Muito Alta. É uma das bases mais completas e limpas do DATASUS, ideal para prever risco de asfixia neonatal ou baixo peso extremo ao nascer.
- **Variável Alvo (Target):**
  - `APGAR5` (Escore de Apgar no 5º Minuto): Numérica discreta de 0 a 10. Valores abaixo de 7 indicam asfixia ou vitalidade comprometida, permitindo binarização em risco (< 7) vs normal (>= 7).
  - `PESO`: Numérica contínua (peso ao nascer em gramas). Ponto de corte < 1500g indica muito baixo peso ao nascer.
  - *Óbito Neonatal:* Variável binária derivada do cruzamento de registros com o SIM (Mortalidade).
- **Variáveis Preditivas Principais (Features):**
  - `CONSPRENAT` (Consultas Pré-Natal): Categórica ordinal. Valores: 1 (Nenhuma), 2 (1 a 3 consultas), 3 (4 a 6 consultas), 4 (7 e mais).
  - `GESTACAO` (Semanas Gestacionais): Categórica ordinal. Valores: 1 (< 22 semanas), 2 (22 a 27 semanas), 3 (28 a 31 semanas), 4 (32 a 36 semanas), 5 (37 a 41 semanas), 6 (42 semanas e mais).
  - `GRAVIDEZ`: Categórica nominal (1 = Única, 2 = Dupla, 3 = Tríplice e mais).
  - `PARTO`: Categórica nominal (1 = Vaginal, 2 = Cesáreo).
  - `IDADEMAE`: Numérica contínua (intervalo observável comum: 10 a 55 anos).

## 4. e-SUS APS e SISAB (Atenção Primária à Saúde)

O e-SUS APS é a ferramenta de registro da Estratégia Saúde da Família e Unidades Básicas de Saúde, abarcando históricos longitudinais de hipertensão, diabetes e puericultura.

- **Repositório Oficial:**
  - SISAB - Sistema de Informação em Saúde para a Atenção Básica: https://sisab.saude.gov.br/
- **Nível na Rede de Atenção à Saúde (RAS):** Atenção Primária à Saúde (APS).
- **Viabilidade para CDSS:** Baixa/Média em nível abertos por microdados individuais. O SISAB disponibiliza relatórios agregados (quantitativo de atendimentos por município ou equipe), não permitindo o download direto de microdados por paciente devido à proteção de privacidade civis. O uso deste tema em pesquisa acadêmica exige convênio institucional ou utilização de subamostras desidentificadas secundárias.

| Versão | Descrição | Autor(es) | Data | Revisor(es) | Data de Revisão |
|---|---|---|---|---|---|
| 1.1 | Atualização das URLs com os links canônicos do Portal Dados Abertos SUS (dadosabertos.saude.gov.br) para SINASC e SIM | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-03 | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-08-03 |
