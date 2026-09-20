# Arquitetura Estruturada de Prompt

## Objetivo

Modelo reutilizável para estruturar prompts destinados a tarefas complexas, reduzindo ambiguidades e organizando a interação com a LLM em etapas.

## Estrutura

1. **Definição da pergunta ou problema principal**
   - Delimitar claramente o que precisa ser resolvido.
   - Identificar o resultado esperado.

2. **Exemplos prévios (quando aplicável)**
   - Fornecer exemplos de entradas e saídas para orientar formato, lógica ou padrão esperado.
   - Quando não houver exemplos, a etapa pode ser omitida.

3. **Decomposição da tarefa**
   - Dividir problemas complexos em subtarefas manejáveis.
   - Definir uma sequência lógica de execução.

4. **Dados reais de entrada**
   - Inserir os dados, contexto e restrições necessários para a tarefa.

5. **Resposta estruturada**
   - Definir o formato esperado do resultado: tabela, lista, análise, campos específicos etc.

## Verificação e validação do output

Após a geração da resposta, verificar:

- se todas as subtarefas foram contempladas;
- se os dados fornecidos foram utilizados corretamente;
- se o formato solicitado foi respeitado;
- se cálculos, premissas e conclusões são coerentes;
- se existem lacunas, ambiguidades ou resultados que exigem validação adicional.

A validação deve ser tratada como etapa do processo, e não como uma atividade opcional posterior.

## Fluxo

**Problema → Exemplos (quando aplicável) → Decomposição → Dados → Resposta estruturada → Verificação/validação**

## Aplicabilidade

O modelo pode ser reutilizado em:

- tomada de decisão;
- análise de cenários;
- classificação;
- comparação;
- extração estruturada;
- análise de documentos;
- resolução de problemas lógicos;
- elaboração de relatórios.

## Origem

Derivado do conteúdo de engenharia de prompt estudado no curso, que apresenta a sequência de definição do problema, inserção de exemplos, decomposição, dados reais e geração de resposta estruturada. O material também identifica a validação de outputs como parte do processo de formulação e uso de prompts.

## Observação

Este é um modelo de arquitetura de prompt. Ele não pressupõe uma técnica específica de exposição do raciocínio interno do modelo; o foco é a **decomposição estruturada da tarefa e a definição de critérios verificáveis para o output**.
