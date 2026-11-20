# Entrega 10 — MoLIC

**Data:** {{dd/mm/aaaa}}  
**Status:** 🟨 em andamento  
**Responsabilidade:** 1 solução completa por integrante

## Objetivo da atividade

Modelar a interação como uma **conversa entre usuário e preposto do designer**, oferecendo visão global dos caminhos que permitem ao usuário atingir seus objetivos — incluindo alternativas e rupturas relevantes. MoLIC não deve ser reduzida a um fluxograma de telas.

> Use a **notação MoLIC ensinada na disciplina**. Este template foca critérios de qualidade e não substitui a legenda/notação apresentada em aula.

## Atenção a TCCs sem interface original

O MoLIC não modela o algoritmo por dentro. Ele modela a **conversa de interação necessária para que uma pessoa use a contribuição**.

Exemplos de conversas:

- usuário escolhe dados/parâmetros → sistema valida → usuário inicia análise → sistema comunica processamento → usuário interpreta resultado;
- usuário consulta histórico → refina filtros → abre execução → compara com outra;
- administrador seleciona perfil → altera permissão → sistema comunica consequências → administrador confirma/cancela;
- analista recebe alerta → examina evidências → classifica ocorrência → registra decisão.

Modele também rupturas plausíveis: entrada inválida, falha de processamento, ausência de resultado, permissão insuficiente, filtro sem resultados, conflito de alteração, cancelamento ou necessidade de recuperação.

## M05 — Acompanhar o estado da turma durante a explicação

**Autor(a):** Isabella Vieira Silva Rosseto — 22.222.036-0  
**Cenário de interação de origem:** CI05 (Entrega 9)  
**Objetivo(s):** O11 a O17 (Entrega 9, CI05)  
**Tarefa(s) relacionada(s):** T03  
**Signos relevantes:** acompanhamento da turma, participantes contribuindo, mínimo de participantes, estado predominante, confiança da estimativa, atualizado há, mudança de estado, qualidade do sinal, momento marcado, resumo da aula, aviso aos participantes

### Diagrama

```mermaid
flowchart TD
    A((" ")):::abertura
    P1[" "]:::proc
    S1("<b>Acompanhar o estado da turma</b><br/>――――――――――――――――<br/>ver estado da turma {<br/>d: estado predominante (cor, ícone, rótulo),<br/>confiança da estimativa, atualizado há }<br/>ver base da estimativa {<br/>d: participantes contribuindo (n de N) }"):::cena
    S4("<b>Entender por que não há estimativa</b><br/>――――――――――――――――<br/>ver motivo {<br/>d: motivo (câmeras, luz, conexão) }<br/>ver base da estimativa {<br/>d: participantes contribuindo, mínimo }"):::alerta
    P2[" "]:::proc
    S2("<b>Examinar a mudança no estado</b><br/>――――――――――――――――<br/>ver mudança {<br/>d: estado anterior, estado atual, desde quando }<br/>ver confiança {<br/>d: confiança, qualidade do sinal }"):::cena
    UA(["acesso ubíquo"]):::ubiquo
    S3("<b>Entender o significado da estimativa</b><br/>――――――――――――――――<br/>ver significado {<br/>d: o que o estado significa,<br/>o que a estimativa não indica }<br/>ver confiança { d: motivo da confiança }"):::cena
    P3[" "]:::proc
    UB(["acesso ubíquo"]):::ubiquo
    P4[" "]:::proc
    S5("<b>Acompanhamento pausado</b><br/>――――――――――――――――<br/>ver pausa {<br/>d: pausado desde, aviso aos participantes }"):::cena
    UC(["acesso ubíquo"]):::ubiquo
    P5[" "]:::proc
    S6("<b>Salvar o registro da aula</b><br/>――――――――――――――――<br/>ver falha {<br/>d: motivo da falha,<br/>dados mantidos no computador }"):::alerta
    BAR["gcc gcc gcc gcc gcc gcc gcc gcc gcc gcc"]:::barra
    E(((" "))):::fim

    A -->|"u: ativar o acompanhamento<br/>gco: Acompanhar o estado da turma"| P1
    P1 -->|"precond: câmeras suficientes<br/>d: acompanhamento ativo"| S1
    P1 -.->|"[SR] d: poucas câmeras ligadas para estimar"| S4
    S4 -.->|"u: tentar novamente"| P1
    S1 -->|"precond: nova janela de tempo"| P2
    P2 -->|"d: estado atualizado"| S1
    P2 -->|"precond: mudança relevante<br/>d: o estado da turma mudou"| S2
    P2 -.->|"[SR] d: sinal insuficiente"| S4
    S2 -->|"u: o que isso significa?"| S3
    S3 -->|"precond: veio do aviso<br/>u: voltar"| S2
    S3 -->|"precond: veio da ajuda<br/>u: voltar"| S1
    UA -->|"u: ajuda"| S3
    S2 -->|"u: marcar este momento"| P3
    P3 -->|"d: momento marcado"| S1
    S2 -->|"u: dispensar o aviso"| S1
    UB -->|"u: pausar acompanhamento"| P4
    P4 -->|"d: acompanhamento pausado<br/>d: participantes avisados"| S5
    S5 -->|"u: retomar o acompanhamento"| P1
    UC -->|"u: encerrar a aula"| P5
    P5 -->|"d: resumo salvo e disponível no Dashboard"| BAR
    P5 -.->|"[SR] d: falha ao salvar o resumo"| S6
    S6 -.->|"u: tentar novamente"| P5
    S6 -->|"u: tentar mais tarde"| BAR
    S4 -->|"u: continuar sem acompanhamento"| BAR
    BAR -->|"gcc: Acompanhar o estado da turma"| E

    classDef abertura fill:#111111,stroke:#111111
    classDef fim fill:#111111,stroke:#111111,stroke-width:3px
    classDef proc fill:#111111,stroke:#111111,color:#111111
    classDef cena fill:#ffffff,stroke:#111111,stroke-width:1.5px,color:#111111
    classDef alerta fill:#ffffff,stroke:#111111,stroke-width:1.5px,stroke-dasharray:6 4,color:#111111
    classDef ubiquo fill:#c4c4c4,stroke:#555555,color:#c4c4c4
    classDef barra fill:#111111,stroke:#111111,color:#111111,font-size:6px
```

**Versão em imagem** (mesmo diagrama, com posicionamento fixo): [PNG](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/10_molic/molic_m05.png) · [SVG editável](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/10_molic/molic_m05.svg)

Notação de Barbosa e Silva (2010), conforme o material da disciplina:

| Elemento | Representação no diagrama | No M05 |
|---|---|---|
| Ponto de abertura | círculo preto, com a fala do usuário e a abertura da conversa sobre a meta (`gco:`) | `u: ativar o acompanhamento` / `gco: Acompanhar o estado da turma` |
| Cena | retângulo de cantos arredondados; tópico em cima e diálogos embaixo, no formato `diálogo { d: signos }` | cinco cenas, como "Acompanhar o estado da turma" |
| Cena de alerta ou captura de erro | cena com borda tracejada | "Entender por que não há estimativa" e "Salvar o registro da aula" |
| Processo do sistema | retângulo preto pequeno, sem texto; o sistema decide o rumo da conversa, e as falas ficam nas saídas | verificar câmeras, atualizar a estimativa, registrar o momento, pausar, salvar o resumo |
| Fala de transição | seta com `u:` (usuário) ou `d:` (preposto do designer); `precond:` indica a condição | `u: marcar este momento`, `precond: mudança relevante` |
| Ruptura e recuperação | seta tracejada; `[SR]` marca a fala do preposto que leva à recuperação da ruptura | `[SR] d: sinal insuficiente`, `u: tentar novamente` |
| Acesso ubíquo | retângulo cinza sem texto, alcançável de qualquer cena; pode ser repetido no diagrama | `u: ajuda`, `u: pausar acompanhamento`, `u: encerrar a aula` |
| Fechamento da conversa | barra preta com `gcc:` e ponto de encerramento (círculo com centro preenchido) | `gcc: Acompanhar o estado da turma` |

### Leitura do diagrama

A meta do M05 é **acompanhar o estado da turma** durante a explicação. A decisão de reforçar o conteúdo fica fora da conversa: o preposto mostra o estado e a confiança da estimativa, e Camila decide o que fazer na aula, como prevê a CI05.

#### Caminho principal

1. **Abertura:** Camila diz `u: ativar o acompanhamento`, o que abre a conversa sobre a meta (`gco: Acompanhar o estado da turma`). O sistema verifica as câmeras.
2. Com `precond: câmeras suficientes`, o preposto responde `d: acompanhamento ativo` e a conversa vai para a cena **Acompanhar o estado da turma**. Nela, os diálogos "ver estado da turma" (estado predominante, confiança, atualizado há) e "ver base da estimativa" (participantes contribuindo) mostram o estado do grupo.
3. A cada `precond: nova janela de tempo`, o sistema atualiza a estimativa e volta à cena com `d: estado atualizado`.
4. Com `precond: mudança relevante`, o preposto diz `d: o estado da turma mudou`, e a conversa vai para **Examinar a mudança no estado** (estado anterior, estado atual, desde quando, confiança e qualidade do sinal).
5. Camila pode dizer `u: marcar este momento`. O sistema registra o momento e responde `d: momento marcado`, voltando ao acompanhamento. Ou pode dizer `u: dispensar o aviso` e voltar direto.
6. Pelo acesso ubíquo, `u: encerrar a aula` leva ao processo que salva o resumo. O preposto responde `d: resumo salvo e disponível no Dashboard`, a conversa é fechada (`gcc: Acompanhar o estado da turma`) e chega ao ponto de encerramento.

Caminhos alternativos:

- Em **Examinar a mudança no estado**, `u: o que isso significa?` leva à cena **Entender o significado da estimativa**. Ela também é alcançada pelo acesso ubíquo `u: ajuda`. A volta depende de onde Camila veio: `precond: veio do aviso / u: voltar` retorna à mudança, e `precond: veio da ajuda / u: voltar` retorna ao acompanhamento.
- Pelo acesso ubíquo, `u: pausar acompanhamento` leva ao processo de pausa. O preposto responde `d: acompanhamento pausado` e `d: participantes avisados`, e a conversa vai para **Acompanhamento pausado**. Dali, `u: retomar o acompanhamento` volta à verificação de câmeras.

#### Alternativas e rupturas

| Situação | Onde ocorre | Como o usuário percebe | Caminho de recuperação/saída |
|---|---|---|---|
| Poucas câmeras ligadas para estimar | Processo de verificação de câmeras, ao ativar | `[SR] d: poucas câmeras ligadas para estimar` e a cena de alerta "Entender por que não há estimativa", com o motivo, os participantes contribuindo e o mínimo | `u: tentar novamente` (nova verificação) ou `u: continuar sem acompanhamento` (fecha a conversa; a aula segue sem o MindFlow) |
| Sinal insuficiente no meio da aula (câmeras desligadas, luz, conexão) | Processo de atualização da estimativa | `[SR] d: sinal insuficiente` e a mesma cena de alerta | As mesmas saídas: tentar novamente ou continuar sem acompanhamento |
| Estimativa que parece errada para a professora | Cena "Examinar a mudança no estado" | Confiança e qualidade do sinal mostradas junto da mudança | `u: o que isso significa?` ou `u: dispensar o aviso` |
| Acompanhamento que atrapalha a aula | Qualquer cena | — | Acesso ubíquo `u: pausar acompanhamento`; depois retomar ou encerrar |
| Falha ao salvar o resumo da aula | Processo de salvar o resumo | `[SR] d: falha ao salvar o resumo` e a cena de alerta "Salvar o registro da aula", informando que os dados continuam no computador | `u: tentar novamente` (volta ao processo) ou `u: tentar mais tarde` (fecha a conversa sem perder os dados) |

### Checklist específico de modelagem

- [x] Existe **ponto de abertura** coerente com o início do objetivo (`u: ativar o acompanhamento` / `gco: Acompanhar o estado da turma`).
- [x] As **cenas de conversa** representam tópicos/assuntos, não nomes de páginas apenas.
- [x] As transições/falas deixam claro o que o usuário ou o sistema comunica.
- [x] Há **ponto(s) de encerramento** para objetivos concluídos/abandonados quando aplicável (barra `gcc:` alcançada pelo resumo salvo, por continuar sem acompanhamento ou por tentar mais tarde).
- [x] Processamentos do sistema estão representados conforme a notação adotada em aula, sem “inventar” fala do usuário (quadrados pretos; a atualização periódica entra no processo por `precond: nova janela de tempo`, sem fala de Camila).
- [x] Rupturas (breakdowns) relevantes têm feedback e caminho de recuperação, não becos sem saída (setas tracejadas com `[SR]` e cenas de alerta tracejadas).
- [x] Acessos ubíquos/atalhos só aparecem quando semanticamente justificáveis (ajuda, pausar e encerrar a aula, que Camila pode precisar em qualquer momento).
- [x] O diagrama cobre caminhos alternativos importantes, e não apenas o “happy path”.
- [x] Nomes de objetivos, tópicos e signos são coerentes com a Entrega 9.
- [x] O diagrama é legível em tamanho normal no GitHub.
- [x] O MoLIC representa a conversa usuário–sistema, não o fluxo interno do algoritmo (a estimativa aparece como um único processamento, sem detalhar o modelo).
- [x] Processamento, filtros, administração, relatórios e históricos incluem retornos/rupturas quando relevantes (falha ao salvar o resumo).

> Repita M01, M02... para os demais integrantes.

## Consolidação da equipe

### Cobertura dos objetivos

| Objetivo | MoLIC que cobre | Lacunas/duplicidades | Decisão |
|---|---|---|---|
| O11 Ativar o acompanhamento da turma | M05 | Deve se repetir nos MoLICs de Karol, Nathanael e Manoel | Manter um único objetivo na consolidação |
| O12 Perceber o estado da turma | M05 | Mesmo objetivo do comunicador nos outros cenários durante a sessão | Manter um único objetivo na consolidação |
| O13 Examinar uma mudança no estado | M05 | — | Manter |
| O14 Entender o significado e a confiança | M05 | Pode se sobrepor à ajuda contextual do Dashboard (F07) | Usar o mesmo texto de explicação nos dois lugares |
| O15 Marcar um momento para revisar depois | M05 | Liga com a revisão de aula concluída (T01/T02) | Conferir no MoLIC do Dashboard se o momento marcado aparece |
| O16 Pausar ou retomar o acompanhamento | M05 | Liga com a interface do participante (T04): o aviso muda quando pausa | Conferir no MoLIC do participante |
| O17 Encerrar a aula com o resumo salvo | M05 | — | Manter |

### Preparação para o Figma

Estados necessários a partir do M05:

- extensão com o acompanhamento desligado e o botão para ativar;
- verificação de câmeras em andamento;
- aviso de "não há participantes suficientes", com motivo, número de participantes, mínimo e as opções tentar novamente / continuar sem acompanhamento;
- Semáforo Cognitivo compacto durante o compartilhamento de tela, nos estados acompanhando, possível tédio, possível confusão, possível frustração e sem estimativa (cor + ícone + rótulo), com confiança, participantes contribuindo e "atualizado há";
- aviso de mudança de estado, com estado anterior e atual, desde quando, e as ações "o que isso significa?", "marcar este momento" e "dispensar";
- explicação do significado e da confiança da estimativa;
- confirmação de "momento marcado";
- acompanhamento pausado, com retomar e encerrar;
- confirmação de resumo salvo e aviso de falha ao salvar, com tentar novamente / tentar mais tarde;
- aviso exibido aos alunos quando o acompanhamento é ativado ou pausado (ligação com o MoLIC do participante).

## Erros frequentes a evitar

- desenhar apenas caixas com nomes de telas e setas de navegação;
- não modelar falhas, cancelamento, volta ou recuperação;
- usar rótulos genéricos (“Tela 1”, “Processo 2”) sem tópico de conversa;
- criar no Figma fluxos que não existem no MoLIC;
- diagrama sem legenda/fonte editável e com texto ilegível.
