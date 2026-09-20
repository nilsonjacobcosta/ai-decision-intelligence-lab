# Candidato 20 — Preparação de contexto para monitoramento

## Status

**Candidato formalizado em `models/monitoring/`.**

## Objetivo

Transformar informações dispersas sobre um problema — causas identificadas, ações corretivas, resultados, dados operacionais, indicadores e contexto de negócio — em uma estrutura consolidada que possa alimentar uma etapa posterior de monitoramento.

O mecanismo não executa o monitoramento em si. Sua função é preparar e normalizar o contexto necessário para que o monitoramento tenha variáveis, referências e limites suficientemente estruturados.

## Posição no processo

O padrão observado na Aula 3.3 é:

```
informações dispersas
        ↓
consolidação do contexto
        ↓
indicadores relevantes
        ↓
valor atual + limite de alerta
        ↓
Monitoring
```

O Candidato 20 ocupa a etapa de **preparação/normalização de contexto antes da operação principal de Monitoring**.

## Entradas

- causas e problemas previamente identificados;
- ações corretivas implementadas;
- resultados dessas ações;
- dados de vendas e demanda;
- informações de marketing;
- indicadores operacionais e financeiros;
- atas ou registros de reuniões;
- expectativas e riscos identificados pelos gestores;
- referências ou limites relevantes para acompanhamento.

## Processo

1. Consolidar as informações disponíveis.
2. Identificar quais elementos são relevantes para acompanhamento preventivo.
3. Selecionar indicadores e variáveis críticas.
4. Organizar cada indicador com descrição, valor atual e limite/condição de alerta, quando disponível.
5. Identificar lacunas de informação que possam comprometer a preparação.
6. Produzir uma estrutura consolidada para alimentar a etapa de Monitoring.

## Saída

Uma estrutura de contexto monitorável, por exemplo:

| Indicador | Descrição | Valor atual | Limite de alerta |
|---|---|---|---|
| Capacidade de armazenagem | Ocupação do armazém | valor atual | condição crítica |
| Lead time | Tempo de reposição | valor atual | condição crítica |
| Conversão | Eficiência das campanhas | valor atual | condição crítica |

A estrutura concreta deve variar conforme o problema e os indicadores disponíveis.

## Evidência de origem

Na Aula 3.3 — Criação de alertas preventivos e ações proativas, o material apresenta uma primeira etapa de **Consolidação de Informações com a IA**. O prompt orienta a IA a consolidar informações anteriores, identificar o que é relevante para monitoramento preventivo, sugerir variáveis importantes e organizar os resultados em uma tabela com **Indicador, Descrição, Valor Atual e Limite de Alerta**.

A etapa seguinte utiliza essa estrutura, juntamente com a ata de reunião e a tabela de indicadores, para criar o sistema de alertas preventivos.

## Limites

- Não é o mecanismo de monitoramento contínuo; isso pertence ao Candidato 18.
- Não é o mecanismo de alerta preventivo; esse padrão permanece associado ao Candidato 19, ainda em observação.
- Não define automaticamente os limites sem considerar o contexto e as evidências disponíveis.
- Não deve substituir informações ausentes por suposições silenciosas.
- A solicitação de informações adicionais quando o contexto é insuficiente permanece uma questão separada, registrada no Candidato 15A em observação.

## Relações

```
Candidato 20 — preparar e normalizar contexto
                    ↓
Candidato 18 — monitorar continuamente
                    ↓
Candidato 19 — alerta quando o limiar é atingido
                    ↓
Action / Diagnosis → Action
```

O Candidato 20 também apresenta um padrão potencialmente recorrente no laboratório: **normalização de contexto antes da operação principal**. Essa recorrência é registrada no índice do laboratório como observação de design, sem criar um novo candidato ou princípio arquitetural neste momento.
