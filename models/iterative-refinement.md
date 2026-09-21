# Refinamento iterativo até estabilização/convergência

**Status:** modelo transversal formalizado como família de mecanismos com quatro subfamílias distintas.

## Objetivo

Representar processos nos quais um estado, artefato, regra ou análise inicial é submetido a feedback ou nova informação, sofre uma transformação identificável e produz um novo estado relacionado ao anterior.

O modelo não trata toda repetição como iteração relevante. Para caracterizar **refinamento iterativo**, é necessário demonstrar continuidade entre estados. Quando o objetivo específico for **estabilização/convergência**, deve existir também uma noção de suficiência, estabilidade ou condição de parada.

O modelo é transversal: suas quatro subfamílias possuem mecanismos e critérios de convergência diferentes e, por isso, **não devem ser reduzidas a um único algoritmo ou framework operacional**.

## Abstração central

```text
Estado inicial
    ↓
feedback / nova informação
    ↓
transformação identificável
    ↓
novo estado relacionado ao anterior
    ↓
avaliação de suficiência / estabilidade
    ↓
continua ou estabiliza
```

A etapa de suficiência/estabilidade pode assumir formas diferentes conforme a subfamília. Ela pode ser algorítmica, analítica, construtiva ou humana/pragmática.

## Cinco critérios operacionais

A identificação de uma manifestação deve ser avaliada pelos cinco critérios abaixo:

1. **Estado inicial identificável** — existe um resultado, artefato, regra, modelo ou análise que serve de ponto de partida.
2. **Feedback ou nova informação** — existe avaliação, erro, lacuna, resposta, observação ou informação adicional que desencadeia a próxima transformação.
3. **Objeto modificado identificável** — é possível apontar o que efetivamente muda entre os ciclos.
4. **Continuidade entre estados** — o novo estado preserva ou incorpora parte relevante do estado anterior, em vez de ser apenas uma execução independente.
5. **Estabilização, suficiência ou convergência** — existe um critério explícito ou suficientemente identificável que indique quando o processo pode parar, estabilizar ou ser considerado adequado.

O quinto critério é deliberadamente mais exigente. **Repetir, reexecutar ou enriquecer um artefato não basta, por si só, para caracterizar convergência.**

## Quatro subfamílias

### A — Iteração algorítmica interna

**Exemplo de origem:** C25 / K-means.

O próprio mecanismo algorítmico possui ciclos de atualização e um critério de estabilidade. A atribuição aos clusters e a atualização dos centróides são repetidas até que o estado atinja a condição de estabilidade definida pelo algoritmo.

Pergunta estrutural:

> O próprio algoritmo possui ciclo explícito de atualização e critério de estabilização?

**Critérios:** 1–5 satisfeitos.

**Convergência:** algorítmica e explicitamente definida.

**Peso da evidência:** forte.

Esta é a manifestação mais completa do modelo quanto ao quinto critério.

### B — Iteração de análise/engenharia de regras

**Exemplo de origem:** C23 — calibração de classificação por regras explícitas.

A classificação inicial pode revelar ambiguidades, negações, modificadores e casos-limite. Referências e regras são então refinadas para uma nova execução.

```text
classificação inicial
    ↓
ambiguidade / caso-limite
    ↓
refinamento de regras e referências
    ↓
nova classificação
```

**Critérios:** 1–4 satisfeitos.

**Convergência:** não demonstrada com o mesmo rigor de A. O mecanismo prevê ajuste quando a calibração é insuficiente, mas não estabelece um critério operacional explícito de estabilização ou condição de parada.

**Peso da evidência:** parcial/fraca especificamente para convergência; forte como evidência da família mais ampla de refinamento de análise/regras.

### C — Iteração de construção de artefato

**Exemplo de origem:** enriquecimento iterativo da matriz de decisão.

Uma matriz inicial pode ser analisada, lacunas identificadas e novas informações ou decisões acrescentadas, produzindo uma versão revisada que incorpora a anterior.

```text
matriz inicial
    ↓
lacunas / novas necessidades
    ↓
enriquecimento
    ↓
matriz revisada
```

**Critérios:** 1–4 satisfeitos.

**Convergência:** não demonstrada. O material estabelece enriquecimento sucessivo, mas não define quando a matriz estará suficientemente completa, estável ou adequada para encerrar o processo.

**Peso da evidência:** parcial/fraca para convergência; forte como evidência de refinamento iterativo de artefatos.

### D — Iteração decisória/analítica

**Exemplo de origem:** SWOT — ajuste/refinamento.

O objeto é uma análise construída em interação com o decisor. A sequência observada é:

```text
SWOT inicial
    ↓
perguntas / feedback do decisor
    ↓
ajustes finos
    ↓
análise revisada
    ↓
nova avaliação
    ↓
suficiência para o decisor
```

**Critérios:** 1–5 satisfeitos em sentido de suficiência prática.

**Convergência:** humana/pragmática. O encerramento decorre da suficiência percebida pelo decisor, e não de uma condição matemática de estabilidade.

**Peso da evidência:** forte, com ressalva quanto à natureza da convergência.

Essa subfamília não deve ser confundida com a categoria A: ambas possuem critério de encerramento, mas os critérios pertencem a níveis diferentes.

## O que não conta automaticamente como refinamento

### Reprocessamento contextual

A instrução de “refazer o processo” após novas respostas do decisor demonstra reprocessamento condicionado por novo contexto, mas não prova, por si só:

- preservação incremental do estado anterior;
- transformação do mesmo objeto;
- critério de estabilização.

Portanto, reexecução não deve ser contada automaticamente como nova ocorrência de convergência.

### Implementação e ajuste pós-decisão

Teste-piloto, monitoramento de resultados, alerta e ação corretiva ocorrem predominantemente **após a decisão**, durante a implementação real.

Esse ciclo pertence à lógica operacional:

```text
decisão
  ↓
implementação / piloto
  ↓
monitoramento
  ↓
alerta / desvio
  ↓
ação / ajuste
  ↓
novo ciclo operacional
```

Ele não deve ser incorporado retroativamente à subfamília D apenas porque contém repetição e ajuste.

## Regra de interpretação das quatro subfamílias

As quatro subfamílias **não constituem quatro ocorrências equivalentes** de um único mecanismo.

A leitura correta do modelo é:

| Subfamília | Objeto refinado | Feedback | Critério de estabilidade/suficiência |
|---|---|---|---|
| A — algorítmica | estado interno do algoritmo | erro/estado do próprio processo | estabilidade algorítmica |
| B — análise/regras | regras, referências, calibração | ambiguidades/casos-limite | ainda não demonstrado explicitamente |
| C — artefato | matriz/documento/estrutura analítica | lacunas/novas necessidades | ainda não demonstrado explicitamente |
| D — decisória/analítica | análise em interação com decisor | perguntas e avaliação humana | suficiência prática do decisor |

O mecanismo transversal comum é **refinar um estado existente mediante feedback, preservando continuidade entre estados**. O modo de estabilização é dependente da subfamília.

## Relações com modelos existentes

### C25 — Segmentação por padrões

C25 fornece a evidência mais completa da subfamília A por meio do K-means e de sua iteração até estabilidade.

### C23 — Calibração de classificação

C23 exemplifica a subfamília B. O refinamento das regras é iterativo, mas a evidência disponível não estabelece convergência explícita.

### Matriz de decisão

O enriquecimento iterativo da matriz exemplifica a subfamília C. O artefato evolui preservando a versão anterior, mas não há critério formal de suficiência no material estudado.

### SWOT

O refinamento da SWOT exemplifica a subfamília D. A análise é revisada a partir do feedback do decisor até uma condição de suficiência prática.

### C16 e C3

O modelo não absorve C16 nem C3.

- **C16** prioriza alternativas por critérios explícitos.
- **C3** define/estrutura o modo de participação da IA no processo decisório.
- **Refinamento iterativo** trata da transformação progressiva de um estado, artefato, regra ou análise a partir de feedback.

Eles podem ser compostos, mas executam funções distintas.

## Limites

- Nem toda repetição é iteração de refinamento.
- Nem todo refinamento possui convergência demonstrável.
- Convergência algorítmica não deve ser confundida com suficiência humana.
- Enriquecimento de artefato não implica, por si só, condição de parada.
- Reprocessamento após nova informação não prova continuidade incremental.
- O modelo não determina quando uma decisão é correta; descreve como um objeto decisório ou analítico pode ser refinado.

## Proveniência

A família foi consolidada a partir das seguintes manifestações observadas durante o curso:

- **C25 / K-means** — iteração algorítmica com estabilidade explícita;
- **C23** — recalibração de regras e referências;
- **matriz de decisão** — enriquecimento iterativo do artefato;
- **SWOT** — ajustes finos mediante feedback e suficiência do decisor.

A classificação histórica foi preservada: B e C permanecem parciais para o critério de convergência, enquanto A e D apresentam critérios de estabilização/suficiência mais claros.

## Critério de reutilização

Este modelo é reutilizável quando houver um objeto existente que:

1. possa ser identificado em um estado inicial;
2. receba feedback ou nova informação;
3. possa ser modificado mantendo continuidade com o estado anterior;
4. produza um novo estado;
5. e, quando se pretender falar em convergência, possua critério de suficiência, estabilidade ou parada.

A implementação deve selecionar a subfamília adequada ao mecanismo observado, em vez de aplicar uma definição única de convergência a todos os contextos.
