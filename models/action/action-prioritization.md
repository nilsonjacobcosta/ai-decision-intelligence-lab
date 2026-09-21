# Candidato 16 — Orquestração e priorização de ações

## Status

**Aprovado para criação e registrado no laboratório.**

## Objetivo

Transformar um diagnóstico previamente realizado em um conjunto estruturado de ações corretivas, avaliar os impactos esperados e aplicar um mecanismo explícito de priorização.

## Posição na sequência

O modelo pressupõe que as causas relevantes já tenham sido identificadas.

```
Diagnóstico
    ↓
Causas identificadas
    ↓
Sugestão de ações
    ↓
Avaliação de impactos
    ↓
Priorização
    ↓
Ações priorizadas
```

## Entradas

- causas identificadas no diagnóstico;
- contexto do problema;
- objetivos estratégicos;
- impactos relevantes para o contexto;
- framework de priorização escolhido.

## Processo

### 1. Sugerir ações

Gerar ações que ataquem diretamente as causas identificadas.

### 2. Avaliar impactos

Para cada ação, explicitar os impactos relevantes. No caso estudado, o curso utiliza:

- impacto financeiro;
- impacto operacional;
- impacto em marketing.

Esses critérios podem ser substituídos ou ampliados conforme o contexto.

### 3. Priorizar

Aplicar um framework explicitamente definido, como:

- Matriz GUT;
- Esforço × Impacto.

O mecanismo não deve presumir um critério de priorização quando o contexto exigir outro.

### 4. Produzir saída estruturada

Entregar uma tabela contendo, conforme aplicável:

- ação proposta;
- impactos;
- critérios de priorização;
- prioridade resultante.

## Saída

Uma lista estruturada de ações priorizadas, suficientemente clara para servir de base à etapa seguinte de execução ou detalhamento.



## Delimitação em relação ao Candidato 26 — Mapeamento de oportunidades

O Candidato 26 **não é uma variação interna do C16**. Os mecanismos são distintos e devem permanecer separados.

### Diferença funcional

**C16 — Orquestração e priorização de ações**
- recebe ações/candidatos de ação;
- avalia impactos;
- aplica um **critério/framework de priorização**;
- produz uma ordem ou seleção relativa entre alternativas.

Seu mecanismo central é, portanto, **priorização dinâmica**: o resultado depende do conjunto de alternativas, dos critérios e do contexto de decisão.

**C26 — Mapeamento de oportunidades**
- parte de uma **classificação analítica já estabelecida**;
- associa cada categoria a uma estratégia/recomendação correspondente;
- produz oportunidades ou recomendações diferenciadas por categoria.

Seu mecanismo central é **mapeamento categorial fixo categoria → estratégia/recomendação**. Ele não exige comparação relativa entre alternativas nem produz, por si só, uma ordem de prioridade.

### Regra de separação

Não considerar C26 como simples modo de entrada do C16, porque isso apagaria uma diferença funcional relevante:

```
C26
classificação analítica
      ↓
categoria
      ↓
estratégia / oportunidade correspondente

C16
conjunto de ações candidatas
      ↓
avaliação de impactos + critérios
      ↓
priorização dinâmica
```

O fato de uma saída do C26 poder posteriormente entrar no C16 não transforma os dois mecanismos em um único modelo.

### Posição relativa na trilha Action

Quando os três mecanismos forem combinados em um fluxo de oportunidade → ação, a relação preferencial é **sequencial, mas não obrigatória**:

```
Fonte de oportunidade / classificação
             ↓
C26 — mapeamento categoria → estratégia
             ↓
candidatos a ação / recomendações
             ↓
C16 — avaliação e priorização
             ↓
ações priorizadas
             ↓
C24 — planejamento operacional 5W2H
             ↓
execução / acompanhamento
```

Entretanto, C16 também pode receber ações provenientes diretamente de um diagnóstico ou de outra fonte, sem passar pelo C26. Da mesma forma, uma classificação pode gerar uma recomendação que não precise de priorização formal antes de ser executada.

Assim, **C26 e C16 não são paralelos como mecanismos equivalentes**, mas também não formam uma cadeia obrigatória. A relação arquitetural é:

- **C26 = geração estruturada de candidatos a partir de categorias/oportunidades**;
- **C16 = seleção/priorização relativa desses candidatos quando houver necessidade de priorização**;
- **C24 = transformação da ação selecionada em plano operacional**.

Essa distinção deve ser preservada quando o C26 for formalizado, evitando que o novo modelo seja absorvido pelo C16 apenas por ambos produzirem recomendações.

## Relação com o Candidato 17

O Candidato 16 deve ser executado **antes** do Candidato 17.

A decomposição hierárquica do Candidato 17 deve ocorrer apenas sobre as ações que tenham sido selecionadas/priorizadas nesta etapa, salvo evidência posterior de que o material ou outro contexto justifique uma ordem diferente.

## Evidência de origem

Na Aula 3.2, o material orienta a IA a propor ações corretivas, analisar seus impactos financeiro, operacional e de marketing e priorizá-las usando Matriz GUT ou Esforço e Impacto. O resultado esperado é uma tabela de ações priorizadas. 

Fonte: Aula 3.2 — Sugestão e priorização de ações corretivas.
