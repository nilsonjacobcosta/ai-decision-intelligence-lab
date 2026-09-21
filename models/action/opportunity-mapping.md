# Candidato 26 — Mapeamento de oportunidades

## Status

**Aprovado para criação e registrado no laboratório.**

## Objetivo

Transformar uma **classificação analítica já estabelecida** em um mapa estruturado de oportunidades, recomendações ou estratégias diferenciadas para cada categoria.

O modelo não se limita a classificar. Seu mecanismo central é utilizar a categoria resultante para determinar **qual oportunidade ou estratégia corresponde àquela categoria**.

## Mecanismo central

```
Dados / contexto
      ↓
Framework analítico
      ↓
Classificação
      ↓
Categoria identificada
      ↓
Oportunidade / estratégia correspondente
      ↓
Recomendação ou candidato a ação
```

A relação categoria → estratégia deve ser explicitada e justificável no contexto do problema.

## Entradas

- dados ou contexto analisado;
- objetivo estratégico;
- framework de classificação adequado ao problema;
- dimensões necessárias para classificar as entidades;
- regras ou definições das categorias;
- estratégias ou oportunidades associadas às categorias.

## Processo

### 1. Escolher ou aplicar o framework analítico

Aplicar um modelo de classificação adequado ao objeto analisado.

No material estudado, aparecem dois exemplos:

- **BCG**, para avaliação estratégica de produtos;
- **RFM**, para mapeamento de oportunidades por região.

O modelo C26 não depende desses frameworks específicos. O elemento reutilizável é a estrutura **classificação → mapeamento de oportunidade/estratégia**.

### 2. Classificar

Determinar a categoria correspondente a cada produto, região ou outra unidade de análise.

No exemplo BCG, os produtos são classificados em:

- Stars;
- Cash Cows;
- Question Marks;
- Dogs.

No exemplo RFM, as regiões são classificadas em grupos de oportunidade, como:

- High Loyalty;
- Growth Potential;
- Underexplored.

### 3. Mapear a categoria para uma oportunidade ou estratégia

Para cada categoria, explicitar a estratégia ou oportunidade correspondente.

Exemplos do mecanismo:

- categoria associada a crescimento → estratégia de crescimento/expansão;
- categoria associada a otimização → estratégia de otimização;
- categoria associada a baixo desempenho → possibilidade de reposicionamento ou retirada;
- categoria associada a potencial ainda não explorado → estratégia de desenvolvimento.

A associação deve ser derivada do framework e do contexto, e não tratada como uma recomendação universal.

### 4. Produzir saída estruturada

A saída deve permitir visualizar, conforme aplicável:

- unidade analisada;
- categoria atribuída;
- características relevantes da categoria;
- oportunidade identificada;
- estratégia/recomendação correspondente;
- eventual candidato a ação.

## Saída

Uma estrutura que transforme a classificação analítica em **oportunidades ou recomendações diferenciadas por categoria**, podendo servir como entrada para etapas posteriores de priorização ou planejamento.

Exemplo conceitual:

| Unidade | Categoria | Oportunidade | Estratégia / recomendação |
|---|---|---|---|
| Produto A | Stars | Crescimento | Expandir presença / portfólio |
| Produto B | Cash Cows | Otimização | Maximizar retorno / eficiência |
| Produto C | Question Marks | Desenvolvimento | Avaliar expansão / investimento |
| Produto D | Dogs | Reposicionamento | Reavaliar oferta / posição |

As categorias e estratégias concretas dependem do framework e do contexto analisado.

## Relação com C16 — Orquestração e priorização de ações

C26 e C16 são **mecanismos distintos**.

### C26 — Mapeamento de oportunidades

Parte de uma classificação analítica e estabelece uma correspondência:

```
classificação
      ↓
categoria
      ↓
estratégia / oportunidade
```

Seu objetivo é **gerar ou estruturar candidatos de oportunidade/recomendação a partir das categorias**.

Não é necessário comparar alternativas entre si para que C26 produza valor.

### C16 — Orquestração e priorização de ações

Parte de um conjunto de ações ou candidatos e aplica avaliação de impactos e critérios de priorização:

```
ações candidatas
      ↓
avaliação de impactos + critérios
      ↓
priorização relativa
      ↓
ações priorizadas
```

Seu objetivo é **selecionar ou ordenar relativamente alternativas quando existe necessidade de priorização formal**.

### Regra de separação

C26 não deve ser tratado como um simples modo de entrada do C16.

A diferença funcional é:

- **C26:** categoria → oportunidade/estratégia;
- **C16:** conjunto de alternativas → avaliação → priorização.

O fato de uma saída do C26 poder posteriormente ser priorizada pelo C16 não elimina essa distinção.

## Relação C26 → C16 → C24

Quando houver necessidade de transformar uma classificação em uma ação operacional e houver múltiplas alternativas que exijam priorização, um fluxo possível é:

```
Classificação / fonte de oportunidade
              ↓
C26 — mapeamento categoria → oportunidade / estratégia
              ↓
Candidatos a ação / recomendações
              ↓
C16 — avaliação e priorização
              ↓
Ações priorizadas
              ↓
C24 — planejamento operacional 5W2H
              ↓
Execução / acompanhamento
```

**Esse fluxo é possível, não obrigatório.**

### Autonomia do C26

C26 **não depende do C16 para ter valor autônomo**.

Uma oportunidade mapeada pode ser suficientemente clara e acionável para seguir diretamente para execução, sem passar por uma etapa formal de priorização.

Exemplo:

```
Classificação
      ↓
C26 — oportunidade claramente identificada
      ↓
Execução
```

O C16 entra quando houver um conjunto de alternativas, necessidade de comparação relativa ou outro motivo contextual que justifique uma priorização explícita.

Da mesma forma, o C24 não é uma etapa obrigatória de todo C26. Ele é utilizado quando a recomendação selecionada precisa ser convertida em um plano operacional estruturado.

Portanto:

- **C26 pode operar isoladamente**;
- **C26 → C16 é um encadeamento possível quando a priorização for necessária**;
- **C16 pode receber candidatos de outras fontes, sem C26**;
- **C24 pode receber uma ação selecionada de C16 ou de outra origem, quando houver necessidade de planejamento 5W2H**.

## Relação com outros modelos

### C25 — Segmentação baseada em padrões

C25 pode fornecer grupos ou segmentos que posteriormente sejam analisados por um framework de oportunidades.

A relação não é obrigatória:

```
C25 — segmentação
      ↓
grupo / segmento
      ↓
C26 — classificação / mapeamento de oportunidade
```

C25 responde principalmente **como agrupar por padrões**; C26 responde **como transformar uma classificação em oportunidade/estratégia diferenciada**.

### C16 — Priorização

C26 pode gerar candidatos que sejam posteriormente avaliados e priorizados pelo C16, mas os dois mecanismos permanecem independentes.

### C24 — Plano operacional 5W2H

C24 pode transformar uma ação derivada de C26 — diretamente ou após C16 — em plano operacional.

## Critério de reutilização

Reutilizar C26 quando o problema apresentar:

1. uma classificação ou categorização analítica relevante;
2. categorias com significados estratégicos distintos;
3. possibilidade de associar cada categoria a oportunidades, estratégias ou recomendações específicas;
4. necessidade de transformar o resultado analítico em direcionamento de ação.

Não utilizar C26 apenas porque existe uma classificação. Se a classificação tiver apenas finalidade descritiva ou se o problema exigir comparação relativa entre ações, outro modelo pode ser mais adequado.

## Evidência de origem

Na Aula 5.2 — **Mapeamento de oportunidades**, o material apresenta o uso de BCG para classificar produtos e associar os quadrantes a estratégias de crescimento, otimização, expansão, reposicionamento ou retirada. Também apresenta RFM para classificar regiões segundo Recência, Frequência e Monetização e, a partir das categorias resultantes, sugerir estratégias diferenciadas para cada região.

A evidência sustenta o mecanismo:

```
framework analítico
      ↓
classificação
      ↓
identificação de oportunidade
      ↓
estratégia / recomendação diferenciada
```

Fonte: Aula 5.2 — Mapeamento de oportunidades.
