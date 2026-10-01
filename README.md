# CreditExplain BR

## Crédito Responsável, IA, Open Finance e Explicabilidade

> Projeto do desafio **“Treinando uma IA de Aprendizagem: Explore o Poder do NotebookLM”**, no **DIO Bootcamp Bradesco — GenAI, Dados & Cyber**.

![Capa do CreditExplain BR](assets/capa-notebooklm-creditexplain-br.png)

## Resumo

O **CreditExplain BR** é um projeto acadêmico e pedagógico de pesquisa e aprendizagem sobre **crédito responsável, Inteligência Artificial, Open Finance e explicabilidade**.

O trabalho começou como um caderno temático no NotebookLM e evoluiu para uma pesquisa auditável com **77 fontes ativas/selecionadas**, experimentos controlados de prompting, revisão humana, refresh temporal e uma **2ª edição narrativa e ampliada do e-book**.

O objetivo não é apenas observar **o que a IA responde**, mas como **qualidade das fontes, formulação do prompt, temporalidade normativa, jurisdição e revisão humana** afetam a confiabilidade do resultado.

> **Natureza:** material acadêmico e pedagógico. Não é parecer jurídico, diagnóstico clínico, política real de concessão de crédito nem sistema automatizado em produção.

## Pergunta norteadora

> **Como instituições financeiras podem utilizar dados — inclusive dados compartilhados via Open Finance — e sistemas automatizados para apoiar decisões de crédito, preservando transparência, proteção de dados e os princípios do crédito responsável?**

## Estado atual

- **Corte documental original:** 22/08/2026.
- **E-book:** 2ª edição revisada e ampliada, com refresh em 27/09/2026.
- **Corpus:** 77 fontes ativas/selecionadas, com hierarquia e auditoria documentadas.
- **Experimentos de prompting:** variações, erros, cicatrizes e correções preservados.
- **Apêndice técnico-regulatório:** publicado no pacote documental.
- **Auditoria do repositório:** materializada em [`AUDIT_STATUS.md`](AUDIT_STATUS.md).
- **Submissão à DIO:** concluída conforme declaração do autor registrada em 27/09/2026; a data exata e o comprovante institucional não estão autenticados neste repositório.
- **Nota, aprovação ou certificação:** não são inferidas da publicação ou da submissão declarada.

## Como navegar pelo material

Para uma leitura progressiva:

1. **E-book principal:** [`docs/miniguia-creditexplain-br.md`](docs/miniguia-creditexplain-br.md)
2. **Mapa de siglas e abreviações:** [`docs/siglas-e-abreviacoes.md`](docs/siglas-e-abreviacoes.md)
3. **Apêndice técnico-regulatório:** [`docs/apendice-tecnico-regulatorio-creditexplain-br.md`](docs/apendice-tecnico-regulatorio-creditexplain-br.md)
4. **Corpus completo:** [`docs/corpus-77-fontes.md`](docs/corpus-77-fontes.md)
5. **Experimentos e cicatrizes:** [`docs/experimentos-e-cicatrizes.md`](docs/experimentos-e-cicatrizes.md)
6. **Guia de leitura da pasta `docs/`:** [`docs/README.md`](docs/README.md)
7. **Histórico de versões:** [`CHANGELOG.md`](CHANGELOG.md)
8. **Gate de auditoria:** [`AUDIT_STATUS.md`](AUDIT_STATUS.md)

Para leitores não especialistas, a recomendação é começar pelo e-book e consultar o mapa de siglas sempre que uma abreviação interromper a leitura.

## Metodologia

O trabalho foi conduzido em camadas:

1. **Definição do tema e da pergunta norteadora.**
2. **Construção e expansão do corpus.** O notebook estabilizou em 77 fontes após pesquisa, curadoria e saneamento.
3. **Auditoria das fontes.** Foram registrados jurisdição, autoridade, tipo, atualidade, capacidade probatória, limites e ação recomendada.
4. **Configuração Brasil-first.** Afirmações sobre obrigação, proibição, permissão ou direito no Brasil passaram a exigir fonte brasileira competente.
5. **Experimentos controlados de prompting.** Foram executadas variações da mesma pergunta e perguntas estratégicas, com controle de histórico e notas.
6. **Auditoria das respostas.** Citação correta não foi tratada como prova automática de conclusão correta; escopo, autoridade, terminologia e vigência foram verificados separadamente.
7. **Consolidação editorial original.** O NotebookLM gerou o miniguia, posteriormente revisado por controle humano.
8. **Revisão editorial v2.** Em 27/09/2026, a entrega foi reestruturada como e-book narrativo, com explicações desenvolvidas, exemplos, estudos de caso sintéticos, playbook de governança, apêndice técnico-regulatório e refresh temporal das fontes mutáveis.

O corpus de 77 fontes é uma expansão autoral do projeto. Para a apresentação enxuta recomendada pelo desafio, cinco fontes âncora são destacadas no README; o índice integral permanece separado em [`docs/corpus-77-fontes.md`](docs/corpus-77-fontes.md).

## Cinco fontes âncora

| Fonte | Função no projeto |
|---|---|
| [LGPD — Lei nº 13.709/2018 — texto atualizado da Câmara](https://www2.camara.leg.br/legin/fed/lei/2018/lei-13709-14-agosto-2018-787077-normaatualizada-pl.html) | Proteção de dados, direitos do titular e decisões automatizadas |
| [Resolução Conjunta nº 1/2020 — Open Finance](https://normativos.bcb.gov.br/Lists/Normativos/Attachments/51028/Res_Conj_0001_v8_L.pdf) | Base regulatória do Open Finance brasileiro |
| [Banco Central — Relatório de Cidadania Financeira 2025](https://www.bcb.gov.br/content/cidadaniafinanceira/documentos_cidadania/RCF/relatorio_de_cidadania_financeira_2025.pdf) | Crédito, vulnerabilidades e cidadania financeira |
| [Simonae, Marcon & Casanova — Bridging AI and Ethics](https://sol.sbc.org.br/index.php/sbsi/article/download/41332/41102/) | Referência acadêmica central para ML-XAI-LLM e explicabilidade |
| [Ministério da Saúde — Guia de Cuidado para Pessoas com Problemas Relacionados a Jogos de Apostas — 2026](https://www.gov.br/saude/pt-br/centrais-de-conteudo/publicacoes/guias-e-manuais/2026/guia-de-cuidado-para-pessoas-com-problemas-relacionados-a-jogos-de-apostas.pdf/@@download/file/Guia%20de%20Cuidado%20para%20Pessoas%20com%20Problemas%20Relacionados%20a%20Jogos%20de%20Apostas.pdf) | Fronteira entre comportamento, sinais de risco, cuidado e diagnóstico clínico |

## Engenharia de prompts e aprendizados

Os testes do NotebookLM foram tratados como experimentos, não como produção automática de verdade.

### Experimento 1A

A primeira síntese foi organizada em regras brasileiras, benefícios, riscos, benchmarks internacionais e lacunas. O resultado foi classificado como `PASSOU_COM_RESSALVAS`: a estrutura era boa, mas a auditoria encontrou problemas de negativas universais, temporalidade e precisão normativa.

### Experimento 1B

O prompt seguinte adicionou travas Brasil-first, controle temporal, distinção entre correlação e causalidade, tratamento de jurisdição e separação entre comportamento financeiro e diagnóstico clínico. Houve melhora real, porém permaneceram sobreafirmações semânticas.

### Aprendizado central

**Prompt engineering melhora o comportamento, mas não substitui auditoria humana.** Uma citação correta pode acompanhar uma frase que extrapola a fonte, e uma resposta fluente pode parecer mais fundamentada do que realmente é.

O registro completo está em [`docs/experimentos-e-cicatrizes.md`](docs/experimentos-e-cicatrizes.md).

## O que mudou no e-book v2

A primeira edição funcionava como miniguia de revisão. A segunda edição foi ampliada para funcionar como material formativo mais autônomo e inclui, entre outros elementos:

- narrativa sobre como uma decisão de crédito se transforma em problema de explicabilidade;
- crédito responsável, superendividamento, Cadastro Positivo, SCR e Open Finance;
- performance, calibração, threshold, data drift, concept drift e model risk;
- capítulos didáticos sobre SHAP e LIME;
- framework ML-XAI-LLM e fronteiras de generalização;
- Art. 20 da LGPD, revisão e contestabilidade;
- benchmarks internacionais separados das obrigações brasileiras;
- três estudos de caso sintéticos;
- playbook de governança de explicações;
- perguntas de auditoria para dados, modelo, explicação e governança;
- glossário comentado;
- dez prompts reutilizáveis;
- apêndice técnico-regulatório com matrizes, controles de evidência e maior densidade técnica.

## Refresh temporal

O estado histórico do projeto permanece preservado pelo Git. A edição v2 realizou refresh em 27/09/2026 para pontos materiais mutáveis.

Entre os itens documentados estão:

- vigência da **Resolução CMN nº 5.320/2026** desde 28/08/2026;
- **IN BCB nº 759/2026**, com Manual de Escopo de Dados e Serviços do Open Finance v8.0 e entrada em vigor em 03/11/2026;
- **IN BCB nº 760/2026**, com Manual de Experiência do Cliente do Open Finance v9.0;
- **Resolução Conjunta nº 20/2026**, com alterações na Resolução Conjunta nº 8/2023;
- atualização norte-americana de model risk pela **SR 26-2**.

O detalhamento permanece no corpus, no e-book e no apêndice. A existência de refresh não transforma o projeto em parecer jurídico permanentemente atualizado.

## Aderência ao desafio DIO

- ✅ contexto e objetivos documentados;
- ✅ cinco fontes abertas destacadas e corpus ampliado de 77 fontes registrado;
- ✅ variações de prompts e perguntas estratégicas preservadas;
- ✅ respostas, referências, erros encontrados e correções auditados;
- ✅ e-book v2 revisado e ampliado;
- ✅ apêndice técnico-regulatório consolidado;
- ✅ glossário e prompts reutilizáveis integrados;
- ✅ repositório próprio no GitHub;
- ✅ submissão à plataforma DIO declarada concluída pelo autor em 27/09/2026.

> A marcação acima registra **submissão**, não nota, aprovação, certificação ou avaliação institucional.

## Estrutura do repositório

```text
creditexplain-br/
├── README.md
├── AUDIT_STATUS.md
├── CHANGELOG.md
├── LICENSE
├── NOTICE.md
├── docs/
│   ├── README.md
│   ├── miniguia-creditexplain-br.md
│   ├── siglas-e-abreviacoes.md
│   ├── apendice-tecnico-regulatorio-creditexplain-br.md
│   ├── corpus-77-fontes.md
│   └── experimentos-e-cicatrizes.md
└── assets/
    └── capa-notebooklm-creditexplain-br.png
```

## Limitações e integridade

- O projeto **não executa decisão real de crédito**.
- O conteúdo **não constitui parecer jurídico** ou avaliação de conformidade de uma instituição real.
- O conteúdo **não produz diagnóstico clínico** ou orientação individualizada de saúde.
- Exemplos não documentados como casos reais são **MATERIAL DIDÁTICO FICTÍCIO/SINTÉTICO**.
- Fontes internacionais são benchmarks técnicos/comparativos quando não vinculantes no Brasil.
- Jurisprudência casuística não é promovida a regra universal.
- Outputs de IA não são promovidos automaticamente a conhecimento validado.
- A publicação e a submissão declarada **não permitem inferir nota, aprovação ou certificado**.

## Contexto acadêmico e créditos

O projeto foi desenvolvido no **DIO Bootcamp Bradesco — GenAI, Dados & Cyber**. A orientação do desafio **“Treinando uma IA de Aprendizagem: Explore o Poder do NotebookLM”** é creditada a **Felipe Silva Aguiar (`@felipeAguiarCode`)**, com referência ao ecossistema educacional da **`@digitalinnovationone`**.

Agradeço pelo conteúdo e pela proposta do desafio. Feedback técnico ou pedagógico sobre esta implementação autoral é bem-vindo.

As menções registram origem acadêmica e reconhecimento; **não implicam endosso, avaliação, certificação, vínculo profissional ou aprovação** por parte do instrutor, da DIO ou do Bradesco.

## Autoria, licença e direitos de terceiros

O material autoral do CreditExplain BR segue os termos de [`LICENSE`](LICENSE). Proveniência e limites de materiais de terceiros estão registrados em [`NOTICE.md`](NOTICE.md).

A publicação pública permite leitura e avaliação nos termos documentados, mas não transforma automaticamente o material em conteúdo open source nem relicencia fontes, marcas, publicações ou conteúdos de terceiros.

## Conclusão

O CreditExplain BR demonstra um processo de **curadoria → prompting → verificação → auditoria → correção editorial → consolidação pedagógica → revisão temporal**.

A segunda edição desloca o projeto de um miniguia concentrado para um e-book que procura explicar o raciocínio por trás dos conceitos, conectando regulação, ciência de dados, governança e experiência do consumidor. O apêndice técnico-regulatório preserva a densidade necessária para auditoria sem sacrificar a leitura do corpo principal, enquanto a pesquisa original permanece rastreável pelo histórico versionado.

---

**CreditExplain BR — Crédito Responsável, IA, Open Finance e Explicabilidade**  
Material acadêmico e pedagógico; submissão à DIO declarada concluída pelo autor; nota/certificação não inferidas.