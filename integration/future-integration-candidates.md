# Candidatos prontos para uma futura avaliação de integração

**Status:** registro de encerramento do ciclo v1.0.  
**Escopo:** curadoria interna do laboratório. Este documento **não autoriza nem executa integração com o ORCHESTRATOR CORE**.

## Critério da curadoria

A lista foi construída a partir dos documentos formais revisados no fechamento, considerando:

- formalização explícita no laboratório;
- mecanismo reutilizável claramente delimitado;
- referências cruzadas explícitas entre candidatos/modelos;
- composição arquitetural demonstrada;
- capacidade de funcionar como componente de outros fluxos sem depender de um contexto único.

A densidade de referências cruzadas é tratada como **evidência de reutilização potencial**, não como ranking ou prova de superioridade. Quando um modelo é importante por suas relações de saída, mas recebe poucas referências, isso é indicado explicitamente.

### Duas dimensões que não devem ser confundidas

A análise de referências recebidas possui um **viés temporal estrutural**: candidatos formalizados mais cedo no curso tiveram mais aulas subsequentes nas quais poderiam ser citados. Portanto, maior número de referências recebidas pode refletir simplesmente **maior tempo de exposição**, e não maior solidez, centralidade ou potencial de integração.

Por isso, esta curadoria separa duas dimensões:

1. **Maturidade por evidência acumulada** — quantidade e diversidade de evidências já observadas, incluindo referências cruzadas documentadas, recorrência, variações de aplicação e explicitação de limites.
2. **Centralidade estrutural na arquitetura** — papel que o componente desempenha na organização dos fluxos e na relação entre outros mecanismos, independentemente de quantas referências ele já acumulou.

Essas dimensões são complementares, mas não equivalentes. Um candidato recente pode ter **alta centralidade estrutural e baixa maturidade por evidência acumulada** simplesmente por ter tido menos tempo de exposição no curso.

Essa distinção é especialmente relevante para **C3, C25 e o modelo de refinamento iterativo**. O checkpoint mestre já registra aspectos estruturais desses componentes que não devem ser penalizados pelo viés temporal: C3 como mecanismo de transição entre modos decisórios, incluindo a passagem Decision → intuição/heurística; C25 como origem de uma ocorrência forte do meta-padrão de seleção contextual do método; e o refinamento iterativo como modelo transversal que consolida mecanismos de diferentes famílias. A menor quantidade de referências recebidas desses componentes não deve ser interpretada isoladamente como menor solidez arquitetural.

Em uma futura avaliação de integração, **referências recebidas devem ser tratadas como um indicador temporalmente condicionado, nunca como proxy único de qualidade ou centralidade**.

## Núcleo curado

### C16 — Orquestração e priorização de ações

É um dos componentes com maior rede de composição explícita nos documentos revisados. É referenciado diretamente por C3, C25, C26 e pelo modelo de refinamento iterativo como mecanismo distinto que pode ser composto. Também se articula com C24 e C17 em sua própria delimitação funcional. O modelo possui três variantes de critérios já demonstradas: GUT, Esforço × Impacto e Impacto × Viabilidade.

### C12 — Validação crítica da saída do Forecast

Recebe referências explícitas de C3 e C23, que o utilizam para delimitar validação crítica reativa em relação a mudança de modo decisório e calibração proativa. No próprio pipeline de previsão, relaciona-se a C10 e C8. Isso lhe dá uma função clara de controle posterior à geração do forecast.

### C23 — Calibração de classificação por regras explícitas

Recebe referências explícitas de C25 e do modelo de refinamento iterativo. Em sua própria definição, mantém relações funcionais com C9 e C12. Assim, participa de dois eixos de reutilização: calibração proativa de classificação e refinamento iterativo de regras/referências.

### C21 — Investigação em dois níveis

Recebe referências explícitas de C3, C22 e C25. O C21 fornece uma estrutura de investigação transversal — visão geral → seleção do foco → aprofundamento — que pode ser combinada com interação humana e segmentação sem absorver essas funções.

### C24 — Estruturação operacional por 5W2H

Recebe composição explícita de C3 e C16 e ocupa uma posição clara na passagem de uma ação selecionada para um plano operacional. Sua função é especializada, mas bem delimitada e complementar a outros mecanismos da trilha Action.

### C3 — Papel da IA conforme o tipo de decisão

O C3 apresenta forte potencial transversal porque referencia explicitamente C15A, C21, C16, C24 e C12, além de possuir uma extensão de transição entre modos decisórios. O modelo de refinamento iterativo também o cita como mecanismo distinto que pode ser composto. A ressalva é importante: nos documentos revisados, a reutilização do C3 aparece mais pela **composição arquitetural que ele habilita** do que por grande número de referências recebidas.

### C25 — Segmentação por padrões de comportamento

O C25 referencia explicitamente C23, C21 e C16 e fornece a evidência mais completa da subfamília de **iteração algorítmica interna** no modelo de refinamento iterativo, por meio do K-means e de sua estabilização. Também constitui uma das ocorrências fortes do meta-padrão de escolha de método conforme as características do problema. Sua rede de referências recebidas é menor, mas sua função de composição é ampla.

### C9 — Guardrails para Previsão

Recebe referência explícita de C23 e ocupa uma posição clara como camada de restrição proativa do processo de previsão. Também aparece no meta-padrão de calibração/restrição proativa. A rede de referências recebidas é menor que a de C16, C21 ou C12; sua inclusão decorre da delimitação forte do mecanismo e da complementaridade com C12 no ciclo de previsão, e não de alta centralidade documental.

### Refinamento iterativo — modelo transversal

Consolida evidências provenientes de C25, C23, enriquecimento de matriz de decisão e SWOT e estabelece uma abstração comum sem fundir mecanismos distintos. Também registra explicitamente sua relação com C16 e C3. Por ser um modelo formalizado mais recentemente, ainda recebe poucas referências diretas de outros documentos; sua força está na **diversidade de mecanismos que consegue explicar e preservar em uma mesma família**, não na centralidade de referências recebidas.

## Como ler a curadoria

A lista não representa uma ordem de prioridade. Ela identifica um **núcleo de componentes com sinais claros de reutilização, composição ou centralidade estrutural** no estado atual do laboratório.

Os exemplos sugeridos no fechamento — C9, C12, C16, C23, C3 e o modelo de refinamento iterativo — foram, portanto, **confirmados com ressalvas diferentes**:

- C16 e C12 apresentam rede explícita de referências recebidas;
- C23 e C21 também possuem múltiplas referências recebidas;
- C3 e C25 são mais fortes pela composição que habilitam;
- C9 possui rede de referências menor, mas mecanismo bem delimitado;
- refinamento iterativo é transversal e consolidante, ainda com pouca referência recebida por sua formalização recente.

## Próximos candidatos, fora do núcleo

- **C26 — Mapeamento de oportunidades:** possui delimitação arquitetural explícita em relação a C16 e fluxo opcional C26 → C16 → C24, mas sua formalização é recente e a rede de referências ainda é menor.
- Outros modelos formalizados permanecem disponíveis para futura avaliação; não foram elevados ao núcleo apenas porque a rede de composição cruzada observada neste fechamento ainda é mais localizada.

## Limite arquitetural

Esta curadoria **não é uma seleção para integração**. Ela apenas registra quais componentes chegam ao fechamento do ciclo com sinais particularmente claros de reutilização e composição.

Uma futura frente, aberta separadamente, poderá avaliar contexto, interfaces, testes e limites de eventual integração com o ORCHESTRATOR CORE.

Até que essa frente seja aberta explicitamente, o laboratório e o ORCHESTRATOR CORE permanecem separados.
