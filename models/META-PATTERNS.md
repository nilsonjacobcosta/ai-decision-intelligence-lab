# Meta-patterns transversais

Registro central de padrões que atravessam mais de uma trilha do laboratório, mas que ainda **não estão formalizados como princípios arquiteturais**.

Este arquivo serve para preservar recorrências observadas sem antecipar sua formalização. Uma ocorrência isolada não basta para criar um meta-padrão; a recorrência deve ser acompanhada quanto a independência de contexto, clareza do mecanismo e utilidade transversal.

## 1. Escolha de método conforme características do problema

**Status:** **promovido a princípio arquitetural.**

### Evidência atual

**Ocorrência 1 — Candidato 13 (Prediction)**

O Candidato 13 representa o padrão de selecionar uma técnica conforme as características do problema de previsão.

**Ocorrência 2 — Diagnosis / Action**

Na aplicação dos frameworks da Aula 3, a seleção contextual de frameworks segue a mesma estrutura: diante de um problema, características relevantes do problema orientam a escolha do método/framework a aplicar. Exemplos apresentados incluem Ishikawa para causas-raiz, Pareto para priorização, PDCA para melhoria contínua e 5W2H para estruturação de ações.

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

**Ocorrência 3 — Candidato 25 (Segmentation)**

O C25 apresenta diferentes estratégias de segmentação — dimensões demográficas/comportamentais e clustering — e orienta a escolha conforme o objetivo, as variáveis disponíveis e o tipo de estrutura que se pretende identificar. fileciteturn123file0L214-L229

### Promoção a princípio arquitetural

A terceira ocorrência independente, em outra trilha funcional, fornece evidência suficiente para promover o padrão a princípio arquitetural do laboratório:

> **Escolher o método conforme as características do problema, dos dados disponíveis e do objetivo, em vez de assumir uma técnica fixa como universalmente adequada.**

A escolha deve ser justificada antes da aplicação quando isso for relevante para a operação.

A promoção não transforma o princípio em um catálogo prescritivo de métodos. Ela estabelece um **critério de seleção**, deixando a escolha concreta dependente do contexto.

### Princípio arquitetural decorrente

O laboratório passa a tratar **seleção contextual do método** como uma regra de composição transversal:

```text
características do problema
        ↓
características dos dados / contexto
        ↓
objetivo da operação
        ↓
escolha justificada do método
        ↓
aplicação
```

Isso não cria uma nova trilha; orienta como componentes de diferentes trilhas devem ser escolhidos.

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

Os registros em observação neste arquivo são **hipóteses transversais**, não candidatos aprovados e não componentes implementáveis. Quando um padrão é promovido, seu princípio arquitetural é explicitado no próprio registro e em `PRINCIPLES.md`.

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

**Status:** em observação.

Na Aula 4.3, o C24 recebe duas fontes distintas — a solicitação do diretor e a tabela de informações sobre o produto — e as combina para construir o plano de ação.

Esse comportamento **não deve ser automaticamente reduzido ao Candidato 15A**.

- **C15A:** identifica informação necessária ausente e solicita sua complementação ao usuário;
- **possível fusão de contexto:** recebe múltiplas fontes disponíveis e as integra em uma representação contextual única para permitir a operação seguinte.

A hipótese de mecanismo de fusão de contexto é conceitualmente mais próxima do **C20**, porque envolve preparação/consolidação de contexto, embora ainda não haja evidência suficiente para afirmar que constitui um modelo independente.

Se o padrão reaparecer em outras aulas e trilhas, avaliar especificamente:
1. se há um processo explícito de integração entre fontes;
2. se as fontes possuem papéis ou estruturas diferentes;
3. se a integração produz um contexto intermediário reutilizável;
4. se o mecanismo é distinto de simples concatenação de informações.

Até nova evidência, permanece como **observação**, sem candidato formal.


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
