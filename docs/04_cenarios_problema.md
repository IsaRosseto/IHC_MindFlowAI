# Entrega 4 — Cenários de análise/problema

**Data:** {{30/08/2026}}  
**Status:** 🟨 iniciada  
**Responsabilidade:** 1 solução completa por integrante

## Objetivo da atividade

Descrever situações atuais em que o usuário tenta alcançar um objetivo e encontra dificuldades. O cenário de análise/problema deve tornar visível **o contexto, os atores, as ações e as rupturas**, sem antecipar a interface que será projetada.

> **Regra central:** cenário de problema é a “história do problema”. Se o texto já diz “o sistema mostra”, “o aplicativo resolve” ou descreve botões/telas futuras, provavelmente está misturando problema com solução.

Sempre que possível, o cenário deve aprofundar uma **situação concreta já registrada na Entrega 1**.

### Quando o TCC não possuía interface

O cenário continua sendo uma história de **problema/atividade humana**, não uma história do futuro sistema. Descreva como o profissional realiza hoje uma atividade semelhante ou como lida atualmente com dados, resultados, configurações, logs, decisões e limitações que o tema do TCC pretende apoiar.

Exemplo: em vez de “o DBA abre o novo dashboard e executa o algoritmo”, descreva “o DBA precisa investigar uma consulta lenta, reúne informações em ferramentas distintas, compara planos manualmente e tem dificuldade para estimar o impacto de uma mudança”.

A interface da disciplina aparecerá somente depois, nos cenários de interação.

Se o integrante escolher um novo problema/situação, explique por que ele passou a ser relevante e indique a evidência que motivou sua inclusão.

## Cenário C01 — Dificuldade em perceber o estado dos participantes durante uma aula on-line

**Autor(a):** {{Kayky Pires — 22.222.040-2}}  
**Persona(s) relacionada(s):** P01 - Karol 
**Necessidade relacionada:** {{R01}}  
**Situação concreta da Entrega 1 relacionada:** H01 — Utilidade de um indicador discreto do estado do grupo em tempo real 
**Hipóteses ainda presentes:** H01, H03

### 1. Cenário inicial

Durante uma aula por videoconferência, o professor precisa apresentar o conteúdo e, ao mesmo tempo, perceber como os alunos estão reagindo. Para isso, observa câmeras, chat, perguntas e reações da plataforma.

Porém, muitos participantes permanecem em silêncio, com poucas reações ou com a câmera desligada. Assim, o professor pode ter dificuldade para identificar se a turma está concentrada, desinteressada, confusa ou com dificuldade para acompanhar o conteúdo.

Essa incerteza dificulta a decisão sobre continuar a explicação, reduzir o ritmo, repetir um conteúdo ou mudar a dinâmica da aula.


### 2. Questões de refinamento

Use os tipos de questões/taxonomia definidos na aula. As perguntas devem revelar informações **ainda ausentes** do cenário, não repetir o que já foi respondido.


| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Quais informações o professor considera mais importantes para perceber se a turma está acompanhando a aula? | Ajuda a identificar quais sinais recebem maior atenção e como ocorre a tomada de decisão do docente. | Entrevista com professores e observação de aulas on-line. |
| Q2 | Em quais momentos da aula o professor sente maior dificuldade para acompanhar as reações dos participantes? | Permite compreender quando há maior sobrecarga de atenção e quais tarefas competem entre si. | Entrevista e observação contextual. |
| Q3 | Como o professor interpreta sinais diferentes ou contraditórios, como silêncio no chat e alunos aparentemente atentos pela câmera? | Ajuda a entender como os docentes atribuem significado aos sinais disponíveis e quais interpretações podem gerar dúvidas. . | Entrevista semiestruturada com docentes. |
| Q4 | Que estratégias o professor utiliza quando não consegue identificar se os alunos compreenderam o conteúdo? | Revela práticas reais adotadas para contornar a falta de informação durante a aula.| Observação de aulas e entrevista com professores. |
| Q5 | Como o número de participantes interfere na capacidade do professor de acompanhar a turma? | Permite compreender como o aumento de informações disponíveis influencia o esforço cognitivo e a atenção do docente. | Entrevista e comparação entre aulas com turmas de tamanhos diferentes. |

### 3. Cenário refinado

Reescreva o cenário incorporando as respostas. Marque o conteúdo novo de forma consistente (por exemplo, `**[NOVO: ...]**`).

Durante uma aula por videoconferência, o professor precisa apresentar o conteúdo e, ao mesmo tempo, perceber como os alunos estão reagindo. Para isso, observa câmeras, chat, perguntas e reações da plataforma.

`**[NOVO: O professor tende a considerar principalmente a participação no chat, as perguntas realizadas e as expressões visíveis dos alunos como sinais de acompanhamento da aula.]**`

Porém, muitos participantes permanecem em silêncio, apresentam poucas reações ou mantêm a câmera desligada. `**[NOVO: Essa dificuldade aumenta principalmente durante momentos em que o professor está explicando conteúdos mais complexos ou precisa dividir sua atenção entre apresentação, chat e participantes.]**`

Quando os sinais são pouco claros ou contraditórios, o professor pode ter dificuldade para identificar se a turma está concentrada, desinteressada, confusa ou com dificuldade para acompanhar o conteúdo.

`**[NOVO: Nesses momentos, o professor costuma fazer perguntas diretamente à turma, solicitar alguma interação ou repetir parte da explicação para tentar confirmar se o conteúdo foi compreendido.]**`

`**[NOVO: Em turmas maiores, acompanhar individualmente os participantes se torna ainda mais difícil, aumentando a quantidade de informações que o professor precisa observar simultaneamente.]**`

Essa incerteza dificulta a decisão sobre continuar a explicação, reduzir o ritmo, repetir um conteúdo ou alterar a dinâmica da aula.

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Professor responsável pela aula e alunos participantes da videoconferência. |
| Objetivo(s) | Compreender como os alunos estão reagindo e se estão acompanhando o conteúdo. |
| Contexto | Aula realizada por videoconferência, com o professor apresentando o conteúdo enquanto acompanha a participação da turma. |
| Recursos/informações | Câmeras, chat, perguntas, reações da plataforma e expressões dos participantes. |
| Ações | Observar os participantes, acompanhar o chat, fazer perguntas, solicitar interação e repetir explicações quando necessário. |
| Problemas/rupturas | Pouca participação, câmeras desligadas, sinais contraditórios, excesso de informações simultâneas e dificuldade maior em turmas grandes. |
| Consequências | Incerteza sobre o estado da turma e dificuldade para decidir se deve continuar, repetir, reduzir o ritmo ou alterar a dinâmica da aula. |



### 5. Implicações para as próximas entregas

Quais tarefas merecem análise? Quais informações precisam ser coletadas? **Não desenhe a solução ainda.**

**Quais tarefas merecem análise?** 
- Acompanhar as reações dos participantes enquanto conduz a aula. 
- Identificar sinais de dúvida, desinteresse, confusão ou dificuldade. 
- Observar simultaneamente chat, câmeras, perguntas e reações. 
- Decidir quando continuar, repetir ou adaptar a explicação. 
- Verificar se a turma compreendeu o conteúdo. 

**Quais informações precisam ser coletadas?** 
- Quais sinais os professores mais utilizam para avaliar a turma. 
- Em quais momentos da aula há maior dificuldade de acompanhamento. 
- Como o professor interpreta silêncio, pouca participação e sinais contraditórios. 
- Quais estratégias utiliza atualmente quando não consegue compreender o estado da turma. 
- Como essas dificuldades influenciam suas decisões durante a aula.

> Repita para C02, C03... com autoria individual.

## Checklist

- [ ] Há um cenário completo por integrante.
- [ ] Cada cenário tem título, ator, objetivo, contexto e problema.
- [ ] O cenário possui origem rastreável na Entrega 1 ou justifica claramente a inclusão de uma nova situação.
- [ ] O texto descreve a situação atual, sem antecipar a solução.
- [ ] Para TCC sem interface original, o cenário descreve uma prática humana plausível relacionada à contribuição técnica, e não “a falta de uma tela”.
- [ ] Questões de refinamento acrescentam informação nova.
- [ ] O refinamento mostra claramente o que foi adicionado/alterado.
- [ ] Cenários são diferentes o suficiente para cobrir objetivos/problemas relevantes.
- [ ] Cada cenário está ligado a persona/necessidade na matriz de rastreabilidade.
