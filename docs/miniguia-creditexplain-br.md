# Miniguia de Estudo: CreditExplain BR
## Crédito Responsável, IA, Open Finance e Explicabilidade no Contexto Brasileiro

> **Nota de escopo:** material pedagógico consolidado do projeto CreditExplain BR, com data de corte em **22/08/2026**. Não constitui parecer jurídico, política real de concessão de crédito, diagnóstico clínico ou sistema automatizado em produção.

Este miniguia de estudo consolida de forma rigorosa as evidências, regulamentações, jurisprudências e metodologias técnicas que cercam a intersecção de análises de crédito por Inteligência Artificial, práticas de crédito responsável, governança de dados via Open Finance, explicabilidade algorítmica e a gestão de vulnerabilidades financeiras (incluindo o mercado de apostas e o transtorno do jogo) no Brasil.

---

## 1. Contexto e Objetivos

### 1.1. O Desafio da Opacidade Algorítmica nos Sistemas de Informação
A integração acelerada de modelos de Aprendizado de Máquina (ML) em Sistemas de Informação (SI) financeiros permitiu um ganho substancial na precisão preditiva da avaliação de risco. Contudo, essa evolução gerou sistemas do tipo "caixa-preta" (black-box), cuja opacidade inerente desafia a confiança dos usuários, pode perpetuar e amplificar vieses discriminatórios e dificulta a conformidade regulatória com legislações de proteção ao consumidor e de dados pessoais. No contexto do Sul Global, e especificamente no Brasil, o acesso ao crédito é um motor essencial de mobilidade social e desenvolvimento econômico, o que torna as barreiras impostas pela opacidade dos modelos de score tradicionais um fator de agravamento de desigualdades históricas.

### 1.2. O Projeto CreditExplain BR e a Explicabilidade Ativa
O projeto **CreditExplain BR** estuda e aplica criticamente, no contexto brasileiro, referenciais de crédito responsável, governança de dados e explicabilidade algorítmica, sem reivindicar autoria do framework acadêmico analisado. Um dos referenciais centrais é o **ML-XAI-LLM**, desenvolvido por **Marcelo Massashi Simonae, Marlon Marcon e Dalcimar Casanova (UTFPR)**, que investiga a tradução de saídas de XAI para linguagem mais compreensível. Neste miniguia, a expressão **"explicabilidade ativa"** é utilizada como eixo pedagógico para discutir como explicações podem apoiar compreensão, contestação e aprendizagem do consumidor, sempre respeitando os limites efetivamente demonstrados pelas fontes.

---

## 2. Crédito Responsável no Brasil

### 2.1. O Arcabouço Protetivo do Consumidor e do Superendividado
O sistema jurídico-econômico brasileiro estabelece deveres e limites para a concessão de crédito, buscando conciliar a estabilidade do Sistema Financeiro Nacional (SFN) com a proteção e a dignidade do consumidor. Esse equilíbrio é sustentado por três pilares normativos vigentes:
*   **Código de Defesa do Consumidor (Lei nº 8.078/1990):** Consagra o princípio da vulnerabilidade do consumidor e estabelece a facilitação da defesa de seus direitos, inclusive com a inversão do ônus da prova (Art. 6º, VIII). O CDC também exige práticas de informação clara e precisa em todas as relações negociais.
*   **Lei do Superendividamento (Lei nº 14.181/2021):** Introduziu o Capítulo VI-A ao CDC, focado na prevenção e no tratamento do superendividamento da pessoa natural de boa-fé. A lei define o superendividamento como a impossibilidade manifesta de o consumidor pagar a totalidade de suas dívidas de consumo, exigíveis e vincendas, sem comprometer o seu **"mínimo existencial"**.
*   **Regulamentação do mínimo existencial:** O Decreto nº 11.150/2022, em sua redação vigente considerada neste projeto, utiliza a referência de **R$ 600,00** para o mínimo existencial no tratamento do superendividamento. Esse valor decorre da redação dada ao art. 3º pelo Decreto nº 11.567/2023. A aplicação concreta do instituto deve ser lida dentro do regime jurídico vigente e do contexto do caso, sem transformar o valor em um teto automático de concessão de crédito.

### 2.2. A Lei do Cadastro Positivo e Fontes de Informação de Crédito
A avaliação do comportamento financeiro no Brasil apoia-se em infraestruturas centralizadas de dados:
*   **Lei do Cadastro Positivo (Lei nº 12.414/2011):** Criou o banco de dados que armazena o histórico de adimplemento das obrigações de pagamento de pessoas naturais e jurídicas. Seu propósito é permitir uma avaliação precisa e individualizada da capacidade de crédito.
*   **Sistema de Informações de Créditos (SCR) do Banco Central:** Instrumento gerido pelo Banco Central do Brasil (BCB) e alimentado mensalmente por instituições autorizadas, registrando operações com risco igual ou superior a R$ 200,00. A consulta de dados consolidados do SCR exige **autorização expressa e específica do cliente**, preservando estritamente o sigilo bancário.

### 2.3. Resoluções do Banco Central e do CMN sobre Transparência e Educação
Para combater o endividamento de risco e aumentar a conscientização do consumidor, o Banco Central editou importantes resoluções setoriais:
*   **Resolução Conjunta nº 8/2023 (BCB/CMN):** Regula as medidas de educação financeira que devem ser obrigatoriamente adotadas pelas instituições financeiras e de pagamento, integrando a educação financeira às práticas de crédito responsável para a prevenção ao superendividamento.
*   **Resolução BCB nº 365/2023 (em vigor desde julho de 2024):** Altera a Resolução BCB nº 96/2021 e reestrutura a fatura do cartão de crédito em três grupos hierárquicos de informação para mitigar o esforço cognitivo do consumidor (Área de Destaque: valor total, vencimento e limite; Alternativas de Pagamento: encargos, financiamentos e juros; Informações Complementares: detalhamento dos lançamentos).
*   **Histórico de Limitação do Rotativo:** A Resolução CMN nº 4.549/2017 limitou o uso do crédito rotativo do cartão a 30 dias, exigindo a migração do saldo remanescente para linhas de parcelamento mais vantajosas. Posteriormente, a Lei nº 14.690/2023 (Programa Desenrola Brasil) determinou que o valor total acumulado de juros e encargos financeiros no rotativo não pode ultrapassar **100% da dívida principal**.

### 2.4. Entendimento do STJ sobre Credit Scoring — REsp 1.419.697/RS
No acórdão paradigmático do **Superior Tribunal de Justiça (STJ) no REsp 1.419.697 RS (Julgado em 12/11/2014)**, fixou-se o entendimento de que:
1.  O sistema de pontuação de crédito (*credit scoring*) é um método estatístico legítimo de avaliação de risco que **não exige o prévio e expresso consentimento do consumidor avaliado**, uma vez que não constitui um cadastro de dados cadastrais em si, mas um modelo de inferência estatística.
2.  A fórmula matemática e a metodologia estatística de cálculo constituem **segredo empresarial**, estando protegidas contra divulgação compulsória (Art. 5º, IV da Lei nº 12.414/2011).
3.  As instituições financeiras e birôs de crédito são, no entanto, **obrigados a fornecer, mediante solicitação, informações claras, precisas e inteligíveis sobre os dados consultados** (histórico de crédito utilizado) para que o consumidor possa verificar sua veracidade e solicitar retificações de dados incorretos ou desatualizados.

---

## 3. Open Finance e Governança de Dados

### 3.1. Definição, Infraestrutura e Base Legal
O **Open Finance** no Brasil foi formalizado pela **Resolução Conjunta nº 1, de 4 de maio de 2020** (CMN/BCB), que estabeleceu as diretrizes para o compartilhamento padronizado de dados e serviços por meio de interfaces de programação de aplicativos (APIs).
*   **Premissa Fundamental:** O cliente é titular dos seus dados pessoais e exerce direitos de acesso, controle e, nos regimes aplicáveis, portabilidade e autorização de compartilhamento. No Open Finance, o compartilhamento ocorre dentro das regras específicas do ecossistema e do consentimento do cliente, sem tratar os dados como propriedade patrimonial absoluta.
*   **Consentimento no Open Finance:** Para os compartilhamentos abrangidos pela Resolução Conjunta nº 1/2020, o consentimento deve observar os atributos e requisitos da norma, incluindo manifestação livre, informada, prévia e inequívoca, finalidades determinadas e prazo de validade compatível. A regulamentação também veda consentimento presumido ou obtido sem manifestação ativa do cliente.
*   **Arquitetura Descentralizada:** Não há um banco de dados centralizado que consolide os dados do Open Finance. O tráfego de informações ocorre bilateralmente, em poucos segundos, por meio de APIs desenvolvidas sob padrões técnicos estritos homologados pela Estrutura de Governança do Open Finance, sob supervisão direta do Banco Central.

### 3.2. Participação e Segmentação Prudencial
A participação no ecossistema do Open Finance segue critérios prudenciais vinculados à Resolução CMN nº 4.553/2017:
*   **Obrigatória:** Para instituições financeiras enquadradas nos **Segmentos 1 (S1) e 2 (S2)** (grandes bancos comerciais de relevância sistêmica e relevância internacional).
*   **Demais participantes e ampliações posteriores:** A participação varia conforme o tipo de compartilhamento, a instituição e as hipóteses previstas na regulamentação. A Resolução Conjunta nº 10/2024 alterou a Resolução Conjunta nº 1/2020 e ampliou hipóteses de participação obrigatória, com efeitos a partir de 2025, inclusive para instituições ou conglomerados que ultrapassem determinados critérios de clientes. Por isso, a regra não deve ser resumida apenas como “S1/S2 obrigatórios e todos os demais voluntários”; devem ser observadas as exceções, dispensas e modalidades previstas na versão consolidada vigente.

### 3.3. Governança Plural e Regulação Híbrida
A governança do Open Finance brasileiro funciona como um modelo híbrido inovador de **regulação e autorregulação assistida**:
*   O Conselho Monetário Nacional (CMN) e o Banco Central do Brasil (BCB) detêm a competência exclusiva de editar as normas gerais, fiscalizar o cumprimento das regras e aplicar sanções administrativas.
*   O mercado, estruturado sob a forma da **Associação Open Finance**, atua de forma proativa para propor e gerenciar os padrões técnicos de APIs, canais de suporte técnico, ferramentas de versionamento de código e o monitoramento operacional de conformidade entre os participantes. Essa estrutura de governança deve assegurar, obrigatoriamente: representatividade e pluralidade de segmentos, acesso não discriminatório a todos os autorizados, mitigação de conflitos de interesse e sustentabilidade financeira do ecossistema.

### 3.4. Interfaces com a LGPD e o Papel das Autoridades
O compartilhamento de dados no Open Finance cruza diretamente as competências da **Autoridade Nacional de Proteção de Dados (ANPD)** e do **Banco Central (BCB)**:
*   **LGPD (Lei nº 13.709/2018):** O tratamento de dados no ecossistema deve atender plenamente aos direitos fundamentais de privacidade do titular, incluindo os direitos de acesso, correção, eliminação, portabilidade de dados (Art. 18) e revogação do consentimento.
*   **Tutela do Crédito como Base Legal:** A LGPD estabelece uma base legal específica em seu **Art. 7º, inciso X, para tratamento de dados pessoais não sensíveis para a proteção do crédito**. No entanto, isso não desobriga as instituições financeiras de cumprir os princípios de transparência, finalidade legítima, minimização de dados e não discriminação.
*   **Coexistência e Interoperabilidade:** Embora a ANPD seja a autoridade nacional central de proteção de dados, o Banco Central atua de forma complementar e altamente rigorosa na regulação prudencial e na exigência de elevados padrões de segurança cibernética e sigilo bancário das conexões das APIs.

---

## 4. IA e Risco de Crédito

### 4.1. Modelos de Machine Learning na Modelagem de Risco
Fintechs e instituições financeiras têm adotado, em diferentes contextos, modelos de Machine Learning não lineares — como Gradient Boosting/XGBoost, Random Forest e redes neurais — ao lado de métodos estatísticos tradicionais, como regressão logística.
*   **Vantagem Técnica:** Capacidade de capturar interações complexas e padrões não lineares em grandes volumes de dados heterogêneos, reduzindo significativamente as taxas de inadimplência e melhorando a alocação de limites.
*   **O Desafio Socioeconômico e Tecnológico:** Esses modelos operam como "caixas-pretas". A falta de transparência cria riscos severos de:
    *   **Deriva de Dados (*Data Drift*):** Degradação da performance preditiva do modelo quando há mudanças estruturais no comportamento do consumidor que diferem substancialmente dos dados históricos de treino (por exemplo, choques macroeconômicos ou crises).
    *   **Falsos Positivos e Exclusão:** Classificação incorreta de indivíduos viáveis como de alto risco, gerando exclusão financeira arbitrária.

### 4.2. Dados Alternativos e Inclusão Financeira
A utilização de dados alternativos (digital footprints, metadados transacionais móveis, consumo de serviços públicos e padrões de pagamento no comércio eletrônico) é um vetor de inclusão financeira crucial para populações desbancarizadas ou trabalhadores informais do Sul Global, que carecem de histórico de crédito nos birôs tradicionais.
*   Documentos do **World Bank Group** e da **International Finance Corporation (IFC)** indicam que dados alternativos podem ampliar a capacidade de avaliação de risco e inclusão em contextos com histórico de crédito limitado, ao mesmo tempo em que introduzem riscos de qualidade, privacidade, proxies e discriminação que exigem governança.
*   **Diretrizes de Governança do Banco Mundial:** A utilização desses dados exige:
    1.  *Minimização de Dados:* Uso estrito de variáveis relevantes e proporcionais para estimar a capacidade de pagamento, excluindo de forma absoluta dados sensíveis de perfilamento íntimo.
    2.  *Rastreabilidade e Cibersegurança:* Auditoria completa da procedência e cadeia de custódia dos dados alternativos coletados por terceiros.
    3.  *Mitigação de Vieses:* Testes frequentes e calibrações estatísticas para garantir que o modelo não incorpore e perpetue discriminações indiretas baseadas em raça, gênero, orientação sexual ou localização geográfica.

---

## 5. Explicabilidade: SHAP, LIME, Reason Codes e LLMs

A explicabilidade de Inteligência Artificial (*Explainable AI - XAI*) subdivide-se em modelos intrinsecamente interpretáveis (Glass-Box) e métodos explicativos *post-hoc*, aplicados após o treinamento de modelos caixa-preta.

```
  +-------------------------------------------------------------+
  |              Camada de Predição (XGBoost)                   |
  |                Decisão: Crédito Negado                      |
  +------------------------------+------------------------------+
                                 | (Dados Quantitativos Oparcos)
                                 v
  +-------------------------------------------------------------+
  |                  Camada de XAI (Layer 1)                    |
  |   SHAP (Atribuição Aditiva)  |  LIME (Perturbação Local)     |
  +------------------------------+------------------------------+
                                 | (JSON Estruturado)
                                 v
               +-----------------------------------+
               |      Consitency Guardrail         |
               | SHAP e LIME convergem no sentido? |
               +-----------------+-----------------+
                                 | Sim (Green Light)
                                 v
  +-------------------------------------------------------------+
  |             Camada Linguística (LLM - Layer 2)              |
  |  Geração de Narrativa Humana + Recomendações Práticas (PTS) |
  +-------------------------------------------------------------+
```

### 5.1. SHapley Additive exPlanations (SHAP)
*   **Fundamentação Teórica:** Baseado na Teoria dos Jogos Cooperativos (valores de Shapley). Trata cada característica de entrada (*feature*) como um jogador em uma coalizão para determinar o "ganho" (a predição do modelo).
*   **Propriedades Fundamentais:** Garante **Consistência** (se um modelo muda de forma que uma característica tem mais impacto, seu valor de SHAP não diminui) e **Aditividade** (as contribuições individuais somam exatamente a diferença entre a predição atual e o valor médio esperado). É uma das técnicas mais difundidas para atribuição de contribuição de variáveis em explicações globais e locais, devendo ser utilizada de acordo com o modelo, o objetivo e suas limitações.

### 5.2. Local Interpretable Model-Agnostic Explanations (LIME)
*   **Funcionamento Técnico:** Explica predições individuais gerando perturbações e amostras sintéticas ao redor da instância específica de interesse, observando a resposta do modelo caixa-preta.
*   A partir dessas perturbações, o LIME ajusta um modelo linear simples (surrogate interpretável), ponderando as instâncias geradas pela similaridade com o ponto original. O LIME responde à pergunta: *"Quais variáveis foram decisivas para esta decisão específica no limite local ao redor deste perfil de cliente?"*.

### 5.3. Códigos de Razão (*Adverse-Action Reason Codes*)
Derivados de exigências legais norte-americanas (como a *Equal Credit Opportunity Act - ECOA* e as circulares da *Consumer Financial Protection Bureau - CFPB*), os *reason codes* são declarações padronizadas fornecidas ao consumidor contendo os motivos primários específicos que levaram à negação do crédito. Como **possibilidade didática estudada no CreditExplain BR**, códigos de razão podem ser construídos a partir de fatores de influência identificados por técnicas como SHAP e LIME. Isso não significa que tais técnicas sejam obrigatórias, universais ou suficientes, nem que o projeto tenha implementado um sistema real de concessão de crédito.

### 5.4. A Camada de Tradução Linguística com LLMs (Framework ML-XAI-LLM)
Embora SHAP e LIME produzam explicações quantitativas úteis, seus outputs brutos (valores de atribuição e regras locais com intervalos de variáveis) podem ser difíceis de interpretar por consumidores e por usuários não especializados.
*   **Solução:** O framework **ML-XAI-LLM** (originalmente proposto por Simonae, Marcon e Casanova, e estudado/aplicado neste projeto) utiliza um modelo de linguagem generativo (LLM) atuando estritamente como um **"tradutor de domínio"** para fins acadêmicos e analíticos.
*   **Processamento:** O LLM recebe a predição estruturada e os pesos numéricos validados das camadas de XAI (Layer 1) e os converte em narrativas em prosa natural fluidas e personalizadas (Layer 2), integrando conselhos estruturados de educação financeira e caminhos práticos para recuperação do crédito.

### 5.5. Validação Numérica com a Métrica MEMC
No estudo acadêmico de Simonae, Marcon e Casanova, a métrica **MEMC (*Mean Evaluation of Metrics Change*)** é empregada como mecanismo quantitativo de validação das explicações *post-hoc* em relação ao comportamento observado do classificador XGBoost. O CreditExplain BR analisa esse mecanismo como referência técnica; não executou um modelo real de concessão de crédito.
*   **Metodologia:** O script de validação realiza a remoção sistemática (mascaramento) das cinco variáveis mais importantes indicadas por SHAP e LIME na instância de predição.
*   **Resultado do Estudo UTFPR:** No experimento reportado, o mascaramento das variáveis apontadas como relevantes produziu queda acentuada da métrica F1-Score, inclusive de **1,0 para 0,0** nas simulações descritas. Esse resultado é evidência de sensibilidade do modelo às variáveis analisadas naquele experimento, mas **não prova causalidade, não revela uma “lógica determinística verdadeira” do XGBoost e não assegura generalização para bases reais de instituições financeiras**.

### 5.6. Salvaguardas contra Alucinações (Tratadas Didaticamente como Sistema de Tripla Salvaguarda)
A geração de narrativas por LLMs em contextos regulados de crédito exige controles de fidelidade e rastreabilidade. Para fins de estudo, o CreditExplain BR **agrupa didaticamente** três controles discutidos a partir do framework acadêmico como uma “salvaguarda tripartite”; essa nomenclatura é uma **síntese pedagógica do projeto**, e não deve ser atribuída aos autores como nome oficial de arquitetura:
1.  **Engenharia de Prompts Estruturada:** O prompt de sistema instrui o LLM a atuar estritamente sob o papel de tradutor semântico. É explicitamente vedado qualquer tipo de inferência de dados cadastrais ou interpolação de dados numéricos ausentes na entrada JSON estruturada fornecida pelo back-end.
2.  **Filtro de Fidelidade (MEMC Guardrail):** Somente características que passaram pela validação da métrica MEMC (com impacto estatístico real comprovado no F1-Score) são inseridas no contexto textual do LLM, eliminando variáveis com significância nula ou marginal.
3.  **Filtro de Consistência (Consistência SHAP-LIME):** O framework exige concordância de evidências. Uma variável só é destacada como fator de influência preditiva negativo ou positivo na explicação textual humanizada se ambos os explicadores (SHAP globalmente/localmente e LIME localmente) concordarem de forma inequívoca sobre a direção de sua influência, blindando o sistema contra anomalias metodológicas individuais.

---

## 6. Apostas, Vulnerabilidade Financeira e Transtorno do Jogo

O tratamento de transações de apostas de quota fixa (*bets*) e jogos on-line no setor financeiro brasileiro exige máximo rigor técnico-legal para evitar a associação indevida entre comportamento transacional e condições clínicas de saúde mental.

### 6.1. A Cadeia de Diferenciação Rigorosa de Evidências

```
  +----------------------------------------------------------------------------------------+
  | 1. Transação Observada (Registro Físico/Pontual - Pix/Transferência)                  |
  +-------------------------------------------+--------------------------------------------+
                                              v
  +----------------------------------------------------------------------------------------+
  | 2. Padrão Financeiro (Agregação: frequência, volume e comprometimento financeiro)      |
  +-------------------------------------------+--------------------------------------------+
                                              v
  +----------------------------------------------------------------------------------------+
  | 3. Vulnerabilidade (Contexto Socioeconômico: Baixa Renda, Bolsa Família, BPC)         |
  +-------------------------------------------+--------------------------------------------+
                                              v
  +----------------------------------------------------------------------------------------+
  | 4. Inferência de Risco (Cálculo Estatístico de Inadimplência / Model Risk de Default)   |
  +-------------------------------------------+--------------------------------------------+
                                              v
  +----------------------------------------------------------------------------------------+
  | 5. Diagnóstico Clínico (avaliação por profissional de saúde habilitado; CID-10/CID-11)  |
  +----------------------------------------------------------------------------------------+
```

Para fins de análise responsável, o miniguia adota a seguinte separação conceitual entre níveis de evidência:
1.  **Transação Observada:** O registro cru e individual de uma operação de pagamento direcionada a um agente operador de apostas devidamente regulado e autorizado (por exemplo, um PIX de R$ 50,00 com código de transação específico). Trata-se de um dado de tráfego financeiro neutro.
2.  **Padrão Financeiro:** O comportamento transacional agregado analisado no tempo, como frequência, volume e evolução dos gastos. Eventual comprometimento financeiro deve ser calculado apenas a partir de dados de renda e obrigações efetivamente disponíveis e legitimamente tratados; o SCR não deve ser descrito como fonte direta de renda.
3.  **Vulnerabilidade:** A condição socioeconômica preexistente ou associada ao cliente que reduz sua capacidade de absorção de perdas e resiliência financeira (como baixo nível salarial comprovado, superendividamento sob a Lei nº 14.181/2021 ou dependência direta de programas governamentais de transferência de renda).
4.  **Inferência de Risco:** A modelagem estatística de probabilidade que correlaciona o *Padrão Financeiro* de apostas em contexto de *Vulnerabilidade* com um risco estatístico elevado de inadimplência (*default*) ou de quebra do mínimo existencial do devedor. É uma proxy numérica de risco de crédito, não uma afirmação de caráter pessoal.
5.  **Diagnóstico Clínico:** A classificação diagnóstica formal e científica de **Jogo Patológico (CID-10 F63.0)**, **Mania de Jogo (Z72.6)** ou de **Transtorno de Jogo (CID-11 6C50.0)**. Trata-se de uma condição clínica que depende de avaliação por profissional de saúde habilitado, segundo critérios clínicos apropriados. **Um modelo de crédito, uma instituição financeira ou a observação isolada de transações não deve converter comportamento financeiro em diagnóstico de transtorno do jogo**.

> ⚠️ **REGRA DE OURO DO AUDITOR:** Comportamento de gastos transacionais de apostas, frequência de apostas ou inferências de risco financeiro **não configuram, sob hipótese alguma, diagnóstico clínico de ludopatia ou transtorno do jogo**. A modelagem de crédito deve tratar esses dados estritamente como indicadores estatísticos de capacidade de pagamento e risco de insolvência.

### 6.2. Estudo de Caso Jurisprudencial: TJSP
Um **acórdão do Tribunal de Justiça do Estado de São Paulo (TJSP)** utilizado no corpus, relacionado ao processo nº 0000967-51.2024.8.26.0601, foi preservado como **estudo de caso casuístico** e não como entendimento universal ou jurisprudência brasileira consolidada. Naquele contexto fático, o tribunal afastou a ampliação automática do dever bancário para uma tutela geral sobre saúde mental e hábitos de jogo do correntista. Os principais pontos úteis para o estudo são:
*   A simples apresentação de diagnóstico médico de jogo patológico, mesmo que de forma superveniente à realização das transações, não acarreta nulidade de contratos bancários ou responsabilidade civil dos bancos se não houver interdição formal prévia ou ciência inconteste da condição patológica pela instituição.
*   No caso analisado, o acórdão afastou a imposição de um dever bancário geral de tutela sobre a saúde mental e os hábitos de jogo do correntista, considerando excessiva a ampliação daquele dever de diligência para esse propósito.
*   Deste modo, as recomendações de cuidado intersetorial e as portarias regulatórias de jogo responsável são deveres de governança dos agentes de apostas e do Estado, não se convertendo em obrigações jurídicas de assistência psicossocial civil para as instituições financeiras.

### 6.3. Restrições Normativas Vigentes e Políticas Públicas de Jogo Responsável
O Ministério da Fazenda, por meio da Secretaria de Prêmios e Apostas (SPA/MF), em consonância com a Lei nº 14.790/2023, estabelece vedações estritas de uso do sistema financeiro para impedir o agravamento de vulnerabilidades:
*   **Bolsa Família e BPC:** A Portaria SPA/MF nº 2.217/2025 disciplina a vedação relacionada a recursos provenientes do **Programa Bolsa Família** e do **Benefício de Prestação Continuada (BPC)**; a Instrução Normativa SPA/MF nº 22/2025 operacionaliza o impedimento de cadastro ou uso dos sistemas de apostas pelos beneficiários. A distinção entre origem dos recursos e condição do beneficiário deve ser preservada.
*   **Programas de Renegociação:** Portarias setoriais estendem o bloqueio e o impedimento de participação em apostas para beneficiários de programas públicos de renegociação de dívidas, com as seguintes distinções normativas específicas:
    *   **Novo Desenrola Brasil:** Veda a participação nas apostas de quota fixa para beneficiários do Programa Extraordinário de Reequilíbrio Financeiro das Famílias - Novo Desenrola Brasil (instituído pela Medida Provisória nº 1.355/2026), conforme a Portaria SPA/MF nº 1.237/2026 e a Instrução Normativa SPA/MF nº 3/2026.
    *   **Fies tradicional:** Veda a participação em apostas para os estudantes beneficiários da renegociação de dívida junto ao Fundo de Financiamento Estudantil (Fies) de que trata o art. 5º-A, § 4º-B da Lei nº 10.260/2001, regulamentado pela Portaria SPA/MF nº 1.638/2026 e pela Instrução Normativa SPA/MF nº 8/2026.
    *   **Fies Empreendedor:** Veda o cadastro ou uso de apostas por beneficiários do Programa Nacional de Incentivo Financeiro à Adimplência no Fundo de Financiamento Estudantil - Fies Empreendedor (conforme a Medida Provisória nº 1.373/2026), sob a regência da Portaria SPA/MF nº 2.066/2026 e da Instrução Normativa MF nº 21/2026.
*   **Portaria SPA/MF nº 2.579/2025 (e IN nº 31/2025):** Aperfeiçoa as diretrizes do Jogo Responsável e impõe obrigações adicionais aos operadores de apostas:
    1.  *Limites Prudenciais Obrigatórios:* O cadastro de qualquer apostador deve, obrigatoriamente, exigir a definição de limites de tempo de uso e de perda financeira máxima diária/mensal.
    2.  *Mecanismo de Autoexclusão Centralizada:* Criação de plataforma centralizada integrada diretamente com a SPA/MF que, mediante provocação voluntária do usuário, bloqueia seu acesso e cadastro em todos os agentes autorizados no país de forma concomitante.
*   **Bloqueio financeiro de operadores irregulares:** A legislação de 2026 criou mecanismos de bloqueio e impedimento de transações ligados a operadores de apostas não autorizados. A operacionalização pela **Resolução CMN nº 5.320, de 25 de junho de 2026**, prevê bloqueio em até **24 horas** após a notificação aplicável, porém **a norma somente entra em vigor em 28 de agosto de 2026**. Assim, na data de corte deste miniguia (**22/08/2026**), trata-se de **norma publicada com vigência futura**; a redação deve passar para o presente apenas após refresh normativo e confirmação de que não houve alteração ou suspensão.

---

## 7. Governança da Explicação ao Consumidor

### 7.1. Direito à Revisão e Informações sobre Decisões Automatizadas
O **Artigo 20 da LGPD** estabelece de forma expressa que o titular dos dados pessoais tem o direito de solicitar a revisão de decisões tomadas unicamente com base em tratamento automatizado de dados que afetem seus interesses, incluindo decisões destinadas a definir o seu perfil de consumo, profissional ou de crédito.
*   **Informações quando solicitadas:** O art. 20 da LGPD assegura ao titular o direito de solicitar revisão de decisão unicamente automatizada que afete seus interesses e prevê o fornecimento, **quando solicitado**, de informações claras e adequadas sobre critérios e procedimentos, observados os segredos comercial e industrial. Recomendações de transparência proativa, portais e painéis devem ser tratadas separadamente como propostas de governança institucional, não como obrigação legal geral já positivada.
*   **Salvaguarda do Segredo Comercial:** A prestação dessas informações deve respeitar os segredos comerciais e industriais do desenvolvedor ou instituição. No entanto, conforme apontado pelas notas do Conselho Nacional de Proteção de Dados (CNPD), a invocação de propriedade intelectual ou segredo comercial **não legitima a omissão completa de esclarecimentos** ao titular sobre quais dados foram analisados e qual o peso geral dessas variáveis em seu score.

### 7.2. Recomendações de Governança do CNPD (GT5)
No relatório final do Grupo de Trabalho 5 do CNPD (Proteção de Dados no Desenvolvimento Econômico e Inovação), propõe-se que as instituições financeiras e os birôs de score estruturem canais permanentes de governança da explicação ao consumidor:
*   **Portal do Titular Ativo:** Disponibilização de ambiente web facilitado contendo os dados processados para geração do score, tanto dados de comportamento de pagamentos históricos quanto dados obtidos via Open Finance.
*   **Painel de Peso de Variáveis:** Exibição clara e graficamente humanizada que mostre como cada dado favoreceu ou prejudicou o escore específico gerado, permitindo fácil compreensão do cliente.
*   **Canais de Contestação e Correção:** Meios integrados que permitam a correção de dados inexatos, o envio de justificativas de capacidade de pagamento e a solicitação de revisão por intervenção humana direta de forma desburocrática.
*   **Notificação de Alterações:** Comunicação proativa e em tempo real ao titular a cada atualização de seus dados cadastrais ou inclusão de novas informações em sua base de cálculo.

---

## 8. Benchmarks Internacionais

As normativas estrangeiras listadas constituem excelentes benchmarks técnicos e melhores práticas globais de governança, mas **não possuem força de lei ou caráter vinculante no ordenamento jurídico brasileiro**, salvo quando expressamente integradas à regulação nacional.

### 8.1. Diretrizes de Originação e Monitoramento de Empréstimos da EBA (União Europeia)
*   As **Diretrizes EBA/GL/2020/06** da Autoridade Bancária Europeia determinam padrões rígidos de controle interno para concessão de crédito.
*   **Exigências Principais:** Separação funcional de atribuições entre a área de negócios (originação) e de controle de risco, gerenciamento ativo de riscos de modelo (*model risk management*), exigência de documentação técnica detalhada das fórmulas preditivas e auditoria contínua dos modelos de regressão ou estatísticos aplicados. As diretrizes também exigem a integração de fatores ambientais, sociais e de governança (ESG) na avaliação de solvabilidade.

### 8.2. O Regulamento Geral de Proteção de Dados (GDPR) e a Diretiva de Crédito ao Consumidor da UE
*   **GDPR (Artigo 22):** Proíbe, como regra geral, que indivíduos sejam submetidos a decisões unicamente automatizadas com efeitos jurídicos relevantes, estabelecendo exceções rígidas que exigem salvaguardas (intervenção humana, direito de expressão de opinião e direito de contestação da decisão).
*   **Diretiva de Crédito ao Consumidor (Diretiva UE 2023/2225):** Veda de forma absoluta o uso de categorias especiais de dados (dados sensíveis, como dados de saúde obtidos em prontuários ou diagnósticos clínicos) na avaliação de risco de crédito, exigindo o direito de revisão humana direta em recusas de propostas por via automatizada.

### 8.3. O Regulamento de Inteligência Artificial da União Europeia (EU AI Act)
*   O **Regulamento (UE) 2024/1689 (EU AI Act)** inclui, no Anexo III, determinados sistemas de IA usados para avaliar a capacidade creditícia ou estabelecer pontuação de crédito de pessoas naturais entre os casos de alto risco, observadas as regras de classificação e as hipóteses previstas no próprio Regulamento.
*   Quando o sistema é classificado como alto risco, aplicam-se requisitos reforçados de gestão de riscos, governança e qualidade de dados, documentação e registros, transparência, supervisão humana, robustez, cibersegurança e monitoramento, conforme o regime europeu aplicável.

### 8.4. O Circular CFPB 2022-03 (Estados Unidos)
*   A circular do órgão de proteção do consumidor financeiro norte-americano (*Consumer Financial Protection Bureau*) estabelece que as obrigações de notificação de ação adversa (*adverse action notices*) exigidas pela ECOA (*Equal Credit Opportunity Act*) **aplicam-se integralmente mesmo quando as instituições financeiras fazem uso de algoritmos altamente complexos e proprietários de IA**.
*   O regulador proíbe o uso de justificativas vagas como *"o modelo de inteligência artificial negou o crédito baseado em fatores proprietários"*. A instituição financeira deve mapear e indicar de forma exata e justificada as razões de declínio específicas de cada perfil individual, independentemente da complexidade técnica do modelo caixa-preta empregado.

### 8.5. NIST AI RMF 1.0 e Cyber Risk Institute (CRI) FS AI RMF
*   **NIST AI RMF 1.0:** Guia estruturado voluntário composto por quatro funções interativas permanentes (**Govern, Map, Measure e Manage**) para mitigação de riscos e promoção de sistemas de IA confiáveis, robustos e livres de vieses discriminatórios.
*   **CRI FS AI RMF:** Adaptação setorial específica para o sistema financeiro global do framework do NIST, estendendo-o para incluir 230 objetivos de controle específicos para mitigar opacidades algorítmicas, vazamentos de dados pessoais e dependências críticas de terceiros.

---

## 9. Limites e Lacunas do Corpus de Fontes

Este miniguia pauta-se no princípio da honestidade intelectual. Durante a análise das fontes fornecidas, mapearam-se as seguintes lacunas empíricas e teóricas:

1.  **Dimensionalidade e Generalização dos Dados no Estudo de UTFPR:** O framework *ML-XAI-LLM* foi testado e validado em uma base de varejo pública (Nerd dos Dados) com apenas 10.476 registros e 17 atributos. A obtenção de F1-Score igual a 1.0 (precisão e recall perfeitos) é um **sinal que exige investigação adicional** sobre separação treino/teste, eventual vazamento de informação, complexidade do conjunto de dados e sobreajuste (*overfitting*). Isoladamente, a métrica perfeita não prova overfitting, mas recomenda cautela antes de qualquer generalização para grandes bases de dados proprietárias de bancos de grande porte caracterizadas por ruídos estocásticos profundos e milhares de variáveis concorrentes.
2.  **Ausência de Avaliação Psicossocial ou Testes Clínicos com Humanos:** O artigo técnico de Simonae et al. registra que não foram realizados testes qualitativos de campo com seres humanos (como oficiais de crédito ou proponentes reais de crédito). A validação de "utilidade percebida" e "compreensão da explicação" apoia-se em proxies estatísticas (métrica MEMC), carecendo de comprovação empírica de campo direta com os indivíduos afetados.
3.  **Vazio Normativo sobre Interoperabilidade Plena de APIs em Ambientes Multi-Setor:** Embora o corpus mencione o início da discussão de interoperabilidade entre Open Finance e Open Insurance (Resolução Conjunta nº 5/2022) e projetos do BIS (Projeto Aperta), as regras de execução operacional e métricas de desempenho sob cargas máximas simultâneas de tráfego de APIs em ecossistemas intersetoriais ainda não estão regulamentadas ou detalhadas nos normativos fornecidos.
4.  **Lacuna na Regulamentação da ANPD sobre Portabilidade:** O dispositivo específico da LGPD que trata do compartilhamento de dados entre empresas privadas (portabilidade do Art. 18, V) ainda carece de regulamentação formal por parte da ANPD, o que gera áreas cinzentas de coexistência e segurança jurídica no trânsito de históricos cadastrais em setores não financeiros.

---

## 10. Glossário de Conceitos (20 Conceitos)

1.  **Open Finance:** Compartilhamento padronizado de dados e serviços por meio de abertura e integração de sistemas (APIs) autorizados e supervisionados pelo Banco Central do Brasil.
2.  **Superendividamento:** Impossibilidade manifesta de o consumidor pessoa natural, de boa-fé, pagar a totalidade de suas dívidas de consumo, exigíveis e vincendas, sem comprometer seu mínimo existencial.
3.  **Mínimo Existencial:** Referência jurídica de preservação de recursos necessários à subsistência no tratamento do superendividamento. Na redação considerada neste projeto, o art. 3º do Decreto nº 11.150/2022 utiliza R$ 600,00, valor introduzido pelo Decreto nº 11.567/2023; não deve ser convertido em teto mecânico de concessão de crédito.
4.  **Autoexclusão Centralizada:** Suspensão voluntária e centralizada das atividades de aposta, realizada em plataforma mantida pela Secretaria de Prêmios e Apostas (SPA/MF), que impede simultaneamente o cadastro ou acesso do usuário a todas as plataformas de apostas reguladas no país.
5.  **SHAP (SHapley Additive exPlanations):** Técnica de explicabilidade pós-hoc baseada na Teoria dos Jogos Cooperativos que atribui valores aditivos e consistentes de contribuição de cada variável de entrada para a predição final de um modelo de aprendizado de máquina.
6.  **LIME (Local Interpretable Model-agnostic Explanations):** Método de explicabilidade pós-hoc que gera perturbações e simulações locais ao redor de uma predição individual para ajustar um modelo *surrogate* interpretável, estimando quais variáveis mais influenciam a predição naquele entorno local. **Não estabelece causalidade**.
7.  **Métrica MEMC (*Mean Evaluation of Metrics Change*):** Métrica quantitativa de fidelidade de XAI que avalia o impacto na performance global do modelo (como a queda no F1-Score) ao ocultar sistematicamente as características mais importantes indicadas pelos explicadores.
8.  **XGBoost:** Algoritmo de aprendizado de máquina baseado em árvores de decisão impulsionadas por gradiente (*Gradient Boosting*), classificado como "caixa-preta" devido ao seu alto nível de não linearidade e opacidade interna.
9.  **Cadastro Positivo:** Banco de dados regulado pela Lei nº 12.414/2011 que registra o histórico de adimplemento e bom comportamento de pagamento de pessoas físicas e jurídicas para fins de cálculo de nota de crédito.
10. **Sistema de Informações de Crédito (SCR):** Central de informações de risco de crédito mantida de forma confidencial pelo Banco Central do Brasil, registrando operações de crédito e coobrigações acima de R$ 200,00 para supervisão e mitigação de inadimplência.
11. **Não Tutoria Bancária — estudo de caso:** Rótulo didático utilizado neste projeto para sintetizar um acórdão específico do TJSP no qual se afastou, naquele contexto, a imposição de tutela bancária geral sobre saúde mental e hábitos de jogo do correntista. **Não constitui jurisprudência universal ou consolidada**.
12. **Bloqueio Financeiro de Operadores Irregulares:** Expressão descritiva adotada neste miniguia para o mecanismo regulatório de bloqueio de contas/transações de operadores de apostas não autorizados. A Resolução CMN nº 5.320/2026 prevê operacionalização em até 24 horas, **com entrada em vigor somente em 28/08/2026**.
13. **Jogo Patológico (CID-10 F63.0):** Código oficial da Classificação Internacional de Doenças correspondente ao comportamento compulsivo e persistente de jogo que prejudica as esferas pessoal, familiar e profissional do paciente.
14. **Transtorno de Jogo (CID-11 6C50.0):** Diagnóstico médico psiquiátrico de padrão persistente de jogo com perda de controle, prioridade dada ao jogo sobre outros interesses e continuidade mesmo diante de consequências negativas graves.
15. **Rede de Atenção Psicossocial (RAPS):** Conjunto intersetorial de pontos de atenção à saúde integrados no SUS para o acolhimento, cuidado e reabilitação psicossocial de pessoas com sofrimento mental ou transtornos decorrentes de adição.
16. **Determinantes Comerciais da Saúde (DCS):** Fatores estruturais decorrentes de estratégias mercadológicas e de publicidade em massa que moldam os hábitos de consumo e influenciam diretamente a ocorrência de problemas de saúde física e psíquica na população.
17. **Model Risk (Risco de Modelo):** Risco de perdas financeiras ou decisões incorretas geradas pelo uso de modelos preditivos inadequados, com erros de formulação matemática, qualidade sofrível de dados de entrada ou falhas de governança.
18. **Data Drift (Deriva de Dados):** Alteração estatística contínua e gradual das propriedades distributivas das variáveis do mundo real em relação aos dados nos quais o modelo foi treinado, provocando perda de precisão e acurácia estatística.
19. **Adverse Action Notice (Notificação de Ação Adversa):** Exigência legal, comum no mercado americano sob a ECOA/FCRA, que impõe o dever de fornecer justificativas específicas e não genéricas ao cliente rejeitado em avaliações de propostas de financiamento.
20. **Contestabilidade:** Capacidade de o titular compreender os principais fundamentos de uma decisão automatizada, identificar dados incorretos, solicitar correção e, quando cabível, requerer revisão. No CreditExplain BR, é tratada como dimensão de governança distinta da mera visualização técnica do modelo.

---

## 11. 10 Prompts Reutilizáveis para Simulação, Estudo e Auditoria do Framework

As diretrizes abaixo apresentam prompts de engenharia configurados exclusivamente para simular, estudar e auditar o comportamento de modelos de linguagem em tarefas integradas ao framework. Estes modelos servem como ferramentas pedagógicas de sandboxing e análise técnica, sendo vedada sua aplicação direta para atuação jurídica real ou intervenções clínicas de saúde:

### Prompt 1:

*Atenção: Este prompt destina-se exclusivamente a fins de estudo acadêmico, pesquisa e auditoria simulada de modelos de crédito (sandboxing). Não deve ser utilizado para fins de assessoria jurídica ativa ou diagnóstico clínico real.*
 Tradução Semântica e Humanizada de Atribuições de XAI (Layer 2)
```text
Papel: Você é o Tradutor Semântico de Explicabilidade do CreditExplain BR.
Instrução: Traduza o JSON quantitativo de SHAP e LIME fornecido em uma narrativa fluida, em português (Brasil), voltada para o consumidor final que teve o crédito negado. Explique de forma empática e didática quais fatores pesaram negativamente. Não utilize termos de jargão de programação (como "arrays", "floats" ou "XGBoost"). Indique quais variáveis justificaram o declínio.

Entrada de Contexto Validada:
{
  "predicao": "Negado",
  "shap_negative_contributors": {
    "VL_IMOVEIS": -3.25,
    "TEMPO_ULTIMO_EMPREGO_MESES": -0.34
  },
  "lime_local_rules": [
    "VL_IMOVEIS \<= 100000.00",
    "TEMPO_ULTIMO_EMPREGO_MESES \<= 12"
  ]
}
Restrição: Limite-se estritamente aos fatos do JSON. É expressamente proibido alucinar dados ou inventar valores que não estejam no JSON fornecido.
```

### Prompt 2:

*Atenção: Este prompt destina-se exclusivamente a fins de estudo acadêmico, pesquisa e auditoria simulada de modelos de crédito (sandboxing). Não deve ser utilizado para fins de assessoria jurídica ativa ou diagnóstico clínico real.*
 Ativação de Travas contra Alucinações (Prompt de Controle)
```text
Papel: Você é um Auditor de Segurança de Explicações do CreditExplain BR.
Instrução: Avalie a explicação textual gerada pelo LLM em comparação com os dados brutos de entrada da Layer 1. Verifique se o texto gerado faz qualquer afirmação estatística ou cadastral que não esteja explicitamente respaldada pelo JSON. Se houver qualquer extrapolação de limites numéricos, dados pessoais ou de correlação causal não justificada, emita um sinal "ALERT: HALLUCINATION" e aponte a inconformidade fática.
```

### Prompt 3:

*Atenção: Este prompt destina-se exclusivamente a fins de estudo acadêmico, pesquisa e auditoria simulada de modelos de crédito (sandboxing). Não deve ser utilizado para fins de assessoria jurídica ativa ou diagnóstico clínico real.*
 Personalização de Recomendações e Educação Financeira (Artigo 54-A do CDC)
```text
Papel: Você é o Especialista em Educação Financeira do CreditExplain BR.
Instrução: Com base nos motivos de recusa de crédito validados (ex: baixo patrimônio imobiliário e curto tempo de emprego formal), elabore recomendações e caminhos de ação realistas e responsáveis para o consumidor, alinhados à prevenção ao superendividamento. Foque em soluções como repactuação de dívidas anteriores de consumo e planejamento de consolidação cadastral estável.
```

### Prompt 4:

*Atenção: Este prompt destina-se exclusivamente a fins de estudo acadêmico, pesquisa e auditoria simulada de modelos de crédito (sandboxing). Não deve ser utilizado para fins de assessoria jurídica ativa ou diagnóstico clínico real.*
 Auditoria Didática de Explicação de Recusa e Reason Codes
```text
Papel: Você é um pesquisador de governança de crédito e explicabilidade.
Instrução: Em um CENÁRIO FICTÍCIO/SINTÉTICO, compare uma explicação simulada de recusa de crédito com os deveres de informação aplicáveis no Brasil e com o benchmark norte-americano do CFPB Circular 2022-03. Identifique informações adequadas, omissões, extrapolações e diferenças de jurisdição. Não gere notificação jurídica real, não decida concessão de crédito e não apresente o benchmark estrangeiro como obrigação brasileira.
```

### Prompt 5:

*Atenção: Este prompt destina-se exclusivamente a fins de estudo acadêmico, pesquisa e auditoria simulada de modelos de crédito (sandboxing). Não deve ser utilizado para fins de assessoria jurídica ativa ou diagnóstico clínico real.*
 Detecção de Drift de Dados e Qualidade Cadastral
```text
Papel: Engenheiro de Modelagem de Risco e Model Risk Management.
Instrução: Analise as métricas de distribuição estatística das faturas do cartão de crédito da carteira atual em relação à base de treino original (dados de 2024 vs 2026). Identifique desvios estruturais significativos que sugiram Deriva de Dados (Data Drift) provocados por mudanças nas faturas (sob os critérios de transparência da Resolução BCB nº 365/2023) e formule as diretrizes técnicas para o retreinamento do modelo.
```

### Prompt 6:

*Atenção: Este prompt destina-se exclusivamente a fins de estudo acadêmico, pesquisa e auditoria simulada de modelos de crédito (sandboxing). Não deve ser utilizado para fins de assessoria jurídica ativa ou diagnóstico clínico real.*
 Personalização de Fatura com Destaque em Educação Financeira (Resolução BCB nº 365/2023)
```text
Papel: Assistente de UX de Sistemas de Pagamento e Faturas Transparentes.
Instrução: Reestruture o layout informacional e os avisos textuais de uma fatura de cartão de crédito. Aplique com rigor a tripartição hierárquica exigida pela Resolução BCB nº 365/2023: organize o texto em (i) Área de Destaque Visual, (ii) Alternativas de Pagamento Contendo o Custo Efetivo Total (CET) e (iii) Informações Complementares. Evite qualquer poluição visual ou dispersão cognitiva do cidadão.
```

### Prompt 7:

*Atenção: Este prompt destina-se exclusivamente a fins de estudo acadêmico, pesquisa e auditoria simulada de modelos de crédito (sandboxing). Não deve ser utilizado para fins de assessoria jurídica ativa ou diagnóstico clínico real.*
 Estudo de Caso sobre Superendividamento e Mínimo Existencial
```text
Papel: Você é um tutor acadêmico de crédito responsável.
Instrução: Analise um CENÁRIO FICTÍCIO/SINTÉTICO de superendividamento e identifique quais informações seriam relevantes para estudar prevenção, repactuação e preservação do mínimo existencial à luz do CDC. Diferencie conceito jurídico, dado financeiro e hipótese de estudo. Não elabore acordo jurídico, petição, decisão ou orientação individualizada.
```

### Prompt 8:

*Atenção: Este prompt destina-se exclusivamente a fins de estudo acadêmico, pesquisa e auditoria simulada de modelos de crédito (sandboxing). Não deve ser utilizado para fins de assessoria jurídica ativa ou diagnóstico clínico real.*
 Auditoria Didática de Vulnerabilidade Financeira Associada a Apostas
```text
Papel: Você é um pesquisador de crédito responsável e jogo responsável.
Instrução: Analise um lote de dados FICTÍCIOS/SINTÉTICOS e agregados de transações para identificar somente padrões financeiros potencialmente relevantes à vulnerabilidade e ao risco de crédito. Diferencie dado observado, padrão financeiro, inferência e diagnóstico clínico. Não diagnostique transtorno do jogo, não use dados reais de clientes e não formule obrigação regulatória que não esteja expressa em fonte brasileira competente.
```

### Prompt 9:

*Atenção: Este prompt destina-se exclusivamente a fins de estudo acadêmico, pesquisa e auditoria simulada de modelos de crédito (sandboxing). Não deve ser utilizado para fins de assessoria jurídica ativa ou diagnóstico clínico real.*
 Revisão Acadêmica sobre Transtorno do Jogo e Fronteira Clínica
```text
Papel: Você é um tutor acadêmico em saúde pública e governança de dados.
Instrução: Com base no Guia do Ministério da Saúde de 2026, explique para fins de estudo a diferença entre sinais de alerta, instrumentos de triagem, avaliação clínica e diagnóstico de transtorno do jogo. Relacione essa distinção aos limites de inferência em modelos financeiros. Não produza roteiro clínico de atendimento, diagnóstico, tratamento ou orientação para pacientes reais.
```

### Prompt 10:

*Atenção: Este prompt destina-se exclusivamente a fins de estudo acadêmico, pesquisa e auditoria simulada de modelos de crédito (sandboxing). Não deve ser utilizado para fins de assessoria jurídica ativa ou diagnóstico clínico real.*
 Auditoria Didática de Fluxo Open Finance
```text
Papel: Você é um pesquisador de governança de dados e Open Finance.
Instrução: Em um CENÁRIO FICTÍCIO/SINTÉTICO, revise um fluxo de compartilhamento de dados para uma proposta de portabilidade de crédito e produza um checklist acadêmico sobre consentimento, finalidade, escopo, prazo, rastreabilidade e segurança. Diferencie regra brasileira vigente de boa prática. Não emita parecer jurídico ou de conformidade real.
```

---

## 12. Checklist de Revisão de Auditoria para Concessão Ética de Crédito

*   [ ] **Conformidade Legal Geral (CDC & LGPD):**
    *   O tratamento dos dados pessoais é estritamente pautado em base legal legítima (tutela do crédito sob Art. 7º, inciso X da LGPD ou legítimo interesse)?
    *   Garantem-se de forma ativa os direitos dos titulares do Artigo 18 da LGPD (acesso, correção de inexatidões, informação de fontes de dados consultadas no SCR)?
*   [ ] **Preservação do Mínimo Existencial (Lei nº 14.181/2021):**
    *   A estimativa estatística de comprometimento de renda para o pagamento do empréstimo avaliado preserva o mínimo existencial de R$ 600,00 da pessoa natural de boa-fé (Decreto nº 11.150/2022)?
    *   O sistema de score bloqueia ativamente a oferta de crédito assediante ou abusiva contra populações de extrema vulnerabilidade (idosos, analfabetos ou superendividados)?
*   [ ] **Fidelidade da Explicabilidade Algorítmica (MEMC & Guardrails):**
    *   As explicações textuais humanizadas fornecidas ao consumidor baseiam-se em saídas quantitativas validadas pela métrica estatística MEMC (com impacto comprovado de F1-Score)?
    *   As três salvaguardas contra alucinações (sintetizadas didaticamente: Structured Prompts, MEMC Guardrail e Consistência SHAP-LIME) estão ativas para blindar a geração linguística da narrativa?
*   [ ] **Mitigação de Vieses e Não Discriminação:**
    *   O modelo passa por testes de disparidade/fairness adequados ao contexto para identificar possíveis impactos discriminatórios, sem importar automaticamente métricas ou limiares estrangeiros como regra brasileira?
    *   O uso de dados pessoais sensíveis foi analisado sob o regime jurídico próprio da LGPD, sem presumir que a base de proteção do crédito do art. 7º, X, autorize tratamento de dados sensíveis e sem utilizar atributos ou proxies de modo discriminatório ilícito ou abusivo?
*   [ ] **Diferenciação e Respeito à Saúde do Consumidor (Apostas vs. Diagnósticos):**
    *   A análise estatística de comportamento transacional em apostas (*bets*) é tratada estritamente como indicador numérico de liquidez/capacidade de pagamento?
    *   O sistema de score evita rotular ou inferir qualquer quadro patológico de ludopatia ou transtorno do jogo a partir de comportamento transacional, reconhecendo que diagnóstico exige avaliação clínica por profissional de saúde habilitado?
    *   A análise preserva o caráter casuístico do estudo de caso do TJSP, sem transformá-lo em regra geral de ausência ou presença de responsabilidade bancária?
*   [ ] **Governança de APIs de Open Finance:**
    *   O compartilhamento de dados observa o fluxo aplicável entre participantes autorizados e os requisitos de consentimento da Resolução Conjunta nº 1/2020 — manifestação livre, informada, prévia e inequívoca, finalidades determinadas, prazo compatível e vedação de consentimento presumido?
    *   O registro dos termos de consentimento ativos está atualizado e auditável para fins de fiscalização pelo Banco Central?
*   [ ] **Model Risk Management & Auditoria de Terceiros (Benchmarks):**
    *   A documentação técnica detalhada das metodologias e limitações do modelo XGBoost é mantida atualizada para auditorias do regulador e supervisores (EBA/GL/2020/06)?
    *   Estão definidos e testados limites operacionais e ferramentas de corte emergencial de processamento (*kill switches*) para cenários de forte instabilidade sistêmica ou colapso cibernético?

---

## Fontes de referência selecionadas

1.  **Câmara dos Deputados — Lei nº 14.790, de 29 de dezembro de 2023** (Dispõe sobre apostas de quota fixa).
2.  **Código de Defesa do Consumidor — Lei nº 8.078, de 11 de setembro de 1990** (Atualizado pela Lei nº 14.181/2021 - Lei do Superendividamento).
3.  **Lei Geral de Proteção de Dados Pessoais (LGPD) — Lei nº 13.709, de 14 de agosto de 2018** (Conformidade com a tutela do crédito e revisão de decisões automatizadas).
4.  **Apostas de Quota Fixa — Ministério da Fazenda** (Relação de Notas Técnicas, Instruções Normativas e Portarias de Jogo Responsável vigentes até julho de 2026).
5.  **Autoexclusão - FAQ — Ministério da Fazenda** (Guia prático da Portaria SPA/MF nº 2.579/2025 sobre autoexclusão centralizada e limites prudenciais).
6.  **Simonae, Marcelo Massashi; Marcon, Marlon; Casanova, Dalcimar (UTFPR) — Bridging AI and Ethics: An LLM-Based Framework for Transparent and Inclusive Credit Decisions** (Framework ML-XAI-LLM, técnicas de explicabilidade e métrica MEMC; a organização em “salvaguarda tripartite” é síntese didática do CreditExplain BR, não nomenclatura atribuída aos autores).
7.  **Banco Central do Brasil — Relatório de Cidadania Financeira 2025** (Marcos normativos, faturas transparentes via Resolução BCB nº 365/2023 e mensuração do superendividamento).
8.  **Conselho Nacional de Proteção de Dados Pessoais (CNPD) — Relatório Final do GT5** (Estudo de caso e recomendações de governança na proteção ao crédito).
9.  **Ministério da Saúde — Guia de Cuidado para Pessoas com Problemas Relacionados a Jogos de Apostas (2026)** (Políticas de saúde mental, Rede de Atenção Psicossocial - RAPS, sinais de alerta de transtorno do jogo e classificação CID-10/CID-11).
10. **Tribunal de Justiça de São Paulo (TJSP) — processo nº 0000967-51.2024.8.26.0601** (estudo de caso casuístico sobre responsabilidade bancária e alegações relacionadas a jogo patológico; não generalizar como jurisprudência consolidada).
11. **EBA (European Banking Authority) — Guidelines on Loan Origination and Monitoring (EBA/GL/2020/06)** (Benchmarks de governança de originação e monitoramento de empréstimos).
12. **OECD — Supervision of Artificial Intelligence in Finance (2026) & AI, ML and Big Data in Finance (2021)** (Benchmarks de governança de modelos de IA e supervisão prudencial internacional).
13. **NIST — Artificial Intelligence Risk Management Framework (AI RMF 1.0) & Cyber Risk Institute (CRI) FS AI RMF** (Melhores práticas internacionais de mitigação de riscos de inteligência artificial).
14. **World Bank Group — Credit Scoring Approaches Guidelines (2019)** (Diretrizes para governança de modelos de escore de crédito e uso ético de dados alternativos).

> O índice ampliado das 77 fontes auditadas está disponível em [`corpus-77-fontes.md`](corpus-77-fontes.md).
