# Priorização de Requisitos da Pesquisa (Matriz MoSCoW)

A aplicação da matriz MoSCoW para a investigação científica em apoio à decisão clínica visa orientar as prioridades de modelagem estatística, relevância epidemiológica e rigor metodológico do projeto, delimitando o escopo acadêmico da pesquisa.

## Must Have (Requisitos Essenciais)
Itens indispensáveis para a fundamentação científica e validade clínica do modelo:
- Utilização de bases públicas nacionais: Os modelos devem ser estruturados e avaliados com dados do ecossistema de saúde brasileiro, originados do OpenDataSUS, SIH/SUS ou repositórios correlatos.
- Explicabilidade analítica (XAI): O modelo deve explicitar quais variáveis clínicas e epidemiológicas impulsionaram o escore de risco calculado, descartando arquiteturas que operem de forma opaca.
- Mensuração de incerteza clínica: Os resultados preditivos devem apresentar intervalo de confiança ou métrica de probabilidade, informando o grau de certeza matemática da previsão.
- Conformidade ética e privacidade: Tratamento de dados secundários desidentificados em respeito às normas civis de proteção de dados e ética em pesquisa médica.

## Should Have (Requisitos Importantes)
Itens que elevam a qualidade metodológica e a completude do estudo:
- Curadoria sistemática de dados: Estabelecimento de rotinas para tratamento de inconsistências, imputação de dados ausentes e padronização de variáveis de registros administrativos da saúde.
- Comparação entre modelos de aprendizado: Avaliação do desempenho preditivo contrastando modelos tradicionais de regressão com algoritmos baseados em árvores ou redes neurais.
- Análise exploratória epidemiológica: Mapeamento estatístico da distribuição dos casos, faixas etárias mais acometidas e prevalência de comorbidades na amostra investigada.

## Could Have (Requisitos Desejáveis)
Extensões analíticas a serem conduzidas caso as etapas primárias sejam concluídas antecipadamente:
- Incorporação de determinantes contextuais: Cruzamento das variáveis clínicas centrais com dados climáticos ou indicadores socioeconômicos regionais para avaliar impacto na precisão preditiva.
- Avaliação de interpretabilidade: Condução de ensaios preliminares com estudantes ou profissionais de saúde para medir a clareza dos alertas preditivos emitidos pelo modelo.

## Won't Have (Fora do Escopo Atual)
Limites metodológicos definidos para a etapa corrente da pesquisa:
- Emissão de diagnóstico automatizado: O modelo não se propõe a fechar laudos clínicos absolutos nem substituir a avaliação do médico assistente.
- Prescrição farmacológica autônoma: Nenhuma recomendação de conduta terapêutica ou medicamentosa será realizada pelo modelo preditivo.
- Intervenção hospitalar em tempo real: O escopo atual compreende a validação computacional em bases de dados retrospectivas, não abrangendo ensaios clínicos intervencionais em unidades do SUS.

| Versão | Descrição | Autor(es) | Data | Revisor(es) | Data de Revisão |
|---|---|---|---|---|---|
| 1.0 | Adequação da matriz MoSCoW para requisitos científicos e clínicos | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-07-27 | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-07-27 |
