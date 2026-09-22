# LAB-GOVERNANCE-TEMPLATE.md

## Propósito

Template genérico para criar um laboratório de conhecimento orientado à identificação e formalização de mecanismos reutilizáveis.

Este documento foi abstraído de um processo de amadurecimento de governança já aplicado a um laboratório de apoio à decisão. Ele deve ser **adaptado ao domínio**, não copiado cegamente.

A regra central é:

> **evidência antes de formalização; distinção antes de integração; integridade documental antes de velocidade.**

---

# 1. Escopo do laboratório

Antes de estudar qualquer fonte, definir explicitamente:

- qual classe de problemas o laboratório cobre;
- quais mecanismos são elegíveis;
- quais mecanismos estão fora do escopo;
- quais são as trilhas funcionais;
- quais são as áreas/capacidades transversais.

### Regra

Uma técnica, ferramenta ou caso não se torna candidato apenas por ser útil. Deve existir um mecanismo reutilizável e delimitável.

---

# 2. Gate de entrada de novas fontes

Antes do primeiro candidato de cada curso, livro, treinamento ou fonte, responder:

1. **Há mecanismo operacional?**
   - problema → entrada → operação → saída → condições/limitações.

2. **O mecanismo é pertinente ao propósito do laboratório?**

3. **Ele cabe em uma trilha funcional ou capacidade transversal existente?**
   - se não, testar se há justificativa estrutural para nova categoria.

4. **É reutilizável fora do contexto original?**

5. **Há evidência suficiente para testar o mecanismo?**

### Regra de parada

Se falhar uma condição central de pertinência ou reutilização, não iniciar a criação de candidatos.

Passar no gate significa apenas que a fonte pode ser estudada. **Não significa que qualquer conceito encontrado será formalizado.**

---

# 3. Régua de evidência

## Evidência forte

Considerar forte quando o material fornece estrutura operacional suficiente para demonstrar um mecanismo reutilizável, incluindo, conforme o caso:

- entradas reconhecíveis;
- operação identificável;
- transformação observável;
- saída ou efeito delimitado;
- condições de uso;
- limites ou critérios;
- possibilidade de reaplicação;
- recorrência ou variação que reduza a dependência de um caso único.

Evidência forte pode sustentar a proposição de um candidato, mas não substitui a análise de sobreposição e a aprovação explícita.

## Evidência secundária / fraca

É evidência que sugere um padrão, mas não demonstra mecanismo independente suficiente para formalização.

Pode incluir:

- ocorrência isolada;
- descrição genérica;
- aplicação de um mecanismo já conhecido;
- similaridade apenas superficial;
- mecanismo incompleto;
- evidência anteriormente avaliada e descartada por insuficiência.

Evidência fraca **não deve ser promovida retroativamente a forte apenas porque posteriormente parece semelhante a um modelo já criado**.

## Princípio de proveniência

A avaliação histórica da evidência faz parte do registro. A semelhança retrospectiva não altera automaticamente a força que a evidência possuía quando foi avaliada.

---

# 4. Maturidade versus centralidade

Separar duas dimensões:

### Maturidade por evidência acumulada

Mede o quanto o mecanismo foi observado e caracterizado:

- recorrência;
- diversidade de contextos;
- variações;
- limites;
- validações;
- estabilidade da abstração.

### Centralidade estrutural

Mede o papel do mecanismo na arquitetura:

- quantos fluxos organiza;
- quantos modelos pode compor;
- se funciona como ponte entre capacidades;
- se define uma transformação recorrente do sistema.

### Viés temporal

Referências recebidas possuem viés temporal: mecanismos formalizados mais cedo têm mais oportunidades de serem citados por fontes posteriores.

Portanto:

> **número de referências recebidas ≠ medida suficiente de maturidade ≠ medida suficiente de centralidade.**

Um mecanismo recente pode ter baixa maturidade por evidência acumulada e alta centralidade estrutural.

---

# 5. Trilha funcional versus área transversal

## Trilha funcional

Representa uma classe funcional do domínio.

Pergunta orientadora:

> “Que tipo de operação principal está sendo realizada?”

Exemplos genéricos:

- previsão;
- diagnóstico;
- ação;
- monitoramento;
- classificação;
- segmentação.

## Área transversal

Representa uma capacidade que pode atravessar várias trilhas.

Pergunta orientadora:

> “Que mecanismo pode ser composto com diferentes operações?”

Exemplos possíveis:

- dados;
- interação;
- investigação;
- refinamento;
- engenharia de prompt, quando tratada como capacidade reutilizável.

### Regra de classificação

Não criar uma nova trilha para cada técnica. Não transformar uma capacidade transversal em domínio funcional artificialmente.

---

# 6. Princípios de governança

Cada princípio deve passar pelo mesmo protocolo de aprovação aplicado aos candidatos.

### Protocolo

1. proposta explícita;
2. identificação da origem e natureza;
3. evidência e relação com modelos/padrões;
4. análise de sobreposição e distinção;
5. limites de aplicação;
6. aprovação explícita;
7. registro de proveniência e decisão.

### Princípios-base recomendados

#### P1 — A IA apoia; não assume automaticamente a autoridade decisória

Define a propriedade da decisão e preserva a autoridade humana/contextual apropriada.

#### P2 — Qualidade e governança dos dados sustentam a confiabilidade da análise e da decisão

Dados, contexto, qualidade e governança condicionam a confiabilidade das etapas posteriores.

#### P3 — Rigor antes de reutilização

A reutilização exige abstração e validação suficientes; utilidade aparente não basta.

#### P4 — Separação entre análise e decisão

O artefato analítico e a decisão dele derivada devem poder ser distinguidos conceitualmente e operacionalmente.

P1 e P4 não são redundantes:

- P1 trata de **autoridade decisória**;
- P4 trata da **separação entre processo/artefato analítico e decisão**.

#### P5 — Validação crítica

Saídas analíticas devem permanecer sujeitas a validação proporcional ao contexto e ao risco.

#### P6 — Não integração automática

A existência de um modelo não implica sua integração automática a outro sistema, laboratório ou arquitetura.

### Regra importante

Princípios não devem ser criados apenas porque “parecem bons”. Devem ter origem, natureza, evidência/justificativa, distinção e aprovação documentadas.

---

# 7. Integridade documental

A documentação do laboratório é parte da governança, não apenas registro editorial.

## Política de edição

- alterações devem ser **direcionadas e específicas por seção**;
- não reescrever um arquivo inteiro como método de editar uma seção;
- antes de qualquer commit, verificar que seções não relacionadas permanecem intactas;
- depois do commit, registrar explicitamente:
  - quais seções foram alteradas;
  - quais arquivos foram alterados;
  - que as demais seções relevantes foram preservadas;
- se a integridade não puder ser verificada, **não realizar o commit**.

## Regra de reconstrução

Nunca reconstruir um arquivo completo a partir de uma leitura parcial para realizar uma edição localizada.

Uma leitura incompleta seguida de regravação integral pode eliminar conteúdo posterior sem que o erro seja perceptível na revisão superficial.

---

# 8. Integridade de candidatos e modelos

Antes de criar um candidato:

- verificar se já existe modelo equivalente;
- verificar modelos adjacentes e possíveis sobreposições;
- definir claramente o que o mecanismo faz;
- definir o que ele não faz;
- registrar relações com modelos existentes;
- registrar a força da evidência.

Antes de formalizar:

- testar recorrência;
- testar independência de contexto;
- testar clareza do mecanismo;
- testar possibilidade de validação;
- testar utilidade para outras aplicações.

---

# 9. Aprovação explícita

Identificação, análise e criação são etapas diferentes.

Fluxo recomendado:

```text
observação
   ↓
hipótese de mecanismo
   ↓
teste de sobreposição / limites
   ↓
proposta de candidato
   ↓
aprovação explícita
   ↓
criação do arquivo
   ↓
formalização / maturação
```

Nenhum candidato deve ser criado apenas porque o sistema de análise o considerou interessante.

---

# 10. Distinção entre observação, candidato e modelo

### Observação

Há um indício ou aplicação interessante, mas o mecanismo ainda não está suficientemente delimitado.

### Candidato

Existe hipótese operacional reutilizável, com evidência suficiente para avaliação formal.

### Modelo formalizado

O mecanismo foi suficientemente caracterizado, distinguido de sobreposições e aprovado para incorporação ao laboratório.

A progressão não é automática.

---

# 11. Meta-padrões

Meta-padrões devem ser registrados separadamente dos candidatos quando descrevem uma regularidade que atravessa múltiplos mecanismos.

Um meta-padrão não deve ser promovido a princípio arquitetural apenas por parecer recorrente.

Registrar:

- evidências;
- força de cada evidência;
- ocorrências descartadas e motivo;
- hipóteses ainda em observação;
- critérios necessários para reforço;
- relações com modelos já formalizados.

---

# 12. Refinamento e revisão

Quando novas evidências surgirem:

- não apagar a avaliação histórica;
- registrar a nova evidência separadamente;
- explicar se ela reforça, delimita, contradiz ou absorve a hipótese anterior;
- preservar a proveniência da decisão original.

Uma hipótese pode amadurecer sem que sua avaliação histórica seja reescrita.

---

# 13. Integração entre modelos

A integração deve ser tratada como uma decisão arquitetural separada.

Perguntar:

1. os mecanismos têm funções distintas?
2. existe fluxo de entrada/saída identificável?
3. a composição é opcional ou obrigatória?
4. existem condições de handoff?
5. a integração cria um mecanismo novo ou apenas compõe mecanismos existentes?

Não criar um novo modelo apenas porque dois modelos podem ser encadeados.

---

# 14. Relação com sistemas externos

Laboratórios independentes devem manter fronteira explícita com sistemas externos.

> **Modelo formalizado ≠ integração automática.**

Qualquer transferência para outra arquitetura exige avaliação própria, compatibilidade, limites e aprovação.

---

# 15. Checklist de governança antes de cada nova fonte

- [ ] A fonte passou pelo gate de escopo?
- [ ] O mecanismo é reutilizável?
- [ ] A evidência foi classificada?
- [ ] A proveniência foi preservada?
- [ ] Há sobreposição com modelo existente?
- [ ] É trilha funcional ou capacidade transversal?
- [ ] É observação, candidato ou modelo?
- [ ] A aprovação necessária foi obtida?
- [ ] A edição documental é direcionada?
- [ ] A integridade das seções não relacionadas foi verificada?
- [ ] A integração externa foi explicitamente separada da formalização?

---

# 16. Regra final

O laboratório deve preferir:

**menos modelos, mais sólidos; menos categorias artificiais, mais mecanismos bem delimitados; menos velocidade de registro, mais integridade e proveniência.**

Este template é um ponto de partida genérico. Cada novo laboratório deve adaptar seu escopo, trilhas, capacidades e princípios ao domínio específico, mantendo o processo de evidência, distinção, aprovação e integridade documental.
