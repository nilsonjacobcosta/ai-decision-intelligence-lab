# Seleção da Técnica de Previsão Conforme o Contexto

## Objetivo

Orientar a escolha da abordagem de modelagem antes da geração do forecast, considerando a natureza do problema, a estrutura dos dados disponíveis e o objetivo da previsão.

## Princípio

A técnica de previsão deve ser escolhida em função do contexto. Não se deve assumir que uma técnica mais sofisticada é automaticamente mais adequada.

A aula apresenta, como possibilidades:

- aprendizado de máquina supervisionado;
- redes neurais;
- séries temporais;
- modelos de regressão;
- sistemas de recomendação;
- análise de cenários com IA;
- análise preditiva e Big Data.

O modelo escolhido deve considerar, entre outros aspectos, a **qualidade dos dados** e a adequação da técnica ao contexto.

## Processo

1. Definir o objetivo da previsão.
2. Identificar a natureza e a estrutura temporal dos dados.
3. Verificar quais variáveis explicativas estão disponíveis e sua qualidade.
4. Identificar características relevantes do problema, como sazonalidade, relações entre variáveis e volume de dados.
5. Selecionar uma ou mais abordagens compatíveis com essas características.
6. Explicar a justificativa da escolha antes de executar o forecast.
7. Prosseguir para a validação do contexto futuro e, então, para a geração da previsão.

## Relação com a pipeline

Este modelo constitui um elo intermediário da **pipeline do Candidato 8 — Pipeline análise → previsão**.

A posição sugerida é:

**Candidato 11 — análise/qualidade dos dados**  
→ **Candidato 13 — seleção da técnica de previsão**  
→ **Candidato 10 — validação contextual antes do forecast**  
→ **Candidato 9 — aplicação dos guardrails**  
→ **Previsão**  
→ **Candidato 12 — validação crítica da saída**

Quando o Candidato 8 for consolidado, deverá referenciar essa sequência em vez de duplicar o conteúdo dos componentes.

### Relação com os demais candidatos

- **Candidato 11:** prepara e verifica a base de dados que sustenta a modelagem.
- **Candidato 13:** usa as características dos dados e do problema para orientar a escolha da abordagem.
- **Candidato 10:** verifica eventos e variáveis futuras conhecidas antes da execução do forecast.
- **Candidato 9:** estabelece limites e salvaguardas para o comportamento da previsão.
- **Candidato 12:** questiona a saída depois que o forecast é produzido.

## Limite de escopo

Este documento registra o **critério de seleção da técnica**, não um catálogo prescritivo de qual modelo deve ser usado em cada situação. A escolha concreta depende dos dados, do objetivo e das características do problema.

A análise de cenários, *what-if* e simulações específicas permanece em observação e não faz parte deste modelo.

A expansão sistemática das variáveis relevantes também permanece em observação até que o padrão apareça novamente conforme o critério definido no laboratório.

## Origem

Derivado do conteúdo “Para saber mais: técnicas de previsão de vendas”, da Aula 2 — Previsões futuras, especialmente da conclusão que destaca a importância da qualidade dos dados e da escolha do modelo apropriado para cada contexto.
