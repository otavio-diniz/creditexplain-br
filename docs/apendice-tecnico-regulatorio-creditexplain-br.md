# CreditExplain BR — Apêndice técnico-regulatório e matriz de evidência

**Complemento da 2ª edição revisada e ampliada**  
**Data de revisão:** 27/09/2026  
**Função:** preservar densidade técnica, detalhes regulatórios, rastreabilidade e controles de evidência sem transformar o corpo narrativo do e-book em uma sequência de listas.

> **Escopo.** Este apêndice é material educacional e analítico. Não constitui parecer jurídico, política de crédito, diagnóstico clínico ou sistema de decisão automatizada. Quando uma informação é temporal, o estado de 27/09/2026 é indicado expressamente. Quando um item provém apenas do registro histórico do projeto e não foi revalidado nesta edição, isso também é declarado.

---

## 1. Como este apêndice se relaciona com o e-book

A 2ª edição do CreditExplain BR foi deliberadamente escrita para ser **lida**, não apenas consultada. Isso exigiu tirar do fluxo principal algumas matrizes, enumerações regulatórias e detalhes que são úteis para auditoria, mas que interrompem a narrativa.

Esses detalhes não foram descartados. Eles foram reorganizados aqui.

A arquitetura documental passa a ser:

```text
README
  ↓
E-book narrativo — docs/miniguia-creditexplain-br.md
  ↓
Apêndice técnico-regulatório — este arquivo
  ↓
Corpus de 77 fontes + refresh — docs/corpus-77-fontes.md
  ↓
Experimentos e cicatrizes — docs/experimentos-e-cicatrizes.md
```

O histórico anterior à v2 continua recuperável pelo Git. Portanto, a nova edição melhora a pedagogia sem apagar a versão que serviu de baseline acadêmica original.

---

# Parte A — Matriz regulatória brasileira

## 2. Crédito responsável, consumidor e superendividamento

| Tema | Base usada no projeto | O que sustenta | Limite de interpretação |
|---|---|---|---|
| Relação de consumo e dever de informação | Código de Defesa do Consumidor — Lei nº 8.078/1990 | proteção do consumidor, informação, práticas de crédito e regime de superendividamento após alterações legais | não fornece fórmula matemática de underwriting |
| Superendividamento | Lei nº 14.181/2021 | prevenção e tratamento do superendividamento da pessoa natural de boa-fé | não equivale a proibição geral de crédito a qualquer pessoa endividada |
| Mínimo existencial | Decreto nº 11.150/2022, com redação do Decreto nº 11.567/2023 | referência jurídica de R$ 600 no regime considerado pelo projeto | não deve ser convertido mecanicamente em threshold de aprovação |
| Educação financeira | Resolução Conjunta nº 8/2023, com alterações posteriores | medidas de educação financeira aplicáveis às instituições alcançadas | alterações posteriores precisam de leitura temporal; a Resolução Conjunta nº 20/2026 possui efeitos em datas próprias |
| Faturas e transparência | Resolução BCB nº 365/2023 e regime relacionado | organização e clareza de informações no cartão de crédito | é exemplo de transparência informacional; não é uma norma de explicabilidade de modelos de IA |

### 2.1. Regra metodológica do projeto

O e-book evita transformar norma de proteção ao consumidor em feature engineering. A passagem de um conceito jurídico para uma regra algorítmica exige uma etapa adicional de desenho, validação e governança.

Exemplo:

```text
Norma: proteger o mínimo existencial
        ↓
NÃO AUTORIZA automaticamente
        ↓
Regra: "aprovar se sobrarem R$ 600"
```

O valor normativo e a decisão de modelagem são objetos diferentes.

---

## 3. Cadastro Positivo, SCR e scoring

### 3.1. Cadastro Positivo

A Lei nº 12.414/2011 integra o núcleo de fontes do projeto para histórico de adimplemento e informações de crédito. O ponto pedagógico não é apresentar o Cadastro Positivo como “base perfeita”, mas mostrar que **qualidade e atualização de dados continuam sendo condições da decisão**.

### 3.2. SCR — Sistema de Informações de Créditos

A fonte institucional do Banco Central foi usada para delimitar o SCR. No escopo documentado pelo projeto:

- há registro individualizado de determinadas operações/exposições de crédito a partir do limite regulatório aplicável;
- o sistema serve à supervisão e à avaliação de risco;
- o acesso consolidado por instituições observa requisitos próprios, incluindo autorização específica e expressa do cliente nas hipóteses descritas pelo Banco Central;
- o SCR **não deve ser descrito como uma base de renda**.

Esse último controle evita uma inferência comum e indevida:

```text
Exposição de crédito ≠ renda
Dívida registrada ≠ capacidade de pagamento completa
Ausência de informação ≠ renda igual a zero
```

### 3.3. Credit scoring e STJ

A Súmula 550 e o REsp 1.419.697/RS foram utilizados para demonstrar que, no contexto jurisprudencial estudado, o credit scoring é reconhecido como método estatístico de avaliação de risco, ao mesmo tempo em que há limites relacionados à privacidade e ao acesso a informações sobre dados valorados e suas fontes.

O projeto não converte esse precedente em licença genérica para:

- usar qualquer dado disponível;
- tratar dado sensível sem fundamento adequado;
- ignorar correção de dados;
- negar qualquer explicação sob alegação automática de segredo empresarial.

---

## 4. LGPD, decisões automatizadas e revisão

O Art. 20 da Lei nº 13.709/2018 é central para o CreditExplain BR porque conecta tratamento automatizado a direitos do titular.

### 4.1. Separação conceitual usada no e-book

| Conceito | Pergunta prática |
|---|---|
| Decisão automatizada | a decisão relevante foi tomada unicamente por tratamento automatizado? |
| Explicação | quais critérios/procedimentos podem ser apresentados de forma clara e adequada dentro do regime aplicável? |
| Segredo comercial/industrial | qual informação pode ser protegida sem esvaziar o direito do titular? |
| Revisão | existe processo capaz de reexaminar materialmente o resultado? |
| Correção | se um dado estiver errado, há caminho para retificação e nova análise? |

### 4.2. Controle contra duas simplificações

O projeto rejeita os dois extremos abaixo:

1. **“LGPD obriga abrir código-fonte e pesos completos do modelo.”** — afirmação excessiva.
2. **“Segredo empresarial permite não explicar nada.”** — simplificação incompatível com a própria lógica de direitos e informações prevista no regime analisado.

A saída de design defendida no e-book é uma explicação **suficientemente informativa para compreensão e contestação, sem prometer transparência absoluta do modelo**.

---

# Parte B — Open Finance com detalhe operacional

## 5. Arquitetura do compartilhamento

O Open Finance não é tratado como um banco centralizado com todos os dados financeiros do cidadão. O projeto adota a arquitetura de compartilhamento padronizado entre instituições participantes, por APIs e segundo as jornadas/regimes aplicáveis.

### 5.1. Jornada conceitual simplificada

```text
Cliente
  ↓
Instituição receptora — define/explica finalidade da jornada
  ↓
Instituição transmissora — autenticação
  ↓
Confirmação/consentimento conforme regras aplicáveis
  ↓
Transmissão padronizada de dados/serviços
  ↓
Uso pela instituição receptora dentro da finalidade e governança aplicáveis
```

A disponibilidade técnica de um campo **não equivale**, por si só, a autorização material para utilizá-lo indiscriminadamente em scoring.

## 6. Temporalidade dos manuais em 27/09/2026

### 6.1. IN BCB nº 759/2026 — Manual de Escopo v8.0

- publicada em 09/07/2026;
- divulga a versão 8.0 do Manual de Escopo de Dados e Serviços do Open Finance;
- incorpora, entre outros pontos, dados e escopo referentes à portabilidade de crédito;
- **entra em vigor em 03/11/2026**.

Consequência para esta edição: a v8.0 pode ser documentada como atualização publicada, mas não deve ser descrita como já vigente em 27/09/2026.

### 6.2. IN BCB nº 760/2026 — Manual de Experiência do Cliente v9.0

- publicada em 09/07/2026;
- divulga a versão 9.0 do Manual de Experiência do Cliente no Open Finance;
- seu foco inclui segurança, clareza, precisão, conveniência e experiência do consentimento/compartilhamento;
- o controle temporal foi atualizado na v2 conforme a publicação oficial consultada.

### 6.3. Regra de uso

Antes de reutilizar o projeto em contexto profissional futuro:

1. consultar a versão consolidada da Resolução Conjunta nº 1/2020;
2. verificar quais manuais estão efetivamente vigentes na data do uso;
3. não confundir data de publicação com data de entrada em vigor.

---

# Parte C — Modelagem, XAI e camada linguística

## 7. Separação entre desempenho, decisão e explicação

O projeto organiza a governança do modelo em três camadas que não se substituem:

### Camada 1 — qualidade preditiva

Perguntas típicas:

- o modelo discrimina risco adequadamente?
- está calibrado?
- houve leakage?
- o conjunto de validação representa a população de uso?
- há drift?

### Camada 2 — regra operacional

Perguntas típicas:

- qual threshold transforma score em ação?
- qual custo de falso positivo/falso negativo?
- há revisão humana?
- a política é compatível com produto e população?

### Camada 3 — explicação

Perguntas típicas:

- a explicação é fiel ao comportamento do modelo?
- é estável?
- distingue associação de causalidade?
- permite correção/contestação?
- a tradução textual acrescentou fato não suportado?

Uma boa Camada 3 não compensa falhas das Camadas 1 e 2.

---

## 8. SHAP — leitura técnica resumida

SHAP é tratado no projeto como técnica de atribuição de contribuição baseada em valores de Shapley.

### 8.1. O que uma atribuição SHAP permite dizer

Formulação adequada:

> “No modelo e na instância analisados, a variável X contribuiu para elevar a saída em relação ao valor de referência.”

### 8.2. O que não permite dizer automaticamente

Formulações que exigem evidência adicional:

- “X causou o risco.”
- “X é a razão econômica real da inadimplência.”
- “Se X mudar, o comportamento real do cliente mudará.”

SHAP descreve comportamento do modelo; causalidade é outro problema metodológico.

---

## 9. LIME — leitura técnica resumida

LIME constrói uma aproximação interpretável na vizinhança de uma observação por meio de perturbações e ajuste de um surrogate local.

### 9.1. Controle fundamental

A explicação é **local**. Ela não deve ser automaticamente generalizada como regra global do modelo.

### 9.2. Estabilidade

Uma auditoria madura deve observar se a explicação é sensível a:

- seed/amostragem;
- definição de vizinhança;
- discretização;
- quantidade de perturbações;
- correlação entre variáveis.

---

## 10. MEMC e fidelidade das explicações

O corpus histórico inclui o uso da **Mean Evaluation of Metrics Change (MEMC)** como referência quantitativa para avaliar técnicas de XAI. A ideia central é perturbar/remover atributos indicados como relevantes e observar mudança em métricas de classificação.

O CreditExplain BR usa esse conceito para sustentar uma regra de engenharia:

> **explicação não deve ser validada apenas porque “parece intuitiva”; seu vínculo com o comportamento do modelo precisa ser testado.**

### 10.1. Limite

Mudança de performance após perturbação é evidência de sensibilidade do modelo às variáveis manipuladas. Não é demonstração automática de causalidade no mundo real.

---

## 11. Framework ML-XAI-LLM — o que é fonte e o que é síntese do projeto

A referência acadêmica central do projeto é o artigo de **Marcelo Massashi Simonae, Marlon Marcon e Dalcimar Casanova**, publicado nos anais do SBSI 2026.

O artigo propõe uma estrutura de duas camadas que combina:

1. modelo preditivo e métodos XAI, incluindo SHAP/LIME;
2. LLM para transformar outputs técnicos em narrativas mais compreensíveis.

O resumo público do trabalho registra estudo experimental aplicado, uso de XGBoost, avaliação de fidelidade com MEMC e protótipo web funcional.

### 11.1. Consistency Guardrail

A documentação pública associada ao trabalho descreve uma lógica de **Consistency Guardrail**, em que a síntese linguística é condicionada à convergência de evidências global/local. No CreditExplain BR, essa ideia é tratada como **controle de consistência**, e não como prova de que dois explicadores concordantes produziram uma verdade causal.

### 11.2. “Tripla salvaguarda”

A primeira edição agrupou didaticamente controles como:

- prompt estruturado;
- filtro de fidelidade/perturbação;
- consistência entre explicadores.

A expressão **“tripla salvaguarda” é síntese pedagógica do CreditExplain BR**. Ela não deve ser atribuída aos autores do artigo como nome oficial da arquitetura sem evidência explícita.

### 11.3. Limites de generalização

O projeto mantém a distinção entre:

```text
Resultado experimental
        ≠
Validação bancária em produção
        ≠
Conformidade regulatória automática
        ≠
Compreensão comprovada por consumidores reais
```

O registro histórico da primeira edição contém detalhes adicionais do dataset e métricas do estudo. Na v2, números específicos que não foram objeto de fresh-read direto do texto integral do artigo não são promovidos a afirmações centrais; permanecem disponíveis no histórico e nas notas do projeto.

---

# Parte D — Reason codes e benchmarks estrangeiros

## 12. Reason codes

Os reason codes são estudados como ferramenta de tradução de motivos e como referência do regime norte-americano de adverse action.

### 12.1. Regra Brasil-first

O CreditExplain BR **não** afirma que ECOA, Regulation B ou circulares do CFPB criam obrigação jurídica no Brasil.

A utilidade comparativa está em uma pergunta de design:

> se o modelo é complexo, a organização consegue ainda apontar motivos específicos, fiéis e compreensíveis para uma decisão?

## 13. União Europeia

O projeto usa GDPR, EU AI Act e EBA como benchmarks de governança e comparação.

Controles:

- não transportar automaticamente artigos do GDPR para a LGPD;
- não apresentar classificação de alto risco do EU AI Act como classificação jurídica brasileira;
- não tratar diretrizes da EBA como obrigação do Banco Central do Brasil.

## 14. Estados Unidos

O projeto usa materiais do CFPB e model risk management como benchmarks.

### 14.1. Atualização de 2026 — SR 26-2

A **SR 26-2**, de 17/04/2026, substituiu SR 11-7 e SR 21-8 no benchmark federal norte-americano consultado. A orientação enfatiza abordagem de model risk management proporcional ao perfil, tamanho, complexidade e uso dos modelos.

No próprio documento do Federal Reserve, a carta é indicada como mais relevante para organizações bancárias supervisionadas pela instituição com mais de US$ 30 bilhões em ativos. Portanto, sua inclusão no e-book é **benchmark técnico**, não regra brasileira nem padrão universal obrigatório.

---

# Parte E — Apostas, impedimentos e fronteira clínica

## 15. Por que esta matriz existe

A primeira edição reuniu vários atos regulatórios de apostas. O corpo narrativo da v2 explica o problema conceitualmente; esta seção preserva o detalhe regulatório de forma auditável.

## 16. Matriz de impedimentos — estado consultado em 27/09/2026

| Grupo/situação | Ato principal registrado | Função na matriz | Observação |
|---|---|---|---|
| Bolsa Família e BPC | Portaria SPA/MF nº 2.217/2025 + IN SPA/MF nº 22/2025 | restringir cadastro/uso dos sistemas de apostas pelos beneficiários alcançados | integrado ao Módulo de Impedidos do SIGAP |
| Novo Desenrola Brasil | Portaria SPA/MF nº 1.237/2026 + IN SPA/MF nº 3/2026 | incluir beneficiários do programa nas hipóteses de vedação e operacionalizar procedimentos | programa/ato específico; não generalizar para qualquer devedor |
| Renegociação Fies — art. 5º-A, §4º-B | Portaria SPA/MF nº 1.638/2026 + IN SPA/MF nº 8/2026 | impedir cadastro/uso pelos beneficiários da renegociação alcançada | distinguir de outros programas Fies |
| Desenrola Adimplentes + Fies Empreendedor | Portaria SPA/MF nº 2.066/2026 + IN MF nº 21/2026 | incluir as duas hipóteses de beneficiários na vedação e operacionalizar procedimentos | manter nomes/programas separados |
| Regras gerais de jogo responsável | Portaria SPA/MF nº 1.231/2024 consolidada e alterações | direitos/deveres, publicidade e controles do ambiente regulado | usar versão consolidada quando houver mudança |
| Autoexclusão e limites prudenciais | Portaria SPA/MF nº 2.579/2025 + IN SPA/MF nº 31/2025 | aperfeiçoar autoexclusão específica/centralizada, cadastro e limites prudenciais | mecanismo de proteção do ecossistema de apostas, não diagnóstico clínico |

### 16.1. Consultas do Módulo de Impedidos

Na implementação divulgada pelo Ministério da Fazenda para Bolsa Família/BPC, os operadores autorizados consultam a base de impedidos:

- na abertura de cadastro;
- no primeiro login do dia;
- periodicamente sobre a base de usuários, conforme regra operacional publicada.

Esse mecanismo é uma obrigação do ecossistema regulado de apostas. Ele **não deve ser transformado em regra de credit scoring bancário**.

---

## 17. Operadores irregulares — Resolução CMN nº 5.320/2026

### Estado temporal

`VIGENTE_DESDE=28/08/2026`

### Escopo

A resolução disciplina o bloqueio de contas e o impedimento de transações financeiras de pessoas naturais e jurídicas que exploram apostas de quota fixa **sem autorização**, quando identificadas no processo regulatório pertinente.

### Prazos centrais registrados

- bloqueio de contas indicadas: até **24 horas** após a notificação da SPA/MF;
- rejeição/impedimento de transações nas hipóteses previstas: também sujeito ao prazo de até **24 horas** da notificação;
- comunicação das providências à SPA/MF: até **48 horas**.

### Controle de interpretação

A norma não sustenta a afirmação:

> “o banco pode bloquear um consumidor porque acha que ele aposta demais.”

O alvo regulatório desta norma é a exploração irregular de apostas pelos operadores/pessoas especificados na notificação, nos termos do regime aplicável.

---

## 18. Autoexclusão, limites e cuidado

A Portaria SPA/MF nº 2.579/2025 aperfeiçoou o regime de jogo responsável e incluiu controles como:

- autoexclusão específica;
- autoexclusão centralizada;
- limites prudenciais obrigatórios;
- requisitos adicionais de cadastro.

No desenho do CreditExplain BR, esses mecanismos ilustram como uma política pública pode criar **instrumentos de proteção sem converter comportamento financeiro em diagnóstico**.

---

## 19. Cadeia de evidência sobre apostas

A cadeia conceitual completa é preservada porque ela é um dos controles mais importantes do projeto:

```text
1. Transação observada
       ↓ exige agregação/contexto
2. Padrão financeiro
       ↓ exige dados de capacidade/vulnerabilidade
3. Vulnerabilidade econômica
       ↓ exige modelo e validação
4. Inferência estatística de risco
       ↓ NÃO autoriza salto automático
5. Diagnóstico clínico
```

O quinto nível pertence ao campo da saúde e demanda avaliação clínica apropriada. Um modelo financeiro não deve produzir diagnóstico de transtorno do jogo.

---

# Parte F — Jurisprudência e estudos de caso

## 20. Uso de decisões judiciais

O corpus contém decisões judiciais específicas, inclusive material do TJSP e TJMG. O projeto as mantém como **estudos de caso**, não como regra universal.

### 20.1. Regra editorial

Uma decisão isolada pode demonstrar:

- como um tribunal tratou determinado conjunto fático;
- quais argumentos foram considerados naquele processo;
- como determinados conceitos foram articulados.

Ela não permite, sozinha, concluir:

- que todos os tribunais decidirão igual;
- que existe súmula/precedente vinculante;
- que a mesma conclusão vale para qualquer contrato ou cliente.

### 20.2. Caso TJSP registrado no corpus

A primeira edição utilizou o processo nº 0000967-51.2024.8.26.0601 como estudo de caso relacionado a apostas, alegações de jogo patológico e responsabilidade bancária.

Na v2, o caso não é usado para criar uma tese geral de “não responsabilidade dos bancos”. O detalhe permanece no corpus/histórico e deve ser relido no inteiro teor antes de qualquer uso jurídico atual.

---

# Parte G — Lacunas e afirmações que foram deliberadamente rebaixadas

## 21. Por que nem todo detalhe da primeira edição foi repetido como fato na v2

Uma revisão robusta não significa conservar toda frase anterior no mesmo nível de certeza. Durante o projeto, alguns tipos de problema foram identificados:

- recomendação técnica apresentada como obrigação;
- benchmark estrangeiro tratado com linguagem brasileira excessiva;
- causalidade sugerida onde havia contribuição preditiva;
- justificativa não sustentada pela fonte;
- atualização normativa posterior ao corte original;
- negativa universal derivada apenas de ausência no corpus.

A v2 preserva **a informação e a cicatriz**, mas pode reduzir o alcance da conclusão.

## 22. Exemplos de rebaixamento controlado

### 22.1. CEP/CONEP

Uma justificativa envolvendo CEP/CONEP para ausência de testes humanos foi identificada como extrapolação não sustentada pela fonte do estudo da UTFPR e chegou a reaparecer em uma reverificação do NotebookLM.

**Estado atual:** não promovida como fato no e-book. A reincidência permanece documentada em `experimentos-e-cicatrizes.md`.

### 22.2. “Blacklist” atribuída ao Banco Mundial

A auditoria histórica identificou atribuição não sustentada de uma proposta de “blacklist”.

**Estado atual:** removida das conclusões; preservada apenas como cicatriz experimental.

### 22.3. Métrica técnica → obrigação regulatória

A primeira edição possuía formulações que podiam fazer técnicas específicas — por exemplo, MEMC ou determinada combinação SHAP/LIME — parecerem requisitos universais de compliance.

**Estado atual:** tratadas como **métodos/controles de engenharia possíveis**, não obrigação legal brasileira.

### 22.4. Recomendação de governança → direito positivado

Painéis, dashboards, portais do titular, notificações proativas e designs de contestação podem ser boas práticas ou recomendações institucionais. Isso não significa que toda forma específica de interface esteja literalmente imposta pela LGPD.

**Estado atual:** separar direito normativo de recomendação de design.

---

# Parte H — Matriz de confiança do material

## 23. Níveis de uso no CreditExplain BR

| Tipo de fonte | Uso preferencial | Cuidado |
|---|---|---|
| lei/decreto/normativo brasileiro | direitos, deveres, proibições e estado regulatório no Brasil | usar texto vigente e controlar temporalidade |
| autoridade brasileira | orientação institucional, explicação operacional, manuais e contexto | distinguir orientação de norma |
| jurisprudência | estudo de aplicação em caso concreto | não generalizar decisão isolada |
| artigo acadêmico peer-reviewed | evidência técnica/metodológica | não promover resultado experimental a norma |
| working paper/preprint | exploração e evidência preliminar | peso menor que publicação consolidada |
| benchmark estrangeiro | comparação e design | sempre identificar jurisdição e não vinculação no Brasil |
| material sintético do projeto | ensino, simulação, demonstração | nunca mascarar dado real ausente |

---

# Parte I — Checklist técnico para um avaliador do CreditExplain BR

## 24. Evidência do projeto

- [x] tema e pergunta norteadora documentados;
- [x] corpus histórico de 77 fontes identificado;
- [x] cinco fontes âncora destacadas;
- [x] hierarquia de fontes preservada;
- [x] experimentos A/B documentados;
- [x] perguntas estratégicas e cicatrizes preservadas;
- [x] separação Brasil × benchmark internacional;
- [x] separação correlação × causalidade;
- [x] separação comportamento financeiro × diagnóstico clínico;
- [x] e-book narrativo v2 publicado no pacote da branch de revisão;
- [x] apêndice técnico-regulatório criado;
- [x] refresh temporal separado do corpus histórico;
- [x] changelog criado;
- [x] proveniência/licenciamento explicitados;
- [x] submissão à DIO registrada como declaração do autor, sem inferência de nota/certificado.

## 25. Limites de reprodutibilidade

- as respostas brutas do NotebookLM e seus marcadores nativos de citação não são republicados integralmente no portfólio público;
- o corpus público é um índice de fontes e não um espelho de todo conteúdo de terceiros;
- alguns fatos históricos do processo permanecem comprovados por documentação interna/Drive e pelo histórico Git, não por cópia integral no repositório;
- uma futura utilização profissional exige novo fresh-read regulatório.

---

# 26. Referências de atualização desta edição

Além das 77 fontes históricas, o refresh de 27/09/2026 utilizou fontes oficiais atuais registradas em `docs/corpus-77-fontes.md`, incluindo:

- Banco Central — Resolução CMN nº 5.320/2026;
- Banco Central — IN BCB nº 759/2026;
- Banco Central — IN BCB nº 760/2026;
- Banco Central — Resolução Conjunta nº 20/2026;
- Ministério da Fazenda/SPA — Módulo de Impedidos e legislação de Jogo Responsável;
- Ministério da Fazenda/SPA — índice atualizado da legislação de apostas de quota fixa;
- Federal Reserve — SR 26-2, usada exclusivamente como benchmark estrangeiro.

O artigo acadêmico central continua sendo:

**SIMONAE, Marcelo Massashi; MARCON, Marlon; CASANOVA, Dalcimar. _Bridging AI and Ethics: An LLM-Based Framework for Transparent and Inclusive Credit Decisions_. Proceedings of the 22nd Brazilian Symposium on Information Systems — SBSI 2026, p. 364–383. DOI 10.5753/sbsi.2026.248352.**

---

# Conclusão do apêndice

O objetivo deste arquivo é impedir duas perdas de qualidade igualmente ruins:

1. transformar o e-book em uma lista interminável de atos, métricas e exceções; ou
2. melhorar a narrativa removendo a densidade técnica que tornou o projeto relevante.

A solução adotada é uma publicação em **duas camadas complementares**:

- **e-book narrativo:** ensina o problema e conecta os conceitos;
- **apêndice técnico-regulatório:** permite conferir detalhe, escopo, temporalidade e decisões editoriais.

Assim, o CreditExplain BR deixa de ser apenas um mapa de tópicos sem sacrificar a rastreabilidade construída durante a pesquisa.
