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

## Relação com o Candidato 17

O Candidato 16 deve ser executado **antes** do Candidato 17.

A decomposição hierárquica do Candidato 17 deve ocorrer apenas sobre as ações que tenham sido selecionadas/priorizadas nesta etapa, salvo evidência posterior de que o material ou outro contexto justifique uma ordem diferente.

## Evidência de origem

Na Aula 3.2, o material orienta a IA a propor ações corretivas, analisar seus impactos financeiro, operacional e de marketing e priorizá-las usando Matriz GUT ou Esforço e Impacto. O resultado esperado é uma tabela de ações priorizadas. 

Fonte: Aula 3.2 — Sugestão e priorização de ações corretivas.
