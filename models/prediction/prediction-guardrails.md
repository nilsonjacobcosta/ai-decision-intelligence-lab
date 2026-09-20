# Guardrails para Previsão

## Objetivo

Estabelecer restrições explícitas para que uma previsão produzida com IA permaneça ancorada em evidências históricas e não extrapole o comportamento observado sem justificativa.

## Problema que resolve

Modelos de previsão podem incorporar ruído recente, picos anômalos ou pressupostos não sustentados pelos dados. Este modelo introduz regras de contenção antes da geração do forecast.

## Guardrails

1. **Sazonalidade histórica**
   - Compare o período previsto com períodos equivalentes de anos anteriores.
   - Considere padrões sazonais identificados nos dados.

2. **Variações de preço**
   - Considere alterações históricas de preço e seu impacto nas vendas quando esses registros estiverem disponíveis.

3. **Suavização de flutuações recentes**
   - Não trate picos anômalos como tendência automaticamente.
   - Utilize suavização ou outra abordagem estatística adequada quando necessário.

4. **Limite de crescimento**
   - Quando o histórico indicar queda ou estabilidade, não projetar crescimento significativo sem justificativa clara.
   - As previsões devem permanecer compatíveis com as variações percentuais históricas, salvo evidências adicionais.

5. **Explicabilidade**
   - Informar qual modelo ou abordagem estatística foi utilizada.
   - Explicar de forma simples como o modelo chegou à previsão.

## Entradas

- Dados históricos de vendas.
- Variáveis relevantes já identificadas.
- Período futuro a prever.
- Eventos ou alterações futuras confirmadas.

## Saída

Uma previsão acompanhada das premissas, ajustes aplicados e justificativas para eventuais desvios em relação ao histórico.

## Relação com o processo de previsão

Este modelo deve funcionar como uma camada de controle do forecast. Ele pode ser acionado depois da análise histórica e antes ou durante a geração da previsão.

O **Candidato 8 — Pipeline análise → previsão**, atualmente em observação, deverá futuramente orquestrar este componente em conjunto com a validação contextual do Candidato 10, sem duplicar seu conteúdo.

## Origem

Derivado da Aula 2.2 — Modelagem de previsões com IA, especialmente das regras de ajuste, suavização e limitação de crescimento apresentadas no segundo prompt de comando.