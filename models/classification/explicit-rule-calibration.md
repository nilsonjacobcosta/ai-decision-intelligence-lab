# Candidato 23 — Calibração de classificação por regras explícitas

## Status

**Candidato formalizado em `models/classification/`.**

## Objetivo

Aumentar a consistência de tarefas de classificação realizadas pela IA quando as categorias possuem fronteiras semânticas, ambiguidades ou casos-limite.

O padrão transforma uma instrução genérica de classificação em um mecanismo calibrado por **categorias explícitas, referências, exemplos e regras de interpretação**.

## Problema que resolve

Classificações qualitativas podem ser interpretadas de maneira inconsistente quando a IA recebe apenas os nomes das categorias.

Isso é especialmente relevante quando:

- uma palavra positiva aparece em uma frase negativa;
- há negações;
- existem modificadores de intensidade;
- uma frase contém sentimentos ou atributos duplos;
- a classificação depende do contexto predominante.

## Padrão

```text
Definição das categorias
        ↓
Exemplos e referências
        ↓
Regras para casos-limite
        ↓
Classificação
        ↓
Verificação dos resultados
        ↓
Recalibração, se necessária
```

## Mecanismos de calibração

### 1. Categorias explícitas

Definir previamente as classes que a IA deverá utilizar.

No exemplo da Aula 4.2:

- positivo;
- neutro;
- negativo.

### 2. Tabela de referência

Fornecer exemplos de frases e palavras-chave associadas a cada categoria.

A referência funciona como orientação para reduzir interpretações inconsistentes.

### 3. Regras para negações

Explicitar que uma palavra normalmente positiva pode mudar de polaridade quando precedida por uma negação.

Exemplo:

- “satisfeito” → positivo;
- “não fiquei satisfeito” → negativo.

### 4. Tratamento de modificadores

Considerar expressões como “um pouco”, “mais ou menos” e “talvez”, que podem reduzir a intensidade da classificação.

### 5. Tratamento de sentimentos duplos

Quando uma frase contém aspectos positivos e negativos, utilizar o contexto predominante da experiência para determinar a classificação.

## Processo

1. Definir as categorias de saída.
2. Fornecer exemplos representativos de cada categoria.
3. Criar uma referência lexical ou semântica adequada ao domínio.
4. Explicitar regras para negações, modificadores e casos-limite.
5. Executar a classificação.
6. Examinar a distribuição e os resultados obtidos.
7. Ajustar referências ou regras quando o resultado não estiver suficientemente calibrado.

## Saída

Uma classificação estruturada e acompanhada, quando aplicável, de contagens, distribuições e visualizações que permitam verificar o comportamento do classificador.

## Evidência de origem

Na Aula 4.2 — Identificando sentimentos nos feedbacks, o material destaca que a classificação de comentários em positivo, neutro e negativo precisa ser calibrada para reduzir erros. O prompt utiliza uma tabela de referência com exemplos e palavras-chave e estabelece regras específicas para negações, modificadores e sentimentos duplos.

A aula também orienta a ajustar palavras e o prompt quando o resultado não for o esperado, reforçando o caráter iterativo da calibração.

## Relação com outros candidatos

### Candidato 9 — calibração/restrição proativa por regras explícitas

O Candidato 23 compartilha com o Candidato 9 o princípio transversal de estabelecer **regras e restrições explicitamente antes da operação principal**, reduzindo a liberdade interpretativa da IA.

A finalidade, entretanto, é diferente:

- Candidato 9: guardrails aplicados ao comportamento/resultado de previsão;
- Candidato 23: calibração das regras de classificação e tratamento de ambiguidades.

### Candidato 12 — validação crítica da saída

O Candidato 12 atua **reativamente**, depois que uma saída foi produzida: questiona resultados inesperados e pode solicitar recalibração.

O Candidato 23 atua **proativamente**, definindo referências e regras antes da classificação e podendo recalibrá-las com base na avaliação dos resultados.

Portanto, os dois mecanismos são complementares e não devem ser fundidos.

## Limitações

- As referências e palavras-chave dependem do domínio.
- Regras lexicais não resolvem sozinhas todas as ambiguidades semânticas.
- A classificação deve ser avaliada pelos resultados; a existência de regras explícitas não garante, por si só, correção.
- A aplicação a outras tarefas de classificação deverá ser validada em contextos adicionais.

## Origem

Derivado da Aula 4.2 — Identificando sentimentos nos feedbacks.
