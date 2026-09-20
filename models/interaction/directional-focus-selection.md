# Candidato 22 — Escolha direcional do foco pelo usuário

## Status

**Candidato formal aprovado para criação.**

## Área

**Interaction — área transversal.**

## Problema

Em investigações com múltiplas dimensões possíveis, a IA pode identificar diversos caminhos de aprofundamento, mas a escolha sobre qual dimensão priorizar pode depender da intenção do usuário.

Nesse caso, a IA solicita uma decisão direcional ao usuário antes de aprofundar a análise.

## Padrão

```text
Visão geral / opções de foco
   ↓
Apresentação das alternativas relevantes
   ↓
Escolha direcional pelo usuário
   ↓
Aprofundamento no foco escolhido
   ↓
Resultado
```

## Evidência de origem

Na Aula 4.1, após a análise macro, o material apresenta uma etapa em que o usuário escolhe uma variável específica — como produto, plataforma ou número de seguidores — para orientar a análise detalhada.

## Entradas

- resultado da análise inicial;
- dimensões ou variáveis disponíveis;
- opções de foco relevantes;
- intenção ou preferência do usuário.

## Processo

1. Produzir ou apresentar a visão geral.
2. Identificar dimensões que podem ser aprofundadas.
3. Apresentar opções de foco ao usuário.
4. Solicitar a escolha direcional.
5. Executar a análise aprofundada na dimensão escolhida.
6. Produzir os insights correspondentes.

## Saída

Uma análise focalizada cuja direção foi explicitamente escolhida pelo usuário.

## Característica reutilizável

O padrão atravessa diferentes trilhas porque a escolha de foco pode ser necessária em:

- Investigation;
- Diagnosis;
- Prediction;
- Decision;
- Classification;
- Monitoring.

Ele representa uma forma de **human-in-the-loop orientada à direção da análise**.

## Distinção em relação ao Candidato 21

O Candidato 21 descreve a **estrutura da investigação em dois níveis**: visão macro seguida de aprofundamento.

O Candidato 22 descreve **quem escolhe a direção do aprofundamento** e como essa escolha entra no fluxo.

```text
C21 → estrutura da investigação
C22 → interação para escolher o foco
```

Os componentes podem ser usados em conjunto, sem duplicação.

## Distinção em relação ao Candidato 15A

O Candidato 15A solicita informação necessária que está faltando.

O Candidato 22 solicita uma escolha entre direções possíveis, mesmo quando o contexto já é suficiente para prosseguir.

## Limitações

- A qualidade das opções apresentadas influencia a escolha.
- O usuário pode escolher um foco pouco relevante para o objetivo original.
- O mecanismo pressupõe que existam alternativas de investigação compreensíveis.
- A generalização para outros contextos ainda deve ser validada além do exemplo de feedbacks.

## Relação com a arquitetura

Interaction é uma área transversal: o componente pode ser chamado por diferentes trilhas funcionais e devolver ao processo uma direção explicitamente escolhida pelo usuário.

Nenhuma integração com o ORCHESTRATOR CORE é presumida.
