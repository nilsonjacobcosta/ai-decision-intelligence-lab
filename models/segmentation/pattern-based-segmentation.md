# Candidato 25 — Segmentação por padrões de comportamento

## Status

**Candidato formal aprovado para criação.**

## Área

**Segmentation — trilha funcional.**

## Problema

Uma base de entidades pode conter grupos com características ou comportamentos semelhantes, mas esses grupos podem não estar explícitos na representação original. A análise precisa identificar e caracterizar segmentos para apoiar personalização, recomendações ou decisões posteriores.

## Distinção em relação à Classification

O C25 é separado do C23 porque os mecanismos têm objetos funcionais diferentes:

- **Classification:** atribuir cada observação a uma categoria previamente definida ou controlada por regras.
- **Segmentation:** agrupar entidades segundo características ou padrões de similaridade, podendo produzir grupos que emergem dos dados.

Em forma simplificada:

```text
Classification
observação → categoria conhecida

Segmentation
entidades + características
        ↓
similaridade / padrões
        ↓
grupos ou segmentos
```

A segmentação pode utilizar categorias explícitas, mas seu objetivo central é estruturar a população em grupos semelhantes, e não apenas atribuir uma classe individual.

## Padrão

```text
Base de entidades
      ↓
Seleção das variáveis relevantes
      ↓
Identificação de similaridades / padrões
      ↓
Formação dos segmentos
      ↓
Caracterização dos grupos
      ↓
Personalização / recomendação / decisão
```

## Escolha do método

O C25 também fornece uma nova ocorrência do meta-padrão **escolha de método conforme as características do problema**.

A Aula 5.1 apresenta mais de uma estratégia de segmentação:

- segmentação por faixa etária e gênero;
- segmentação por localidade;
- segmentação por produto e método de pagamento;
- clustering, como K-means ou agrupamento hierárquico, como opção avançada.

A escolha entre essas abordagens depende do objetivo da análise, das variáveis disponíveis e do tipo de estrutura que se pretende identificar.

Isso constitui a terceira ocorrência independente do meta-padrão, junto ao Candidato 13 e à seleção contextual de frameworks em Diagnosis/Action.

## Evidência de origem

Na Aula 5.1, o material propõe dois prompts: um para mapeamento descritivo dos padrões de compra e outro para segmentação da clientela. O segundo agrupa clientes por variáveis demográficas e comportamentais e apresenta, como opção avançada, técnicas de clustering. fileciteturn123file0L200-L229

O material também afirma que há muitas combinações possíveis de variáveis e que o objetivo da IA é fornecer clareza para apoiar a decisão, não tomar a decisão pelo usuário. fileciteturn123file0L284-L288

## Entradas

- conjunto de entidades/clientes;
- variáveis demográficas;
- variáveis comportamentais;
- variáveis de localização;
- produtos ou categorias relevantes;
- objetivo da segmentação.

## Processo

1. Definir o objetivo da segmentação.
2. Selecionar as variáveis relevantes.
3. Determinar se a segmentação será feita por dimensões explícitas ou por método de clustering.
4. Formar os segmentos.
5. Caracterizar cada grupo.
6. Verificar se os grupos possuem interpretação útil para o objetivo.
7. Utilizar os segmentos como insumo para personalização, recomendação ou decisão.

## Saída

Uma representação da população em segmentos caracterizados por padrões de comportamento ou características compartilhadas.

## Exemplos de aplicação

- segmentação de clientes por faixa etária e gênero;
- segmentação por região geográfica;
- identificação dos produtos mais comprados por segmento;
- identificação dos métodos de pagamento predominantes em cada segmento;
- agrupamento por clustering para descobrir grupos semelhantes.

## Relações com outros candidatos

### C23 — Classification

C23 controla a atribuição de categorias. C25 estrutura entidades em grupos de similaridade.

### C21 — Investigation

C21 seleciona um foco para aprofundamento. C25 cria grupos ou segmentos. Um segmento pode posteriormente tornar-se o foco de uma investigação.

### C16 — Recomendações

Os segmentos podem fornecer contexto para recomendações posteriores, mas a segmentação não produz, por si só, a recomendação.

## Limitações

- segmentos dependem das variáveis escolhidas;
- diferentes critérios podem produzir agrupamentos diferentes;
- clustering não garante que os grupos encontrados tenham significado de negócio;
- a interpretação dos segmentos precisa ser validada antes de orientar decisões;
- a existência de um segmento não determina automaticamente uma ação.

## Governança

A segmentação é um mecanismo de apoio analítico. A interpretação dos segmentos e as decisões decorrentes permanecem sob responsabilidade humana.

## Relação com o ORCHESTRATOR CORE

Nenhuma integração é presumida. O C25 permanece como componente experimental do laboratório até eventual validação e seleção futura.
