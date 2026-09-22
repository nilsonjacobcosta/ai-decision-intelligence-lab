# AI Decision Intelligence Lab

Laboratório experimental de modelos, métodos, prompts e componentes reutilizáveis para **tomada de decisão apoiada por dados e inteligência artificial**.

Este README é o ponto de entrada para quem não acompanhou a construção histórica do laboratório.

## 1. O que é este laboratório?

O repositório transforma aprendizado e experimentação em componentes progressivamente mais estruturados:

**conceito → método → modelo → prompt/componente → experimento → reutilização potencial**

O laboratório não é uma extensão automática do **ORCHESTRATOR CORE — NILSON COSTA**. Ele funciona como espaço separado para estudar, formalizar, comparar limites e registrar evidências antes de qualquer eventual integração futura.

> **Regra central:** nada neste repositório é integrado ao ORCHESTRATOR CORE automaticamente.

## 2. Como navegar

| Área | O que encontrar |
|---|---|
| `course/` | Material e registros derivados do percurso de aprendizagem |
| `models/` | Modelos reutilizáveis já formalizados |
| `models/META-PATTERNS.md` | Padrões transversais, hipóteses e evidências que atravessam vários modelos |
| `models/README.md` | Índice e organização detalhada dos modelos |
| `prompts/` | Prompts reutilizáveis |
| `templates/` | Estruturas reutilizáveis, como matriz de decisão |
| `case-studies/` | Casos e aplicações |
| `experiments/` | Experimentações |
| `integration/` | Registros relacionados a possíveis avaliações futuras de integração; não contém integração automática com o ORCHESTRATOR CORE |
| `PRINCIPLES.md` | Princípios e regras de governança do laboratório |

## 3. Arquitetura atual

O diretório `models/` distingue **trilhas funcionais** de **áreas transversais**.

### Trilhas funcionais

- **Decision** — estruturação da tomada de decisão e do papel da IA.
- **Prediction** — previsão e controle de forecasts.
- **Diagnosis** — investigação de causas e validação analítica.
- **Action** — geração, priorização e operacionalização de ações.
- **Monitoring** — acompanhamento de estados, desvios e alertas.
- **Classification** — classificação controlada e calibrada.
- **Segmentation** — agrupamento por características ou padrões de similaridade.

### Áreas transversais

- **Data** — qualidade, granularidade, preparação e contexto dos dados.
- **Prompt Engineering** — técnicas e estruturas para construção de prompts.
- **Investigation** — investigação aplicável a diferentes trilhas.
- **Interaction / Human-in-the-loop** — solicitação de informação, escolhas direcionais e outros mecanismos de participação humana.
- **Refinamento iterativo** — modelo transversal para transformação progressiva de estados, regras, artefatos ou análises mediante feedback/nova informação.

## 4. Modelos que estruturam o laboratório

Alguns componentes importantes do ciclo atual:

- **C3 — Papel da IA conforme o tipo de decisão**: define como a IA participa conforme a natureza da decisão e o contexto.
- **C9 — Guardrails para Previsão**: estabelece restrições explícitas para manter forecasts ancorados em evidências e premissas verificáveis.
- **C12 — Validação Crítica da Saída do Forecast**: questiona e recalibra resultados inesperados antes de utilizá-los na decisão.
- **C16 — Orquestração e priorização de ações**: avalia alternativas por critérios explícitos e produz priorização contextual.
- **C23 — Calibração de classificação por regras explícitas**: reduz ambiguidades por meio de categorias, referências, exemplos e regras.
- **C25 — Segmentação por padrões de comportamento**: estrutura grupos por similaridade e pode selecionar entre estratégias de segmentação.
- **Refinamento iterativo**: consolida quatro subfamílias distintas — iteração algorítmica, refinamento de regras/análise, construção iterativa de artefatos e refinamento decisório/analítico.

A lista curada dos componentes que chegaram ao fechamento do ciclo com sinais particularmente claros de reutilização e composição está em:

**[Candidatos prontos para uma futura avaliação de integração](integration/future-integration-candidates.md)**

Essa lista **não é uma autorização de integração**. Ela apenas registra candidatos que poderão ser avaliados em uma frente futura, separadamente.

## 5. Como interpretar os números dos candidatos

Os identificadores C3, C9, C12 etc. são referências históricas do processo de construção do laboratório. Eles não representam uma escala de qualidade.

Um candidato pode ser formalizado como modelo próprio, absorvido por outro modelo, mantido como meta-padrão ou permanecer em observação. O histórico dessas decisões é preservado nos documentos de governança e nos próprios modelos.

## 6. Meta-padrões

Além dos modelos individuais, o laboratório registra padrões que aparecem em diferentes contextos.

Exemplos atuais:

- escolha de método conforme as características do problema;
- normalização de contexto antes da operação principal;
- calibração/restrição proativa por regras explícitas;
- transformação categorial de representações;
- refinamento iterativo;
- adaptação da saída à audiência;
- cenários e simulação;
- outras hipóteses transversais em observação.

Consulte **[models/META-PATTERNS.md](models/META-PATTERNS.md)** para o estado consolidado dessas hipóteses.

## 7. Governança

O laboratório segue alguns princípios estruturais:

1. **IA apoia, não decide.**
2. **Qualidade e governança dos dados sustentam a confiabilidade da análise e da decisão.**
3. **Rigor antes de reutilização.**
4. **Separação entre análise e decisão.**
5. **Validação crítica.**
6. **Não integração automática com o ORCHESTRATOR CORE.**

A proveniência, os limites e as decisões de formalização devem permanecer explícitos.

Consulte **[PRINCIPLES.md](PRINCIPLES.md)** para o registro completo.

## 8. Relação com o ORCHESTRATOR CORE

A arquitetura deliberadamente mantém dois espaços:

```text
fontes / estudo / experimentos
            ↓
AI Decision Intelligence Lab
            ↓
modelos formalizados
            ↓
candidatos prontos para futura avaliação
            ↓
[futura frente separada]
            ↓
ORCHESTRATOR CORE
```

A etapa entre o laboratório e o ORCHESTRATOR CORE **não está sendo executada neste ciclo**.

## 9. Estado no fechamento do ciclo v1.0

A **v1.0** marca o fechamento deste ciclo de construção do laboratório.

Neste ponto:

- a estrutura de modelos e áreas transversais está consolidada;
- candidatos e meta-padrões foram distinguidos;
- hipóteses arquivadas ou absorvidas foram registradas;
- o modelo de refinamento iterativo foi formalizado como transversal;
- o checkpoint de observações foi consolidado;
- foi criada uma lista curada de candidatos para uma eventual avaliação futura;
- nenhuma integração com o ORCHESTRATOR CORE foi realizada ou presumida.

A evolução posterior deve partir deste estado versionado, preservando a rastreabilidade das mudanças.
