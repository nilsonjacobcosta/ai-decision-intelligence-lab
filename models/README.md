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

### 4. Action — Ação

Foco: transformar causas diagnosticadas em ações estruturadas, avaliar seus impactos e priorizar o que deve avançar.

- `models/action/` — modelos de sugestão, priorização e decomposição de ações.
- `action-prioritization.md` — Candidato 16: sugestão, avaliação de impactos e priorização de ações.
- `action-decomposition.md` — Candidato 17: decomposição hierárquica de ações já priorizadas.

**Ordem estabelecida entre os candidatos 16 e 17:**

```
Diagnosis
    ↓
Candidato 16 — sugerir, avaliar e priorizar ações
    ↓
Candidato 17 — decompor somente as ações priorizadas
```

Essa ordem reflete o material da Aula 3.2: primeiro ocorre a priorização das ações; posteriormente, uma ação selecionada pode ser expandida em ações secundárias e terciárias. A ordem poderá ser revista se evidência posterior do próprio material justificar outra sequência.

### 5. Monitoring — Monitoramento

Foco: acompanhar continuamente o estado observado, detectar desvios relevantes e retroalimentar o processo.

- `models/monitoring/` — modelos de monitoramento, preparação de contexto e detecção de desvios.
- `continuous-monitoring.md` — Candidato 18: monitoramento contínuo e detecção de desvios.
- `context-preparation.md` — Candidato 20: preparação e normalização de contexto antes do monitoramento.

**Status:** Monitoring está confirmada como trilha própria. **Control permanece separado e poderá ser formalizado como trilha própria posteriormente.**

A arquitetura não é uma cadeia linear que termina em Monitoring. Monitoring funciona como mecanismo de retroalimentação:

```
Decision → Prediction → Monitoring
                 ↓
          desvio / alerta
                 ↓
       ┌─────────┴─────────┐
       ↓                   ↓
causa conhecida      causa desconhecida
       ↓                   ↓
    Action             Diagnosis
                           ↓
                         Action
                           ↓
                      Monitoring
```

A regra de handoff é explícita: **causa conhecida → Action; causa desconhecida → Diagnosis → Action**. O retorno a Decision não é o fluxo padrão desse handoff diagnóstico; Decision pode participar em outros pontos do ciclo quando o problema exigir uma nova decisão estratégica.

**Mantidos em observação:**
- Candidato 19 — alertas preventivos;
- reposição automatizada de estoques;
- Control como possível trilha própria futura.


## Separação das trilhas

A distinção entre as trilhas é deliberada:

```
Decision
   └── Como estruturar e apoiar decisões

Prediction
   └── Como analisar dados e produzir/validar previsões

Diagnosis
   └── Como compreender causas antes de definir ações

Action
   └── Como transformar causas em ações e priorizá-las
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

### Feedback da IA sobre a própria priorização

Permanece como **observação**, mas não é tratado neste índice como um mecanismo novo. O comportamento observado — contestar uma saída da IA e solicitar sua revisão/refazimento — parece ser uma instância do padrão geral de **validação crítica da saída**, já observado nos Candidatos 10 e 12.

Isso não formaliza nem amplia os Candidatos 10 e 12; apenas registra a recorrência do mesmo padrão no contexto da priorização.

## Observação de design — normalização de contexto

Os Candidatos **6, 11 e 20** apresentam um padrão recorrente de **normalização de contexto antes da operação principal**: organizar, preparar ou estruturar o contexto antes que a etapa funcional subsequente seja executada.

Esta recorrência é registrada **como observação de design, não como candidato e não como princípio arquitetural formalizado**.

Se uma **quarta ocorrência independente, em outra trilha**, surgir no material, o laboratório deverá avaliar se há evidência suficiente para formalizar esse padrão como princípio arquitetural reutilizável.

## Checkpoint consolidado de itens em observação

Este checkpoint registra o estado atual sem criar ou formalizar automaticamente nenhum dos itens abaixo.

### Evidência já suficiente para avaliação como candidato formal

**Candidato 15A — solicitar informação adicional quando o contexto é insuficiente**
- O mecanismo reaparece de forma explícita na Aula 3.3 e foi necessário na própria execução do exercício.
- Há uma regra operacional clara: quando as informações necessárias não foram fornecidas, interromper a geração da saída dependente e solicitar os dados.
- **Conclusão:** há evidência suficiente para ser tratado como **candidato formal pendente de aprovação**.
- Pasta sugerida: `models/context/` ou `models/input-validation/`, a definir antes da criação.

**Candidato 19 — alertas preventivos**
- O mecanismo aparece estruturado por indicadores + limites + condição de disparo + ação preventiva.
- A Aula 3.3 fornece vários exemplos concretos de thresholds e descreve o alerta como etapa própria entre monitoramento e ação.
- **Conclusão:** há evidência suficiente para ser tratado como **candidato formal pendente de aprovação**.
- Pasta sugerida: `models/monitoring/`.

### Ainda sem evidência suficiente para formalização

**Candidato 15B — taxonomia de categorias de evidência**
- A presença de diferentes tipos de informação é clara, mas ainda não há recorrência suficiente de uma taxonomia estável e independente de contexto.
- **Status:** observação.

**Reposição automatizada de estoques**
- O material apresenta automação da reposição como aplicação de IA, mas ainda não foi demonstrado um mecanismo suficientemente geral e separado para justificar um modelo próprio.
- **Status:** observação.

**Handoff Diagnosis → Action**
- O fluxo agora aparece explicitamente: causa conhecida → Action; causa desconhecida → Diagnosis → Action.
- A recorrência já é relevante, mas ainda é possível tratá-lo como uma regra de integração entre trilhas, e não necessariamente como um modelo independente.
- **Status:** observação de arquitetura/handoff; reavaliar se surgirem outras instâncias com regras próprias.

**Control**
- O material menciona monitoramento e ações, mas não estabeleceu ainda um mecanismo de controle suficientemente distinto de Monitoring e Action.
- **Status:** observação de possível trilha futura.

**Candidatos 3 e 4**
- Os padrões identificados anteriormente permanecem úteis como hipóteses reutilizáveis, mas ainda não receberam evidência adicional suficiente para superar o limiar de formalização estabelecido.
- **Status:** observação.

## Regra de maturação

Um padrão observado não deve ser formalizado apenas porque aparece uma vez.

O laboratório prioriza:
1. recorrência;
2. independência de contexto;
3. clareza do mecanismo;
4. possibilidade de validação;
5. utilidade para outras aplicações.

O fato de um mecanismo parecer promissor ou semelhante a um candidato existente não substitui esse processo.

