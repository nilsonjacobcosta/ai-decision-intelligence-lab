# Validação Contextual Antes do Forecast

## Objetivo

Garantir que a previsão considere informações futuras conhecidas que possam alterar o comportamento esperado das vendas.

## Problema que resolve

O histórico pode não capturar eventos futuros já conhecidos, como campanhas promocionais, alterações de preço ou outros fatores extraordinários. Uma previsão baseada apenas no histórico pode, portanto, ignorar contexto relevante.

## Processo

Antes de gerar o forecast, a IA deve perguntar ao usuário se haverá eventos ou mudanças que possam impactar o período previsto.

### Se houver evento confirmado

1. Identificar o evento.
2. Verificar se existem eventos semelhantes no histórico.
3. Estimar o impacto observado nesses eventos.
4. Incorporar esse efeito à previsão, explicitando a premissa utilizada.

### Se não houver evento confirmado

Adotar uma projeção conservadora baseada no histórico e na sazonalidade identificada, evitando aumentos sem justificativa.

## Entradas

- Período futuro.
- Eventos ou mudanças previstas.
- Histórico de eventos semelhantes, quando disponível.
- Variáveis relevantes já identificadas.

## Saída

Um contexto futuro validado que possa ser utilizado pelo modelo de previsão, com os eventos considerados e suas respectivas premissas.

## Relação com outros modelos

Este componente complementa os **Guardrails para Previsão**, que estabelecem limites para o comportamento do forecast.

O **Candidato 8 — Pipeline análise → previsão**, atualmente em observação, deverá futuramente orquestrar a sequência entre análise histórica, validação contextual e aplicação dos guardrails, referenciando este documento em vez de reproduzir suas regras.

## Origem

Derivado da Aula 2.2 — Modelagem de previsões com IA, especialmente da instrução para verificar eventos especiais antes de iniciar o cálculo das previsões.