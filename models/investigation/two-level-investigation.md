# Candidato 21 — Investigação em dois níveis

## Status

**Candidato formal aprovado para criação.**

## Problema

Análises de dados podem começar com uma visão ampla do conjunto disponível e, somente depois, aprofundar a investigação sobre uma dimensão específica que seja relevante para o problema.

O padrão evita iniciar imediatamente uma análise estreita sem antes compreender a estrutura geral dos dados.

## Padrão

```text
Dados
  ↓
Análise descritiva geral
  ↓
Identificação do que merece atenção
  ↓
Seleção do foco / variável
  ↓
Análise aprofundada
  ↓
Insights
```

## Evidência de origem

Na Aula 4.1, a primeira etapa solicita uma análise macro dos feedbacks: quantidade de registros, distribuição temporal, médias por plataforma, produto, categoria, ano e média global, acompanhadas de visualizações. 

Em seguida, a aula apresenta uma segunda etapa em que o usuário escolhe uma variável específica — por exemplo, produto, plataforma ou número de seguidores — para uma análise detalhada, incluindo média, mediana, desvio padrão, distribuição, padrões/anomalias e visualização.

## Entradas

- conjunto de dados;
- contexto do problema;
- dimensões/variáveis disponíveis;
- objetivo da investigação.

## Processo

1. Construir uma visão descritiva geral dos dados.
2. Observar distribuições, diferenças e possíveis pontos de interesse.
3. Identificar ou selecionar uma dimensão relevante.
4. Aprofundar a investigação nessa dimensão.
5. Produzir estatísticas, visualizações e insights adequados ao foco escolhido.

## Saída

Uma investigação progressiva que parte do panorama geral e chega a uma análise focalizada, mantendo rastreabilidade entre o contexto inicial e o aprofundamento.

## Característica reutilizável

O padrão não depende de feedbacks de clientes. Pode ser aplicado, com adaptações, a:

- vendas;
- operações;
- indicadores de desempenho;
- riscos;
- dados de clientes;
- mercados;
- processos;
- outros conjuntos de dados estruturados.

## Distinção em relação ao Candidato 22

O Candidato 21 descreve a **estrutura da investigação**: visão macro seguida de aprofundamento.

O Candidato 22, ainda em observação, descreve um mecanismo de **human-in-the-loop para escolha direcional do foco**: a IA pergunta ao usuário qual variável ele deseja investigar.

Eles podem ser usados em conjunto, mas não são o mesmo componente.

## Limitações

O material de origem demonstra o padrão em um contexto de análise de feedbacks. Sua generalização para outras classes de investigação ainda deverá ser validada.

## Relação com os meta-padrões

Este candidato não deve ser contado, por enquanto, como uma nova ocorrência dos meta-padrões já registrados no laboratório. Ele representa uma arquitetura de investigação em camadas, cuja recorrência em outras trilhas ainda precisa ser observada.
