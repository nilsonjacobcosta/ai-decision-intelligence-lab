# Candidato 3 — Papel da IA conforme o tipo de decisão

**Status:** formalizado como modelo reutilizável da trilha **Decision**.

## Problema

Determinar **como a IA deve participar de um processo decisório** de acordo com as características da decisão, especialmente o tipo de decisão e a disponibilidade de dados.

O modelo parte da distinção apresentada no curso entre decisões:

- **Racionais** — apoiadas por dados, análises e previsões;
- **Intuitivas** — baseadas em experiência, aprendizados e julgamento do decisor;
- **Colaborativas** — apoiadas pela contribuição de outras pessoas ou especialistas.

## Evidência de origem

O candidato foi observado inicialmente na **Aula 1.3**, que apresentou a relação entre tipo de decisão e papel da IA:

| Tipo de decisão | Papel da IA |
|---|---|
| Racional | apoiar com dados, insights, previsões e análises |
| Intuitiva | atuar como conselheira/mentora, explorar experiência e julgamento e oferecer questionamentos construtivos |
| Colaborativa | ampliar perspectivas, apoiar consenso, comunicação e contribuição de outras pessoas |

Na **Aula 6.1 — Decisão na ausência de dados**, essa hipótese recebeu evidência operacional mais estruturada.

O caso apresentado estabelece que, na ausência de dados concretos, a abordagem intuitiva e colaborativa deve ser utilizada de forma mais intensa. O processo inclui:

1. reconhecimento do contexto da empresa e do decisor;
2. projeção de cenários e riscos;
3. exploração de decisões intuitivas a partir de experiência, valores, características de liderança e histórico de decisões anteriores;
4. colaboração com outras pessoas/especialistas;
5. decisão final pelo responsável.

A nova evidência é relevante porque transforma uma distinção conceitual da Aula 1.3 em um **mecanismo de escolha do modo de participação da IA**.

## Abstração operacional

```text
Características da decisão
        ↓
Tipo de decisão / disponibilidade de dados
        ↓
Modo de participação da IA
        ├── Racional
        │     → dados / análises / previsões
        │
        ├── Intuitiva
        │     → exploração de experiência / julgamento / questionamento
        │
        └── Colaborativa
              → perspectivas / especialistas / consenso
        ↓
Decisão humana
```

## Entradas

- natureza/tipo da decisão;
- disponibilidade ou ausência de dados;
- contexto organizacional;
- perfil e experiência do decisor;
- histórico de decisões relevantes;
- necessidade de perspectivas externas ou colaboração.

## Processo

1. Identificar as características da decisão.
2. Determinar qual forma de participação é mais adequada ao contexto.
3. Configurar a interação da IA de acordo com esse papel.
4. Utilizar a IA para estruturar, explorar, questionar ou ampliar o processo.
5. Preservar a decisão final sob responsabilidade humana.

O modelo não exige que apenas um modo seja utilizado. Em situações complexas, os modos podem ser combinados. A Aula 6.1, por exemplo, combina exploração intuitiva e colaboração quando os dados são insuficientes.

## Saída

Um **modo de participação da IA explicitamente adequado ao tipo de decisão e ao contexto**, em vez de aplicar uma única forma de interação independentemente do problema.

## Extensão funcional — transição entre modos decisórios

A evidência da **Aula 6.3** amplia o C3: além de selecionar inicialmente o modo de participação da IA, o modelo pode **conduzir uma transição contextual entre modos decisórios** quando o processo já estiver em andamento.

O caso observado parte de uma decisão previamente estruturada por uma **Matriz de Decisão Multicritério**, representando uma etapa racional/analítica, e conduz o decisor a uma etapa posterior de reflexão sobre experiência, pressões internas e externas, heurísticas e intuição antes da confirmação final. fileciteturn245file0L179-L205

```text
análise racional / multicritério
        ↓
decisão candidata
        ↓
C3 — transição de modo
        ↓
experiência + heurísticas + intuição
        ↓
confirmação ou ajuste pelo decisor
```

Isso não constitui um novo modelo independente. É uma **extensão do mesmo mecanismo de C3**, porque a função continua sendo determinar/estruturar **como a IA participa do processo decisório conforme o modo decisório e o contexto**.

### Função de roteamento

A nova evidência também reforça a hipótese arquitetural de C3 como possível roteador:

- **seleção/direcionamento:** o processo pode passar do modo racional para o intuitivo/heurístico;
- **critério identificável:** a transição decorre da natureza da etapa decisória e da necessidade de incorporar experiência, julgamento e heurísticas;
- **autoridade:** a confirmação ou ajuste permanece sob responsabilidade humana.

A hipótese de C3 como **roteador transversal entre trilhas funcionais** permanece, contudo, em observação. A evidência atual demonstra seleção entre **modos decisórios distintos**, mas ainda não demonstra recorrência suficiente atravessando múltiplas trilhas funcionais do laboratório.

### Relação com C16

C16 continua responsável pela priorização racional mediante critérios explícitos. C3 não absorve essa função.

A composição observada é:

```text
C16 — avaliação/priorização racional
        ↓
C3 — transição de modo
        ↓
modo intuitivo/heurístico
        ↓
decisão humana
```

Portanto, trata-se de **handoff entre mecanismos**, não de fusão entre C3 e C16.

### Delimitação em relação ao C12

C12 continua tratando da **validação crítica de uma saída analítica**. A extensão de C3 trata da **mudança de modo decisório** e da forma de participação da IA, tendo a decisão candidata como objeto do processo.

## Limites

- O modelo não transforma intuição em evidência objetiva.
- Ausência de dados não significa que a IA possa substituir evidência empírica por certeza.
- Cenários produzidos sem dados concretos devem ser tratados como construções exploratórias, não como previsões verificadas.
- A IA apoia o processo; a decisão permanece sob responsabilidade humana.
- O modelo define **como a IA participa**, não qual decisão deve ser tomada.

## Relação com outros componentes

### C15A — solicitação de informação adicional

C15A pergunta **se falta informação necessária para continuar**.

C3 pergunta **qual modo de participação da IA é adequado à natureza da decisão**.

Os mecanismos podem ser compostos:

```text
C3 identifica o modo adequado
        ↓
C15A pode solicitar informações necessárias
        ↓
IA atua segundo o modo selecionado
```

### C21 — investigação em dois níveis

C21 estrutura o aprofundamento da investigação.

C3 determina o papel/modo de participação da IA no processo decisório.

### C16 / C24

C3 pode anteceder mecanismos de ação e priorização, mas não determina por si só quais ações devem ser priorizadas nem como serão operacionalizadas.

## Delimitação em relação ao meta-padrão “Escolha de método conforme características do problema”

Foi avaliado explicitamente se C3 deveria contar como ocorrência desse meta-padrão.

### Decisão

**C3 não será contado, neste momento, como ocorrência do meta-padrão.**

Há uma analogia estrutural real:

```text
características do contexto
        ↓
escolha de uma forma apropriada de operação
```

Entretanto, os mecanismos operam em **níveis funcionais diferentes**.

O meta-padrão existente trata da escolha de um **método/técnica analítica** para executar uma operação:

```text
problema
  ↓
características relevantes
  ↓
método/framework analítico
  ↓
aplicação
```

Exemplos já registrados incluem a escolha de estratégias de segmentação no C25 e a seleção de técnica conforme características do problema no C13.

C3, por outro lado, escolhe o **papel ou modo de participação da IA no processo decisório**:

```text
tipo/contexto da decisão
  ↓
modo de participação da IA
  ↓
forma de interação e apoio
  ↓
decisão humana
```

Portanto, embora exista uma semelhança formal entre os dois padrões, **“escolher uma técnica analítica” e “escolher o modo de participação da IA” não são tratados como a mesma operação**. Fundi-los agora ampliaria o significado de “método” retrospectivamente e reduziria a precisão da taxonomia.

C3 deve, portanto, ser registrado como **caso de fronteira relacionado**, mas **não como ocorrência plena** do meta-padrão de seleção contextual do método.

Essa decisão segue o mesmo critério utilizado em outros casos de fronteira do laboratório: a semelhança estrutural é reconhecida, mas a ocorrência só é contabilizada quando o mecanismo e o nível funcional forem suficientemente equivalentes.

## Hipótese arquitetural futura — possível roteamento entre trilhas

C3 também deve ser acompanhado por uma hipótese adicional, ainda **não decidida**.

À medida que o laboratório acumular evidências, C3 pode deixar de ser apenas um modelo local da trilha Decision e eventualmente funcionar como um **mecanismo de roteamento entre trilhas funcionais**.

Hipótese:

```text
características do problema
        ↓
roteamento
        ├── Decision / racional
        ├── Prediction
        ├── julgamento intuitivo
        └── colaboração / outras trilhas
```

A hipótese não implica que essas trilhas sejam atualmente selecionadas automaticamente por C3. Ela apenas registra uma possibilidade arquitetural para futura avaliação.

Para eventual promoção dessa hipótese, será necessário observar evidência adicional de que C3:

1. seleciona ou direciona sistematicamente diferentes trilhas;
2. utiliza critérios explícitos para esse roteamento;
3. atravessa mais de um domínio funcional;
4. produz ganho arquitetural que não possa ser obtido mantendo C3 apenas como modelo de Decision.

**Não decidir agora.** O tema permanece como hipótese de evolução arquitetural futura.

## Princípio de autoridade decisória

C3 não atribui autoridade decisória à IA. A escolha do modo de participação serve para estruturar e ampliar o processo, mantendo a decisão sob responsabilidade humana.

## Exemplo de uso

### Decisão com dados disponíveis

Uma decisão predominantemente racional pode utilizar a IA para:

- analisar dados;
- construir previsões;
- comparar alternativas;
- explicitar premissas e riscos.

### Decisão com ausência de dados históricos

Como no caso da Aula 6.1:

- a IA estrutura o contexto;
- constrói cenários exploratórios;
- ajuda a explicitar riscos;
- explora a experiência e o julgamento do decisor;
- estimula colaboração com outras pessoas;
- não substitui a decisão do responsável.

## Critério de reutilização

C3 é reutilizável quando a principal necessidade não é simplesmente executar uma técnica analítica, mas **determinar de que maneira a IA deve participar do processo decisório em função da natureza da decisão e do contexto disponível**.
