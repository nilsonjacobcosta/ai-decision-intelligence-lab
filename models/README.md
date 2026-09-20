# Models

Modelos reutilizáveis derivados de conceitos estudados e posteriormente validados.

Um modelo deve explicitar, sempre que possível:
- problema que resolve;
- entradas;
- processo;
- saída;
- premissas;
- limitações;
- contexto de uso;
- exemplos de aplicação.

## Índice das trilhas

À medida que o laboratório cresce, os modelos estão sendo organizados por **trilhas funcionais**.

### 1. Decision — Tomada de decisão

Foco: estruturar decisões e formas de apoio da IA.

- `models/decision/` — modelos conceituais relacionados à decisão.
- `prompts/decision-matrix-enrichment.md` — prompt reutilizável para enriquecimento de matriz de decisão.
- `templates/decision-matrix.md` — estrutura reutilizável da matriz.

### 2. Prediction — Previsão

Foco: organizar dados, preparar contexto, construir e ajustar previsões e validar resultados.

- `models/prediction/` — componentes da pipeline de previsão.
- A trilha está sendo construída como uma sequência modular, evitando duplicação entre etapas.
- Candidatos já definidos incluem componentes de preparação/qualidade de dados, análise, validação de contexto, previsão e validação da saída.

### 3. Diagnosis — Diagnóstico

Foco: compreender problemas e suas causas antes de definir ações corretivas.

- `models/diagnosis/` — modelos de diagnóstico e análise estruturada de causas.
- `structured-root-cause-diagnosis.md` — Candidato 14: diagnóstico estruturado de causas usando MECE, Ishikawa e análise quantitativa/qualitativa.

## Separação das trilhas

A distinção entre as trilhas é deliberada:

```text
Decision
   └── Como estruturar e apoiar decisões

Prediction
   └── Como analisar dados e produzir/validar previsões

Diagnosis
   └── Como compreender causas antes de definir ações
```

Uma mesma aplicação pode atravessar mais de uma trilha. Isso não significa que os modelos devam ser fundidos; a integração deve ocorrer somente depois de validação e seleção.

## Observações em evolução

### Candidato 15 — entrada estruturada de evidências

Permanece **em observação** e foi dividido em dois mecanismos diferentes, que não devem ser tratados como formalizados até passarem pelo protocolo de candidatos:

**A. Solicitar informação adicional quando a evidência é insuficiente — hipótese de mecanismo reutilizável**

O conteúdo da Aula 3.1 sugere um mecanismo recorrente: antes de executar a análise, o sistema deve identificar se as informações disponíveis são suficientes e, quando houver lacunas relevantes, solicitar os dados necessários em vez de preencher as lacunas com suposições.

Esse mecanismo **não está formalizado como candidato próprio neste momento**. Ele deve passar pelo mesmo protocolo dos demais candidatos: identificação explícita, definição de pasta, justificativa de reutilização e aprovação antes de qualquer criação.

**B. Taxonomia específica de categorias de evidência — ainda em observação**

A classificação em atas, indicadores, processos internos, fatores externos, percepções, feedbacks etc. ainda não está formalizada como modelo próprio. É necessário observar se a estrutura reaparece em outros contextos antes de transformá-la em componente reutilizável.

## Regra de maturação

Um padrão observado não deve ser formalizado apenas porque aparece uma vez.

O laboratório prioriza:
1. recorrência;
2. independência de contexto;
3. clareza do mecanismo;
4. possibilidade de validação;
5. utilidade para outras aplicações.

O fato de um mecanismo parecer promissor ou semelhante a um candidato existente não substitui esse processo.

