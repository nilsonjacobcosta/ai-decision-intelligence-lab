# Meta-patterns transversais

Registro central de padrões que atravessam mais de uma trilha do laboratório, mas que ainda **não estão formalizados como princípios arquiteturais**.

Este arquivo serve para preservar recorrências observadas sem antecipar sua formalização. Uma ocorrência isolada não basta para criar um meta-padrão; a recorrência deve ser acompanhada quanto a independência de contexto, clareza do mecanismo e utilidade transversal.

## 1. Escolha de método conforme características do problema

**Status:** em observação.

### Evidência atual

**Ocorrência 1 — Candidato 13 (Prediction)**

O Candidato 13 representa o padrão de selecionar uma técnica conforme as características do problema de previsão.

**Ocorrência 2 — Diagnosis / Action**

Na aplicação dos frameworks da Aula 3, a seleção contextual de frameworks segue a mesma estrutura: diante de um problema, características relevantes do problema orientam a escolha do método/framework a aplicar. Exemplos apresentados incluem Ishikawa para causas-raiz, Pareto para priorização, PDCA para melhoria contínua e 5W2H para estruturação de ações.

### Abstração provisória

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

### Critério de evolução

Com **duas ocorrências em trilhas diferentes**, o padrão já merece rastreamento como possível meta-padrão transversal, mas **ainda não deve ser formalizado como princípio arquitetural**.

Uma nova ocorrência independente em outra trilha poderá fornecer evidência adicional para avaliar sua formalização.

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

Meta-padrões neste arquivo são **observações transversais**, não candidatos aprovados e não componentes implementáveis.

A formalização de qualquer meta-padrão exige evidência adicional e avaliação explícita segundo os critérios de maturação do laboratório:

1. recorrência;
2. independência de contexto;
3. clareza do mecanismo;
4. possibilidade de validação;
5. utilidade para outras aplicações.

Nenhum registro neste arquivo implica integração automática com o ORCHESTRATOR CORE.


---

## 4. Estruturação categorial de saída versus normalização de contexto

**Decisão:** **não contar o Candidato 24 como quarta ocorrência do meta-padrão de normalização de contexto.**

A semelhança superficial existe: tanto o padrão de normalização quanto o 5W2H transformam informação menos estruturada em uma representação organizada por categorias predefinidas.

A diferença funcional, porém, é suficiente para manter as famílias separadas:

- **C6 / C11 / C20 — normalização de contexto:** preparação, organização ou consolidação da **entrada/contexto** antes da operação principal;
- **C24 — 5W2H:** estruturação da **saída/plano de ação**, depois que uma ação ou oportunidade já foi identificada.

Em termos de fluxo:

```text
C6 / C11 / C20
contexto bruto
    ↓
normalização da entrada
    ↓
operação principal

C24
ação identificada
    ↓
estruturação da saída/plano
    ↓
execução
```

Portanto, a orientação de que uma quarta ocorrência independente do padrão de normalização deve disparar sua reavaliação **permanece válida**. O C24 não satisfaz esse critério porque pertence a outra etapa funcional do processo.

A semelhança sugere, contudo, uma hipótese mais ampla de **transformação categorial de representações**. Ela não será formalizada como meta-padrão neste momento; somente deverá ser considerada se novas ocorrências mostrarem que a mesma operação estrutural aparece de forma independente em diferentes etapas e com utilidade transversal.

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
