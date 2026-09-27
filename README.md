# CreditExplain BR

## Crédito Responsável, IA, Open Finance e Explicabilidade

> Projeto do desafio **“Treinando uma IA de Aprendizagem: Explore o Poder do NotebookLM”**, no **DIO Bootcamp Bradesco — GenAI, Dados & Cyber**.
>
> **Corte documental original:** 22/08/2026  
> **Edição atual do e-book:** 2ª edição — revisada e ampliada — 27/09/2026  
> **Submissão à DIO:** concluída, conforme declaração do autor registrada em 27/09/2026; a data exata/comprovante da submissão não está versionada neste repositório.  
> **Natureza:** material acadêmico e pedagógico. Não é parecer jurídico, diagnóstico clínico, política real de concessão de crédito nem sistema automatizado em produção.

![Capa do CreditExplain BR](assets/capa-notebooklm-creditexplain-br.png)

## 1. Visão geral

O **CreditExplain BR** nasceu como um caderno temático construído com NotebookLM para estudar, de forma integrada e crítica:

- crédito responsável e prevenção ao superendividamento;
- Inteligência Artificial e Machine Learning em avaliação de risco;
- Open Finance e governança de dados;
- explicabilidade, contestabilidade e limites de inferência em decisões automatizadas;
- fronteiras entre comportamento financeiro, vulnerabilidade e diagnóstico clínico.

O projeto foi além de uma geração automática de resumo. O corpus foi ampliado para **77 fontes ativas/selecionadas**, auditado fonte a fonte e submetido a testes controlados de prompting. O objetivo foi observar não apenas **o que a IA responde**, mas **como qualidade das fontes, formulação do prompt, temporalidade normativa e revisão humana afetam a confiabilidade do resultado**.

Em 27/09/2026, após nova auditoria editorial, o antigo miniguia foi transformado em uma **2ª edição narrativa e ampliada do e-book**. A nova edição preserva a pesquisa original e seu histórico, mas aprofunda explicações, conexões conceituais, exemplos, estudos de caso sintéticos, governança e aplicação prática.

➡️ **Leia o e-book:** [`docs/miniguia-creditexplain-br.md`](docs/miniguia-creditexplain-br.md)

➡️ **Consulte o apêndice técnico-regulatório:** [`docs/apendice-tecnico-regulatorio-creditexplain-br.md`](docs/apendice-tecnico-regulatorio-creditexplain-br.md)

➡️ **Veja o histórico de versões:** [`CHANGELOG.md`](CHANGELOG.md)

➡️ **Veja o gate de auditoria:** [`AUDIT_STATUS.md`](AUDIT_STATUS.md)

## 2. Pergunta norteadora

> **Como instituições financeiras podem utilizar dados — inclusive dados compartilhados via Open Finance — e sistemas automatizados para apoiar decisões de crédito, preservando transparência, proteção de dados e os princípios do crédito responsável?**

## 3. Metodologia do projeto

O trabalho foi conduzido em camadas:

1. **Definição do tema e da pergunta norteadora.**
2. **Construção e expansão do corpus.** O notebook estabilizou em 77 fontes após pesquisa, curadoria e saneamento.
3. **Auditoria das fontes.** Jurisdição, autoridade, tipo, atualidade, capacidade probatória, limites e ação recomendada foram registrados.
4. **Configuração Brasil-first.** Afirmações sobre obrigação, proibição, permissão ou direito no Brasil passaram a exigir fonte brasileira competente.
5. **Experimentos controlados de prompting.** Foram executadas variações da mesma pergunta e perguntas estratégicas, com controle de histórico e notas.
6. **Auditoria das respostas.** Citação correta não foi tratada como prova automática de conclusão correta; escopo, autoridade, terminologia e vigência foram verificados separadamente.
7. **Consolidação editorial original.** O NotebookLM gerou o miniguia, posteriormente revisado por controle humano.
8. **Revisão editorial v2.** Em 27/09/2026, a entrega foi reestruturada como e-book narrativo, com explicações desenvolvidas, exemplos, estudos de caso, playbook de governança, apêndice técnico-regulatório e refresh temporal das fontes mutáveis.

> O corpus de 77 fontes é uma expansão autoral do projeto. Para a apresentação enxuta **recomendada** pelo desafio, o README destaca cinco fontes âncora; o índice integral permanece separado em [`docs/corpus-77-fontes.md`](docs/corpus-77-fontes.md).

## 4. Cinco fontes âncora

| Fonte | Função no projeto |
|---|---|
| [LGPD — Lei nº 13.709/2018 — texto atualizado da Câmara](https://www2.camara.leg.br/legin/fed/lei/2018/lei-13709-14-agosto-2018-787077-normaatualizada-pl.html) | Proteção de dados, direitos do titular e decisões automatizadas |
| [Resolução Conjunta nº 1/2020 — Open Finance](https://normativos.bcb.gov.br/Lists/Normativos/Attachments/51028/Res_Conj_0001_v8_L.pdf) | Base regulatória do Open Finance brasileiro |
| [Banco Central — Relatório de Cidadania Financeira 2025](https://www.bcb.gov.br/content/cidadaniafinanceira/documentos_cidadania/RCF/relatorio_de_cidadania_financeira_2025.pdf) | Crédito, vulnerabilidades e cidadania financeira |
| [Simonae, Marcon & Casanova — Bridging AI and Ethics](https://sol.sbc.org.br/index.php/sbsi/article/download/41332/41102/) | Referência acadêmica central para ML-XAI-LLM e explicabilidade |
| [Ministério da Saúde — Guia de Cuidado para Pessoas com Problemas Relacionados a Jogos de Apostas — 2026](https://www.gov.br/saude/pt-br/centrais-de-conteudo/publicacoes/guias-e-manuais/2026/guia-de-cuidado-para-pessoas-com-problemas-relacionados-a-jogos-de-apostas.pdf/@@download/file/Guia%20de%20Cuidado%20para%20Pessoas%20com%20Problemas%20Relacionados%20a%20Jogos%20de%20Apostas.pdf) | Fronteira entre comportamento, sinais de risco, cuidado e diagnóstico clínico |

## 5. Engenharia de prompts e cicatrizes

Os testes do NotebookLM foram tratados como experimentos, não como produção automática de verdade.

### Experimento 1A

A primeira síntese foi organizada em regras brasileiras, benefícios, riscos, benchmarks internacionais e lacunas. O resultado foi classificado como `PASSOU_COM_RESSALVAS`: a estrutura era boa, mas a auditoria encontrou problemas de negativas universais, temporalidade e precisão normativa.

### Experimento 1B

O prompt seguinte adicionou travas Brasil-first, controle temporal, distinção entre correlação e causalidade, tratamento de jurisdição e separação entre comportamento financeiro e diagnóstico clínico. Houve melhora real, porém permaneceram sobreafirmações semânticas.

### Aprendizado central

**Prompt engineering melhora o comportamento, mas não substitui auditoria humana.** Uma citação correta pode acompanhar uma frase que extrapola a fonte, e uma resposta fluente pode parecer mais fundamentada do que realmente é.

O registro completo está em [`docs/experimentos-e-cicatrizes.md`](docs/experimentos-e-cicatrizes.md).

## 6. O que mudou no e-book v2

A primeira edição era adequada como **miniguia de revisão**, mas condensava informação demais em tópicos, listas e definições. A segunda edição foi reescrita para servir como material formativo autônomo.

A v2 agora inclui:

- narrativa sobre como uma decisão de crédito se transforma em problema de explicabilidade;
- explicação desenvolvida de crédito responsável, superendividamento, Cadastro Positivo, SCR e Open Finance;
- distinção entre performance, calibração, threshold, data drift, concept drift e model risk;
- capítulos didáticos sobre SHAP e LIME, incluindo o que cada técnica demonstra e o que não demonstra;
- discussão aprofundada do framework ML-XAI-LLM e de sua fronteira de generalização;
- interpretação do Art. 20 da LGPD, revisão e contestabilidade;
- atualização temporal do eixo de apostas, incluindo a vigência da Resolução CMN nº 5.320/2026;
- benchmarks internacionais explicitamente separados das obrigações brasileiras;
- três estudos de caso sintéticos;
- playbook prático de governança de explicações;
- perguntas de auditoria para dados, modelo, explicação e governança;
- glossário comentado;
- dez prompts reutilizáveis para estudo e auditoria;
- **apêndice técnico-regulatório**, que preserva matrizes, detalhes, controles de evidência e itens que seriam excessivamente densos no fluxo narrativo;
- referências selecionadas e ligação direta com o corpus de 77 fontes.

## 7. Refresh temporal

O projeto original foi fechado com corte documental em **22/08/2026**. Esse estado histórico permanece preservado pelo Git.

A edição v2 possui **refresh em 27/09/2026** para pontos materiais mutáveis. Entre eles:

- a **Resolução CMN nº 5.320/2026**, que no corte original ainda tinha vigência futura, está vigente desde 28/08/2026;
- o Banco Central publicou a **IN BCB nº 759/2026**, com o Manual de Escopo de Dados e Serviços do Open Finance v8.0, cuja entrada em vigor é 03/11/2026; até então, a temporalidade precisa ser respeitada;
- a **IN BCB nº 760/2026** publicou o Manual de Experiência do Cliente do Open Finance v9.0;
- a **Resolução Conjunta nº 20/2026** altera a Resolução Conjunta nº 8/2023, com efeitos nas datas previstas pelo próprio normativo;
- a orientação norte-americana de model risk foi atualizada pela **SR 26-2**, que substituiu SR 11-7 e SR 21-8.

O detalhamento está no corpus, no e-book e no apêndice. A existência de refresh atual não transforma o projeto em parecer jurídico permanentemente atualizado.

## 8. Checklist de aderência ao desafio DIO

- ✅ **Contexto e objetivos:** documentados.
- ✅ **Curadoria de fontes:** cinco fontes abertas destacadas e corpus ampliado de 77 fontes registrado.
- ✅ **Engenharia de prompts:** variações 1A/1B e perguntas estratégicas preservadas.
- ✅ **Respostas, referências e cicatrizes:** resultados auditados e troubleshooting documentados.
- ✅ **Entrega pedagógica:** e-book v2 revisado e ampliado em [`docs/miniguia-creditexplain-br.md`](docs/miniguia-creditexplain-br.md).
- ✅ **Detalhamento técnico e regulatório:** consolidado em [`docs/apendice-tecnico-regulatorio-creditexplain-br.md`](docs/apendice-tecnico-regulatorio-creditexplain-br.md).
- ✅ **Glossário e prompts reutilizáveis:** integrados à segunda edição.
- ✅ **Repositório próprio no GitHub:** `otavio-diniz/creditexplain-br`.
- ✅ **Submissão na plataforma DIO:** concluída conforme declaração do autor registrada em 27/09/2026. **A data exata e o comprovante institucional da submissão não foram autenticados neste repositório.**

> A marcação acima registra **submissão**, não nota, aprovação, certificação ou avaliação institucional.

## 9. Estrutura do repositório

```text
creditexplain-br/
├── README.md
├── AUDIT_STATUS.md
├── CHANGELOG.md
├── LICENSE
├── NOTICE.md
├── docs/
│   ├── miniguia-creditexplain-br.md
│   ├── apendice-tecnico-regulatorio-creditexplain-br.md
│   ├── corpus-77-fontes.md
│   └── experimentos-e-cicatrizes.md
└── assets/
    └── capa-notebooklm-creditexplain-br.png
```

### Arquivos principais

- [`docs/miniguia-creditexplain-br.md`](docs/miniguia-creditexplain-br.md) — e-book completo, 2ª edição revisada e ampliada.
- [`docs/apendice-tecnico-regulatorio-creditexplain-br.md`](docs/apendice-tecnico-regulatorio-creditexplain-br.md) — matrizes regulatórias, detalhe técnico, controles de evidência e preservação de densidade da pesquisa.
- [`docs/corpus-77-fontes.md`](docs/corpus-77-fontes.md) — índice do corpus, hierarquia das fontes e refresh temporal.
- [`docs/experimentos-e-cicatrizes.md`](docs/experimentos-e-cicatrizes.md) — evolução dos prompts, resultados, auditoria e troubleshooting.
- [`AUDIT_STATUS.md`](AUDIT_STATUS.md) — gate atual de prontidão e controle de proveniência.
- [`CHANGELOG.md`](CHANGELOG.md) — evolução entre a edição original e a v2.
- [`NOTICE.md`](NOTICE.md) — proveniência e limites de materiais de terceiros.
- [`LICENSE`](LICENSE) — política de direitos do material autoral.

## 10. Limitações e integridade

- O projeto **não executa decisão real de crédito**.
- O conteúdo **não constitui parecer jurídico** ou avaliação de conformidade de uma instituição real.
- O conteúdo **não produz diagnóstico clínico** ou orientação individualizada de saúde.
- Exemplos não documentados como casos reais são **MATERIAL DIDÁTICO FICTÍCIO/SINTÉTICO**.
- Fontes internacionais são benchmarks técnicos/comparativos quando não vinculantes no Brasil.
- Jurisprudência casuística não é promovida a regra universal.
- Outputs de IA não são promovidos automaticamente a conhecimento validado.
- A publicação e a submissão declarada **não permitem inferir nota, aprovação ou certificado**.

## 11. Conclusão

O CreditExplain BR demonstra um processo de **curadoria → prompting → verificação → auditoria → correção editorial → consolidação pedagógica → revisão temporal**.

A segunda edição desloca o projeto de um miniguia concentrado para um e-book que procura explicar o raciocínio por trás dos conceitos, conectando regulação, ciência de dados, governança e experiência do consumidor. O apêndice técnico-regulatório preserva a densidade necessária para auditoria sem sacrificar a leitura do corpo principal. A pesquisa original continua rastreável e o histórico permanece preservado no Git.

---

**Desafio:** Treinando uma IA de Aprendizagem: Explore o Poder do NotebookLM  
**Projeto:** CreditExplain BR — Crédito Responsável, IA, Open Finance e Explicabilidade  
**Estado documental:** e-book v2 revisado e ampliado; apêndice técnico publicado no pacote; repositório auditado; submissão à DIO declarada concluída pelo autor; nota/certificação não inferidas.

## 12. Leitura acessível, orientação e reconhecimento

Para quem chega ao tema sem formação técnica, a leitura recomendada começa pelo [e-book completo](docs/miniguia-creditexplain-br.md) e pode ser acompanhada pelo [mapa de siglas e abreviações](docs/siglas-e-abreviacoes.md). O [índice de leitura](docs/README.md) organiza o percurso entre e-book, apêndice, corpus e experimentos.

Este projeto foi desenvolvido no **DIO Bootcamp Bradesco — GenAI, Dados & Cyber**. A orientação do desafio **“Treinando uma IA de Aprendizagem: Explore o Poder do NotebookLM”** é creditada a **Felipe Silva Aguiar (`@felipeAguiarCode`)**, com referência ao ecossistema educacional da **`@digitalinnovationone`**.

Agradeço pelo conteúdo e pela proposta do desafio. Feedback técnico ou pedagógico sobre esta implementação autoral é bem-vindo. As menções registram origem acadêmica e reconhecimento; **não implicam endosso, avaliação, vínculo profissional ou aprovação** por parte do instrutor, da DIO ou do Bradesco.