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

## 3. Rigor antes de reutilização

Um conceito estudado não deve ser transformado automaticamente em componente permanente.

A formalização exige evidência suficiente de:
1. recorrência;
2. independência de contexto;
3. clareza do mecanismo;
4. possibilidade de validação;
5. utilidade para outras aplicações.

## 4. Separação entre análise e decisão

Resultados analíticos, previsões, classificações, segmentos, diagnósticos e recomendações são artefatos de apoio. Eles devem permanecer distinguíveis da decisão que eventualmente será tomada a partir deles.

## 5. Validação crítica

Uma saída de IA deve poder ser questionada, validada e, quando necessário, recalibrada.

Esse princípio é especialmente materializado pelo C12, mas também aparece nos guardrails do C9 e na calibração do C23.

## 6. Seleção contextual do método

**Status:** ainda não formalizado como princípio arquitetural.

O padrão está em **META-PATTERNS.md**, que é a fonte de verdade para suas ocorrências, peso de evidência, critérios de maturação e eventual promoção.

Enquanto permanecer em observação, não deve ser tratado como princípio arquitetural vigente.

## 7. Não integração automática

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
