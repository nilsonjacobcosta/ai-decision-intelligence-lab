# Few-Shot Prompting

## Objetivo

Técnica reutilizável de orientação de uma LLM por meio do fornecimento de exemplos prévios de entradas e saídas esperadas.

## Conceito

Em vez de apenas descrever a tarefa, o prompt apresenta alguns exemplos que demonstram o padrão que a LLM deve seguir.

**Estrutura básica:**

**Instrução → Exemplos de entrada/saída → Novo caso → Resposta no padrão esperado**

## Quando utilizar

A técnica é especialmente útil quando é necessário orientar:

- formato específico de resposta;
- padrão de classificação;
- estilo ou estrutura de saída;
- transformação de dados;
- regras que são difíceis de descrever apenas por texto;
- tarefas em que exemplos concretos tornam o resultado esperado mais claro.

## Como aplicar

1. Defina claramente a tarefa.
2. Selecione exemplos representativos.
3. Apresente cada exemplo com entrada e saída esperada.
4. Mantenha os exemplos consistentes entre si.
5. Apresente o novo caso a ser processado.
6. Verifique se a resposta segue o padrão demonstrado.

## Cuidados

- Os exemplos devem ser relevantes para a tarefa.
- Exemplos inconsistentes podem induzir padrões incorretos.
- Poucos exemplos não garantem correção em todos os casos.
- O output continua sujeito à validação.

## Relação com outras técnicas

O Few-Shot pode ser combinado com uma arquitetura estruturada de prompt, especialmente quando exemplos são necessários para orientar o formato ou a lógica da tarefa.

## Origem

O material estudado define Few-Shot como a técnica de fornecer alguns exemplos prévios de entradas e saídas dentro do prompt para ensinar o padrão desejado à LLM.
