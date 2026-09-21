# Principles

Princípios centrais de governança do AI Decision Intelligence Lab.

## 1. IA apoia, não decide

A IA deve ampliar a capacidade humana de compreender problemas, explorar dados, estruturar alternativas, identificar padrões e avaliar possibilidades.

A decisão permanece sob responsabilidade humana.

Em termos operacionais:

```text
IA
 ↓
análise / estruturação / alternativas / evidências
 ↓
julgamento humano
 ↓
decisão
```

O princípio não significa que a IA não possa executar operações ou automatizar etapas. Significa que a automação de uma operação não deve ser confundida com a transferência automática da responsabilidade decisória.

### Componentes que já encarnam o princípio

**C9 — Guardrails de previsão**

Estabelece limites e restrições para a operação de previsão antes de sua execução. Os guardrails reduzem o espaço de comportamento da IA, mas não transformam a previsão em decisão autônoma.

**C12 — Validação crítica da saída**

Introduz uma etapa humana de questionamento e validação depois que a IA produz a saída. O resultado da IA é tratado como objeto de análise crítica, não como conclusão automaticamente aceita.

**C23 — Calibração de classificação por regras explícitas**

Controla previamente a classificação por categorias, referências e regras, buscando maior consistência sem eliminar a necessidade de interpretação e validação humana.

**C25 — Segmentação por padrões de comportamento**

A segmentação produz grupos e padrões que podem apoiar personalização, recomendações ou decisões. A existência de um segmento não determina automaticamente uma ação; sua interpretação e uso permanecem sujeitos ao julgamento humano.

## 2. Qualidade e governança dos dados sustentam a confiabilidade da análise e da decisão

A qualidade dos dados e a governança sobre sua origem, estrutura, consistência, integração e tratamento constituem condições para que análises, previsões, classificações e recomendações produzidas a partir desses dados sejam confiáveis.

Em termos operacionais:

```
Fontes de dados
      ↓
integração / estruturação
      ↓
qualidade + governança
      ↓
análise / previsão / classificação
      ↓
evidências e recomendações
      ↓
decisão humana
```

O princípio não significa que dados de alta qualidade garantam, por si só, uma decisão correta. Significa que **qualidade e governança inadequadas podem comprometer a confiabilidade das etapas analíticas que dependem desses dados**, tornando necessária a verificação das condições da informação antes de atribuir confiança ao resultado.

### Componentes relacionados

**C6, C11 e C20 — Normalização/preparação de contexto**

Esses componentes apresentam o padrão de organizar, preparar, consolidar ou normalizar dados/contexto antes da operação funcional principal. Eles representam manifestações operacionais da necessidade de tornar a entrada adequada para o processamento subsequente.

**Integração de múltiplas fontes**

A integração de fontes distintas também se relaciona a este princípio quando a combinação, estruturação e tratamento das informações são necessários para formar um contexto analítico coerente. O mecanismo permanece em observação no `META-PATTERNS.md`.

### Limite do princípio

O princípio é de **confiabilidade da informação**, não de suficiência da informação.

Mesmo dados bem governados podem não capturar todos os fatores relevantes de um problema. Portanto:

- qualidade dos dados não substitui análise crítica;
- governança não elimina incerteza;
- dados consistentes não tornam automaticamente uma conclusão correta;
- a decisão continua sujeita ao julgamento humano, em coerência com o Princípio 1.

## Protocolo de aprovação e proveniência dos princípios

As entradas de `PRINCIPLES.md` passam a seguir o mesmo protocolo de aprovação item a item adotado para candidatos e modelos reutilizáveis.

Para cada novo princípio, a formalização exige:

1. identificação explícita da proposta;
2. análise de origem e natureza;
3. exame da evidência e dos candidatos/padrões relacionados, quando houver;
4. avaliação de distinções, sobreposições e limites;
5. aprovação explícita do item antes de sua entrada no arquivo;
6. registro da decisão e de sua proveniência.

### Auditoria retroativa dos princípios existentes

Os Princípios 1 e 2 passaram por discussão e aprovação explícitas nesta conversa.

Os Princípios 3 a 7, em sua formulação histórica, **não passaram por esse mesmo rito de aprovação item a item nesta conversa**. A auditoria posterior pode validar sua coerência e fundamento, mas essa validação retroativa **não é equivalente à aprovação original**.

Fica registrada, portanto, a distinção entre **origem histórica**, **auditoria retroativa** e **aprovação explícita**. A partir deste registro, nenhum novo princípio deve ser incluído ou alterado sem aprovação explícita do item específico.

## 3. Rigor antes de reutilização

Um conceito estudado não deve ser transformado automaticamente em componente permanente.

A formalização exige evidência suficiente de:

1. recorrência;
2. independência de contexto;
3. clareza do mecanismo;
4. possibilidade de validação;
5. utilidade para outras aplicações.

### Natureza e origem

**Princípio metodológico de governança do laboratório**, destinado a estabelecer o critério de promoção de conceitos observados a componentes reutilizáveis.

**Auditoria retroativa:** fundamento considerado válido, mas sem aprovação item a item registrada nesta conversa antes de sua formalização histórica.

## 4. Separação entre análise e decisão

Resultados analíticos, previsões, classificações, segmentos, diagnósticos e recomendações são artefatos de apoio. Eles devem permanecer distinguíveis da decisão que eventualmente será tomada a partir deles.

### Distinção em relação ao Princípio 1

Este princípio **não é redundante** com “IA apoia, não decide”. Os dois compartilham base epistemológica, mas regulam dimensões diferentes:

| Princípio | Pergunta central | Objeto protegido |
|---|---|---|
| **1. IA apoia, não decide** | **Quem possui a autoridade decisória?** | responsabilidade e autoridade sobre a decisão |
| **4. Separação entre análise e decisão** | **O artefato analítico pode ser distinguido da decisão derivada dele?** | arquitetura do processo e rastreabilidade entre evidência, recomendação e decisão |

Assim, o Princípio 1 trata de **autoridade decisória**; o Princípio 4 trata de **separação de etapas e artefatos no processo**.

Uma IA pode não possuir autoridade decisória e, ainda assim, sua saída ser tratada indevidamente como decisão final. O Princípio 4 evita essa fusão conceitual.

### Evidência relacionada

A distinção aparece transversalmente em:

- **C9** — previsão com guardrails não equivale a decisão;
- **C12** — a saída da IA é objeto de validação antes de ser aceita;
- **C23** — classificação calibrada continua sendo classificação;
- **C25** — segmentos não determinam automaticamente uma ação;
- **C26** — oportunidade/estratégia mapeada é candidata de ação, não decisão final;
- **C16/C24** — priorização e planejamento são etapas posteriores à produção de evidências/candidatos.

A base de evidência é parcialmente sobreposta à do Princípio 1, mas a regra extraída é diferente: **Princípio 1 limita a transferência de autoridade; Princípio 4 preserva a separação estrutural entre análise e decisão.**

### Natureza e origem

**Princípio arquitetural/epistemológico transversal**, validado retroativamente por múltiplos candidatos e fluxos.

**Auditoria retroativa:** fundamento considerado válido, mas sem aprovação item a item registrada nesta conversa antes de sua formalização histórica.

## 5. Validação crítica

Uma saída de IA deve poder ser questionada, validada e, quando necessário, recalibrada.

Esse princípio é especialmente materializado pelo **C12**, com apoio dos guardrails do **C9** e da calibração do **C23**.

### Natureza e origem

**Princípio arquitetural/operacional transversal**, com evidência direta no C12 e apoio de C9/C23.

**Auditoria retroativa:** fundamento considerado válido, mas sem aprovação item a item registrada nesta conversa antes de sua formalização histórica.

## 6. Não integração automática

Nenhum modelo desenvolvido no laboratório implica integração automática com o ORCHESTRATOR CORE.

A relação permanece:

```text
Conhecimento
   ↓
Laboratório
   ↓
Modelo
   ↓
Validação
   ↓
Seleção humana
   ↓
eventual integração
```

### Natureza e origem

**Regra arquitetural de governança do laboratório**, destinada a preservar a separação entre experimentação, validação e integração com o ORCHESTRATOR CORE.

Ela não depende de recorrência em candidatos do curso e não deve ser apresentada como meta-padrão empírico.

**Auditoria retroativa:** fundamento considerado válido como regra de governança, mas sem aprovação item a item registrada nesta conversa antes de sua formalização histórica.

## Meta-padrão em observação — Seleção contextual do método

A hipótese de **selecionar o método conforme as características do problema** permanece exclusivamente no `META-PATTERNS.md`.

**Status:** **meta-padrão fortalecido — aguardando reforço.**

Não é princípio arquitetural vigente. O `META-PATTERNS.md` é a fonte de verdade para suas ocorrências, peso de evidência, critérios de maturação e eventual promoção.
