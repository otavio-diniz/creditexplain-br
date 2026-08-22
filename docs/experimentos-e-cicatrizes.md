# Experimentos e Cicatrizes — CreditExplain BR

> Registro publicável dos testes realizados no NotebookLM. Os rótulos 1A/1B e as perguntas estratégicas são controles do projeto; não pressupõem memória interna ou integração do NotebookLM com este repositório.

## Objetivo experimental
O objetivo não foi apenas obter uma boa resposta do NotebookLM. O projeto testou se um corpus amplo e curado, uma configuração Brasil-first e prompts progressivamente mais específicos melhoravam rastreabilidade, precisão normativa, explicabilidade e reconhecimento de limites.
O NotebookLM foi tratado como ferramenta externa: os rótulos 1A, 1B e Perguntas Estratégicas 2/3 são controles do projeto, não memória interna presumida da ferramenta.

## Experimento 1A — síntese base
- **Status Final:** PASSOU_COM_RESSALVAS.
- **Desenho:** síntese em cinco blocos sobre normas brasileiras, benefícios, riscos, benchmarks internacionais e lacunas.
- **Acertos:** estrutura aderente; separação geral entre Brasil e benchmark; reconhecimento de lacunas; distinção entre comportamento financeiro e diagnóstico clínico.
- **Ressalvas:** negativas universais; temporalidade; linguagem normativa excessiva; cobertura Brasil-first incompleta em pontos específicos; necessidade de validar referências indiretas pelas citações nativas.
- **Aprendizado:** uma resposta bem estruturada pode parecer mais precisa do que realmente é; a auditoria precisa separar aparência de fundamentação de suporte efetivo.

## Experimento 1B — mesma pergunta, prompt refinado
- **Status Final:** PASSOU_COM_RESSALVAS.
- **Controle:** histórico zerado; mesma configuração do notebook; corpus de 77 fontes; notas anteriores desmarcadas.
- **Incidente:** uma versão extensa do prompt foi rejeitada pela interface. A solução foi mover regras permanentes para a configuração e usar um prompt operacional compacto.
- **Resultado:** melhoria clara de proveniência, temporalidade e Brasil-first, mas sem eliminar sobreafirmações semânticas.
- **Achados De Auditoria:** houve afirmações corretas, afirmações que exigiam qualificação e pelo menos dois casos materiais a remover/corrigir: atribuição de uma suposta proposta de 'blacklist' ao Banco Mundial e justificativa CEP/CONEP não sustentada pela fonte do estudo da UTFPR.
- **Conclusão A B:** o refinamento do prompt melhorou o comportamento, mas não substituiu a revisão humana. Citação correta não garante automaticamente escopo, autoridade, terminologia ou vigência corretos.

## Pergunta estratégica 2 — convergências, divergências e lacunas
- **Status:** CONCLUÍDA_COM_RESSALVAS.
- **Objetivo:** testar síntese comparativa do corpus, não repetir a pergunta 1.
- **Acertos:** separou convergências brasileiras, divergências, lacunas e benchmarks não vinculantes.
- **Ressalva-Chave:** o NotebookLM reincidiu na justificativa CEP/CONEP para a ausência de testes humanos no artigo da UTFPR mesmo após essa extrapolação já ter sido identificada. A reincidência foi preservada como cicatriz, não corrigida por repetição indefinida de prompts.

## Pergunta estratégica 3 — explicabilidade aplicada
- **Status:** PASSOU_COM_RESSALVAS.
- **Objetivo:** testar transformação de evidência em framework explicável, separando dado observado, métrica, inferência, decisão e limite clínico.
- **Acertos:** framework didático; exemplos de explicação adequada/inadequada; checklist de governança; tratamento explícito de SHAP, LIME e reason codes.
- **Ressalvas:** algumas formulações elevaram recomendação técnica a obrigação, exageraram o alcance de variáveis proibidas ou usaram linguagem causal onde havia apenas influência preditiva.

## Miniguia
- **Status:** GERADO_PELO_NOTEBOOKLM_E_REVISADO_EDITORIALMENTE.
O miniguia final foi gerado a partir do corpus de 77 fontes e posteriormente corrigido para preservar autoria acadêmica, jurisdição, temporalidade, limites de XAI, fronteira clínica e natureza didática dos exemplos/prompts.

## Cicatrizes e troubleshooting
01 — PROMPT LONGO DEMAIS: a interface rejeitou um prompt extenso. Solução: regras persistentes na configuração; prompts curtos e específicos para execução.
02 — CITAÇÃO NATIVA ≠ MARKDOWN: a cópia em Markdown pode perder marcadores visuais de citação. Solução: salvar respostas como notas brutas no NotebookLM e auditar citações na interface antes de classificar falha.
03 — CITAÇÃO CORRETA NÃO GARANTE CONCLUSÃO CORRETA: a fonte pode estar certa e a frase extrapolar escopo, autoridade, terminologia ou vigência.
04 — RECUPERAÇÃO PARCIAL PODE ENGANAR A AUTOAUDITORIA: o NotebookLM pode interpretar um trecho recuperado incompleto como ausência de suporte, mesmo quando a fonte completa contém evidência explícita.
05 — NEGATIVAS UNIVERSAIS SÃO PERIGOSAS: ausência no corpus não prova inexistência no mundo. Preferência: 'não foi identificado nas fontes selecionadas'.
06 — TEMPORALIDADE É SUBSTANTIVA: norma publicada com vigência futura não deve ser escrita como obrigação atual. Exemplo de controle: Resolução CMN nº 5.320/2026.
07 — BRASIL-FIRST É NECESSÁRIO: benchmarks estrangeiros podem enriquecer a análise, mas não criam dever jurídico brasileiro.
08 — FRONTEIRA CLÍNICA: transação observada → padrão financeiro → vulnerabilidade → inferência de risco ≠ diagnóstico de transtorno do jogo.
09 — ALUCINAÇÃO PODE REINCIDIR: a justificativa CEP/CONEP reapareceu após pedido de reverificação. Solução: interromper ciclos improdutivos e corrigir na consolidação editorial com base na fonte.
10 — DEEP RESEARCH EXIGE CURADORIA: relatórios sintéticos autoimportados e fontes secundárias foram excluídos/substituídos para evitar circularidade e vazamento de jurisdição.
11 — QUANTIDADE NÃO É QUALIDADE: o diferencial do corpus de 77 fontes decorre da auditoria fonte a fonte, hierarquia de evidência e controles de uso — não da contagem isolada.
12 — HISTÓRICO E NOTAS ALTERAM O TESTE: comparações independentes exigem histórico controlado e notas brutas desmarcadas; correções da mesma resposta podem manter histórico quando a continuidade é intencional.

## O que mudou do 1A para o 1B
- **Proveniência:** melhorou.
- **Controle Temporal:** melhorou.
- **Brasil First:** melhorou.
- **Negativas Universais:** melhoraram, mas não desapareceram completamente.
- **Precisão Semântica:** continuou exigindo auditoria humana.
- **Resultado:** prompt engineering gerou ganho real, porém o ganho mais importante foi mostrar onde o modelo ainda precisa de controle.

## Evidência pública de respostas e referências
As respostas integrais e suas citações nativas foram preservadas como notas brutas no NotebookLM para manter a rastreabilidade da interface. Para o portfólio público, este documento registra os **resultados auditados**, as correções e as cicatrizes, evitando publicar material bruto redundante.

As referências utilizadas para verificar os experimentos incluem normas e fontes brasileiras primárias, relatórios institucionais, o artigo acadêmico de Simonae, Marcon e Casanova e benchmarks internacionais devidamente classificados. A curadoria completa e os links estão em [`corpus-77-fontes.md`](corpus-77-fontes.md).

## Resultado do conjunto experimental
- **Conjunto:** SUFICIENTE_PARA_O_DESAFIO.
- **Justificativa:** foram testadas variação A/B da mesma pergunta, síntese comparativa, aplicação de explicabilidade e geração de miniguia; o projeto acumulou troubleshooting real e demonstrável.
- **Decisão:** NÃO realizar novos experimentos apenas para aumentar volume. A publicação estruturada no GitHub e o refresh temporal de 22/08/2026 foram concluídos; resta somente a submissão autoral na DIO.

## Nota de integridade
Os exemplos e cenários simulados do projeto são MATERIAL DIDÁTICO FICTÍCIO/SINTÉTICO quando não derivam de um caso real documentado. O projeto não executa decisão real de crédito, parecer jurídico, diagnóstico clínico ou avaliação formal em nome de Otávio.

- **Status:** PUBLICADO_E_AUDITADO_PARA_SUBMISSÃO.
