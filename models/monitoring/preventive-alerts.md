# Candidato 19 — Alertas preventivos

## Status

**Candidato formal aprovado para criação.**

## Problema

Monitoramento identifica estados e desvios, mas uma aplicação de IA pode precisar transformar um indicador em um aviso antecipado que dispare uma ação preventiva antes que o desvio se agrave.

## Padrão

```text
Indicador
   ↓
Valor atual
   ↓
Limite / threshold
   ↓
Condição de disparo
   ↓
Alerta preventivo
   ↓
Ação preventiva
```

## Evidência de origem

Na Aula 3.3, o material estrutura o uso de alertas a partir de indicadores, valores atuais, limites/thresholds e condições de disparo, associando o alerta a uma ação preventiva.

Os exemplos apresentados tratam o alerta como mecanismo intermediário entre o acompanhamento de um indicador e a resposta operacional.

## Entradas

- indicador a ser acompanhado;
- valor ou estado atual;
- limite, faixa ou condição relevante;
- contexto da operação;
- ação preventiva associada.

## Processo

1. Definir o indicador relevante.
2. Obter ou calcular seu estado atual.
3. Comparar o estado com o limite ou condição estabelecida.
4. Verificar se a condição de disparo foi satisfeita.
5. Emitir o alerta.
6. Associar o alerta à ação preventiva definida.

## Saída

Um alerta contextualizado, acionado quando uma condição previamente definida é atingida, com indicação da resposta preventiva correspondente.

## Característica reutilizável

O padrão pode ser aplicado a diferentes contextos de monitoramento, desde que exista:

- um indicador observável;
- uma condição de disparo;
- um limiar ou regra verificável;
- uma resposta preventiva definida.

## Distinção em relação ao Candidato 18

O Candidato 18 trata do **monitoramento contínuo e da detecção de desvios**.

O Candidato 19 trata da **transformação de uma condição monitorada em alerta preventivo e ação associada**.

Assim:

```text
C18 — acompanhar / detectar
          ↓
C19 — alertar preventivamente
          ↓
ação
```

Os componentes podem ser compostos, mas não representam o mesmo mecanismo.

## Limitações

- Um threshold inadequado pode produzir alertas excessivos ou insuficientes.
- Nem todo indicador possui uma relação simples entre desvio e ação preventiva.
- O mecanismo depende da definição prévia das condições de disparo e das respostas associadas.
- O material de origem demonstra o padrão em contextos específicos; sua generalização para outros domínios deve ser validada.

## Relação com outras trilhas

O candidato pertence à área funcional **Monitoring**, mas pode alimentar **Action**, **Diagnosis** ou outras etapas quando o alerta exigir resposta posterior.

Nenhuma integração com o ORCHESTRATOR CORE é presumida.
