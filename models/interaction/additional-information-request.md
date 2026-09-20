# Candidato 15A — Solicitação de informação adicional

## Status

**Candidato formal aprovado para criação.**

## Área

**Interaction — área transversal.**

## Problema

Uma análise ou decisão pode depender de informações que não foram fornecidas ou que são insuficientes para produzir uma resposta confiável. Nessa situação, a IA não deve preencher as lacunas por suposição: deve identificar a insuficiência e solicitar os dados necessários ao usuário.

## Padrão

```text
Solicitação
   ↓
Verificação de suficiência do contexto
   ↓
Contexto insuficiente
   ↓
Solicitação de informação adicional
   ↓
Complementação pelo usuário
   ↓
Prosseguimento da operação
```

## Evidência de origem

O material do curso apresenta situações em que informações necessárias precisam ser fornecidas antes da execução da análise e demonstra a solicitação de dados complementares quando o contexto disponível não é suficiente.

## Entradas

- solicitação original;
- contexto disponível;
- requisitos mínimos da operação;
- informação necessária ainda ausente.

## Processo

1. Identificar quais informações a operação exige.
2. Comparar esses requisitos com o contexto disponível.
3. Detectar lacunas relevantes.
4. Solicitar ao usuário somente as informações necessárias para prosseguir.
5. Receber a complementação.
6. Retomar a operação com o contexto atualizado.

## Saída

Contexto suficientemente especificado para que a operação dependente possa prosseguir sem preencher lacunas críticas por inferência não autorizada.

## Característica reutilizável

O padrão atravessa diferentes trilhas porque a necessidade de informação adicional pode surgir em:

- Prediction;
- Diagnosis;
- Action;
- Monitoring;
- Classification;
- Decision;
- Investigation.

Ele representa uma forma de **human-in-the-loop orientada à completude do contexto**.

## Distinção em relação ao Candidato 22

O Candidato 15A solicita **informação necessária ou faltante**.

O Candidato 22 solicita uma **escolha direcional** sobre qual foco o usuário deseja investigar.

```text
C15A → "Que informação necessária está faltando?"
C22  → "Qual direção/foco você quer escolher?"
```

São subfamílias distintas de interação humana e podem ser combinadas.

## Limitações

- É necessário distinguir lacuna realmente necessária de informação apenas desejável.
- Solicitações excessivas podem aumentar o atrito da interação.
- A suficiência do contexto depende da operação e do domínio.
- O mecanismo não garante, por si só, que a informação fornecida pelo usuário seja correta.

## Relação com a arquitetura

Interaction é uma área transversal: o componente pode ser acionado por diferentes trilhas funcionais e devolve contexto ao processo que o solicitou.

Nenhuma integração com o ORCHESTRATOR CORE é presumida.
