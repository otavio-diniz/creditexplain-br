# CreditExplain BR

## Crédito Responsável, IA, Open Finance e Explicabilidade

> Projeto do desafio **“Treinando uma IA de Aprendizagem: Explore o Poder do NotebookLM”**, no Bootcamp Bradesco — GenAI, Dados & Cyber.
>
> **Data de corte documental:** 22/08/2026
> **Status:** repositório publicado; auditoria pré-submissão concluída em 22/08/2026.
> **Natureza:** material acadêmico e pedagógico. Não é parecer jurídico, diagnóstico clínico, política real de concessão de crédito nem sistema automatizado em produção.

![Capa do CreditExplain BR](assets/capa-notebooklm-creditexplain-br.png)

## 1. Contexto

O **CreditExplain BR** é um caderno temático construído com NotebookLM para estudar, de forma integrada e crítica, quatro eixos que se cruzam no crédito contemporâneo:

- crédito responsável e prevenção ao superendividamento;
- uso de Inteligência Artificial e Machine Learning em avaliação de risco;
- Open Finance e governança de dados;
- explicabilidade, contestabilidade e limites de inferência em decisões automatizadas.

O projeto foi além de uma simples geração de resumo. O corpus foi ampliado, auditado fonte a fonte e submetido a testes controlados de prompting. O objetivo foi observar não apenas **o que a IA responde**, mas **como a qualidade das fontes, a formulação do prompt, a temporalidade normativa e a revisão humana afetam a confiabilidade da resposta**.

## 2. Pergunta norteadora

> **Como instituições financeiras podem utilizar dados — inclusive dados compartilhados via Open Finance — e sistemas automatizados para apoiar decisões de crédito, preservando transparência, proteção de dados e os princípios do crédito responsável?**

## 3. Objetivos de estudo

1. Mapear o arcabouço brasileiro relevante para crédito responsável, proteção de dados, Open Finance e decisões automatizadas.
2. Investigar benefícios e riscos do uso de IA, Machine Learning e dados alternativos na avaliação de crédito.
3. Estudar técnicas de explicabilidade como SHAP, LIME e reason codes sem confundir influência preditiva com causalidade.
4. Diferenciar norma brasileira vinculante de orientação institucional, evidência empírica, artigo acadêmico e benchmark internacional.
5. Avaliar como o NotebookLM responde a prompts de síntese, comparação, auditoria e aplicação de explicabilidade.
6. Registrar falhas, extrapolações, problemas de citação, limitações de interface e estratégias de correção.
7. Consolidar um miniguia reutilizável com resumos, glossário e prompts para futuras revisões.

## 4. Metodologia

O trabalho foi conduzido em camadas:

1. **Definição do tema e pergunta norteadora.**
2. **Construção e expansão do corpus.** O notebook estabilizou em **77 fontes ativas/selecionadas** após pesquisa, curadoria e saneamento.
3. **Auditoria Zero.** As 77 fontes foram classificadas por jurisdição, autoridade, tipo, atualidade, capacidade probatória, limites e ação recomendada.
4. **Configuração Brasil-first.** Afirmações sobre obrigação, proibição, permissão ou direito no Brasil passaram a exigir fonte brasileira competente.
5. **Experimentos controlados de prompting.** Foram executadas variações da mesma pergunta, com controle de histórico e notas.
6. **Auditoria das respostas.** Citação correta não foi tratada como prova automática de conclusão correta; escopo, autoridade, terminologia e vigência foram revisados separadamente.
7. **Consolidação editorial.** O miniguia final foi revisado para preservar autoria acadêmica, fronteiras de jurisdição, temporalidade, limites de XAI e distinção entre comportamento financeiro e diagnóstico clínico.

> O corpus de 77 fontes é uma expansão autoral do projeto. A DIO recomenda que o README destaque **3 a 5 fontes abertas**; por isso, foram selecionadas cinco fontes âncora para apresentação e o índice completo foi separado em documento próprio.

## 5. Cinco fontes âncora

| Fonte | Função no projeto |
|---|---|
| [LGPD — Lei nº 13.709/2018 — Texto Atualizado da Câmara](https://www2.camara.leg.br/legin/fed/lei/2018/lei-13709-14-agosto-2018-787077-normaatualizada-pl.html) | Proteção de dados, direitos do titular, bases legais e decisões automatizadas |
| [Resolução Conjunta nº 1/2020 — Open Finance](https://normativos.bcb.gov.br/Lists/Normativos/Attachments/51028/Res_Conj_0001_v8_L.pdf) | Base regulatória brasileira do compartilhamento de dados e serviços no Open Finance |
| [Banco Central — Relatório de Cidadania Financeira 2025](https://www.bcb.gov.br/content/cidadaniafinanceira/documentos_cidadania/RCF/relatorio_de_cidadania_financeira_2025.pdf) | Evidência institucional sobre crédito, vulnerabilidades, cidadania financeira, Open Finance e Endiv-IA |
| [Simonae, Marcon & Casanova — Bridging AI and Ethics](https://sol.sbc.org.br/index.php/sbsi/article/download/41332/41102/) | Referência acadêmica brasileira para ML-XAI-LLM, explicabilidade e tradução de explicações |
| [Ministério da Saúde — Guia de Cuidado para Pessoas com Problemas Relacionados a Jogos de Apostas — 2026](https://www.gov.br/saude/pt-br/centrais-de-conteudo/publicacoes/guias-e-manuais/2026/guia-de-cuidado-para-pessoas-com-problemas-relacionados-a-jogos-de-apostas.pdf/@@download/file/Guia%20de%20Cuidado%20para%20Pessoas%20com%20Problemas%20Relacionados%20a%20Jogos%20de%20Apostas.pdf) | Fronteira entre sinais de risco, triagem, cuidado e diagnóstico clínico |

O índice do corpus ampliado está em [`docs/corpus-77-fontes.md`](docs/corpus-77-fontes.md).

## 6. Engenharia de Prompts

### Experimento 1A — síntese base

O primeiro teste pediu uma síntese estruturada em cinco blocos: regras brasileiras, benefícios, riscos, benchmarks internacionais e lacunas. O prompt exigia uso exclusivo das fontes do notebook, citações e separação entre tipos de evidência.

Trecho central do prompt:

```text
Com base exclusivamente nas fontes deste notebook, apresente uma síntese do que é possível afirmar sobre o uso de inteligência artificial, Open Finance e dados alternativos em decisões de crédito responsável no Brasil.

Organize a resposta em cinco blocos:
1. O que a legislação e as autoridades brasileiras efetivamente estabelecem;
2. O que a literatura acadêmica e institucional indica sobre benefícios;
3. Principais riscos: discriminação, proxies, privacidade, qualidade de dados, explicabilidade e superendividamento;
4. O que fontes internacionais sugerem apenas como benchmark ou comparação, sem tratá-las como obrigação brasileira;
5. Lacunas ou questões que as fontes não permitem concluir com segurança.
```

**Resultado:** `PASSOU_COM_RESSALVAS`.

A resposta apresentou boa estrutura e reconheceu várias fronteiras importantes, mas exigiu correções em negativas universais, controle temporal, precisão normativa e alguns pontos Brasil-first.

### Experimento 1B — prompt refinado

O segundo teste manteve a mesma questão substantiva, mas tornou as travas mais explícitas e operacionais. O histórico foi zerado, a configuração permaneceu a mesma e as notas anteriores ficaram desmarcadas.

```text
Produza uma síntese auditável, com base apenas nas fontes selecionadas deste notebook, sobre IA, Open Finance e dados alternativos em decisões de crédito responsável no Brasil.

Use as citações nativas do NotebookLM após cada afirmação material.

Organize em 5 blocos:
1. O que normas e autoridades brasileiras efetivamente estabelecem.
2. Benefícios indicados por literatura acadêmica e institucional.
3. Riscos: discriminação/proxies, privacidade, qualidade de dados, explicabilidade, contestabilidade e superendividamento.
4. Benchmarks internacionais, sempre identificados como comparação não vinculante no Brasil.
5. Lacunas do corpus.

Regras:
- Para afirmar obrigação, proibição, permissão ou direito no Brasil, use fonte brasileira competente.
- Diferencie norma vigente de norma publicada com vigência futura.
- Não generalize decisão judicial isolada.
- Não transforme correlação em causalidade.
- Em apostas, diferencie comportamento financeiro observável, sinal de vulnerabilidade, inferência e diagnóstico clínico.
- Não conclua “não existe” apenas por ausência no corpus; prefira “não foi identificado nas fontes selecionadas”.
- Se uma fonte citar documento que não integra o notebook, trate-o como referência secundária.
- Se houver dúvida ou divergência, reduza o alcance da conclusão e explicite o limite.
```

**Resultado:** `PASSOU_COM_RESSALVAS`.

O refinamento melhorou proveniência, controle temporal e Brasil-first, mas não eliminou sobreafirmações semânticas. A principal conclusão experimental foi que **prompt engineering melhora o comportamento, mas não substitui auditoria humana**.

A documentação completa está em [`docs/experimentos-e-cicatrizes.md`](docs/experimentos-e-cicatrizes.md).

## 7. Cicatrizes e troubleshooting

O projeto preservou dificuldades reais, em vez de apresentar apenas o resultado final “limpo”. Entre as principais cicatrizes:

- **Prompt longo demais:** uma versão extensa foi rejeitada pela interface. A solução foi manter regras permanentes na configuração e usar prompts de execução mais compactos.
- **Citação nativa ≠ Markdown:** a cópia da resposta pode perder marcadores visuais de citação. As respostas foram preservadas como notas brutas para auditoria na interface.
- **Citação correta não garante conclusão correta:** uma fonte pode estar corretamente citada e ainda assim a frase extrapolar escopo, autoridade, terminologia ou vigência.
- **Recuperação parcial pode enganar a autoauditoria:** um trecho recuperado incompleto pode parecer ausência de suporte, mesmo quando a fonte completa contém a evidência.
- **Negativas universais são perigosas:** ausência no corpus não prova inexistência externa. A formulação preferida tornou-se “não foi identificado nas fontes selecionadas”.
- **Temporalidade é substantiva:** norma publicada com vigência futura não deve ser apresentada como obrigação já vigente.
- **Brasil-first é necessário:** benchmarks internacionais enriquecem a análise, mas não criam dever jurídico brasileiro.
- **Fronteira clínica:** transação observada → padrão financeiro → vulnerabilidade → inferência de risco **não equivale** a diagnóstico de transtorno do jogo.
- **Alucinação pode reincidir:** uma justificativa não sustentada pela fonte reapareceu mesmo após reverificação. O ciclo de prompts foi interrompido e a correção foi feita editorialmente com base na fonte.
- **Quantidade não é qualidade:** o valor do corpus de 77 fontes decorre da curadoria e da hierarquia de evidência, não da contagem isolada.

## 8. Principais aprendizados

### 8.1. Fontes precisam de hierarquia

Norma, página institucional, relatório técnico, artigo acadêmico, working paper, benchmark internacional e jurisprudência casuística não têm a mesma capacidade probatória. O projeto passou a registrar explicitamente essas diferenças.

### 8.2. Rastreabilidade é necessária, mas não suficiente

Uma citação nativa ajuda a localizar o trecho utilizado. Ainda assim, é preciso verificar se a conclusão respeita o escopo da fonte, sua jurisdição, seu status e sua vigência.

### 8.3. Explicabilidade não é causalidade

SHAP e LIME podem ajudar a identificar fatores de influência preditiva, mas não demonstram automaticamente causalidade. O framework ML-XAI-LLM foi estudado como referência técnica, sem reivindicação de autoria pelo CreditExplain BR e sem implementação de sistema real de crédito.

### 8.4. Contestabilidade vai além de uma visualização bonita

Uma explicação útil deve apoiar compreensão, identificação de dados incorretos e possibilidade de contestação/revisão, sem expor segredo industrial indevidamente nem prometer transparência absoluta não prevista pela norma.

### 8.5. Comportamento financeiro não é diagnóstico clínico

Transações relacionadas a apostas podem compor análises financeiras e estatísticas dentro de limites jurídicos e metodológicos. Elas não autorizam converter padrões de gasto em diagnóstico de ludopatia ou transtorno do jogo.

## 9. Miniguia de estudo

A entrega pedagógica consolidada está em [`docs/miniguia-creditexplain-br.md`](docs/miniguia-creditexplain-br.md).

O miniguia contém:

- resumos estruturados sobre crédito responsável, Open Finance, IA e risco de crédito;
- explicações de SHAP, LIME, reason codes e framework ML-XAI-LLM;
- seção específica sobre apostas, vulnerabilidade financeira e fronteira clínica;
- governança da explicação ao consumidor;
- benchmarks internacionais claramente separados do direito brasileiro;
- limites e lacunas do corpus;
- glossário com 20 conceitos;
- 10 prompts reutilizáveis para estudo, simulação e auditoria.

## 10. Estrutura do repositório

```text
creditexplain-br/
├── README.md
├── docs/
│   ├── miniguia-creditexplain-br.md
│   ├── corpus-77-fontes.md
│   └── experimentos-e-cicatrizes.md
└── assets/
    └── capa-notebooklm-creditexplain-br.png
```

### O que fica fora do repositório público

Respostas brutas do NotebookLM e artefatos internos de governança permanecem fora do portfólio público. O repositório contém apenas os materiais necessários para compreender, reproduzir em nível pedagógico e avaliar o projeto.

## 11. Limitações e integridade

- O projeto **não executa decisão real de crédito**.
- O conteúdo **não constitui parecer jurídico** ou avaliação de conformidade para uma instituição real.
- O conteúdo **não produz diagnóstico clínico** ou orientação individualizada de saúde.
- Exemplos e cenários não documentados como casos reais são tratados como **MATERIAL DIDÁTICO FICTÍCIO/SINTÉTICO**.
- Fontes internacionais são utilizadas como benchmark técnico/comparativo quando não vinculantes no Brasil.
- Decisões judiciais isoladas são tratadas como estudos de caso, não como regra universal.
- O NotebookLM foi tratado como ferramenta externa ao projeto; os rótulos internos de experimentos não pressupõem memória ou estado interno da ferramenta.
- Outputs de IA foram submetidos a revisão humana e não são promovidos automaticamente a conhecimento validado.

## 12. Refresh normativo pré-submissão — 22/08/2026

A revalidação dos pontos normativos sensíveis foi executada em **22/08/2026**, antes do fechamento acadêmico do projeto:

- **Resolução CMN nº 5.320/2026:** confirmada como publicada, com entrada em vigor em **28/08/2026**. Portanto, no corte deste projeto, obrigações específicas dessa resolução permanecem descritas como **vigência futura**. Se a submissão ocorrer em ou após 28/08/2026, este ponto deve ser rechecado.
- **Resolução Conjunta nº 1/2020 — Open Finance:** confirmada como norma-base vigente do ecossistema; o projeto referencia a versão consolidada disponibilizada pelo Banco Central.
- **Atos SPA/MF sobre apostas:** a página oficial de legislação foi revalidada, incluindo a cadeia normativa usada no projeto para Bolsa Família/BPC, autoexclusão, Novo Desenrola Brasil, Fies tradicional e Fies Empreendedor.
- **ANPD:** a nomenclatura institucional atual foi ajustada para **Agência Nacional de Proteção de Dados**, conforme a transformação institucional ocorrida em 2026.

**Resultado do refresh:** `PASS` para a data de corte de 22/08/2026.

## 13. Checklist de aderência ao desafio DIO

- ✅ **Contexto e objetivos:** apresentados nas seções 1 a 3 deste README.
- ✅ **Curadoria de fontes:** cinco fontes abertas destacadas e corpus ampliado de 77 fontes documentado.
- ✅ **Engenharia de prompts:** perguntas estratégicas e variações 1A/1B registradas.
- ✅ **Respostas, referências e cicatrizes:** resultados auditados e troubleshooting consolidados em [`docs/experimentos-e-cicatrizes.md`](docs/experimentos-e-cicatrizes.md); respostas brutas e citações nativas permanecem preservadas nas notas do NotebookLM.
- ✅ **Miniguia final:** resumos estruturados, glossário e prompts reutilizáveis em [`docs/miniguia-creditexplain-br.md`](docs/miniguia-creditexplain-br.md).
- ✅ **Repositório próprio no GitHub:** publicado em `otavio-diniz/creditexplain-br`.
- ⬜ **Submissão na plataforma DIO:** ação final a ser realizada pelo autor, com a URL principal deste repositório.

## 14. Arquivos do projeto

- [`docs/miniguia-creditexplain-br.md`](docs/miniguia-creditexplain-br.md) — miniguia final, glossário e prompts reutilizáveis.
- [`docs/corpus-77-fontes.md`](docs/corpus-77-fontes.md) — cinco fontes âncora e índice do corpus auditado.
- [`docs/experimentos-e-cicatrizes.md`](docs/experimentos-e-cicatrizes.md) — evolução dos prompts, resultados, auditoria e troubleshooting.

## 15. Conclusão

O principal resultado do CreditExplain BR não é apenas um conjunto de respostas produzidas por IA. O projeto demonstra um processo de **curadoria → prompting → verificação → auditoria → correção editorial → consolidação pedagógica**.

A experiência mostrou que um bom prompt reduz erros, mas não elimina a necessidade de controle humano. Em temas que combinam crédito, dados pessoais, regulação, IA e vulnerabilidade, a qualidade do resultado depende tanto da engenharia de prompts quanto da qualidade das fontes, da leitura crítica e da capacidade de reconhecer limites.

---

**Desafio:** Treinando uma IA de Aprendizagem: Explore o Poder do NotebookLM
**Projeto:** CreditExplain BR — Crédito Responsável, IA, Open Finance e Explicabilidade
**Status documental:** repositório publicado, auditado e academicamente pronto para submissão; a submissão na DIO permanece ação autoral.
