# Matriz de rastreabilidade de IHC

A matriz deve ser atualizada ao longo do semestre. Ela ajuda a demonstrar que a interface não surgiu arbitrariamente e registra **como o conhecimento da equipe evoluiu**.

Para projetos cujo TCC não previa interface, esta matriz é especialmente importante: deve ficar visível a passagem da **contribuição técnica do TCC** para um **cenário de uso plausível**, e desse cenário para as decisões de interação.

## 1. Derivação do escopo de IHC a partir do TCC

| Elemento | Registro da equipe | Evidência/justificativa | Estado |
|---|---|---|---|
| Tema do TCC | MindFlow AI, Classificação Temporal de Estados Cognitivos em Videoconferências utilizando Redes LSTM e Fusão Multimodal | Artigo do TCC1 | definido |
| Resultado técnico esperado | Sistema/aplicação interativa + modelo de IA/ML (LSTM multi-saída) | Artigo do TCC1, Seção IV | definido |
| O TCC previa interface? | sim | Entrega 1 de IHC, item 0.5 | definido |
| Capacidade/contribuição central | Classificar em tempo real e localmente no dispositivo o estado afetivo-cognitivo (engajamento, tédio, confusão, frustração) de participantes de uma videoconferência a partir da webcam | Entrega 1 de IHC, item 1.3 | definido |
| Possíveis beneficiários/stakeholders | Comunicador (professor/palestrante/facilitador), participante da videochamada, instituição/empresa que promove a sessão, encarregado de dados/DPO | Entrega 1 de IHC, itens 2.2 e 2.3 | H |
| Usuário escolhido para IHC | Comunicador | É quem efetivamente olha a interface e decide algo com base nela | H |
| Objetivo principal do usuário | Perceber em tempo real, sem tirar atenção da condução da sessão, se o grupo está engajado, entediado, confuso ou frustrado, pra agir enquanto ainda dá tempo | Entrega 1 de IHC, item 7.3 | H |
| Contexto de uso adotado | Aula remota/híbrida, treinamento corporativo, apresentação técnica, em notebook/desktop com webcam | Entrega 1 de IHC, item 5.1 e 5.2 | H |
| Interface/recorte de IHC | Semáforo Cognitivo em tempo real (foco principal) + Dashboard pós-sessão (recorte secundário) | Entrega 1 de IHC, item 7.4 | proposta |
| Relação com o TCC | parte prevista | Já descrita como requisito funcional na metodologia do TCC1, ainda não implementada | definido |

> Se o escopo de IHC mudar ao longo do semestre, preserve a decisão anterior no histórico e registre **qual evidência motivou a mudança**.

## 2. Registro de hipóteses e lacunas da Entrega 1

Use esta tabela para itens importantes marcados como `[H]` ou `[?]`. Preserve o histórico: não apague uma hipótese refutada.

| ID | Afirmação / dúvida inicial | Tipo | Por que importa | Como/onde investigar | Evidência obtida | Estado atual | Impacto no projeto |
|---|---|---|---|---|---|---|---|
| H01 | Professor/palestrante acha útil um indicador discreto do estado do grupo durante a própria aula, sem virar mais uma distração | H | Se for falsa, o semáforo precisa virar outra coisa, tipo só resumo pós-sessão | Entrega 2 / 3 | PENDENTE | aberta | Define se o recorte principal continua sendo o tempo real ou muda pro pós-sessão |
| H02 | O nível de confiança do modelo precisa aparecer na tela pra não deixar o comunicador confiar cegamente numa classificação errada | H | Muda como o dashboard e o semáforo mostram a informação | Entrega 7 / 8 | PENDENTE | aberta | Impacta diretamente o design visual do semáforo e do dashboard |
| H03 | Participante da chamada sentiria desconforto sabendo que o comportamento dele tá sendo classificado, mesmo com processamento local | H | Pode exigir tela de consentimento, ampliando o escopo além do comunicador | Entrega 2 / 4 | PENDENTE | aberta | Pode adicionar um novo perfil de usuário e uma nova tela ao escopo |
| H04 | O MindFlow se diferencia de ferramentas tipo Read AI justamente por atuar em tempo real e não só no pós-reunião | H | Se for falsa, o valor central do produto precisa ser repensado | Entrega 2 | PENDENTE | aberta | Sustenta (ou não) a escolha do trilho de tempo real como recorte principal de IHC |
| ? 01 | Quais outras ferramentas de meeting analytics/proctoring já existem além do Read AI, e o que elas fazem em tempo real | ? | Falta esse levantamento pra saber se o recorte escolhido é realmente diferenciado | Entrega 2 | PENDENTE | aberta | Pode confirmar ou enfraquecer a justificativa do Caminho A (item 7.1) |

## 3. Rastreabilidade entre contribuição técnica, necessidades e artefatos

| ID | Capacidade do TCC utilizada | Necessidade/problema | Persona | Cenário problema | Objetivo/tarefa | HTA/GOMS/CTT | Cenário de interação / signos | MoLIC | Tela(s) Figma | Heurística / problema | Tarefa no teste | Decisão/melhoria |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R01 | Classificação em tempo real do estado do grupo (engajamento, tédio, confusão, frustração) | Cegueira situacional do facilitador durante a sessão | PENDENTE | PENDENTE | T01, perceber o estado do grupo durante a sessão | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE |
| R02 | Agregação por janela temporal + alerta discreto (Semáforo Cognitivo) | Necessidade de ajustar a condução da aula/apresentação a tempo | PENDENTE | PENDENTE | T02, ajustar a condução da sessão em resposta ao estado percebido | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE |
| R03 | Persistência de representações reduzidas + timeline agregada | Falta de feedback estruturado sobre a própria condução, depois que a sessão já acabou | PENDENTE | PENDENTE | T03, revisar após a sessão quais momentos geraram mais dificuldade | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE |

## 4. Rastreabilidade de padrões de interface

Use esta tabela quando o projeto incorporar padrões como dashboard, relatório, histórico, filtros ou administração. O objetivo é **justificar o padrão**, não apenas listar telas.

| ID da tela/fluxo | Padrão de interface | Objetivo/tarefa que justifica | Informação/ação principal | Evidência de necessidade | Artefatos relacionados |
|---|---|---|---|---|---|
| F01 | alertas/ocorrências (Semáforo Cognitivo) | T01, perceber o estado do grupo em tempo real sem tirar a atenção da condução da sessão | Estado predominante do grupo (engajado/entediado/confuso/frustrado) em um alerta discreto e de leitura rápida | Entrega 1, itens 2.4 e 7.3 (comunicador tem atenção dividida) | R01/R02 |
| F02 | dashboard | T03, revisar após a sessão quais momentos tiveram mais dificuldade | Timeline de engajamento ao longo da sessão | Entrega 1, item 8 (Dashboard/visão geral marcado como "sim") | R03 |
| F03 | relatório/resultados | T03, consolidar o que aconteceu na sessão de forma resumida | Resumo dos estados predominantes e momentos críticos | Entrega 1, item 8 (Relatório/resultados marcado como "sim") | R03 |
| F04 | explicabilidade/detalhamento | Sustentar a confiança do comunicador na classificação, dado que o modelo ainda erra bastante em algumas dimensões | Justificativa de por que um momento foi classificado como "confuso" ou "frustrado" | Entrega 1, item 8 e hipótese H02 | H02 |

## 5. Registro de mudanças de escopo

| Data | O que mudou | Evidência/feedback que motivou | Artefatos afetados | Responsável |
|---|---|---|---|---|
| 13/08/2026 | Definição inicial do escopo de IHC: Semáforo Cognitivo em tempo real como recorte principal, Dashboard pós-sessão como secundário | Análise da Entrega 1 (entendimento do TCC, do usuário e do problema) | Toda a matriz (Seções 1, 2 e 4) | Equipe |

## Como usar

- Use identificadores estáveis (`H01`, `P01`, `C01`, `T01`, `M01`, `F01`, `UT01`).
- Quando uma necessidade/problema tiver origem em hipótese da Entrega 1, cite o ID correspondente.
- Em TCC sem interface original, pelo menos uma linha deve mostrar claramente **como uma capacidade técnica chega até uma tarefa de usuário e uma tela/fluxo**.
- Uma linha pode se desdobrar quando um objetivo possui múltiplos caminhos.
- Não force relação inexistente: se algo ainda não foi modelado, marque `PENDENTE`.
- Ao remover uma funcionalidade, registre a decisão em vez de apagar silenciosamente o histórico.
- Dashboard, CRUD, filtros e relatórios só devem aparecer quando houver objetivo/tarefa que os justifique.
