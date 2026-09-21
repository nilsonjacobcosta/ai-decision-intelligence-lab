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

## 2. Rigor antes de reutilização

Um conceito estudado não deve ser transformado automaticamente em componente permanente.

A formalização exige evidência suficiente de:
1. recorrência;
2. independência de contexto;
3. clareza do mecanismo;
4. possibilidade de validação;
5. utilidade para outras aplicações.

## 3. Separação entre análise e decisão

Resultados analíticos, previsões, classificações, segmentos, diagnósticos e recomendações são artefatos de apoio. Eles devem permanecer distinguíveis da decisão que eventualmente será tomada a partir deles.

## 4. Validação crítica

Uma saída de IA deve poder ser questionada, validada e, quando necessário, recalibrada.

Esse princípio é especialmente materializado pelo C12, mas também aparece nos guardrails do C9 e na calibração do C23.

## 5. Seleção contextual do método

O laboratório não assume uma técnica universalmente adequada. A escolha do método deve considerar as características do problema, os dados/contexto disponíveis e o objetivo da operação.

```text
problema + dados/contexto + objetivo
            ↓
     escolha do método
            ↓
          aplicação
```

Este princípio foi promovido após três ocorrências independentes:
- C13 — seleção da técnica de previsão conforme o contexto;
- seleção contextual de frameworks em Diagnosis/Action;
- C25 — escolha entre estratégias de segmentação e clustering.

A escolha concreta continua dependente do contexto e deve ser justificada quando relevante.

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
