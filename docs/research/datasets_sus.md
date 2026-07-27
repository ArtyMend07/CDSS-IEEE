# Bases de Dados Públicas em Saúde no Brasil

A pesquisa em sistemas de apoio à decisão clínica no contexto brasileiro depende da utilização de bases secundárias mantidas pelo Ministério da Saúde. O Sistema Único de Saúde disponibiliza dados epidemiológicos e assistenciais que permitem investigar padrões clínicos, embora apresentem desafios inerentes aos registros administrativos, como subnotificação e assincronia de preenchimento.

## 1. OpenDataSUS
O portal OpenDataSUS é o repositório oficial de dados abertos de saúde pública do governo federal, agregando registros anonimizados de vigilância epidemiológica e imunização.
- Link de acesso: https://opendatasus.saude.gov.br/
- Principais recortes: Notificações de agravos de notificação compulsória oriundas do SINAN (como dengue, zika, chikungunya e malária), além dos registros de Síndrome Respiratória Aguda Grave (SRAG).
- Estrutura dos dados: Arquivos em formato tabular aberto (.csv ou .parquet), estruturados por notificações individuais anonimizadas com variáveis demográficas, sinais e sintomas clínicos e evolução do caso.

## 2. Sistema de Informações Hospitalares (SIH/SUS) e TABNET
O SIH/SUS armazena os dados de internações hospitalares financiadas pelo sistema público através das Autorizações de Internação Hospitalar (AIH). Permite avaliar o perfil de morbidade hospitalar, tempo de permanência, procedimentos clínicos executados e desfechos de internação.
- Transferência de arquivos brutos: https://datasus.saude.gov.br/transferencia-de-arquivos/
- Consulta tabular (TABNET): https://datasus.saude.gov.br/informacoes-de-saude-tabnet/
- Características técnicas: Os microdados são compactados no padrão .dbc, exigindo a biblioteca PySUS para decodificação e estruturação em tabelas analíticas. É fundamental considerar que o SIH foi concebido com propósitos financeiros e administrativos, havendo necessidade de tratamento estatístico rigoroso para uso clínico.

## 3. Repositórios Secundários e Pesquisa Reproduzível
Diversos grupos de pesquisa e universidades brasileiras publicam recortes curados e pré-processados de bases do DATASUS no Kaggle, visando facilitar a reprodutibilidade científica.
- Busca geral de dados do SUS: https://www.kaggle.com/search?q=SUS+Brazil
- Recortes do OpenDataSUS: https://www.kaggle.com/search?q=OpenDataSUS

A escolha da base analítica para modelagem preditiva deve alinhar a disponibilidade de variáveis clínicas com a relevância epidemiológica do agravo estudado.

| Versão | Descrição | Autor(es) | Data | Revisor(es) | Data de Revisão |
|---|---|---|---|---|---|
| 1.0 | Revisão e aprofundamento sobre bases epidemiológicas do SUS | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-07-27 | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-07-27 |
