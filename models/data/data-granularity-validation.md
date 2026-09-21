# Validação da Granularidade dos Dados

## Objetivo

Garantir que a unidade de análise utilizada nos cálculos seja adequada e que múltiplos registros referentes ao mesmo evento ou período não distorçam métricas e análises.

## Problema que resolve

Bases transacionais podem conter várias linhas para a mesma data. Se cada linha for tratada como uma observação diária independente, médias, totais e outras métricas podem ser distorcidos.

## Regra

Quando houver múltiplos registros referentes ao mesmo dia:

1. Identificar a unidade correta de análise.
2. Agrupar os registros pela data relevante.
3. Somar as quantidades ou agregações apropriadas.
4. Calcular médias e totais sobre a unidade agregada, evitando duplicidade.

A regra deve ser adaptada à granularidade efetivamente necessária para cada análise. Não se deve assumir que a granularidade diária seja universal.

## Aplicação

Pode ser utilizada em:

- análise descritiva;
- indicadores de desempenho;
- séries temporais;
- análises de vendas;
- preparação de dados para modelos estatísticos;
- outros processos em que a unidade de observação possa gerar dupla contagem.

## Validação

Antes de calcular métricas, verificar:

- qual é a unidade de observação;
- se existem múltiplos registros para a mesma unidade;
- se esses registros representam eventos distintos ou partes do mesmo agregado;
- qual regra de agregação deve ser aplicada.

## Evidência considerada — integração de múltiplas fontes

O laboratório também registrou evidência de integração de informações provenientes de fontes distintas para formar um contexto mais completo, incluindo a combinação de solicitações/entradas de naturezas diferentes e a orientação de integrar dados de diversas fontes.

Essa evidência é **considerada, mas tratada como manifestação de C20, não como candidato próprio**.

A razão é funcional: a integração de fontes, quando utilizada para preparar, consolidar ou tornar adequada a representação dos dados/contexto antes da operação analítica, está contida no escopo de preparação e qualidade de dados do C20. Não há, no material estudado, mecanismo independente suficientemente delimitado que justifique uma trilha própria.

A conexão deve permanecer explícita para evitar que futuras ocorrências sejam interpretadas como um candidato separado apenas por apresentarem múltiplas fontes. Novas evidências devem ser avaliadas primeiro contra o mecanismo de C20; somente um mecanismo que demonstre função, estrutura e limites próprios poderá justificar reabertura da hipótese de um modelo independente.

## Relação com previsão

Esta regra pode ser utilizada como etapa de preparação de dados antes de qualquer modelo preditivo, mas **não é exclusiva de forecast**. Por isso, pertence ao domínio de qualidade e preparação de dados.

## Origem

Derivado da Aula 2.2 — Modelagem de previsões com IA, especialmente das orientações para agrupar registros do mesmo dia e evitar distorções nos cálculos de médias e totais.