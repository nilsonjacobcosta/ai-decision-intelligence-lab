# Structured Root-Cause Diagnosis

## Status

Reusable model — candidate 14.

## Purpose

Structure a diagnosis of an ongoing problem before defining corrective actions.

The model separates **diagnosis** from **prescription**: first identify and organize plausible causes using available evidence; only afterward move to prioritization and action definition.

## Core flow

```text
Problem
  ↓
Evidence gathering
  ↓
Cause mapping
  ├── MECE
  ├── Ishikawa
  └── Quantitative + qualitative analysis
  ↓
Structured causes
  ↓
Prioritization / corrective actions
```

## Inputs

The diagnosis may use different evidence sources, including:

- meeting minutes or internal reports;
- stakeholder or manager perspectives;
- operational indicators;
- historical performance data;
- process information;
- external factors;
- qualitative observations and feedback.

The evidence categories are examples, not a mandatory fixed taxonomy.

## Method

### 1. Define the problem

State the problem to be investigated and its observable effect.

### 2. Gather sufficient evidence

Ask for relevant information before drawing conclusions. If the available evidence is insufficient, request additional information rather than filling gaps with assumptions.

### 3. Map causes with MECE

Organize the causal space so that categories are as mutually exclusive and collectively exhaustive as practical.

A useful distinction is:

- internal causes — factors under organizational control;
- external causes — factors outside direct organizational control.

The categories should be adapted to the problem rather than treated as a fixed checklist.

### 4. Structure causes with Ishikawa

Organize the identified causes and subcauses around the problem/effect, using categories appropriate to the context.

### 5. Combine quantitative and qualitative evidence

Consider both:

- quantitative evidence: indicators, historical data, deviations, volumes, lead times, costs, etc.;
- qualitative evidence: behavior, perceptions, market tendencies, process observations, and contextual information.

### 6. Produce a diagnosis, not an action plan

The initial output should identify and structure causes.

Do **not** automatically prescribe corrective actions in this stage. The causes become inputs for a subsequent prioritization and action-design stage.

## Output

A structured diagnosis containing, as appropriate:

1. problem definition;
2. internal and external causes;
3. Ishikawa-style causal structure;
4. quantitative evidence;
5. qualitative evidence;
6. relationships or dependencies among causes;
7. uncertainties or evidence gaps;
8. causes requiring further validation.

## Quality rules

- Distinguish observed evidence from inference.
- Do not treat stakeholder opinions as established facts without supporting evidence.
- Do not invent missing data.
- Request additional information when the current evidence is insufficient.
- Avoid premature corrective recommendations.
- Keep the causal structure adaptable to the problem.
- Preserve traceability between a cause and the evidence supporting it.

## Relationship to other models

This model belongs to the **diagnosis** track of the laboratory.

It is intentionally separate from action recommendation: diagnosis identifies and structures causes; a later model can prioritize causes and define actions.

## Source-derived pattern

The course material for Aula 3.1 presents the same general sequence: understand the context, analyze underlying causes with MECE and Ishikawa, combine quantitative and qualitative analysis, and leave corrective actions for a later stage.

## Limitations

MECE and Ishikawa are structuring methods, not guarantees that the identified causes are true. A structured cause map still requires evidence and, where appropriate, validation.

