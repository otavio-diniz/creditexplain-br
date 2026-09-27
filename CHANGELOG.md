# Changelog — CreditExplain BR

Este arquivo registra a evolução editorial e documental do projeto sem apagar seu estado histórico.

## [2.0] — 27/09/2026 — E-book revisado e ampliado

### Motivação

A reavaliação humana do material identificou que a primeira edição concentrava conteúdo técnico relevante, porém funcionava melhor como **miniguia de consulta/revisão** do que como e-book autônomo de aprendizagem. O texto era excessivamente orientado por tópicos, definições e listas para o volume e a diversidade da pesquisa realizada.

### Alterado

- reescrita substancial de `docs/miniguia-creditexplain-br.md` como e-book narrativo;
- desenvolvimento de contexto, relações de causa e consequência, limites e aplicações;
- aprofundamento de crédito responsável, Open Finance, dados alternativos, model risk, drift, SHAP, LIME, reason codes, LGPD e contestabilidade;
- expansão da análise do framework ML-XAI-LLM, separando evidência experimental de generalização para produção;
- inclusão de estudos de caso sintéticos;
- inclusão de playbook de governança e perguntas de auditoria;
- glossário comentado e prompts reutilizáveis revisados;
- criação de `docs/apendice-tecnico-regulatorio-creditexplain-br.md` para preservar matrizes, detalhes normativos, controles de evidência e itens que seriam excessivamente densos no fluxo narrativo;
- explicitação, no apêndice, de afirmações históricas rebaixadas ou removidas por extrapolação, evitando perda silenciosa de informação;
- refresh temporal de fontes mutáveis em 27/09/2026;
- atualização da Resolução CMN nº 5.320/2026 para estado vigente desde 28/08/2026;
- registro temporal da IN BCB nº 759/2026: publicada com Manual de Escopo v8.0, entrada em vigor em 03/11/2026;
- registro da IN BCB nº 760/2026 — Manual de Experiência do Cliente v9.0;
- registro da Resolução Conjunta nº 20/2026 com controle de efeitos temporais próprios;
- atualização do benchmark de model risk para Federal Reserve SR 26-2;
- atualização de README, corpus, experimentos e gate de auditoria;
- registro de que a submissão à DIO já foi concluída conforme declaração do autor em 27/09/2026, sem inventar data institucional exata, nota ou certificado.

### Preservado

- corpus histórico de **77 fontes** usado no projeto original;
- resultados dos experimentos 1A, 1B e perguntas estratégicas 2/3;
- cicatrizes e limitações do NotebookLM;
- distinção Brasil-first;
- informação técnica válida da primeira edição, agora distribuída entre e-book narrativo, apêndice, corpus e histórico Git;
- versões anteriores pelo histórico Git;
- licença e proveniência de terceiros.

### Corrigido/rebaixado

A v2 não promove como conhecimento válido formulações que a própria auditoria histórica já havia identificado como problemáticas. O registro permanece nas cicatrizes, mas o alcance foi corrigido. Exemplos:

- justificativa CEP/CONEP não sustentada pela fonte acadêmica;
- atribuição não sustentada de uma proposta de “blacklist”;
- técnicas específicas de XAI tratadas com linguagem excessivamente próxima de obrigação regulatória;
- benchmarks estrangeiros que exigiam qualificação explícita de jurisdição;
- causalidade sugerida onde havia contribuição preditiva.

### Não executado

- nova submissão na DIO;
- alteração de nota;
- inferência de aprovação ou certificado;
- novo experimento no NotebookLM para substituir os experimentos históricos;
- implementação de sistema real de decisão de crédito.

---

## [1.x] — 22/08/2026 — Fechamento acadêmico original

### Estado

- NotebookLM construído e estabilizado com 77 fontes selecionadas;
- curadoria e auditoria de proveniência;
- configuração Brasil-first;
- experimentos de prompting 1A/1B e perguntas estratégicas;
- miniguia gerado pelo NotebookLM e revisado editorialmente;
- cinco fontes âncora destacadas no README;
- respostas brutas e citações nativas preservadas fora do portfólio público;
- refresh normativo realizado para o corte de 22/08/2026;
- repositório publicado e preparado para submissão.

### Observação histórica

Na data de corte original, a Resolução CMN nº 5.320/2026 ainda era norma publicada com vigência futura em 28/08/2026. A v2 preserva esse fato histórico e registra separadamente sua vigência posterior.

---

## Princípio de versionamento

Uma nova edição pode atualizar conteúdo mutável e melhorar a pedagogia sem fingir que a versão anterior continha conhecimento posterior. O Git preserva o estado histórico; este changelog torna explícita a transição entre os estados.
