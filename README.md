# AI Decision Intelligence Lab

Biblioteca experimental de modelos, métodos e componentes reutilizáveis para tomada de decisão apoiada por dados e inteligência artificial.

## Objetivo

Este repositório funciona como um laboratório de aprendizagem e experimentação.

Os conteúdos estudados são transformados, progressivamente, em:

**conceitos → métodos → modelos → prompts → componentes reutilizáveis → experimentos → possíveis integrações**

O repositório é deliberadamente separado do **ORCHESTRATOR CORE**.

Nada aqui é considerado parte do ORCHESTRATOR CORE automaticamente. Um componente somente deverá ser incorporado ao sistema principal depois de ser compreendido, testado e validado.

## Princípios

- Preservar a origem e o contexto de cada método.
- Separar conteúdo estudado de interpretação e adaptação.
- Não transformar um conceito em framework permanente antes de validá-lo.
- Registrar hipóteses, experimentos e limitações.
- Priorizar modelos reutilizáveis e independentes de contexto.
- Manter a decisão humana como parte explícita dos modelos quando aplicável.
- Distinguir trilhas funcionais de áreas transversais.

## Estrutura atual

A estrutura abaixo reflete as pastas existentes no repositório. Em `models/`, seis áreas são tratadas como **trilhas funcionais** e quatro como **áreas transversais**.

```text
ai-decision-intelligence-lab/
│
├── README.md
│
├── course/
│   └── learning-path/
│       ├── 01-decisao/
│       ├── 02-previsoes-futuras/
│       ├── 03-cenarios/
│       ├── 04-feedbacks/
│       ├── 05-recomendacoes/
│       └── 06-decisao-na-ausencia-de-dados/
│
├── models/
│   ├── action/                    # trilha funcional
│   ├── classification/            # trilha funcional
│   ├── data/                      # área transversal
│   ├── diagnosis/                 # trilha funcional
│   ├── interaction/               # área transversal — human-in-the-loop
│   ├── investigation/             # área transversal — técnica de análise
│   ├── monitoring/                # trilha funcional
│   ├── prediction/                # trilha funcional
│   ├── prompt-engineering/        # área transversal
│   └── META-PATTERNS.md
│
├── prompts/
├── templates/
├── case-studies/
├── experiments/
└── integration/
    └── orchestrator-core/
```

### Trilhas funcionais

- **Decision** — tomada de decisão; os componentes atuais estão em `prompts/` e `templates/`, sem diretório físico próprio em `models/`.
- **Prediction** — previsão.
- **Diagnosis** — diagnóstico.
- **Action** — ação.
- **Monitoring** — monitoramento.
- **Classification** — classificação.

### Áreas transversais

- **Data** — preparação e tratamento de dados.
- **Prompt Engineering** — construção e ajuste de prompts.
- **Investigation** — técnica de investigação aplicável a diferentes trilhas.
- **Interaction** — mecanismos de interação e human-in-the-loop.

Essa distinção evita que uma técnica transversal seja confundida com um domínio funcional e facilita a composição entre componentes.

## Fluxo de maturação

Cada ideia pode passar por quatro estágios:

1. **Estudo** — compreensão do conceito em sua fonte.
2. **Modelagem** — transformação em uma estrutura reutilizável.
3. **Validação** — teste com exemplos e casos.
4. **Integração** — avaliação de possível uso no ORCHESTRATOR CORE.

## Relação com o ORCHESTRATOR CORE

O laboratório é uma fonte potencial de componentes para o ORCHESTRATOR CORE, mas não uma extensão automática dele.

A relação pretendida é:

```text
Conhecimento
    ↓
Laboratório
    ↓
Modelos reutilizáveis
    ↓
Validação
    ↓
Seleção
    ↓
ORCHESTRATOR CORE
```

## Status

O repositório está em fase de estruturação e validação. Os modelos são desenvolvidos progressivamente conforme o aprendizado e os experimentos avancem.
