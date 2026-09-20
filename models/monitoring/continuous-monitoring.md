# Candidato 18 — Monitoramento contínuo e detecção de desvios

## Status

Candidato formalizado em `models/monitoring/`.

## Objetivo

Estruturar um mecanismo de monitoramento contínuo de indicadores e estados operacionais para detectar desvios relevantes em relação ao comportamento esperado e gerar um sinal para reavaliação.

O mecanismo não se limita a registrar dados. Seu papel é acompanhar o estado atual, identificar mudanças ou desvios e retroalimentar o processo decisório.

## Padrão

```
estado observado
    ↓
monitoramento contínuo
    ↓
detecção de desvio
    ↓
reavaliação
    ↙        ↘
Diagnosis   Decision
```

A saída do monitoramento não é necessariamente uma ação. Quando um desvio é identificado, o processo pode precisar:

- retornar a **Diagnosis**, quando é necessário compreender a causa do desvio;
- retornar a **Decision**, quando a causa/contexto já é suficientemente conhecido e é necessário decidir como responder.

## Origem no material

Na Aula 3.1, o conteúdo apresenta **monitoramento em tempo real** como aplicação de IA no gerenciamento de estoque. A combinação de sensores IoT e IA permite acompanhar os estoques continuamente e apoiar decisões de reabastecimento diante de mudanças no mercado.

O candidato abstrai esse padrão para além do caso de estoque, preservando o mecanismo central: observar continuamente o estado, detectar alterações relevantes e retroalimentar o processo.

## Entradas

- indicadores ou métricas relevantes;
- estado atual observado;
- histórico ou referência esperada, quando disponível;
- eventos ou sinais externos relevantes;
- critérios de desvio.

## Processo

1. acompanhar os sinais relevantes de forma contínua ou periódica;
2. comparar o estado observado com referências, limites ou padrões esperados;
3. identificar desvios relevantes;
4. distinguir alteração normal de sinal que exige reavaliação;
5. encaminhar o desvio para **Diagnosis** ou **Decision**, conforme a natureza da necessidade identificada.

## Saída

Um sinal estruturado de desvio contendo, quando possível:

- indicador afetado;
- estado observado;
- referência ou condição esperada;
- magnitude/natureza do desvio;
- contexto temporal;
- necessidade de reavaliação;
- trilha sugerida para o próximo passo: Diagnosis ou Decision.

## Limites

- Monitoramento não equivale a diagnóstico de causa.
- Monitoramento não equivale a decisão ou ação.
- O candidato não formaliza ainda mecanismos específicos de **alerta preventivo**.
- A automação da reposição permanece em observação e não faz parte deste modelo.
- A definição de limites, thresholds e frequência de monitoramento depende do contexto de aplicação.

## Relação com as demais trilhas

O Candidato 18 introduz uma lógica cíclica no laboratório:

```
Decision → Prediction → Monitoring
                 ↓
          desvio detectado
             ↙       ↘
       Diagnosis    Decision
             ↓
           Action
             ↓
          Monitoring
```

Essa representação é conceitual, não uma sequência obrigatória para todos os casos. Dependendo do problema, o fluxo pode entrar ou retornar a diferentes trilhas.

## Observação

O material da Aula 3.1 também apresenta monitoramento como suporte à tomada de decisão sobre reabastecimento. Neste candidato, o conceito foi deliberadamente mantido no nível de **Monitoring**, sem incorporar automaticamente mecanismos de Control, Alertas ou Action.
