# Candidato 24 — Estruturação operacional de ações por 5W2H

## Status

**Candidato formal aprovado para criação.**

## Área

**Action — trilha funcional.**

## Problema

Uma ação identificada ou priorizada ainda pode estar abstrata demais para execução. É necessário transformar a ação em um plano operacional que explicite o que será feito, por que, onde, quando, por quem, como e com qual custo.

## Padrão

~~~text
Ação / melhoria identificada
        ↓
Estruturação 5W2H
        ↓
What — o que
Why — por quê
Where — onde
When — quando
Who — quem
How — como
How Much — quanto custa
        ↓
Plano de ação executável
~~~

## Evidência de origem

Na Aula 4.3, o material utiliza o framework 5W2H para transformar os problemas e oportunidades identificados nos feedbacks da Batedeira em um plano de ação. O prompt define explicitamente as sete dimensões What, Why, Where, When, Who, How e How Much e solicita que o resultado seja prático e aplicável.

O material também demonstra que o plano pode combinar informações provenientes da solicitação do gestor e de uma tabela sobre o produto.

## Entradas

- ação ou oportunidade identificada;
- problema ou objetivo que a ação pretende tratar;
- contexto de implementação;
- responsável ou área envolvida, quando disponível;
- prazo ou cronograma, quando disponível;
- modo de execução;
- estimativa de custo, quando disponível.

## Processo

1. Identificar a ação que precisa ser operacionalizada.
2. Definir **What** — o que será feito.
3. Definir **Why** — por que a ação é necessária.
4. Definir **Where** — onde será implementada.
5. Definir **When** — quando será realizada.
6. Definir **Who** — quem será responsável.
7. Definir **How** — como será executada.
8. Definir **How Much** — quanto custará.
9. Organizar os elementos em um plano de ação coerente.

## Saída

Um plano de ação estruturado em 5W2H, com elementos suficientes para orientar implementação, atribuição de responsabilidades, cronograma e estimativa de recursos.

## Característica reutilizável

O mecanismo pode ser aplicado a diferentes tipos de ação em:

- produtos;
- processos;
- operações;
- atendimento;
- projetos;
- tecnologia;
- marketing;
- melhoria contínua.

Sua reutilização decorre da estrutura fixa do método, e não do contexto específico da Batedeira ou da Zoop.

## Distinção em relação ao Candidato 16

O Candidato 16 trata da **sugestão, avaliação de impactos e priorização de ações**.

O Candidato 24 atua depois que existe uma ação que deve ser operacionalizada.

~~~text
C16
sugerir / avaliar / priorizar
        ↓
C24
estruturar a execução em 5W2H
~~~

## Distinção em relação ao Candidato 17

O Candidato 17 trata da **decomposição hierárquica de uma ação priorizada** em ações secundárias e terciárias.

O Candidato 24 não tem como objetivo principal decompor a ação, mas especificar suas dimensões de execução.

Os mecanismos podem ser compostos:

~~~text
ação priorizada
      ↓
C17 — decomposição
      ↓
ações resultantes
      ↓
C24 — estruturação operacional 5W2H
~~~

## Distinção em relação ao Candidato 15A

O Candidato 15A é um mecanismo de Interaction para solicitar informação necessária quando o contexto é insuficiente.

O Candidato 24 é um mecanismo de Action para estruturar uma ação já identificada.

O C15A pode ser acionado durante a construção do C24 se faltarem informações necessárias para preencher o plano, mas os componentes têm funções diferentes.

## Relação com a integração de múltiplas fontes

A Aula 4.3 combina uma solicitação do gestor e uma tabela de informações do produto para construir o plano. Esta característica foi registrada separadamente como **observação de possível mecanismo de fusão de contexto**.

Ela não é tratada como parte constitutiva do C24 neste estágio, pois o 5W2H pode ser aplicado com uma única fonte de contexto suficientemente completa.

## Limitações

- O 5W2H organiza a execução, mas não determina se a ação escolhida é a mais adequada.
- Campos como custo, prazo ou responsável podem exigir informação adicional antes de serem preenchidos.
- Uma estrutura completa não garante viabilidade operacional.
- A qualidade do plano depende da qualidade e suficiência das informações de entrada.
- O framework pode precisar de complementação por métodos de priorização, decomposição ou avaliação de impacto.

## Relação com a arquitetura

C24 pertence à trilha **Action** e pode receber ações provenientes de Diagnosis, Decision ou outros processos.

Nenhuma integração com o ORCHESTRATOR CORE é presumida.