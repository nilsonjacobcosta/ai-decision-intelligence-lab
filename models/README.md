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

## Organização estrutural

O diretório `models/` distingue **trilhas funcionais de domínio** de **áreas transversais**.

### Trilhas funcionais

São trilhas cujo objeto principal corresponde a uma classe funcional de decisão/análise/operação:

1. **Decision — Tomada de decisão**
   - foco: estruturar decisões e formas de apoio da IA;
   - os componentes atuais de matriz de decisão estão em `prompts/` e `templates/`; não há, neste momento, um diretório físico `models/decision/`.

2. **Prediction — Previsão**
   - foco: organizar dados, preparar contexto, construir e ajustar previsões e validar resultados;
   - `models/prediction/`.

3. **Diagnosis — Diagnóstico**
   - foco: compreender problemas e suas causas antes de definir ações corretivas;
   - `models/diagnosis/`.

4. **Action — Ação**
   - foco: transformar causas diagnosticadas em ações estruturadas, avaliar impactos e priorizar o que deve avançar;
   - `models/action/`.

5. **Monitoring — Monitoramento**
   - foco: acompanhar estados, detectar desvios e produzir sinais para retroalimentar o processo;
   - `models/monitoring/`.

6. **Classification — Classificação**
   - foco: atribuir categorias de forma controlada, com referências e mecanismos de calibração;
   - `models/classification/`.

### Áreas transversais

São mecanismos que podem atravessar várias trilhas funcionais e, portanto, não devem ser tratados como domínios de negócio independentes.

1. **Data — Dados**
   - preparação, qualidade, estruturação e tratamento da entrada;
   - `models/data/`.

2. **Prompt Engineering — Engenharia de Prompt**
   - padrões e técnicas de construção/ajuste de prompts;
   - `models/prompt-engineering/`.

3. **Investigation — Investigação**
   - técnica de análise aplicável a diferentes trilhas, e não uma trilha funcional de domínio;
   - `models/investigation/`.
   - Candidato 21 — investigação em dois níveis: visão macro → seleção do foco → análise aprofundada.

4. **Interaction — Interação / Human-in-the-loop**
   - mecanismos de interação em que o usuário fornece informação, direção ou decisão necessária para a continuidade da operação;
   - `models/interaction/`.
   - Candidato 15A — solicitação de informação adicional;
   - Candidato 22 — escolha direcional do foco pelo usuário.

A separação entre trilhas e áreas transversais evita transformar técnicas reutilizáveis em domínios artificiais e permite que um mesmo componente seja composto com diferentes trilhas.

## Monitoring

O Candidato 18 trata do monitoramento contínuo e da detecção de desvios.

O Candidato 19 trata da transformação de uma condição monitorada em **alerta preventivo**, com threshold/condição de disparo e ação preventiva associada.

Fluxo conceitual:

```text
Monitoring
    ↓
detecção / condição relevante
    ↓
C19 — alerta preventivo
    ↓
ação preventiva
```

O alerta pode alimentar Action, Diagnosis ou outra etapa, conforme o contexto.

## Decision

Os componentes atuais relacionados à tomada de decisão estratégica estão organizados fora de `models/decision/`:

- `prompts/decision-matrix-enrichment.md` — prompt reutilizável para enriquecimento de matriz de decisão;
- `templates/decision-matrix.md` — estrutura reutilizável da matriz.

## Diagnosis → Action

A arquitetura registra uma regra de handoff:

```text
causa conhecida
    ↓
Action

causa desconhecida
    ↓
Diagnosis
    ↓
Action
    ↓
Monitoring
```

Essa regra permanece tratada como **integração entre trilhas**, e não como um modelo independente.

## Investigation

O Candidato 21 — Investigação em dois níveis — permanece formalizado em `models/investigation/`, mas agora é classificado como **área transversal**.

Seu núcleo é:

```text
visão geral
   ↓
seleção do foco
   ↓
análise aprofundada
```

Visualizações e ações decorrentes dos achados são operações downstream e não constituem, por si só, uma nova técnica de investigação.

O Candidato 22 pode ser composto com o C21: o C21 define a estrutura da investigação; o C22 define a interação pela qual o usuário escolhe a direção do aprofundamento.

## Interaction / Human-in-the-loop

A área `models/interaction/` reúne mecanismos em que a continuidade ou a direção da operação depende explicitamente do usuário.

### Candidato 15A — Solicitação de informação adicional

A IA verifica se o contexto é suficiente e, diante de lacunas relevantes, solicita os dados necessários antes de prosseguir.

É um mecanismo de human-in-the-loop orientado à **completude do contexto**.

### Candidato 22 — Escolha direcional do foco

A IA apresenta opções de aprofundamento e solicita ao usuário qual dimensão deseja investigar.

É um mecanismo de human-in-the-loop orientado à **direção da análise**.

Os dois mecanismos são distintos:

```text
C15A → falta informação necessária
C22  → falta uma escolha direcional
```

Eles podem ser usados em conjunto e atravessar diferentes trilhas.

## Classification

O Candidato 23 — calibração de classificação por regras explícitas — permanece em `models/classification/`.

O mecanismo utiliza categorias, referências, exemplos e regras explícitas para reduzir ambiguidades antes da classificação, distinguindo-se da validação reativa do Candidato 12.

## Meta-padrões transversais

Os padrões que atravessam múltiplas trilhas são registrados separadamente para evitar que observações transversais se confundam com candidatos ou modelos já formalizados.

Consulte **[META-PATTERNS.md](META-PATTERNS.md)** para o registro consolidado.

No estado atual, estão em observação três padrões:
- **Escolha de método conforme características do problema** — duas ocorrências, incluindo o Candidato 13 e a seleção contextual de frameworks em Diagnosis/Action.
- **Normalização de contexto antes da operação principal** — três ocorrências, nos Candidatos 6, 11 e 20; a segmentação de bases grandes não conta como quarta ocorrência porque representa particionamento da entrada, não normalização de contexto.
- **Calibração/restrição proativa via regras explícitas** — duas ocorrências, nos Candidatos 9 e 23; o Candidato 12 representa controle reativo da saída e permanece conceitualmente separado.

Esses registros são observações de design e **não constituem princípios arquiteturais formalizados**.

## Checkpoint de observações

### Ainda em observação

**15B — taxonomia de categorias de evidência**
- A presença de diferentes tipos de informação é clara, mas ainda não há recorrência suficiente de uma taxonomia estável e independente de contexto.

**Reposição automatizada de estoques**
- O material apresenta a automação da reposição como aplicação de IA, mas ainda não demonstrou um mecanismo suficientemente geral e separado para justificar um modelo próprio.

**Control**
- Monitoramento e Action estão formalizados, mas ainda não foi estabelecido um mecanismo de controle suficientemente distinto para justificar uma trilha própria.

**Candidatos 3 e 4**
- Permanecem como hipóteses reutilizáveis em observação, sem evidência adicional suficiente para formalização.

### Já formalizados

- **15A** — solicitação de informação adicional → `models/interaction/`;
- **19** — alertas preventivos → `models/monitoring/`;
- **21** — investigação em dois níveis → `models/investigation/`, como área transversal;
- **22** — escolha direcional do foco pelo usuário → `models/interaction/`;
- **23** — calibração de classificação por regras explícitas → `models/classification/`.

## Regra de maturação

Um padrão observado não deve ser formalizado apenas porque aparece uma vez.

O laboratório prioriza:
1. recorrência;
2. independência de contexto;
3. clareza do mecanismo;
4. possibilidade de validação;
5. utilidade para outras aplicações.

Nenhum modelo ou área neste laboratório implica integração automática com o ORCHESTRATOR CORE.
