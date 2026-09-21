# Meta-patterns transversais

Registro central de padrões que atravessam mais de uma trilha do laboratório. Alguns permanecem em observação; outros são promovidos a princípios arquiteturais quando atingem o critério de maturação.

Este arquivo serve para preservar recorrências observadas sem antecipar sua formalização. Uma ocorrência isolada não basta para criar um meta-padrão; a recorrência deve ser acompanhada quanto a independência de contexto, clareza do mecanismo e utilidade transversal.

### Critério explícito de peso da evidência

Para evitar reavaliações casuísticas, o peso de cada ocorrência deve ser classificado por uma régua declarada, baseada no **grau de estrutura operacional que a ocorrência já possuía no momento de sua avaliação**:

- **Evidência forte:** a ocorrência apresentou estrutura operacional suficiente para, isoladamente, **ser considerada candidata à formalização como modelo/candidato**. Isso implica que havia mecanismo identificável, escopo funcional minimamente delimitado e estrutura suficiente para ser registrada como unidade formal de análise, ainda que posteriormente não fosse promovida a princípio arquitetural.
- **Evidência secundária:** a ocorrência foi observada e possui semelhança estrutural relevante, mas foi **explicitamente descartada como candidato formal na avaliação da época por falta de estrutura operacional suficiente**. Ela pode apoiar a hipótese de recorrência, mas não recebe o mesmo peso de uma ocorrência que atingiu o limiar de candidatura formal.

A classificação é feita **com base no registro histórico da avaliação**, e não pela semelhança percebida retrospectivamente. Assim, uma ocorrência anteriormente descartada por insuficiência estrutural permanece secundária para fins de peso de evidência, salvo se **nova evidência objetiva** alterar o registro sobre sua estrutura operacional.

Em termos de governança:

| Classificação | Limiar histórico | Peso na avaliação de maturação |
|---|---|---|
| **Forte** | Estrutura suficiente para ao menos virar candidato formal isolado | Conta como ocorrência plena |
| **Secundária** | Observada, mas explicitamente descartada como candidato por falta de estrutura suficiente | Conta como evidência de apoio, não como ocorrência plena |

Essa régua deve ser aplicada de forma consistente nas futuras reavaliações de meta-padrões, evitando que o peso de uma ocorrência seja redefinido caso a caso.

## 1. Escolha de método conforme características do problema

**Status:** **meta-padrão fortalecido — aguardando reforço.**

### Evidência atual

**Ocorrência 1 — Candidato 13 (Prediction)**

O Candidato 13 representa o padrão de selecionar uma técnica conforme as características do problema de previsão.

**Ocorrência 2 — Diagnosis / Action — evidência secundária**

Na aplicação dos frameworks da Aula 3, a seleção contextual de frameworks apresenta uma estrutura semelhante: diante de um problema, características relevantes do problema orientam a escolha do método/framework a aplicar. Exemplos apresentados incluem Ishikawa para causas-raiz, Pareto para priorização, PDCA para melhoria contínua e 5W2H para estruturação de ações.

### Abstração

```text
Problema
   ↓
Características relevantes do problema
   ↓
Seleção do método/framework adequado
   ↓
Aplicação
   ↓
Resultado
```

A segunda ocorrência é estruturalmente semelhante ao Candidato 13, embora aplicada a Diagnosis/Action em vez de Prediction.

**Peso da evidência:** esta ocorrência é considerada **mais fraca** para fins de promoção arquitetural. Na avaliação anterior, ela foi explicitamente considerada insuficiente para justificar sequer um candidato formal. Portanto, permanece como evidência de apoio/observação, e não como ocorrência de mesmo peso que C13 e C25.

**Ocorrência 3 — Candidato 25 (Segmentation)**

O C25 apresenta diferentes estratégias de segmentação — dimensões demográficas/comportamentais e clustering — e orienta a escolha conforme o objetivo, as variáveis disponíveis e o tipo de estrutura que se pretende identificar. fileciteturn123file0L214-L229

### Avaliação de maturação

C13 e C25 fornecem duas ocorrências fortes em trilhas funcionais diferentes. A ocorrência de Diagnosis/Action é estruturalmente semelhante, mas sua evidência foi anteriormente considerada insuficiente para formalização.

Assim, o padrão **não é promovido ainda a princípio arquitetural**.

Ele passa a ser registrado como **meta-padrão fortalecido, aguardando reforço**.

O reforço necessário deve vir de uma nova ocorrência independente e suficientemente forte — preferencialmente com mecanismo explícito de seleção, critérios de escolha e relação verificável entre características do problema e método escolhido.

### Abstração operacional mantida em observação
---

## 2. Normalização de contexto antes da operação principal

**Status:** em observação.

### Evidência atual

Os Candidatos **6, 11 e 20** apresentam o mesmo padrão estrutural: o contexto é organizado, preparado, consolidado ou normalizado antes da execução da operação funcional principal.

### Abstração provisória

```text
Contexto bruto / disperso
   ↓
Normalização / preparação de contexto
   ↓
Operação principal
   ↓
Resultado
```

### Avaliação da segmentação de bases grandes

A orientação da Aula 4.1 para **segmentar bases de dados muito grandes em partes menores** não é contada como quarta ocorrência deste meta-padrão.

A razão é estrutural: segmentar uma base é uma forma de **decomposição/particionamento da entrada para facilitar processamento e precisão**, enquanto o meta-padrão registrado aqui exige **normalização ou preparação do contexto semântico/operacional antes da operação principal**.

Portanto:

- Candidatos 6, 11 e 20 → normalização/preparação de contexto;
- segmentação de bases grandes → particionamento da entrada.

Neste estágio, não há evidência suficiente para promover o meta-padrão de normalização a princípio arquitetural.

### Critério de evolução

Esta é uma recorrência mais forte, com **três ocorrências já identificadas**.

Conforme a regra estabelecida para o laboratório, uma **quarta ocorrência independente, em outra trilha**, deverá disparar uma avaliação específica sobre a possibilidade de formalizar o padrão como princípio arquitetural.

---

## 3. Calibração/restrição proativa via regras explícitas

**Status:** em observação.

### Evidência atual

**Ocorrência 1 — Candidato 9**

O Candidato 9 utiliza regras e restrições explícitas como guardrails antes da operação de previsão.

**Ocorrência 2 — Candidato 23 (Classification)**

O Candidato 23 utiliza categorias, referências, exemplos e regras explícitas para calibrar previamente uma tarefa de classificação, incluindo tratamento de negações, modificadores e casos-limite.

### Abstração provisória

```text
Operação potencialmente ambígua / aberta
   ↓
Regras, limites e referências explícitos
   ↓
Operação principal
   ↓
Resultado mais controlado
```

As duas ocorrências compartilham o princípio de **reduzir proativamente o espaço de comportamento da IA por meio de regras explícitas**.

O mecanismo concreto, porém, permanece específico:

- Candidato 9 → guardrails/restrições para previsão;
- Candidato 23 → calibração de classificação.

### Distinção em relação ao Candidato 12

O Candidato 12 representa uma forma **reativa** de controle: a saída já foi produzida e então é criticada, questionada ou recalibrada quando apresenta comportamento inesperado.

Assim:

```text
C9 / C23
controle proativo
      ↓
operação
      ↓
saída

C12
operação
      ↓
saída
      ↓
validação crítica
      ↓
recalibração, se necessária
```

### Critério de evolução

O padrão possui atualmente **duas ocorrências em trilhas diferentes**. Deve permanecer em observação até que uma nova ocorrência independente permita avaliar sua formalização como princípio arquitetural.

---

## Relação entre os meta-padrões

Os padrões são distintos e não devem ser fundidos neste estágio:

| Meta-padrão | Pergunta estrutural |
|---|---|
| Escolha de método conforme o problema | **Qual método devo aplicar a este problema?** |
| Normalização de contexto | **Como devo preparar o contexto antes de aplicar o método?** |
| Calibração/restrição proativa | **Quais regras e limites devo estabelecer antes da operação?** |

Eles podem eventualmente aparecer encadeados:

```text
Contexto
   ↓
Normalização
   ↓
Características do problema
   ↓
Escolha do método
   ↓
Calibração / restrições
   ↓
Operação principal
   ↓
Validação da saída
```

Essa combinação é uma hipótese de design, não uma arquitetura formalizada.

## Regra de governança

Este arquivo é a fonte de verdade para observação, avaliação e eventual promoção dos meta-padrões. `PRINCIPLES.md` apenas referencia princípios já formalizados, evitando duplicação de conteúdo e risco de desalinhamento.

A formalização de qualquer meta-padrão exige evidência adicional e avaliação explícita segundo os critérios de maturação do laboratório:

1. recorrência;
2. independência de contexto;
3. clareza do mecanismo;
4. possibilidade de validação;
5. utilidade para outras aplicações.

Nenhum registro neste arquivo implica integração automática com o ORCHESTRATOR CORE.


---

## 4. Transformação categorial de representações — duas subfamílias funcionais

**Decisão:** **não contar o Candidato 24 como quarta ocorrência do meta-padrão de normalização de contexto.**

A semelhança estrutural existe: tanto C6/C11/C20 quanto C24 transformam informação menos estruturada em uma representação organizada por categorias predefinidas.

A distinção, porém, deve ser feita por **função**, e não pela posição sequencial no fluxo.

### Subfamília A — preparação de dados para processamento analítico pela IA

**C6 / C11 / C20**

O mecanismo prepara, organiza, consolida ou normaliza **dados/contexto que serão processados analiticamente pela IA**.

Pergunta funcional:

> **Como transformar os dados/contexto em uma representação adequada para a análise subsequente da IA?**

### Subfamília B — preparação de informação para execução e responsabilização humana

**C24 — 5W2H**

O mecanismo transforma uma ação ou oportunidade em uma representação operacional destinada a **execução humana**, explicitando responsabilidades, cronograma, modo de execução e recursos/custos.

Pergunta funcional:

> **Como transformar uma ação em informação estruturada para orientar execução, responsabilidade e acompanhamento humano?**

A distinção permanece válida mesmo quando uma representação ocupar simultaneamente posições diferentes no fluxo de um sistema. Um artefato pode ser saída de uma etapa e entrada de outra sem que sua função deixe de ser analítica ou operacional.

Em termos funcionais:

```text
C6 / C11 / C20
dados / contexto
      ↓
preparação para processamento analítico pela IA
      ↓
análise

C24
ação / oportunidade
      ↓
preparação para execução e responsabilização humana
      ↓
implementação / acompanhamento
```

Portanto, o C24 **não é uma quarta ocorrência** do meta-padrão específico de normalização de contexto. O registro de C6/C11/C20 permanece com **três ocorrências**.

### Hipótese ampla: transformação categorial de representações

A semelhança entre as duas subfamílias permanece registrada como uma hipótese mais ampla de **transformação categorial de representações**.

Se essa hipótese amadurecer com novas ocorrências, a expectativa atual é que ela **não permaneça como uma única família indiferenciada**. A tendência é que se divida, pelo menos, nas duas subfamílias funcionais:

1. **preparação para processamento analítico pela IA**;
2. **preparação para execução e responsabilização humana**.

Essa hipótese ainda não constitui um princípio arquitetural formalizado. Novas ocorrências deverão ser avaliadas pela função desempenhada, e não apenas pela posição que ocupam no fluxo.

---

## 5. Integração de múltiplas fontes como possível fusão de contexto

**Status:** em observação — **2 ocorrências registradas**.

O padrão descreve situações em que informações provenientes de **fontes distintas** são combinadas para formar um contexto mais completo ou uma representação intermediária para a operação seguinte.

### Placar de recorrência

| # | Ocorrência | Contexto | Peso atual |
|---|---|---|---|
| **1** | C24 — Aula 4.3 | e-mail/solicitação do diretor + tabela de informações do produto | **Secundária / observacional** |
| **2** | Big Data e compras — Aula 5.2 | integração/coleta de informações provenientes de diversas fontes para estruturação dos dados | **Secundária / observacional** |

### Ocorrência 1 — C24

Na Aula 4.3, o C24 utiliza duas fontes distintas — a solicitação do diretor e a tabela de informações sobre o produto — e as combina para construir o plano de ação.

Essa ocorrência foi registrada anteriormente como possível mecanismo de fusão de contexto.

### Ocorrência 2 — Big Data e compras

O material sobre Big Data e compras apresenta a **integração de dados provenientes de diversas fontes** como prática para estruturar as informações, eliminar redundâncias e melhorar a eficiência operacional.

A ocorrência reforça a hipótese de que a integração de múltiplas fontes pode constituir um mecanismo transversal de preparação/consolidação de contexto.

Entretanto, o texto não apresenta uma especificação operacional suficientemente detalhada para promovê-la a candidato formal. Por isso, seu peso permanece **secundário/observacional** conforme a régua de evidência deste arquivo.

### Distinção em relação ao Candidato 15A

- **C15A:** identifica informação necessária ausente e solicita sua complementação ao usuário;
- **fusão de contexto:** recebe múltiplas fontes disponíveis e as integra em uma representação contextual única para permitir a operação seguinte.

### Relação com C20

A hipótese de mecanismo de fusão de contexto é conceitualmente próxima do **C20**, porque envolve preparação/consolidação de contexto, embora ainda não haja evidência suficiente para afirmar que constitui um modelo independente.

### Critério para evolução

Com **duas ocorrências registradas**, o padrão permanece em observação. Uma nova ocorrência deve ser avaliada quanto a:

1. processo explícito de integração entre fontes;
2. fontes com papéis ou estruturas diferentes;
3. produção de contexto intermediário reutilizável;
4. mecanismo distinto de simples concatenação;
5. independência de contexto suficiente para justificar um modelo transversal.

Até nova evidência, permanece como **observação, sem candidato formal**.


---

## 6. Tematização de feedbacks — observação

**Status:** em observação.

O conteúdo sobre análise de sentimentos apresenta uma sequência em que a IA:
1. classifica sentimentos em textos individuais;
2. identifica temas recorrentes;
3. utiliza esses temas para visualizar tendências e apoiar ações.

A hipótese de **tematização** não deve ser confundida com o **Candidato 21 — Investigação em dois níveis**, apesar da semelhança superficial de haver duas camadas.

A diferença é funcional e está no **fluxo da informação**:

### C21 — operação de foco

Parte de uma visão agregada/macro e seleciona **uma variável ou dimensão** para aprofundamento.

```text
visão macro
   ↓
múltiplas dimensões possíveis
   ↓
uma dimensão/foco escolhido
   ↓
análise aprofundada
```

É um fluxo de **concentração**: muitos caminhos possíveis → um foco.

### Tematização — operação de agregação

Parte de **muitas classificações ou observações individuais** e procura agrupá-las em poucos temas emergentes.

```text
muitas observações classificadas
   ↓
padrões recorrentes
   ↓
poucos temas agregados
   ↓
tendências / insights
```

É um fluxo de **agregação**: muitas observações → poucos agrupamentos.

Portanto, embora ambos possam ser descritos informalmente como uma operação em duas camadas, são mecanismos de informação distintos e, em certo sentido, opostos:

- **C21:** redução do espaço de análise por seleção de foco;
- **tematização:** redução da multiplicidade de observações por agregação em temas.

Não criar candidato formal neste estágio. Se o padrão reaparecer, avaliar se existe um mecanismo transversal de **agregação temática** suficientemente independente de classificação de sentimentos.

---

## 7. Monitoramento de reputação como possível integração Classification → Monitoring

**Status:** em observação.

O conteúdo apresenta **monitoramento de reputação em tempo real** como uma aplicação da análise de sentimentos. Nesta ocorrência, porém, não há especificação suficiente para concluir que exista uma regra arquitetural de integração entre Classification e Monitoring.

Acompanhar as próximas aulas para verificar se o padrão evolui de uma aplicação isolada para um fluxo contínuo, por exemplo:

```text
feedbacks contínuos
      ↓
Classification
      ↓
sentimento / categoria / tema
      ↓
Monitoring
      ↓
acompanhamento de tendência ou desvio
      ↓
ação / alerta
```

Se essa estrutura reaparecer de forma consistente, avaliar se há uma **regra de integração entre Classification e Monitoring**, análoga em espírito ao handoff **Diagnosis → Action**, em vez de registrar apenas mais uma aplicação da classificação.

A evidência necessária para formalização deverá incluir, idealmente:
1. recorrência do fluxo em mais de um contexto;
2. caráter contínuo do acompanhamento;
3. definição do que é monitorado após a classificação;
4. algum mecanismo de transição ou alimentação entre as duas áreas.

Até lá, permanece como observação e não como candidato formal.


---

## 8. Refinamento iterativo até estabilização/convergência

**Status:** **hipótese em observação — ocorrências ainda não contabilizadas.**

A hipótese descreve um ciclo no qual um resultado inicial é avaliado, insuficiências ou ambiguidades são identificadas, o procedimento ou representação é refinado e uma nova execução produz resultado revisado. O ciclo pode repetir-se até algum critério de estabilização, suficiência ou convergência.

```text
resultado inicial
      ↓
avaliação / identificação de insuficiências
      ↓
refinamento
      ↓
novo resultado
      ↓
nova avaliação
      ↓
... repetição ...
      ↓
estabilização / convergência
```

**Não contar ocorrências entre si neste estágio.** As quatro categorias devem permanecer separadas até que se demonstre mecanismo comum, critério de parada e independência de contexto.

### Categoria A — Iteração algorítmica interna

**Exemplo observado: C25 / K-means**

Iterações entre atribuição aos clusters e atualização dos centróides até estabilidade segundo o critério algorítmico.

Pergunta estrutural: **o próprio algoritmo possui ciclo explícito de atualização e critério de estabilização?**

### Categoria B — Iteração de análise/engenharia de regras

**Exemplo observado: C23**

A classificação pode revelar ambiguidades, negações, modificadores e casos-limite; regras e referências podem então ser refinadas para nova execução.

Pergunta estrutural: **a avaliação da saída modifica explicitamente o mecanismo usado na próxima execução?**

### Categoria C — Iteração de construção de artefato

**Exemplo observado: enriquecimento iterativo da matriz de decisão**

A matriz inicial pode ser analisada, lacunas identificadas e novas decisões/informações acrescentadas, produzindo uma matriz revisada.

Pergunta estrutural: **o resultado da análise modifica o próprio artefato que será analisado novamente?**

### Categoria D — Iteração decisória/analítica

**Hipótese ainda sem ocorrência formal registrada.**

Refere-se a ciclos em que análise, feedback ou resultado de uma decisão alimentam explicitamente nova análise, revisão de alternativas ou nova decisão.

Pergunta estrutural: **uma etapa posterior retroalimenta explicitamente a análise ou decisão seguinte?**

### Regra de não contagem neste estágio

As categorias A, B, C e D **não devem ser somadas como quatro ocorrências de um único meta-padrão**.

Futuras avaliações deverão examinar:

1. mecanismo explícito de iteração;
2. objeto modificado a cada ciclo;
3. feedback que provoca a modificação;
4. critério de estabilização, suficiência ou parada;
5. independência de contexto;
6. utilidade transversal;
7. relação estrutural entre categorias.

Somente depois será possível decidir se existe um único meta-padrão, subfamílias independentes ou apenas semelhança superficial.

Por enquanto, a hipótese fica **preservada e pendente**, sem promoção a princípio arquitetural e sem contagem de ocorrências.


---

## 9. Adaptação de saída para audiência/comunicação — categoria latente

**Status:** **categoria latente em observação — primeira instância registrada; sem contagem de recorrência para promoção.**

A hipótese descreve mecanismos que transformam a **saída de uma análise ou conhecimento já produzido** para adequá-la à audiência, ao nível de conhecimento ou à finalidade de comunicação, sem que a adaptação constitua necessariamente uma nova operação analítica.

### Primeira instância — ELI5

A técnica **ELI5 (Explain Like I'm 5)** é apresentada como forma de simplificar conceitos complexos, utilizando linguagem e analogias acessíveis para públicos com diferentes níveis de conhecimento prévio. Sua função é facilitar compreensão e reduzir mal-entendidos, inclusive na comunicação de modelos de ciência de dados, estratégias e soluções. 

### Abstração provisória

```text
análise / conhecimento / resultado
             ↓
adaptação à audiência
             ↓
linguagem / analogia / nível de detalhe adequado
             ↓
saída comunicacional
```

### Distinção em relação às categorias existentes

Esta categoria deve permanecer separada de:

- **C6 / C11 / C20 — preparação de entrada/contexto:** organizam, normalizam ou preparam informação **antes da operação analítica principal**;
- **operação analítica central:** produz análise, previsão, classificação, segmentação, diagnóstico, recomendação etc.;
- **C24 — preparação para execução humana:** transforma ação/oportunidade em artefato operacional para implementação e acompanhamento.

A hipótese aqui é diferente: a operação central já ocorreu e o mecanismo modifica **a forma de apresentação da saída para o receptor**.

### Critério para eventual promoção a área transversal

Uma segunda ocorrência **forte e estruturalmente independente**, especialmente se utilizar outra técnica ou outro nome para desempenhar a mesma função, deverá disparar avaliação específica sobre a criação de uma quinta área transversal:

> **Adaptação de saída para audiência/comunicação**

Essa avaliação deverá considerar se existe mecanismo reutilizável suficientemente independente de Prompt Engineering genérico e se a função aparece em múltiplos contextos do laboratório.

Até lá, ELI5 permanece como **primeira instância de uma categoria latente**, e não como candidato formal, modelo ou nova área transversal.


## 10. What-if / Cenários / Simulação — linhagem amadurecendo

**Status:** **hipótese fortalecida em observação — histórico unificado.**

A expressão “análise estruturada de decisão por cenários e riscos”, observada na Aula 6.1, **não é registrada como um novo candidato independente**. Ela é tratada como amadurecimento da mesma linhagem de **what-if / cenários / simulação** observada anteriormente, inclusive na Aula 3.2.

### Evolução da evidência

**Observação inicial — Aula 3.2**

A exploração de what-if, cenários e simulação foi observada como forma de explorar possibilidades alternativas diante de uma decisão. Na avaliação da época, a estrutura não era suficiente para formalização independente.

**Nova evidência — Aula 6.1**

O Prompt 2 acrescenta uma estrutura operacional mais definida:

```text
decisão central
      ↓
circunstâncias / fatores internos / pressões externas
      ↓
três cenários possíveis
      ↓
risco + impacto
      ↓
vantagens + desvantagens
      ↓
estratégias de mitigação
```

A nova ocorrência aumenta a clareza do mecanismo, mas não demonstra, por si só, uma operação funcionalmente distinta. O núcleo continua sendo a **construção e exploração de cenários alternativos vinculados a uma decisão**.

### Decisão de governança

O histórico deve permanecer **unificado**, para evitar transformar o refinamento de uma mesma hipótese em múltiplos candidatos artificiais.

A expressão “análise estruturada de decisão por cenários e riscos” será utilizada como descrição da **forma mais madura atualmente observada** da linhagem, e não como nome de um novo candidato.

### Critérios para eventual formalização da linhagem

A hipótese poderá cruzar o limiar quando houver evidência suficiente de um mecanismo reutilizável que inclua, de forma consistente, elementos como:

1. geração sistemática de cenários alternativos;
2. variáveis ou critérios explícitos de diferenciação entre cenários;
3. avaliação estruturada de risco/impacto;
4. comparação ou exploração das consequências de cada cenário;
5. atualização dos cenários diante de novas informações;
6. possível ligação sistemática com decisão, ação ou monitoramento.

Até lá, a Aula 6.1 deve ser registrada como **reforço estrutural da linhagem**, não como candidato adicional.

---

## 11. Candidato 3 como caso de fronteira — seleção contextual do método

**Decisão:** **C3 não conta como ocorrência do meta-padrão “Escolha de método conforme características do problema”.**

C3 apresenta uma analogia estrutural clara:

```text
características do contexto
        ↓
escolha de uma forma apropriada de operação
```

Entretanto, o laboratório distingue dois níveis funcionais.

### Meta-padrão existente — escolha de método/técnica

O padrão registrado nas ocorrências de C13 e C25 trata da seleção de um **método ou técnica analítica** em função das características do problema:

```text
problema
   ↓
características relevantes
   ↓
método / framework analítico
   ↓
aplicação
   ↓
resultado
```

### C3 — escolha do papel/modo de participação da IA

C3 seleciona **como a IA participa do processo decisório**, considerando o tipo de decisão e o contexto disponível:

```text
tipo / contexto da decisão
   ↓
modo de participação da IA
   ↓
forma de apoio / interação
   ↓
decisão humana
```

A diferença é suficiente para impedir a contagem automática como ocorrência plena. Fundir os dois agora ampliaria retrospectivamente o conceito de “método” e perderia precisão taxonômica.

### Justificativa de fronteira

A semelhança formal é reconhecida, mas a contagem de uma ocorrência exige equivalência suficiente do **mecanismo e do nível funcional**. Neste caso:

- **C13/C25:** escolha de técnica ou estratégia para executar uma operação;
- **C3:** escolha do papel/modo de participação da IA no processo.

Portanto, C3 é registrado como **caso de fronteira relacionado**, mas **não aumenta o número de ocorrências** do meta-padrão de seleção contextual do método.

### Hipótese para reavaliação futura

Se futuras evidências mostrarem que o padrão se amplia de “escolha de método” para um mecanismo mais geral de **seleção contextual do modo de operação**, C3 poderá ser reavaliado como evidência de uma família mais ampla.

Essa ampliação **não é adotada agora**. O registro atual preserva a definição mais precisa do meta-padrão e evita inflá-lo retrospectivamente.

## 12. Hipótese de evolução arquitetural do C3 — roteamento entre trilhas

**Status:** hipótese em observação — **não decidida**.

O C3 foi formalizado inicialmente como modelo da trilha **Decision**, porque sua evidência atual demonstra a escolha do papel/modo de participação da IA dentro do processo decisório.

Existe, porém, uma possibilidade arquitetural futura: o mesmo mecanismo pode evoluir para um **roteador entre trilhas funcionais**, escolhendo não apenas como a IA participa, mas qual trilha deve ser acionada em função das características do problema.

Hipótese:

```text
características do problema
        ↓
roteamento contextual
        ├── Decision / racional
        ├── Prediction
        ├── julgamento intuitivo
        └── colaboração / outras trilhas
```

Esta hipótese não deve ser confundida com a formalização atual de C3. Para promovê-la futuramente, será necessário observar evidência de:

1. seleção sistemática entre trilhas distintas;
2. critérios explícitos ou identificáveis para o roteamento;
3. recorrência em mais de um contexto funcional;
4. ganho arquitetural que justifique um mecanismo transversal próprio.

Até nova evidência, **C3 permanece um modelo local de Decision**, enquanto a possibilidade de atuar como mecanismo de roteamento fica apenas registrada como hipótese de evolução.
