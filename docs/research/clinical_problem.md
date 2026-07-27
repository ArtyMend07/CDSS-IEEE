# Sistemas de Apoio à Decisão Clínica e Propostas de Investigação Médica

Os Sistemas de Apoio à Decisão Clínica (CDSS) atuam como ferramentas analíticas destinadas a auxiliar a equipe de saúde na avaliação de riscos, triagem e conduta terapêutica. No âmbito do Sistema Único de Saúde, sua aplicação principal reside na estratificação precoce de pacientes com risco atípico ou agravamento clínico, permitindo otimizar fluxos de atendimento em um cenário de demanda assistencial elevada. O modelo analítico opera como suporte probabilístico, mantendo a responsabilidade diagnóstica sob encargo exclusivo do corpo clínico.

## Diretrizes de Aplicação Clínica

Para o desenvolvimento de um projeto científico voltado ao SUS, é viável explorar diferentes patologias epidemiologicamente relevantes cujos dados estejam publicamente disponíveis no DATASUS ou OpenDataSUS. A seguir são descritas sugestões temáticas com aderência técnica e relevância para a saúde pública brasileira.

### Predição de Agravamento em Casos de Dengue
As epidemias sazonais de dengue representam um dos maiores desafios de triagem na atenção de urgência. A maioria dos pacientes cursa com sinais clássicos benignos, mas uma parcela evolui de forma súbita para quadros graves e hemorrágicos.
- Contexto epidemiológico: A triagem precoce de sinais de alarme em unidades de pronto atendimento é decisiva para evitar desfechos fatais e otimizar a internação hospitalar.
- Base de investigação: Registros de notificação compulsória do SINAN (OpenDataSUS).
- Variáveis clínicas indicadas: Sintomas febris iniciais, presença de mialgia, cefaleia, histórico de contaminações anteriores, hemograma (contagem de plaquetas) e teste de fragilidade capilar (prova do laço).
- Objetivo da modelagem: Estimar a probabilidade estatística de evolução para dengue grave a partir dos dados do atendimento inicial.

### Estratificação de Risco Cardiovascular na Atenção Primária
As doenças crônicas não transmissíveis, com ênfase nas cardiopatias, constituem a principal causa de mortalidade na população brasileira.
- Contexto epidemiológico: O acompanhamento longitudinal na Estratégia Saúde da Família visa estabilizar comorbidades antes da ocorrência de eventos agudos, como infarto agudo do miocárdio ou acidente vascular cerebral.
- Base de investigação: Dados da Atenção Primária à Saúde (e-SUS APS e históricos do programa Hiperdia).
- Variáveis clínicas indicadas: Pressão arterial sistólica e diastólica, perfil glicêmico, índice de massa corporal, idade, sexo, tabagismo e histórico familiar de patologias cardiovasculares.
- Objetivo da modelagem: Identificar pacientes cadastrados em unidades básicas de saúde com risco elevado de descompensação cardiovascular no curto prazo.

### Risco de Readmissão Hospitalar na Média e Alta Complexidade
A taxa de reinternação em um curto intervalo após a alta é um indicador de qualidade assistencial e estabilidade clínica.
- Contexto epidemiológico: Infeções hospitalares, descompensação terapêutica ou altas precoces geram retornos que elevam a mortalidade e pressionam o tempo de ocupação de leitos.
- Base de investigação: Sistema de Informações Hospitalares (SIH/SUS).
- Variáveis clínicas indicadas: Código da classificação internacional de doenças (CID-10) principal e secundário, duração da internação prévia, porte do procedimento realizado, faixa etária e tipo de saída.
- Objetivo da modelagem: Prever a probabilidade de um paciente hospitalizado necessitar de nova internação em um intervalo de trinta dias após a alta médica.

### Vigilância de Risco e Mortalidade Materno-Infantil
A atenção pré-natal e o cuidado durante o puerpério são metas prioritárias nos indicadores de saúde pública do país.
- Contexto epidemiológico: Complicações gestacionais como pré-eclâmpsia, diabetes gestacional e hemorragias exigem acompanhamento especializado contínuo para evitar mortalidade materna ou parto pré-termo.
- Base de investigação: Sistema de Informações sobre Nascidos Vivos (SINASC) em cruzamento com o Sistema de Informações sobre Mortalidade (SIM).
- Variáveis clínicas indicadas: Número de consultas pré-natal realizadas, idade gestacional, tipo de gravidez, comorbidades da gestante, peso ao nascer e índice de Apgar.
- Objetivo da modelagem: Identificar gestantes com risco clínico de desfecho obstétrico desfavorável para priorização no acompanhamento nas unidades de saúde.

| Versão | Descrição | Autor(es) | Data | Revisor(es) | Data de Revisão |
|---|---|---|---|---|---|
| 1.0 | Detalhamento de subproblemas clínicos e justificativas epidemiológicas | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-07-27 | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 2026-07-27 |
