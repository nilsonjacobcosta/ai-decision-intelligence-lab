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

### Critério de evolução

Esta é uma recorrência mais forte, com **três ocorrências já identificadas**.

Conforme a regra estabelecida para o laboratório, uma **quarta ocorrência independente, em outra trilha**, deverá disparar uma avaliação específica sobre a possibilidade de formalizar o padrão como princípio arquitetural.

---

## Relação entre os dois meta-padrões

Os padrões são distintos e não devem ser fundidos neste estágio:

| Meta-padrão | Pergunta estrutural |
|---|---|
| Escolha de método conforme o problema | **Qual método devo aplicar a este problema?** |
| Normalização de contexto | **Como devo preparar o contexto antes de aplicar o método?** |

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
Operação principal
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
