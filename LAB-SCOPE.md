# LAB-SCOPE.md

## Finalidade

O `ai-decision-intelligence-lab` existe para identificar, formalizar e preservar **mecanismos reutilizáveis de apoio à decisão**.

O laboratório não é um repositório de resumos de cursos, ferramentas, casos de negócio ou técnicas isoladas. Um conteúdo só entra no escopo quando pode ser abstraído em um mecanismo que possa ser reaplicado em outros contextos.

## Escopo funcional

O laboratório cobre mecanismos relacionados às seguintes trilhas funcionais:

1. **Decision — Tomada de decisão**
   - estruturação de decisões e formas de participação/apoio da IA.

2. **Prediction — Previsão**
   - preparação de contexto, construção, ajuste e validação de previsões.

3. **Diagnosis — Diagnóstico**
   - investigação de problemas e causas antes da definição de ações.

4. **Action — Ação**
   - transformação de achados em ações, planos, avaliação e priorização.

5. **Monitoring — Monitoramento**
   - acompanhamento de estados, detecção de desvios e produção de sinais para retroalimentação.

6. **Classification — Classificação**
   - atribuição controlada de categorias, incluindo calibração por referências e regras.

7. **Segmentation — Segmentação**
   - agrupamento por características ou padrões de similaridade, inclusive por clustering quando aplicável.

## Capacidades transversais

Também fazem parte do escopo mecanismos que atravessam mais de uma trilha:

- **Data — Dados:** qualidade, preparação, estruturação e tratamento da entrada;
- **Interaction / Human-in-the-loop — Interação:** solicitação de informação, direção, confirmação e outras formas de participação humana;
- **Investigation — Investigação:** estruturas de investigação aplicáveis a diferentes trilhas;
- **Iterative Refinement — Refinamento iterativo:** mecanismos de transformação sucessiva de estados, regras, artefatos ou análises mediante feedback/nova informação.

Engenharia de prompt e outras técnicas instrumentais podem ser registradas quando constituírem mecanismos reutilizáveis, mas não ampliam, por si só, o escopo funcional do laboratório.

## O que está fora do escopo

Não constituem, por si só, candidatos do laboratório:

- conteúdo puramente conceitual sem mecanismo operacional reutilizável;
- conhecimento específico de um setor, empresa, produto ou ferramenta;
- descrição de um caso de uso único sem abstração transferível;
- automações pontuais sem mecanismo geral suficientemente delimitado;
- recomendações ou conclusões de um curso que não possam ser decompostas em um mecanismo;
- mera repetição de um modelo já existente sem nova delimitação;
- qualquer item cuja única justificativa seja “parece útil”, sem evidência e sem mecanismo identificável.

## Teste objetivo de compatibilidade

Antes de iniciar qualquer curso novo, aplicar este gate **antes da criação do primeiro candidato**.

### Pergunta 1 — Há mecanismo?

> O curso ensina ou demonstra algo que possa ser descrito como **problema → entradas → operação/mecanismo → saída → condições/limitações**?

- **Sim:** prossiga.
- **Não:** curso fora do escopo ou ainda não compatível; não criar candidato.

### Pergunta 2 — Há relação com apoio à decisão?

> O mecanismo melhora, estrutura, informa, valida, prioriza, monitora ou operacionaliza alguma etapa de um processo de decisão/análise?

- **Sim:** prossiga.
- **Não:** não criar candidato; registrar, no máximo, como conhecimento externo ao laboratório.

### Pergunta 3 — Cabe em uma trilha ou capacidade transversal?

> O mecanismo pode ser localizado em uma das trilhas funcionais ou nas capacidades transversais de Dados, Interação, Investigação ou Refinamento iterativo?

- **Sim:** prossiga.
- **Não:** não criar candidato automaticamente. Primeiro avaliar se existe nova trilha/capacidade realmente necessária.
- **Importante:** uma técnica não deve ganhar uma nova categoria apenas por ser diferente; a distinção precisa ser estrutural.

### Pergunta 4 — É reutilizável fora do contexto original?

> O mecanismo continua fazendo sentido quando retirado do caso, empresa, setor, ferramenta ou exemplo em que foi apresentado?

- **Sim:** prossiga.
- **Não:** tratar como aplicação/observação, não como candidato.

### Pergunta 5 — Existe evidência suficiente para formalização futura?

> O material apresenta operação, condições, exemplos ou variações suficientes para testar a existência de um mecanismo, ainda que ele não esteja maduro para formalização?

- **Sim:** o curso é compatível e pode ser estudado; candidatos só serão criados conforme o protocolo de evidência.
- **Não:** o curso pode até conter informação útil, mas não há base suficiente para criação de candidato.

## Regra de decisão

Um curso é **compatível com o laboratório** quando:

- Perguntas 1, 2 e 4 = **Sim**;
- Pergunta 3 = **Sim**, ou existe justificativa explícita para investigar uma nova categoria;
- Pergunta 5 = **Sim** para pelo menos uma linha de evidência.

Se qualquer uma das três condições centrais (1, 2 ou 4) falhar, **não iniciar a extração de candidatos**.

Compatibilidade do curso não significa aprovação prévia de candidatos. O curso pode ser compatível e, ainda assim, produzir zero candidatos formalizáveis.

## Processo após o gate

Somente depois de o curso passar pelo teste:

1. estudar o material;
2. identificar ocorrências de mecanismos;
3. distinguir mecanismo de aplicação;
4. classificar a evidência;
5. testar sobreposição com modelos existentes;
6. registrar candidatos em observação quando houver base suficiente;
7. obter aprovação explícita antes de criar/alterar arquivos de candidato;
8. formalizar apenas quando os critérios de maturação forem satisfeitos.

## Duas dimensões de avaliação

A quantidade de referências recebidas por um candidato não deve ser tratada como sinônimo de qualidade.

Há duas dimensões distintas:

- **Maturidade por evidência acumulada:** recorrência, diversidade de evidências, variações, limites e validações observadas.
- **Centralidade estrutural:** importância do mecanismo para organizar relações, fluxos ou composição da arquitetura.

Existe viés temporal: mecanismos formalizados mais cedo têm naturalmente mais oportunidades de receber referências em aulas posteriores. Portanto, contagem bruta de referências não é proxy suficiente de maturidade, centralidade ou potencial de integração.

## Regra de separação

O laboratório deve preservar a distinção entre:

- **trilha funcional:** responde a “que tipo de operação de decisão/análise está sendo realizada?”;
- **área transversal:** responde a “que capacidade reutilizável atravessa várias operações?”.

A mesma capacidade transversal pode ser composta com várias trilhas. Uma integração entre modelos também não cria automaticamente um novo modelo.

## Relação com outros sistemas

A existência de um mecanismo no laboratório **não implica integração automática com o ORCHESTRATOR CORE** ou com qualquer outro sistema.

Qualquer integração futura exige avaliação própria e decisão explícita.

## Gate resumido

```text
Curso futuro
   ↓
[1] Há mecanismo operacional?
   ├─ Não → fora do escopo / não criar candidato
   └─ Sim
       ↓
[2] Apoia processo de decisão/análise?
   ├─ Não → fora do escopo / não criar candidato
   └─ Sim
       ↓
[3] Cabe em trilha ou área transversal?
   ├─ Não → avaliar nova categoria antes de formalizar
   └─ Sim
       ↓
[4] É reutilizável fora do contexto original?
   ├─ Não → aplicação/observação
   └─ Sim
       ↓
[5] Há evidência suficiente para testar o mecanismo?
   ├─ Não → registrar apenas como observação externa
   └─ Sim → curso compatível → iniciar protocolo de candidatos
```

## Fonte normativa

Este arquivo define o **escopo e o gate de entrada** do laboratório.

A governança detalhada de evidência, classificação, princípios, integridade documental e aprovação deve ser consultada em:

- `PRINCIPLES.md`
- `models/META-PATTERNS.md`
- `models/README.md`
- `governance/LAB-GOVERNANCE-TEMPLATE.md`

O template de governança é deliberadamente genérico para permitir a criação de laboratórios futuros em outros domínios sem depender da história específica deste laboratório.
