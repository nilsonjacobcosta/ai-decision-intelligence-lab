# Candidatos prontos para uma futura avaliação de integração

**Status:** registro de encerramento do ciclo v1.0.  
**Escopo:** curadoria interna do laboratório. Este documento **não autoriza nem executa integração com o ORCHESTRATOR CORE**.

## Critério da curadoria

A lista reúne modelos que, ao final deste ciclo, apresentam combinação particularmente consistente de:

- formalização explícita no laboratório;
- mecanismo reutilizável claramente delimitado;
- referências ou composição explícita com outros candidatos/modelos;
- presença em mais de uma relação arquitetural, quando demonstrada;
- capacidade de funcionar como componente de outros fluxos sem depender de um contexto único.

A densidade de referências cruzadas é tratada como **evidência de reutilização potencial**, não como ranking ou prova de superioridade.

## Núcleo curado

### C16 — Orquestração e priorização de ações
É um dos componentes com maior rede de composição explícita: C3 o utiliza na transição do modo racional para o intuitivo; C26 é delimitado em relação a ele; C16 também se articula com C24 e C17, enquanto a documentação do refinamento iterativo o preserva como mecanismo distinto que pode ser composto. O modelo ainda possui três variantes de critérios já demonstradas: GUT, Esforço × Impacto e Impacto × Viabilidade.

### C3 — Papel da IA conforme o tipo de decisão
O C3 apresenta forte potencial transversal porque articula explicitamente C15A, C21, C16, C24 e C12, além de possuir uma extensão de transição entre modos decisórios. A documentação do refinamento iterativo também o cita diretamente como mecanismo distinto que pode ser composto. A evidência de reutilização do C3 aparece mais pela **composição arquitetural explícita** do que por grande número de referências recebidas.

### C12 — Validação crítica da saída do Forecast
O C12 é reutilizado explicitamente pelo C3 para delimitar a diferença entre mudança de modo decisório e validação da saída analítica, e pelo C23 para distinguir validação reativa de calibração proativa. No próprio pipeline de previsão, também se relaciona ao C10 e ao C8. Isso lhe dá uma posição clara como componente de controle/validação posterior à geração do forecast.

### C23 — Calibração de classificação por regras explícitas
O C23 é diretamente relacionado ao C9 e ao C12, e também fornece uma das quatro manifestações do modelo transversal de refinamento iterativo. Além disso, C25 o utiliza como contraponto para separar classificação de segmentação. A combinação de referências cruzadas e recorrência em um meta-padrão torna o mecanismo particularmente reutilizável.

### C25 — Segmentação por padrões de comportamento
O C25 se articula explicitamente com C23, C21 e C16 e fornece a evidência mais completa da subfamília de **iteração algorítmica interna** no modelo de refinamento iterativo, por meio do K-means e de sua estabilização. Também é uma das ocorrências fortes do meta-padrão de escolha de método conforme as características do problema.

### C9 — Guardrails para Previsão
O C9 mantém relação explícita com C23 por compartilhar o mecanismo transversal de restrições/regras proativas e com o C12 no ecossistema de validação de previsão. A documentação do laboratório também o utiliza como uma das ocorrências do padrão de calibração/restrição proativa. Sua rede de referências recebidas é menor que a de C16/C23, mas o mecanismo está bem delimitado e possui papel complementar claro no ciclo de previsão.

### Refinamento iterativo — modelo transversal
O modelo transversal consolida evidências provenientes de C25, C23, enriquecimento de matriz de decisão e SWOT, e explicita uma abstração comum sem fundir mecanismos distintos. Ele também registra separadamente sua relação com C16 e C3. Sua força está menos em referências recebidas — por ser um modelo consolidado mais recentemente — e mais na quantidade e diversidade de mecanismos que consegue explicar sem apagar suas diferenças.

## Candidatos próximos do núcleo

Alguns modelos apresentam composição relevante, mas a rede de referências cruzadas observada neste ciclo ainda é menor ou mais localizada. Eles permanecem formalizados e podem entrar em uma futura avaliação, sem necessidade de incluí-los nesta curadoria nuclear.

- **C21 — Investigação em dois níveis:** articula-se com C22 e C25 e serve como estrutura transversal de investigação, mas sua rede de composição ainda é mais concentrada.
- **C24 — Estruturação operacional por 5W2H:** recebe composição explícita de C3 e C16 e ocupa uma posição clara na passagem de ação para execução, mas permanece mais especializado na operacionalização.
- **C26 — Mapeamento de oportunidades:** possui delimitação arquitetural explícita em relação a C16 e fluxo opcional C26 → C16 → C24; sua formalização é recente, portanto a rede de referências ainda é menor.

## Leitura correta da lista

Esta curadoria **não é uma seleção para integração**. Ela apenas registra quais componentes chegam ao fechamento do ciclo com sinais particularmente claros de reutilização e composição.

A próxima decisão, em momento separado, poderá avaliar:

1. quais desses componentes merecem teste de integração;
2. em que contexto do ORCHESTRATOR CORE;
3. com quais interfaces e limites;
4. quais evidências adicionais ainda seriam necessárias.

Até que essa frente seja aberta explicitamente, o laboratório e o ORCHESTRATOR CORE permanecem separados.
