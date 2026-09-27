# CreditExplain BR
## Crédito responsável, IA, Open Finance e explicabilidade no Brasil

**2ª edição — revisada e ampliada**  
**Revisão editorial e normativa:** 27/09/2026  
**Origem acadêmica:** DIO Bootcamp Bradesco — GenAI, Dados & Cyber  
**Desafio:** “Treinando uma IA de Aprendizagem: Explore o Poder do NotebookLM”  
**Corpus histórico do projeto:** 77 fontes curadas e auditadas  

> **Escopo e integridade.** Este e-book é material educacional e analítico. Não constitui parecer jurídico, recomendação individual de crédito, política real de concessão, diagnóstico clínico, laudo de saúde, consultoria de investimentos nem sistema automatizado em produção. As normas brasileiras são tratadas como fonte primária quando o tema é obrigação, direito ou proibição no Brasil; fontes estrangeiras aparecem como benchmark comparativo. Exemplos não vinculados a casos reais são **MATERIAL DIDÁTICO FICTÍCIO/SINTÉTICO**.

---

## Nota editorial da segunda edição

A primeira versão deste material cumpria bem o papel de **miniguia de revisão**: concentrava conceitos, normas, técnicas e resultados do projeto em uma estrutura rápida de consultar. Essa mesma característica, porém, limitava sua utilidade como leitura formativa. Havia informação, mas muitas vezes ela aparecia em formato de tópicos, enumerações e definições condensadas. Para quem já dominava o assunto, isso funcionava como mapa. Para quem queria **aprender o raciocínio por trás do mapa**, faltava uma narrativa que conectasse causa, consequência, contexto e aplicação.

Esta segunda edição foi reescrita para resolver esse problema. O objetivo não é aumentar páginas por volume, e sim transformar a pesquisa em **compreensão transferível**. Por isso, os capítulos agora explicam por que cada tema importa, como os conceitos se conectam, onde começam e terminam os direitos e obrigações, o que uma técnica de IA realmente demonstra, o que ela não demonstra e como traduzir resultados técnicos para pessoas não especialistas sem criar uma falsa sensação de certeza.

O projeto original foi fechado com corte documental em **22/08/2026**. A edição atual preserva essa proveniência, mas incorpora um **refresh normativo em 27/09/2026** para pontos materiais que mudaram depois do corte. Um exemplo importante é a Resolução CMN nº 5.320/2026: na primeira edição ela ainda era norma publicada com vigência futura; nesta edição ela já é tratada como vigente desde 28/08/2026.

O histórico da versão anterior permanece preservado pelo Git. A pesquisa de 77 fontes continua documentada em [`corpus-77-fontes.md`](corpus-77-fontes.md), e os testes com NotebookLM, incluindo falhas e correções, permanecem em [`experimentos-e-cicatrizes.md`](experimentos-e-cicatrizes.md).

---

# Parte I — Por que explicar o crédito ficou tão importante

## 1. Crédito não é apenas um “sim” ou “não”

Quando alguém solicita crédito, o resultado que aparece na tela costuma ser extremamente simples: aprovado, negado, limite concedido, taxa oferecida ou pedido sujeito a análise adicional. Por trás dessa simplicidade existe uma decisão muito mais complexa. A instituição precisa estimar a probabilidade de pagamento, o tamanho de uma eventual perda, a capacidade de absorver risco, o custo de capital, o comportamento esperado da carteira e uma série de restrições operacionais e regulatórias.

Durante décadas, parte relevante desse trabalho foi realizada com regras de negócio e modelos estatísticos relativamente interpretáveis. Um analista conseguia explicar uma regressão logística, uma política de renda mínima ou um conjunto de critérios de comprometimento de renda com razoável clareza. O avanço do aprendizado de máquina alterou esse equilíbrio. Modelos como gradient boosting, XGBoost, Random Forest e redes neurais podem capturar interações que uma regra manual dificilmente perceberia. Isso pode melhorar previsão, mas cria um novo problema: **quanto maior a capacidade de encontrar padrões, maior pode ser a distância entre o resultado matemático e uma explicação compreensível para a pessoa afetada**.

Esse problema é maior do que uma questão de experiência do usuário. Uma pessoa que recebe uma recusa de crédito pode precisar saber se o resultado decorreu de dados incorretos, de um histórico efetivamente observado, de uma variável que funciona como proxy de outra característica ou de uma política de risco legítima. A instituição, por sua vez, precisa distinguir entre “o modelo encontrou um padrão” e “o padrão é adequado, lícito, estável e justificável”.

É nesse ponto que o CreditExplain BR se posiciona. O projeto não parte da ideia de que todo modelo complexo é indevido, nem da ideia oposta de que maior acurácia resolve todos os problemas. Ele parte de uma pergunta mais difícil:

> **Como usar dados e modelos avançados para apoiar decisões de crédito sem perder transparência, proteção do consumidor, governança de dados e capacidade de contestação?**

A resposta exige cruzar disciplinas. Direito do consumidor, proteção de dados, ciência de dados, model risk management, Open Finance, experiência do cliente e explicabilidade algorítmica deixam de ser assuntos separados. Eles passam a formar uma única cadeia de responsabilidade.

### 1.1. Previsão não é certeza

Um modelo de risco não “descobre quem vai inadimplir”. Ele estima probabilidades a partir de padrões observados em dados passados. Essa distinção é fundamental. Um cliente com probabilidade estimada de inadimplência de 12% não é um inadimplente “em 12%”, nem alguém condenado a não pagar. Ele pertence a um conjunto de perfis que, sob determinadas condições e segundo um modelo específico, apresentou determinado comportamento estatístico.

A diferença parece semântica, mas muda toda a governança. Quando uma previsão é apresentada como certeza, o sistema tende a esconder incerteza, erro de medição e mudança de contexto. Quando é tratada como estimativa, abrem-se perguntas úteis: qual foi a base de treino? Qual período econômico ela representa? A distribuição dos clientes mudou? Há grupos para os quais o erro é maior? O dado usado continua correto? O threshold de decisão faz sentido para o objetivo de negócio?

### 1.2. O custo do erro é assimétrico

Em classificação de crédito, dois erros recebem atenção especial. O primeiro é aprovar alguém que depois não paga. O segundo é rejeitar alguém que pagaria. Para a instituição, o primeiro pode gerar perda financeira. Para o consumidor, o segundo pode significar exclusão de uma oportunidade econômica legítima. Ambos importam, mas não têm a mesma consequência para todas as partes.

Por isso, “o modelo com maior acurácia” não é automaticamente o melhor modelo. Se uma base contém 95% de bons pagadores, um classificador ingênuo que sempre prevê “bom pagador” já teria 95% de acurácia — e seria inútil para identificar risco. Métricas precisam ser lidas no contexto de custo, prevalência da classe, estratégia comercial e impacto sobre pessoas.

Essa lógica reaparece em todo este e-book: **uma métrica isolada raramente é suficiente para governar uma decisão complexa**.

---

# Parte II — Crédito responsável no contexto brasileiro

## 2. O que significa “crédito responsável”

Crédito responsável não significa simplesmente conceder menos crédito. Também não significa que uma instituição deva aprovar toda proposta desde que o consumidor queira assumir o risco. O conceito envolve uma combinação de informação adequada, avaliação responsável, prevenção de práticas abusivas, proteção contra superendividamento e desenho de produtos que não explorem assimetrias de informação.

A Lei nº 14.181/2021, conhecida como Lei do Superendividamento, alterou o Código de Defesa do Consumidor e reforçou a lógica de prevenção. O ponto central é reconhecer que o crédito pode ser um instrumento de mobilidade econômica e, ao mesmo tempo, tornar-se fonte de deterioração financeira quando oferecido ou utilizado de forma incompatível com a capacidade real de pagamento.

O **superendividamento** é tratado juridicamente como a impossibilidade manifesta de o consumidor pessoa natural, de boa-fé, pagar a totalidade de suas dívidas de consumo, exigíveis e vincendas, sem comprometer seu mínimo existencial. A definição importa porque desloca o foco de uma dívida isolada para a **situação financeira global do consumidor**.

### 2.1. O mínimo existencial não é um “score de aprovação”

O Decreto nº 11.150/2022, com redação dada pelo Decreto nº 11.567/2023, utiliza **R$ 600,00** como referência de mínimo existencial para a prevenção, tratamento e conciliação de situações de superendividamento. O valor tem uma função jurídica específica. Ele não deve ser transformado mecanicamente em regra de concessão do tipo “se sobram R$ 600, o crédito é responsável”.

Essa distinção evita um erro frequente de tradução entre norma e algoritmo. Uma norma pode estabelecer uma proteção mínima dentro de um procedimento jurídico sem oferecer, por isso, uma fórmula de underwriting. Em uma política real de crédito, capacidade de pagamento depende de renda, despesas, outras obrigações, estabilidade financeira, produto, prazo, juros, garantias e contexto. O mínimo existencial é uma referência protetiva; não substitui avaliação prudencial nem análise individualizada.

### 2.2. Informação clara é parte da própria gestão de risco

A Resolução BCB nº 365/2023, vigente desde 1º de julho de 2024, reorganizou a apresentação de informações da fatura de cartão de crédito. A lógica é simples e poderosa: se o consumidor não entende valor total, vencimento, alternativas de pagamento, encargos e custo efetivo, uma decisão formalmente disponível pode não ser materialmente compreensível.

Esse exemplo ajuda a entender por que explicabilidade não é apenas “mostrar como a IA funciona”. Muitas vezes, a melhor explicação é aquela que organiza a informação na ordem em que uma pessoa precisa dela para agir. Um gráfico sofisticado de SHAP pode ser tecnicamente correto e ainda assim inútil para um consumidor. Da mesma forma, uma explicação textual simples pode ser útil, desde que não esconda limitações ou invente causalidade.

A Resolução Conjunta nº 8/2023 estabeleceu medidas de educação financeira para instituições autorizadas pelo Banco Central, e foi posteriormente alterada pela Resolução Conjunta nº 20/2026. Para o CreditExplain BR, a lição é que **educação financeira e transparência não devem ser tratadas como adereços de comunicação**. Elas fazem parte do ambiente de decisão responsável.

### 2.3. Credit scoring é lícito, mas não é uma zona sem limites

A Súmula 550 do Superior Tribunal de Justiça consolidou entendimento relevante sobre credit scoring. O STJ registra que o escore de crédito, como método estatístico de avaliação de risco, dispensa consentimento do consumidor para sua utilização nos termos ali analisados, mas assegura ao consumidor o direito de solicitar esclarecimentos sobre as informações pessoais valoradas e as fontes dos dados considerados no cálculo.

Esse precedente precisa ser lido com precisão. Ele não equivale a uma autorização genérica para qualquer tratamento de dado, qualquer variável ou qualquer forma de decisão. O próprio REsp 1.419.697/RS enfatiza limites de privacidade, transparência e uso de informações adequadas, e reconhece a possibilidade de abuso quando são utilizados dados excessivos, sensíveis, incorretos ou desatualizados.

Para um projeto de IA, a consequência prática é clara: **um score pode ser legítimo e ainda assim sua implementação concreta ser problemática**. A avaliação não termina na pergunta “é permitido usar score?”. Ela começa ali.

---

## 3. De onde vêm os dados usados para compreender risco

Uma decisão de crédito só é tão confiável quanto os dados que a sustentam. Em termos simplificados, um modelo pode receber informações declaradas pelo cliente, dados cadastrais, histórico de relacionamento, informações de crédito, dados obtidos por compartilhamento autorizado e variáveis derivadas dessas fontes. Cada origem tem finalidade, qualidade e regras próprias.

### 3.1. Cadastro Positivo: histórico de adimplemento como informação econômica

A Lei nº 12.414/2011 estruturou o Cadastro Positivo. A ideia é complementar uma visão baseada apenas em ocorrências negativas com histórico de obrigações e pagamentos. Em termos de modelagem, isso amplia a possibilidade de diferenciar perfis que, sob uma ótica meramente negativa, poderiam parecer semelhantes.

Mas mais dados não eliminam a necessidade de qualidade. Um histórico incorreto ou desatualizado pode amplificar erro quando alimenta uma cadeia automatizada. Em sistemas modernos, o problema raramente está em um único banco de dados. Ele pode surgir na integração entre origem, transformação, feature engineering, modelo e interface de decisão.

### 3.2. SCR: o que o sistema mostra — e o que ele não mostra

O Sistema de Informações de Créditos (SCR) do Banco Central registra de forma individualizada operações e exposições de crédito quando o risco direto do cliente na instituição atinge **R$ 200,00 ou mais**. O sistema é alimentado mensalmente por instituições e serve tanto à supervisão quanto à avaliação de risco.

Para consulta das informações consolidadas de um cliente por uma instituição, o Banco Central informa a necessidade de **autorização específica e expressa** do cliente. Isso é diferente de afirmar que o SCR é uma base de renda ou que contém tudo o que uma instituição precisa saber sobre a situação econômica de uma pessoa.

O SCR informa exposição e histórico de crédito, não “salário verdadeiro”. Esse cuidado é particularmente importante quando se tenta calcular comprometimento de renda ou interpretar sinais de vulnerabilidade. Uma variável ausente não pode ser fabricada a partir de outra que mede fenômeno distinto.

### 3.3. Open Finance: compartilhamento controlado, não “banco de dados gigante”

O Open Finance brasileiro é frequentemente descrito de forma imprecisa como se fosse uma central que armazena todos os dados financeiros dos clientes. Essa imagem está errada. O modelo é baseado em **compartilhamento padronizado entre instituições participantes**, por APIs, conforme consentimento ou autorização do cliente nas jornadas aplicáveis.

O Banco Central explica que o cliente inicia a jornada na instituição que deseja receber seus dados, verifica finalidade e condições, autentica-se na instituição que mantém os dados e confirma o compartilhamento. Os dados são enviados da instituição transmissora para a recebedora; não são despejados em um grande repositório central do Open Finance.

Essa arquitetura importa por três razões. Primeiro, reduz a tentação de imaginar um “perfil financeiro estatal completo”. Segundo, deixa claro que governança depende das duas instituições envolvidas e das APIs que realizam a transmissão. Terceiro, torna o consentimento uma **jornada operacional**, não apenas uma caixa de seleção jurídica.

Em 2025, o Banco Central atualizou a explicação sobre participação obrigatória: além de instituições S1 e S2, determinadas instituições ou conglomerados com mais de cinco milhões de clientes passaram a integrar hipóteses de transmissão obrigatória, e existem regras próprias para serviços de pagamento. Em julho de 2026, o BC publicou novas versões dos manuais de escopo de dados e de experiência do cliente. Isso ilustra um ponto importante: Open Finance é infraestrutura regulatória viva. Uma análise séria precisa consultar a versão vigente do regramento e dos manuais, não memorizar uma fotografia antiga.

### 3.4. Por que Open Finance pode melhorar — e complicar — o crédito

Do ponto de vista de risco, Open Finance pode ampliar a visão sobre fluxo de caixa, compromissos financeiros e relacionamento. Para um trabalhador autônomo com pouca informação tradicional, dados transacionais podem revelar regularidade de entradas que um score convencional não captura. Para uma pequena empresa, podem ajudar a demonstrar capacidade operacional de forma mais granular.

Ao mesmo tempo, mais granularidade cria risco de sobreinterpretação. Um modelo pode descobrir correlações fortes que não deveriam ser tratadas como explicações causais. Pode aprender proxies de localização, padrão de consumo ou comportamento social. Pode amplificar diferenças históricas. Pode ainda tornar a decisão quase impossível de explicar se centenas de variáveis derivadas forem usadas sem uma arquitetura de governança.

Por isso, a promessa do Open Finance não é “quanto mais dados, melhor”. A promessa mais defensável é: **dados mais relevantes, obtidos em contexto adequado, podem permitir decisões mais individualizadas — se houver finalidade, qualidade, segurança, governança e capacidade de explicação**.

---

# Parte III — O que a inteligência artificial realmente muda

## 4. Do score tradicional ao machine learning

Modelos de crédito tradicionais costumam trabalhar com relações relativamente estáveis entre atributos e resultado. Uma regressão logística, por exemplo, pode produzir coeficientes que ajudam a explicar a direção e a intensidade de uma associação. Isso não significa que modelos tradicionais sejam automaticamente justos ou transparentes, mas a estrutura matemática costuma ser mais fácil de inspecionar.

Modelos baseados em árvores e boosting conseguem representar relações não lineares, interações e efeitos condicionais. Uma variável pode ter impacto diferente dependendo da combinação com outras. Essa flexibilidade pode melhorar performance, principalmente quando o problema possui padrões complexos.

O custo é a perda de legibilidade direta. Em um modelo XGBoost com centenas de árvores, não existe um único coeficiente simples que responda por toda a decisão. É nesse ambiente que surgem técnicas de **Explainable AI (XAI)**.

### 4.1. Performance, calibração e threshold são coisas diferentes

Imagine um modelo que estime probabilidade de inadimplência. A saída pode ser 0,08 para um cliente e 0,31 para outro. A política de negócio precisa então decidir em que ponto transformar probabilidade em ação. Esse ponto é o **threshold**.

Mudar o threshold pode aumentar aprovação ou reduzir inadimplência, mas sempre altera o equilíbrio de erros. Por isso, uma análise madura separa pelo menos três perguntas:

1. **Discriminação:** o modelo ordena razoavelmente clientes de maior e menor risco?
2. **Calibração:** probabilidades previstas correspondem à frequência observada?
3. **Decisão:** o threshold usado é compatível com custo, produto, estratégia e impacto?

Explicabilidade entra depois dessas perguntas, não no lugar delas. Um modelo perfeitamente explicável e mal calibrado continua sendo um modelo ruim. Da mesma forma, um modelo muito preciso e impossível de governar pode ser inadequado para um caso de uso sensível.

### 4.2. Data drift: quando o passado deixa de representar o presente

Modelos aprendem a partir de distribuições históricas. Se o contexto muda, a relação entre variáveis e resultado também pode mudar. Inflação, desemprego, novas formas de pagamento, mudanças regulatórias, alterações na oferta de crédito e transformações de comportamento podem modificar a base de clientes.

**Data drift** descreve mudanças na distribuição dos dados de entrada. **Concept drift** descreve mudança na relação entre entrada e resultado. Ambos exigem monitoramento.

Em crédito, drift é especialmente relevante porque uma explicação pode continuar parecendo plausível mesmo quando o modelo já perdeu qualidade. Uma narrativa bonita produzida por uma camada de IA generativa não corrige um classificador desatualizado. Por isso, qualquer arquitetura que traduza explicações precisa receber como entrada um modelo previamente monitorado e validado.

### 4.3. Model risk é risco de decisão, não só risco de código

Em 2026, as agências bancárias federais dos Estados Unidos publicaram a **SR 26-2 — Revised Guidance on Model Risk Management**, substituindo a histórica SR 11-7. Embora não seja norma brasileira, o documento é um benchmark útil porque reforça uma ideia central: model risk pode produzir perdas, erros de reporte e decisões inadequadas, e deve ser gerido de forma proporcional à natureza, escala e uso do modelo.

Isso ajuda a deslocar a discussão de “o algoritmo funciona?” para “o sistema de decisão é governado?”. Um modelo pode executar sem bugs e ainda gerar risco porque foi treinado na população errada, porque recebe dados inadequados, porque foi aplicado a finalidade diferente da original ou porque ninguém revisou seus resultados após mudança de contexto.

---

## 5. Dados alternativos: inclusão financeira ou nova forma de exclusão?

Uma das promessas mais atraentes de IA em crédito é usar dados alternativos para avaliar pessoas com pouco histórico tradicional. Estudos e relatórios do World Bank, IFC, BIS e literatura acadêmica mostram o potencial de dados transacionais, footprints digitais e outras fontes para ampliar capacidade preditiva.

A lógica econômica é compreensível. Se uma pessoa trabalha como autônoma e não possui holerite, um fluxo recorrente de recebimentos pode conter informação relevante sobre sua estabilidade financeira. Se uma pequena empresa tem histórico de vendas e pagamentos consistente, isso pode ser mais informativo do que uma única declaração cadastral.

O risco aparece quando “dado alternativo” se transforma em “qualquer dado disponível”. Um algoritmo consegue encontrar correlações em quase tudo. A questão de governança é decidir quais correlações são apropriadas para influenciar crédito.

### 5.1. Proxy não é neutralidade

Uma variável não precisa conter explicitamente raça, gênero ou outra característica protegida para carregar parte dessa informação. CEP, padrão de consumo, dispositivo usado, horários de atividade e rede de relacionamentos podem funcionar como **proxies** dependendo do contexto.

Isso não significa que toda variável correlacionada deva ser automaticamente proibida. Significa que a equipe precisa investigar impacto, necessidade e proporcionalidade. O dado melhora materialmente a avaliação de risco? Existe uma alternativa menos invasiva? O ganho de performance compensa o risco de discriminação indireta? O modelo erra mais para determinados grupos? A variável continua necessária ao longo do tempo?

### 5.2. Correlação, causalidade e justificativa

Se clientes que usam determinada categoria de serviço apresentam maior inadimplência na base histórica, isso não prova que o serviço “causa” inadimplência. Pode haver variáveis omitidas, contexto socioeconômico ou seleção de amostra.

Essa diferença é decisiva na comunicação. Uma explicação responsável pode dizer: “essa variável contribuiu para a estimativa do modelo”. Não deve automaticamente dizer: “essa variável é a causa do seu risco”. Técnicas como SHAP e LIME ajudam a descrever comportamento do modelo; não transformam correlações em causas.

---

# Parte IV — Explicabilidade sem simplificações perigosas

## 6. Interpretabilidade e explicabilidade não são sinônimos perfeitos

Um modelo **intrinsecamente interpretável** possui estrutura que pode ser compreendida diretamente em nível adequado ao problema. Uma regressão linear simples ou uma árvore de decisão pequena são exemplos intuitivos.

Um método **post-hoc** tenta explicar o comportamento de um modelo depois de ele já ter sido treinado. SHAP e LIME pertencem a essa família em muitos usos. Eles não “abrem a mente” do algoritmo como se revelassem uma intenção oculta. Eles constroem representações úteis sobre como as entradas influenciam determinadas saídas.

Essa distinção ajuda a evitar marketing exagerado. Uma instituição não deve afirmar que “SHAP prova por que o algoritmo decidiu”. Formulações mais rigorosas são: “SHAP estima contribuições de atributos para a saída do modelo segundo sua estrutura matemática” ou “LIME aproxima localmente o comportamento do modelo em torno de uma instância”.

### 6.1. Explicação global e explicação local

Uma explicação **global** pergunta como o modelo se comporta em uma população ou conjunto de dados. Quais variáveis tendem a ser mais influentes? Existem regiões onde a resposta muda abruptamente? Há dependência excessiva de determinado atributo?

Uma explicação **local** pergunta o que aconteceu em uma observação específica. Quais fatores contribuíram para esta previsão? A decisão mudaria se uma variável fosse diferente? A explicação é estável a pequenas perturbações?

Misturar os dois níveis produz erros. Uma variável importante globalmente pode ser pouco relevante para um cliente específico. Uma variável decisiva em uma predição local pode não ser dominante na carteira como um todo.

---

## 7. SHAP: o que ele explica e como ler sem exagerar

SHAP, abreviação de **SHapley Additive exPlanations**, deriva de ideias dos valores de Shapley da teoria dos jogos cooperativos. Em termos intuitivos, o método distribui a diferença entre uma previsão e um valor de referência entre as variáveis de entrada.

Imagine um modelo de inadimplência cujo valor de referência para determinada população seja 10%. Para um cliente, o modelo estima 18%. A explicação SHAP pode mostrar que algumas características empurraram a previsão para cima e outras para baixo. O resultado não precisa ser convertido em causalidade. Ele descreve **contribuição dentro do modelo**.

### 7.1. Um exemplo didático

Suponha o seguinte cenário sintético:

- referência do modelo: risco de 10%;
- risco previsto: 18%;
- utilização elevada de limite: contribuição positiva para risco;
- histórico de pagamentos pontuais: contribuição negativa para risco;
- curto tempo de relacionamento: contribuição positiva moderada.

Uma explicação inadequada seria:

> “Seu risco aumentou porque você utiliza muito o limite e tem pouco tempo de relacionamento.”

A frase parece natural, mas sugere causalidade. Uma versão mais rigorosa seria:

> “No modelo utilizado nesta simulação, a utilização elevada do limite e o menor tempo de relacionamento contribuíram para elevar a estimativa de risco em relação ao valor de referência, enquanto o histórico de pagamentos pontuais contribuiu na direção oposta.”

Essa segunda formulação mantém três proteções: identifica que se trata de comportamento **do modelo**, explicita que há fatores em direções diferentes e evita afirmar causa real.

### 7.2. SHAP não resolve tudo

Mesmo uma atribuição matematicamente consistente depende do modelo e dos dados de entrada. Se o modelo aprendeu relação inadequada, SHAP pode explicar com precisão um comportamento que não deveria existir. Se duas variáveis são fortemente correlacionadas, a distribuição de contribuição pode ser sensível à forma como dependência é tratada. Se os dados são enviesados, a explicação não remove o viés.

O papel de SHAP é iluminar comportamento; governança ainda precisa avaliar legitimidade, qualidade e impacto.

---

## 8. LIME: uma aproximação local que precisa de estabilidade

LIME, ou **Local Interpretable Model-Agnostic Explanations**, cria perturbações ao redor de uma observação e observa como o modelo responde. Com essas amostras, ajusta um modelo interpretável simples que aproxima o comportamento do modelo complexo naquela região.

A palavra mais importante é **local**. LIME não pretende representar o modelo inteiro. Ele tenta responder “como o modelo se comportou próximo deste caso?”.

### 8.1. Por que isso é útil

Se um modelo possui milhares de regras implícitas, um surrogate local pode indicar quais características tiveram maior peso na vizinhança de uma decisão. Para auditoria de casos, isso é valioso porque permite comparar explicações entre clientes e investigar resultados atípicos.

### 8.2. Por que estabilidade importa

Como LIME envolve perturbações e escolhas de vizinhança, duas execuções podem produzir diferenças se configuração e amostragem não forem controladas. Por isso, uma explicação local não deve ser aceita apenas porque parece intuitiva. É recomendável testar estabilidade, sensibilidade a parâmetros e coerência com outros métodos.

No CreditExplain BR, a comparação entre SHAP e LIME foi estudada como uma forma de reduzir dependência de um único explicador. Concordância entre métodos pode aumentar confiança operacional, mas **não transforma concordância em prova de causalidade**.

---

## 9. Reason codes: explicar a decisão em linguagem acionável

No mercado norte-americano, a ECOA e a Regulation B exigem razões específicas para determinadas ações adversas de crédito. O CFPB Circular 2022-03 reforçou que o uso de algoritmos complexos não elimina essa obrigação: a instituição não pode dizer simplesmente “o algoritmo decidiu”.

Esse regime é estrangeiro e não deve ser apresentado como obrigação brasileira. Ainda assim, é um benchmark extremamente útil porque traduz uma preocupação técnica em requisito de comunicação: **uma decisão automatizada precisa ser conectada a razões compreensíveis e efetivamente relacionadas aos fatores considerados**.

No Brasil, a LGPD e a jurisprudência sobre scoring criam um conjunto próprio de direitos e limites. O Art. 20 da LGPD assegura a possibilidade de solicitar revisão de decisões tomadas unicamente com base em tratamento automatizado que afetem interesses do titular e prevê, quando solicitadas, informações claras e adequadas sobre critérios e procedimentos utilizados, observados segredos comercial e industrial. A Súmula 550 do STJ, em seu contexto, reconhece o direito do consumidor de solicitar esclarecimentos sobre informações pessoais valoradas e fontes dos dados usados no scoring.

A lição de design é importante: **reason code não deveria ser sinônimo de “frase padrão”**. Uma explicação útil precisa conectar decisão, dados e caminho de contestação.

---

# Parte V — Do XAI para linguagem humana: o framework ML-XAI-LLM

## 10. O problema que o framework tenta resolver

Mesmo quando SHAP e LIME produzem resultados tecnicamente válidos, a saída ainda pode ser inacessível a quem não trabalha com ciência de dados. Um cliente não precisa receber um vetor de contribuições em log-odds. Ele precisa compreender, em linguagem proporcional ao contexto, quais fatores foram relevantes e o que pode ser conferido ou corrigido.

O artigo **“Bridging AI and Ethics: An LLM-Based Framework for Transparent and Inclusive Credit Decisions”**, de Marcelo Massashi Simonae, Marlon Marcon e Dalcimar Casanova, apresentado no SBSI 2026, propõe uma arquitetura em duas camadas: uma camada preditiva/XAI e uma camada linguística baseada em LLM para traduzir resultados técnicos em narrativas mais acessíveis.

O CreditExplain BR trata esse trabalho como **referência acadêmica**, não como padrão regulatório nem arquitetura comprovada para produção bancária.

### 10.1. A primeira camada: modelo e explicadores

Na camada técnica, um classificador produz a previsão e métodos de XAI ajudam a identificar fatores relevantes. O artigo trabalha com XGBoost e técnicas como SHAP e LIME. A pesquisa também discute uma métrica denominada **MEMC — Mean Evaluation of Metrics Change** para avaliar fidelidade das técnicas de explicação por meio de mudanças de métricas após perturbação ou remoção de atributos relevantes.

O ponto conceitual é mais importante que uma leitura literal da métrica: uma explicação precisa ser **testada**, não apenas exibida. Se uma técnica afirma que determinadas variáveis são decisivas, é razoável investigar se perturbar essas variáveis altera de fato o comportamento do modelo.

### 10.2. A segunda camada: tradução, não invenção

A camada de LLM recebe informação estruturada e transforma o conteúdo em linguagem natural. O risco óbvio é a alucinação: o modelo de linguagem pode enriquecer a narrativa com fatos não presentes na evidência.

Por isso, uma arquitetura responsável deveria impor uma fronteira rigorosa:

> **O LLM pode mudar a forma de expressão; não pode mudar a substância dos dados.**

Se o JSON de entrada diz apenas que “tempo de relacionamento” contribuiu negativamente, o LLM não pode inventar que a pessoa “mudou frequentemente de emprego”, “tem renda instável” ou “deveria comprar determinado produto”. Tradução semântica não autoriza inferência cadastral.

### 10.3. O que o estudo demonstra — e o que não demonstra

O corpus do CreditExplain BR registra que o trabalho acadêmico utiliza uma base pública de varejo com 10.476 registros e 17 atributos. O estudo relata desempenho muito elevado em parte dos experimentos e utiliza MEMC para analisar fidelidade de explicações.

Isso é evidência de viabilidade experimental, não prova de generalização bancária. Uma carteira real pode ter milhões de clientes, variáveis altamente correlacionadas, mudanças macroeconômicas, novos produtos, erros cadastrais, regras regulatórias, diferentes populações e custos assimétricos.

Também não houve, segundo a documentação analisada no projeto, validação de campo extensa com consumidores reais para demonstrar que uma narrativa produzida pelo LLM é efetivamente mais compreensível, justa ou acionável em produção.

A conclusão equilibrada é que o framework é **promissor como arquitetura de pesquisa e design**, mas precisa de validação adicional para uso operacional de alto impacto.

### 10.4. Uma arquitetura de explicação responsável inspirada no estudo

A síntese pedagógica do CreditExplain BR propõe uma cadeia de controles:

```text
Dados autorizados e validados
          ↓
Modelo preditivo monitorado
          ↓
Explicadores XAI (ex.: SHAP / LIME)
          ↓
Teste de fidelidade e estabilidade
          ↓
Filtro de evidência estruturada
          ↓
LLM como tradutor semântico
          ↓
Validação automática de factualidade
          ↓
Revisão humana proporcional ao risco
          ↓
Explicação + canal de correção/contestação
```

A palavra-chave é **cadeia**. Nenhuma etapa corrige automaticamente a anterior. XAI não corrige dados ruins. LLM não corrige XAI inadequado. Revisão humana superficial não corrige um processo que apenas carimba a decisão algorítmica.

---

# Parte VI — LGPD, revisão e contestabilidade

## 11. O Art. 20 da LGPD na prática

A Lei Geral de Proteção de Dados prevê que o titular pode solicitar revisão de decisões tomadas unicamente com base em tratamento automatizado de dados pessoais que afetem seus interesses, incluindo decisões destinadas a definir perfil pessoal, profissional, de consumo e de crédito.

A lei também prevê que o controlador forneça, sempre que solicitado, informações claras e adequadas sobre critérios e procedimentos utilizados para a decisão automatizada, respeitados os segredos comercial e industrial. A ANPD, em materiais de orientação ao titular, descreve ainda a possibilidade de solicitar explicação sobre critérios e procedimentos.

A leitura responsável precisa evitar dois extremos.

O primeiro extremo seria dizer que a LGPD obriga toda instituição a revelar código-fonte, pesos completos e propriedade intelectual. O texto legal preserva segredos comercial e industrial.

O segundo extremo seria concluir que basta invocar segredo empresarial e não explicar nada. Essa interpretação esvaziaria o próprio direito a informações claras e adequadas.

A governança precisa, portanto, construir uma explicação **suficientemente informativa para permitir compreensão e contestação sem exigir divulgação integral do modelo**.

### 11.1. Revisão humana precisa ser material

Uma revisão que apenas repete o resultado do modelo não muda substancialmente a decisão automatizada. A discussão regulatória internacional e notas técnicas da ANPD reforçam a importância de participação humana significativa quando ela é usada como salvaguarda.

Um revisor humano precisa ter autoridade, informação e tempo para questionar o resultado. Isso exige acesso aos dados relevantes, motivos da decisão, limites do modelo e mecanismos para corrigir informação incorreta.

### 11.2. Contestabilidade como propriedade do sistema

Contestabilidade não é um botão escrito “contestar”. Um sistema é contestável quando:

- a pessoa consegue saber que houve decisão automatizada relevante;
- recebe explicação compatível com seu nível de compreensão;
- consegue identificar quais dados podem estar errados;
- existe canal de correção;
- existe processo para revisão;
- o processo registra o que foi revisto e por quê;
- o resultado da revisão pode, de fato, alterar a decisão quando houver fundamento.

Essa visão transforma explicabilidade em arquitetura de serviço. O desafio deixa de ser apenas gerar um texto e passa a ser **desenhar uma jornada de confiança**.

---

## 12. Um modelo de governança em sete perguntas

Antes de colocar IA em uma decisão de crédito, uma instituição poderia responder, no mínimo, às seguintes perguntas.

### Pergunta 1 — Qual problema estamos tentando resolver?

“Usar IA” não é objetivo. O objetivo pode ser reduzir tempo de análise, melhorar previsão de inadimplência, ampliar inclusão de clientes sem histórico ou detectar inconsistências. Quanto mais claro o problema, mais fácil avaliar se IA é necessária.

### Pergunta 2 — Quais dados são realmente necessários?

Uma base de dados ampla pode aumentar poder preditivo e, simultaneamente, elevar risco de privacidade e discriminação. Necessidade deve ser demonstrada, não presumida.

### Pergunta 3 — O modelo é adequado para a população e o produto?

Um modelo validado para cartão de crédito pode não funcionar para financiamento de longo prazo. Um modelo treinado em clientes bancarizados pode falhar em um público de inclusão financeira.

### Pergunta 4 — Como sabemos que ele continua funcionando?

É necessário monitorar performance, calibração, drift, erro por segmentos relevantes e qualidade dos dados.

### Pergunta 5 — Conseguimos explicar uma decisão individual?

A explicação precisa ser fiel ao modelo e compreensível. Se a instituição não consegue traduzir o resultado sem inventar motivos, existe um problema de governança.

### Pergunta 6 — O cliente consegue corrigir erro?

Explicar sem permitir correção cria transparência incompleta. O sistema deve conectar explicação a processo operacional.

### Pergunta 7 — Quem é responsável quando algo falha?

Responsabilidade precisa ser atribuída entre negócio, dados, risco, tecnologia, compliance e atendimento. “Foi a IA” não é uma função organizacional.

### 12.1. NIST AI RMF como benchmark de processo

O NIST AI Risk Management Framework 1.0 organiza gestão de risco em quatro funções: **Govern, Map, Measure e Manage**. O NIST ressalta que essas funções não são uma checklist linear; governança atravessa todo o ciclo de vida.

Aplicado didaticamente ao crédito:

- **Govern:** definir papéis, políticas, limites e accountability;
- **Map:** compreender contexto de uso, pessoas afetadas e riscos;
- **Measure:** medir performance, explicabilidade, robustez, viés e incerteza;
- **Manage:** priorizar riscos, decidir mitigação e acompanhar resultados.

O valor do framework não está em “cumprir quatro caixas”, mas em impedir que a organização trate o modelo como componente isolado.

---

# Parte VII — Apostas, vulnerabilidade financeira e o limite entre risco e diagnóstico

## 13. Por que esse tema entrou no CreditExplain BR

O crescimento das apostas de quota fixa criou um problema interdisciplinar. Transações relacionadas a apostas podem aparecer em dados financeiros e, em determinados contextos, ter relação com vulnerabilidade econômica. Ao mesmo tempo, existe um risco grave de transformar comportamento financeiro em inferência clínica.

O projeto incluiu esse eixo justamente para estudar a **fronteira**.

### 13.1. Cinco níveis que não podem ser confundidos

A melhor forma de evitar extrapolação é separar níveis de evidência:

**1. Transação observada.** Existe um pagamento ou transferência identificável. Isso é um fato transacional.

**2. Padrão financeiro.** A agregação mostra frequência, valor ou evolução dos gastos. Isso é uma descrição de comportamento financeiro.

**3. Vulnerabilidade econômica.** Dados de renda, dívida e despesas podem indicar menor capacidade de absorver perdas. Isso exige informação adicional; não pode ser deduzido de uma única transação.

**4. Inferência de risco de crédito.** Um modelo pode associar determinados padrões a maior probabilidade de inadimplência. Essa é uma inferência estatística, sujeita a validação e governança.

**5. Diagnóstico clínico.** Transtorno do jogo é tema de saúde e depende de avaliação clínica apropriada. Uma instituição financeira ou um algoritmo de crédito não deve converter transação ou score em diagnóstico.

A passagem de um nível para o seguinte exige nova evidência. **Nenhuma etapa comprova automaticamente a próxima.**

### 13.2. O que mudou no ambiente regulatório brasileiro

O Ministério da Fazenda estruturou mecanismos específicos para proteção no mercado regulado de apostas. Beneficiários do Bolsa Família e do Benefício de Prestação Continuada integram hipóteses de impedimento operacionalizadas pelo Módulo de Impedidos do SIGAP. A Portaria SPA/MF nº 2.579/2025 e a Instrução Normativa nº 31/2025 reforçaram mecanismos de autoexclusão e limites prudenciais obrigatórios no cadastro dos sistemas de apostas regulados.

A **autoexclusão centralizada** permite que a pessoa solicite suspensão de sua participação em todos os operadores autorizados alcançados pela plataforma central. Isso é diferente de uma instituição financeira diagnosticar comportamento de jogo. É um mecanismo regulatório específico do ecossistema de apostas.

### 13.3. Resolução CMN nº 5.320/2026 — agora vigente

Na primeira edição deste e-book, a Resolução CMN nº 5.320/2026 ainda não havia entrado em vigor. A norma passou a vigorar em **28/08/2026**.

Ela disciplina bloqueio de contas e impedimento de transações de pessoas e empresas que explorem apostas de quota fixa sem autorização. Após notificação da Secretaria de Prêmios e Apostas, instituições alcançadas devem adotar o bloqueio das contas especificadas no prazo normativo e implementar medidas de impedimento de transações relacionadas aos operadores irregulares.

É importante não ampliar o alcance da norma. Ela trata de **operadores irregulares identificados no processo regulatório**, não cria autorização genérica para bancos bloquearem consumidores por “parecerem apostar demais”.

### 13.4. O erro que uma IA deve evitar

Considere duas frases:

> “O cliente realizou 14 pagamentos para operadores de apostas no mês.”

Isso pode ser um fato transacional, se os dados forem confiáveis.

> “O cliente é jogador compulsivo e, portanto, não deve receber crédito.”

Essa segunda frase contém saltos não demonstrados: diagnóstico clínico, causalidade e decisão normativa. É exatamente o tipo de extrapolação que um sistema de explicação precisa bloquear.

---

# Parte VIII — Benchmarks internacionais: aprender sem importar obrigações

## 14. União Europeia

A União Europeia oferece referências relevantes em proteção de dados, crédito ao consumidor e regulação de IA. O GDPR possui regime próprio para decisões automatizadas. O EU AI Act classifica determinados usos de IA em avaliação de capacidade creditícia ou credit scoring de pessoas naturais como sistemas de alto risco, sujeitos ao regime europeu aplicável.

Esses instrumentos ajudam a pensar documentação, supervisão humana, gestão de risco e qualidade de dados, mas não devem ser descritos como lei brasileira. O valor para o CreditExplain BR é comparativo: observar como outra jurisdição transforma princípios de transparência e risco em requisitos mais explícitos.

## 15. Estados Unidos

O CFPB Circular 2022-03 é especialmente útil para o tema de explicabilidade. A mensagem é direta: a complexidade do algoritmo não é justificativa para deixar de fornecer razões específicas em contextos de adverse action cobertos pela legislação norte-americana.

Em model risk management, a SR 26-2 de 2026 substituiu a tradicional SR 11-7 e reforçou abordagem proporcional ao perfil de risco, uso e complexidade do modelo.

Novamente, esses documentos não criam obrigações no Brasil. Eles servem para responder a uma pergunta de governança: **como outros sistemas regulatórios tratam o argumento “o modelo é complexo demais para explicar”?**

## 16. NIST e frameworks voluntários

O NIST AI RMF é voluntário e não deve ser vendido como certificação. Seu valor é estruturar perguntas sobre confiança, risco e ciclo de vida. O Cyber Risk Institute também desenvolve referenciais específicos para serviços financeiros.

Para uma instituição brasileira, esses frameworks podem complementar — nunca substituir — legislação e regulamentação local.

---

# Parte IX — Três estudos de caso sintéticos

## 17. Caso A — Recusa de crédito com dado possivelmente incorreto

**Cenário fictício.** Mariana solicita crédito pessoal. O modelo recusa a proposta. A explicação identifica como fatores relevantes a alta utilização de crédito rotativo e um histórico recente de atraso.

Mariana afirma que o atraso não é dela e que houve erro de associação cadastral.

Uma arquitetura frágil responderia: “A decisão foi tomada automaticamente e não pode ser alterada.”

Uma arquitetura responsável segue outra sequência:

1. registra os fatores que influenciaram a previsão;
2. identifica a origem do dado contestado;
3. permite correção ou investigação;
4. suspende a interpretação do fator questionado quando apropriado;
5. executa nova análise conforme o processo interno;
6. registra o resultado e a justificativa.

O valor da explicabilidade aparece aqui: **não é explicar melhor um erro; é tornar o erro detectável e corrigível**.

## 18. Caso B — Open Finance e trabalhador autônomo

**Cenário fictício.** Carlos é eletricista autônomo. Sua renda formal declarada é irregular, mas ele possui fluxo recorrente de recebimentos em duas instituições diferentes. Com autorização de compartilhamento pelo Open Finance, a instituição recebedora passa a enxergar uma visão mais completa de entradas e compromissos.

Um modelo pode identificar estabilidade que não aparecia em dados tradicionais. Isso pode ampliar acesso ao crédito.

Mas o mesmo conjunto de dados contém despesas pessoais detalhadas. A instituição precisa evitar transformar toda a vida financeira em variável de score sem necessidade. O ganho de inclusão depende de **seleção responsável de atributos**, não da extração indiscriminada de tudo que a API disponibiliza.

## 19. Caso C — Transações de apostas

**Cenário fictício.** Uma base mostra várias transações para operadores autorizados de apostas. O modelo detecta correlação histórica entre determinado padrão agregado e atraso de pagamento.

Uma explicação aceitável poderia dizer:

> “Na simulação, o padrão de despesas discricionárias recentes contribuiu para elevar a estimativa de risco do modelo. Essa contribuição é estatística e não constitui diagnóstico de comportamento ou saúde.”

Uma explicação inadequada seria:

> “Seu crédito foi negado porque você sofre de compulsão por apostas.”

A diferença não é mera escolha de palavras. A segunda frase transforma associação financeira em diagnóstico clínico e ultrapassa o que os dados demonstram.

---

# Parte X — O que o experimento com NotebookLM realmente ensinou

## 20. O valor não estava em “perguntar para a IA”

O desafio acadêmico poderia ter sido cumprido de forma superficial: importar algumas fontes, fazer perguntas e publicar respostas. O CreditExplain BR adotou outro caminho. O NotebookLM foi tratado como um **ambiente de pesquisa assistida**, e não como autoridade.

O corpus chegou a 77 fontes ativas após curadoria. As fontes foram classificadas por jurisdição, autoridade, atualidade e capacidade probatória. Normas brasileiras ficaram no núcleo para afirmações sobre direitos e obrigações no Brasil. Estudos acadêmicos e benchmarks internacionais foram usados para tecnologia, comparação e contexto.

### 20.1. Experimento 1A — uma resposta boa pode esconder erros

O primeiro prompt pediu uma síntese sobre regras brasileiras, benefícios, riscos, benchmarks e lacunas. A resposta ficou organizada e convincente. A auditoria, porém, encontrou problemas de temporalidade, negativas universais e formulações normativas excessivas.

A lição foi importante: **fluência não é validade**. Um texto bem organizado pode induzir confiança maior do que a evidência permite.

### 20.2. Experimento 1B — prompt melhor reduz, mas não elimina, erro

O segundo experimento adicionou travas Brasil-first, controle temporal, separação entre correlação e causalidade, limitação de negativas universais e distinção clínica.

O resultado melhorou, mas ainda exigiu revisão humana. O projeto identificou, por exemplo, atribuições não sustentadas e justificativas que o modelo insistiu em repetir mesmo após reverificação.

Essa experiência desmonta uma promessa comum de prompt engineering: **não existe um prompt mágico que transforme automaticamente um modelo generativo em fonte de verdade**.

### 20.3. Citação correta também pode acompanhar uma frase errada

Uma das cicatrizes mais importantes foi perceber que uma citação visualmente associada a uma frase não prova que a frase respeita o escopo da fonte. O trecho pode ter sido recuperado parcialmente. A fonte pode ser de outra jurisdição. Pode ser um working paper sendo tratado como norma. Pode haver uma conclusão causal onde o artigo só mostrou correlação.

Rastreabilidade é condição necessária; não é condição suficiente.

### 20.4. O corpus de 77 fontes não vale por ser grande

Quantidade de fontes pode produzir uma falsa sensação de rigor. Setenta e sete fontes mal classificadas seriam piores do que dez fontes primárias bem usadas.

O diferencial do projeto está na **hierarquia**:

- fonte normativa brasileira para regra brasileira;
- autoridade institucional para orientação e contexto;
- artigo científico para evidência técnica;
- benchmark estrangeiro explicitamente tratado como comparação;
- jurisprudência casuística sem generalização;
- fonte secundária usada com peso proporcional.

Essa hierarquia é uma das contribuições mais reutilizáveis do trabalho.

---

# Parte XI — Um playbook prático de explicabilidade em crédito

## 21. Antes de treinar o modelo

Defina a decisão que o modelo apoiará. Registre objetivo, população, produto, horizonte de previsão e consequência do erro. Identifique variáveis proibidas ou inadequadas e documente proveniência dos dados.

Pergunte se um modelo complexo é realmente necessário. Em alguns contextos, um modelo mais simples e interpretável pode entregar performance suficiente com menor custo de governança.

## 22. Durante o desenvolvimento

Separe treino, validação e teste de forma coerente com o problema. Avalie vazamento de informação. Meça discriminação, calibração, estabilidade e desempenho por segmentos relevantes. Documente feature engineering e decisões de exclusão.

Teste explicadores como parte do pipeline, não como decoração posterior.

## 23. Antes da implantação

Construa exemplos de explicação para decisões reais e peça a pessoas não técnicas que interpretem o texto. Verifique se conseguem responder:

- qual foi o resultado?
- quais fatores influenciaram?
- quais dados podem ser conferidos?
- o que é fato e o que é inferência?
- como corrigir um erro?
- existe revisão?

Se o usuário não consegue responder, a explicação ainda não está pronta.

## 24. Em produção

Monitore drift, estabilidade das explicações e mudança de performance. Registre incidentes. Revise prompts e templates. Nunca permita que a camada de LLM introduza novos fatos no processo decisório sem fonte estruturada.

Uma explicação gerada deve ser auditável: entrada, versão do modelo, versão do explicador, versão do template ou prompt e saída precisam ser rastreáveis de forma proporcional ao risco.

## 25. Quando houver contestação

Não trate contestação como atendimento separado do modelo. Ela é feedback de qualidade. Um padrão de contestações pode indicar dados ruins, regra desatualizada, falha de integração ou viés não detectado.

Governança madura fecha o ciclo:

```text
Decisão → Explicação → Contestação → Investigação → Correção → Monitoramento
```

---

# Parte XII — Perguntas que um avaliador deveria fazer a qualquer solução de IA para crédito

## 26. Sobre os dados

- Qual é a origem de cada grupo de variáveis?
- Há autorização ou base legal adequada para o tratamento?
- Quais dados são realmente necessários?
- Como o sistema lida com erro, desatualização e ausência?
- Existem variáveis que funcionam como proxies de características sensíveis?

## 27. Sobre o modelo

- Qual população foi usada no treino?
- Como foi definido o target?
- Como performance e calibração são medidas?
- Como o threshold foi escolhido?
- O modelo funciona igualmente bem para diferentes segmentos relevantes?
- Como drift é detectado?

## 28. Sobre a explicação

- A explicação é global, local ou ambas?
- Ela descreve comportamento do modelo ou sugere causalidade?
- O método é estável?
- A linguagem é compreensível?
- O LLM consegue inventar fatos?
- A explicação permite ação ou correção?

## 29. Sobre governança

- Quem aprova mudanças?
- Quem revisa incidentes?
- O modelo possui inventário e versionamento?
- Existe validação independente proporcional ao risco?
- Há canal de revisão e contestação?
- A organização consegue demonstrar por que uma decisão ocorreu meses depois?

---

# Parte XIII — Limitações do próprio CreditExplain BR

## 30. O projeto não é uma implementação bancária

O CreditExplain BR é um projeto de estudo e portfólio. Ele não recebeu base proprietária de instituição financeira, não operou concessão real e não executou validação regulatória de produção.

## 31. O artigo central é evidência acadêmica, não certificação de solução

O framework ML-XAI-LLM foi estudado porque oferece uma arquitetura relevante para aproximar explicabilidade técnica e linguagem humana. Resultados experimentais elevados precisam ser interpretados dentro do dataset, desenho e escopo do estudo.

## 32. O corpus tem amplitude maior que profundidade uniforme

As 77 fontes não têm o mesmo peso. Algumas são normas, outras relatórios, artigos, working papers, FAQs e estudos de caso. O documento de curadoria registra essas diferenças.

## 33. Regulação muda

Open Finance, IA, crédito e apostas são temas regulatórios dinâmicos. A edição atual contém refresh em 27/09/2026, mas não deve ser tratada como atualização permanente. Antes de qualquer uso profissional, normas vigentes precisam ser verificadas novamente.

---

# Parte XIV — Glossário comentado

## 34. Conceitos essenciais

**Acurácia** — proporção total de previsões corretas. Pode ser enganosa em bases desbalanceadas.

**Adverse action** — conceito do regime norte-americano para determinadas decisões desfavoráveis de crédito. Não deve ser importado automaticamente como categoria jurídica brasileira.

**Calibração** — grau em que probabilidades previstas correspondem a frequências observadas.

**Cadastro Positivo** — infraestrutura regulada pela Lei nº 12.414/2011 relacionada ao histórico de adimplemento e informações de crédito.

**Concept drift** — mudança na relação entre variáveis e resultado ao longo do tempo.

**Contestabilidade** — capacidade prática de compreender, questionar, corrigir dados e solicitar revisão de uma decisão.

**Data drift** — mudança na distribuição estatística dos dados de entrada.

**Explicabilidade** — conjunto de métodos e práticas que tornam comportamento e resultados de modelos mais compreensíveis a públicos específicos.

**Fairness** — campo que estuda critérios e impactos de equidade em sistemas algorítmicos. Não existe uma única métrica universal de justiça.

**Feature** — variável usada pelo modelo como entrada.

**LIME** — técnica post-hoc que aproxima localmente o comportamento de um modelo complexo por meio de um modelo interpretável.

**LLM** — Large Language Model; modelo de linguagem capaz de gerar e transformar texto. No framework estudado, atua como camada de tradução semântica, não como fonte autônoma de fatos.

**MEMC** — Mean Evaluation of Metrics Change; métrica discutida no corpus para avaliar explicadores por alteração de métricas após perturbação de atributos relevantes.

**Mínimo existencial** — referência jurídica usada na prevenção e tratamento do superendividamento; não é threshold automático de concessão.

**Model risk** — risco de consequências adversas decorrentes de decisões baseadas em modelos incorretos, mal aplicados ou mal governados.

**Open Finance** — compartilhamento padronizado de dados e serviços entre instituições participantes segundo regras do Banco Central e jornadas autorizadas pelo cliente.

**Proxy** — variável que pode carregar informação relacionada a outra característica não explicitamente presente.

**Reason code** — motivo estruturado associado a uma decisão; no CreditExplain BR é estudado principalmente como referência de design e benchmark regulatório estrangeiro.

**SCR** — Sistema de Informações de Créditos do Banco Central.

**SHAP** — técnica de atribuição baseada em valores de Shapley para explicar contribuição de variáveis para saídas de modelos.

**Superendividamento** — impossibilidade manifesta de consumidor pessoa natural de boa-fé pagar dívidas de consumo sem comprometer mínimo existencial.

**Threshold** — ponto de corte usado para transformar uma probabilidade ou score em classe ou decisão operacional.

**XAI** — Explainable Artificial Intelligence; conjunto de técnicas voltadas à explicação e interpretação de modelos de IA.

---

# Parte XV — Prompts reutilizáveis para estudo e auditoria

> Todos os prompts abaixo são **MATERIAL DIDÁTICO FICTÍCIO/SINTÉTICO**. Eles não devem ser usados para conceder ou negar crédito real, emitir parecer jurídico ou produzir diagnóstico clínico.

## Prompt 1 — Traduzir uma explicação XAI sem inventar fatos

```text
Você atua como tradutor semântico de explicabilidade.

Receberá apenas dados estruturados sobre uma predição e suas atribuições de importância.

Tarefa:
1. explicar em linguagem simples quais fatores contribuíram para elevar ou reduzir a saída do modelo;
2. deixar claro que se trata de contribuição preditiva, não causalidade;
3. não criar fatos cadastrais ausentes;
4. separar dados observados de inferências;
5. indicar quais dados poderiam ser conferidos pelo titular.

Se a evidência fornecida não for suficiente para uma conclusão, diga explicitamente que não é possível concluir.
```

## Prompt 2 — Auditoria de alucinação

```text
Compare a explicação textual com o JSON de evidências.

Para cada frase material, classifique:
- SUPORTADA;
- SUPORTADA_COM_QUALIFICAÇÃO;
- NÃO_SUPORTADA;
- CAUSALIDADE_NÃO_DEMONSTRADA.

Não corrija usando conhecimento externo. Aponte exatamente qual trecho da entrada sustenta ou não sustenta cada afirmação.
```

## Prompt 3 — Separar regra brasileira de benchmark estrangeiro

```text
Analise as fontes fornecidas e crie duas seções independentes:
A) Brasil — somente normas, autoridades e jurisprudência brasileira aplicável;
B) Benchmark internacional — práticas e regras de outras jurisdições.

É proibido apresentar norma estrangeira como obrigação no Brasil.
Quando houver apenas recomendação ou estudo, use linguagem de recomendação ou evidência, não de dever jurídico.
```

## Prompt 4 — Revisão de decisão automatizada em cenário sintético

```text
Em um cenário fictício, receba:
- decisão automatizada;
- variáveis utilizadas;
- origem dos dados;
- explicação XAI;
- contestação do usuário.

Monte um roteiro de revisão que identifique:
1. dado contestado;
2. origem;
3. possibilidade de erro;
4. impacto no modelo;
5. necessidade de análise humana;
6. registro de decisão final.

Não conceda nem negue crédito real.
```

## Prompt 5 — Auditoria de drift

```text
Compare estatísticas de uma base de treino e de uma base atual.
Identifique mudanças de distribuição, possíveis alterações de população e variáveis com desvio relevante.

Não conclua automaticamente que existe concept drift.
Indique quais testes adicionais seriam necessários para verificar perda de validade do modelo.
```

## Prompt 6 — Open Finance e minimização de dados

```text
Dada uma lista de campos disponíveis por Open Finance e um objetivo específico de análise de crédito, classifique cada campo como:
- NECESSÁRIO;
- POSSIVELMENTE_RELEVANTE;
- NÃO_DEMONSTRADO;
- ALTO_RISCO_DE_PROXY.

Justifique em termos de finalidade, necessidade, qualidade e risco de inferência.
Não presuma que disponibilidade técnica equivale a autorização de uso irrestrito.
```

## Prompt 7 — Avaliação de explicação para consumidor

```text
Avalie uma explicação de crédito segundo quatro critérios:
1. fidelidade à evidência;
2. clareza;
3. acionabilidade;
4. ausência de causalidade indevida.

Reescreva somente se a nova versão puder permanecer estritamente dentro da evidência apresentada.
```

## Prompt 8 — Apostas: impedir salto clínico

```text
Receba um conjunto sintético de transações financeiras.
Separe explicitamente:
- transação observada;
- padrão financeiro calculável;
- vulnerabilidade que exigiria dados adicionais;
- inferência de risco estatístico;
- diagnóstico clínico, que não pode ser produzido.

Se o texto de entrada misturar esses níveis, sinalize o salto lógico.
```

## Prompt 9 — Auditoria de reason codes

```text
Em um cenário acadêmico, compare motivos de uma decisão com:
- fatores efetivamente usados pelo modelo;
- explicações SHAP/LIME;
- linguagem apresentada ao usuário.

Marque qualquer motivo genérico, contraditório ou não relacionado a fator efetivamente considerado.
Não trate requisitos estrangeiros como obrigação brasileira.
```

## Prompt 10 — Red team da explicação

```text
Tente encontrar falhas na explicação apresentada.
Procure especialmente:
- dado inexistente;
- causalidade inventada;
- regra estrangeira apresentada como brasileira;
- variável sensível ou proxy não discutida;
- omissão de incerteza;
- ausência de caminho de correção;
- linguagem que transforma score em diagnóstico pessoal.

Retorne achados priorizados por gravidade e evidência.
```

---

# Parte XVI — Referências e trilha de evidência

## 35. Fontes brasileiras centrais

A lista abaixo não substitui o corpus completo; ela oferece uma rota de leitura para os pontos mais importantes do e-book.

1. **Lei Geral de Proteção de Dados — Lei nº 13.709/2018.** Texto atualizado da Câmara dos Deputados:  
   <https://www2.camara.leg.br/legin/fed/lei/2018/lei-13709-14-agosto-2018-787077-normaatualizada-pl.html>

2. **Código de Defesa do Consumidor — Lei nº 8.078/1990**, com alterações da Lei nº 14.181/2021 relacionadas ao superendividamento.

3. **Decreto nº 11.150/2022**, alterado pelo Decreto nº 11.567/2023 — mínimo existencial:  
   <https://www.planalto.gov.br/ccivil_03/_ato2019-2022/2022/decreto/d11150.htm>

4. **Lei nº 12.414/2011 — Cadastro Positivo.**

5. **STJ — Súmula 550 e REsp 1.419.697/RS** — credit scoring, informações valoradas e fontes consideradas:  
   <https://processo.stj.jus.br/SCON/pesquisar.jsp?b=SUMU&sumula=550>

6. **Banco Central — Sistema de Informações de Créditos (SCR):**  
   <https://www.bcb.gov.br/estabilidadefinanceira/scr/>

7. **Resolução Conjunta nº 1/2020 — Open Finance** e alterações posteriores:  
   <https://normativos.bcb.gov.br/Lists/Normativos/Attachments/51028/Res_Conj_0001_v8_L.pdf>

8. **Banco Central — FAQ Open Finance:**  
   <https://www.bcb.gov.br/meubc/faqs/s/open-finance>

9. **Instrução Normativa BCB nº 759/2026 — Manual de Escopo de Dados e Serviços v8.0:**  
   <https://www.bcb.gov.br/estabilidadefinanceira/exibenormativo?numero=759&tipo=Instru%C3%A7%C3%A3o+Normativa+BCB>

10. **Instrução Normativa BCB nº 760/2026 — Manual de Experiência do Cliente v9.0:**  
    <https://www.bcb.gov.br/estabilidadefinanceira/exibenormativo?numero=760&tipo=Instru%C3%A7%C3%A3o+Normativa+BCB>

11. **Resolução Conjunta nº 8/2023 — Educação financeira**, com alterações da Resolução Conjunta nº 20/2026.

12. **Resolução BCB nº 365/2023 — transparência de faturas de cartão de crédito.**

13. **ANPD — Direitos dos Titulares:**  
    <https://www.gov.br/anpd/pt-br/assuntos/titular-de-dados/direito-dos-titulares>

14. **Lei nº 14.790/2023 — apostas de quota fixa.**

15. **SPA/MF — legislação de apostas de quota fixa:**  
    <https://www.gov.br/fazenda/pt-br/composicao/orgaos/secretaria-de-premios-e-apostas/apostas-de-quota-fixa/legislacao/apostas>

16. **SPA/MF — Módulo de Impedidos / autoexclusão:**  
    <https://www.gov.br/fazenda/pt-br/composicao/orgaos/secretaria-de-premios-e-apostas/modulo-de-impedidos>

17. **Resolução CMN nº 5.320/2026 — bloqueio de contas e impedimento de transações de operadores irregulares de apostas:**  
    <https://www.bcb.gov.br/estabilidadefinanceira/exibenormativo?numero=5320&tipo=Resolu%C3%A7%C3%A3o+CMN>

18. **Ministério da Saúde — Guia de Cuidado para Pessoas com Problemas Relacionados a Jogos de Apostas — 2026.**

## 36. Referências técnicas e internacionais selecionadas

19. **Simonae, M. M.; Marcon, M.; Casanova, D. — Bridging AI and Ethics: An LLM-Based Framework for Transparent and Inclusive Credit Decisions. SBSI 2026.**  
    DOI: 10.5753/sbsi.2026.248352

20. **NIST — AI Risk Management Framework 1.0:**  
    <https://airc.nist.gov/airmf-resources/airmf/5-sec-core/>

21. **CFPB Circular 2022-03 — adverse action e algoritmos complexos:**  
    <https://www.consumerfinance.gov/compliance/circulars/circular-2022-03-adverse-action-notification-requirements-in-connection-with-credit-decisions-based-on-complex-algorithms/>

22. **Federal Reserve — SR 26-2, Revised Guidance on Model Risk Management:**  
    <https://www.federalreserve.gov/supervisionreg/srletters/SR2602.htm>

23. **World Bank/ICCR — Credit Scoring Approaches Guidelines.**

24. **IFC — Cracking the Credit Code: Alternative Data and AI for Financial Inclusion.**

25. **OECD — Artificial Intelligence, Machine Learning and Big Data in Finance.**

26. **BIS/FSI — materiais sobre explainability e governança de IA em finanças.**

27. **EBA — Guidelines on Loan Origination and Monitoring (EBA/GL/2020/06).**

28. **Regulamento (UE) 2024/1689 — EU AI Act.**

## 37. Corpus completo

O índice de todas as **77 fontes originais**, com classificação por jurisdição, nível de evidência, status e limites de uso, permanece em:

[`corpus-77-fontes.md`](corpus-77-fontes.md)

As fontes adicionais usadas no refresh de 27/09/2026 são registradas separadamente no próprio arquivo de corpus para preservar a contagem histórica do projeto.

---

# Conclusão

A principal tese do CreditExplain BR é simples de formular e difícil de executar:

> **Uma decisão de crédito não se torna responsável apenas porque o modelo é preciso, e uma explicação não se torna confiável apenas porque está escrita em linguagem natural.**

Crédito responsável exige dados adequados, finalidade, avaliação proporcional, proteção contra superendividamento e mecanismos de correção. IA exige validação, monitoramento e gestão de risco. XAI exige fidelidade e estabilidade. LLMs exigem limites explícitos para não transformar tradução em invenção. Open Finance amplia a capacidade de personalização, mas também aumenta a responsabilidade sobre uso e minimização dos dados. E contestabilidade exige processos reais, não apenas interfaces bonitas.

O estudo de 77 fontes e os experimentos com NotebookLM mostraram algo ainda mais importante: **qualidade de pesquisa depende de hierarquia de evidência**. Uma fonte pode estar corretamente citada e ainda ser usada fora de contexto. Uma regra estrangeira pode ser excelente benchmark e, ao mesmo tempo, não ter qualquer força jurídica no Brasil. Um artigo pode demonstrar viabilidade experimental sem provar generalização. Uma correlação pode ser preditiva sem ser causal. Uma transação financeira pode ser observável sem autorizar diagnóstico clínico.

É justamente essa capacidade de distinguir níveis de evidência que transforma um conjunto de informações em conhecimento utilizável.

O CreditExplain BR não termina com uma promessa de que a IA conseguirá explicar tudo. Ele termina com uma exigência mais realista: **quando uma decisão automatizada afetar pessoas, a organização precisa ser capaz de demonstrar o que sabe, o que inferiu, o que não sabe e como alguém pode contestar um erro**.

Essa é a diferença entre produzir um score e construir um sistema de decisão responsável.
