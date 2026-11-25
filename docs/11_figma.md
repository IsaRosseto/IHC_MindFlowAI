# Entrega 11 — Protótipo no Figma

**Data:** {{dd/mm/aaaa}}  
**Status:** 🟨 em andamento  
**Responsabilidade:** 1 protótipo integrado por equipe, com identificação dos responsáveis por fluxo.

## Objetivo da atividade

Materializar o modelo de interação em um protótipo navegável, preservando a lógica dos objetivos, tópicos, signos, feedbacks, alternativas e recuperações definidos nas entregas anteriores.

O protótipo do MindFlow AI representa a interação do instrutor corporativo com a extensão durante um treinamento on-line, permitindo acompanhar os estados estimados do grupo por meio de um pop-up compacto ou expandido.

A interface apresenta os indicadores de engajamento, tédio, confusão e frustração. O instrutor pode visualizar os resultados resumidos ou expandir o pop-up para acompanhar a evolução dos indicadores em um gráfico de linhas.

## Link do Figma

**Protótipo:** {{URL_DO_PROTOTIPO}}  
**Arquivo editável:** {{URL_DO_FIGMA}}  
**Última verificação de permissão:** {{dd/mm/aaaa}}

> Os links serão preenchidos após a disponibilização do protótipo no Figma. O acesso deverá ser testado em janela anônima para garantir que o avaliador consiga visualizar as telas sem solicitar permissão.

## Cobertura MoLIC → Figma

---
O fluxo M04 corresponde ao acompanhamento dos estados do grupo durante um treinamento on-line, relacionado à persona P03 — Nathanael Lima.

**Responsável:** Rafael Dias — 22.222.039-4  
**Cenário de origem:** CI04 (Entrega 9)  
**MoLIC:** M04 — Acompanhar os estados do grupo durante o treinamento on-line.

| MoLIC | Objetivo | Fluxo/telas no Figma | Estados de erro/recuperação | Responsável |
|---|---|---|---|---|
| M04 | Iniciar a análise do estado do grupo | `F00 → F03 → F01` | `F04` | Rafael Dias |
| M04 | Acompanhar os indicadores do grupo durante o treinamento | `F01` | `F04` | Rafael Dias |
| M04 | Expandir o pop-up para visualizar todos os indicadores | `F01 → F02` | Retornar para `F01` | Rafael Dias |
| M04 | Recolher o pop-up expandido | `F02 → F01` | — | Rafael Dias |
| M04 | Consultar a evolução dos estados do grupo | `F02` | `F04` quando não houver dados disponíveis | Rafael Dias |
| M04 | Recuperar o acompanhamento após indisponibilidade | `F04 → F03 → F01` | Tentar novamente ou continuar sem análise | Rafael Dias |

**Observação:** F01 e F02 correspondem às interfaces apresentadas nas imagens do sistema. F00, F03 e F04 são estados complementares propostos para cobrir o fluxo do MoLIC e deverão ser representados no Figma.

---

O fluxo M05 corresponde ao acompanhamento da turma durante a explicação de um conteúdo novo, relacionado à persona P02 — Camila Duarte. Ele usa as mesmas telas da extensão do fluxo M04 (F00 a F04) e acrescenta os estados F05 a F08, que o M05 exige.

**Responsável:** Isabella Vieira Silva Rosseto — 22.222.036-0  
**Cenário de origem:** CI05 (Entrega 9)  
**MoLIC:** M05 — Acompanhar o estado da turma durante a explicação (Entrega 10).

| MoLIC | Objetivo | Fluxo/telas no Figma | Estados de erro/recuperação | Responsável |
|---|---|---|---|---|
| M05 | O11 — Ativar o acompanhamento da turma | `F00 → F03 → F01` | `F04` (poucas câmeras ligadas) | Isabella Rosseto |
| M05 | O12 — Perceber o estado da turma | `F01`, com `F02` para detalhes | `F04` (sinal insuficiente no meio da aula) | Isabella Rosseto |
| M05 | O13 — Examinar uma mudança no estado | `F01 → F05` | Dispensar o aviso e voltar para `F01` | Isabella Rosseto |
| M05 | O14 — Entender o significado e a confiança | `F05 → F06` (ou `F06` pela ajuda, de qualquer tela) | Voltar para `F05` ou `F01`, conforme a origem | Isabella Rosseto |
| M05 | O15 — Marcar o momento para revisar depois | `F05 → F01`, com a confirmação "momento marcado" | — | Isabella Rosseto |
| M05 | O16 — Pausar ou retomar o acompanhamento | `F01/F02 → F07 → F03 → F01` | — | Isabella Rosseto |
| M05 | O17 — Encerrar a aula com o resumo salvo | `F01/F02/F07 → F08` | `F08`, estado de falha: tentar novamente ou tentar mais tarde | Isabella Rosseto |

**Observação:** F01 e F02 existem nas imagens do sistema. F05 a F08 são estados propostos para cobrir o M05 e ainda precisam ser desenhados no Figma. As decisões de F01, F04 e F07 também respondem a problemas da minha avaliação heurística (Entrega 13): V10 (estado da turma em primeiro plano no modo compacto), V11 (mínimo de participantes) e V16 (pausar pelo pop-up).

---

## Catálogo de telas/estados

### F00 — Acompanhamento não iniciado

**Objetivo do usuário:** iniciar a análise dos estados do grupo durante o treinamento on-line.

**Descrição:** estado inicial proposto para a extensão, antes do início da análise. O usuário encontra o botão para iniciar o acompanhamento.

**Signos principais:**
- Acompanhamento da reunião;
- Estado da análise;
- Iniciar análise.

**Origem no MoLIC:** M04 — cena "Iniciar acompanhamento".

**Interações:**
- `u: iniciar análise` → F03.

**Estado:** proposto para o protótipo, ainda não representado nas imagens fornecidas.

### F01 — Pop-up compacto de acompanhamento

![F01 — Pop-up compacto](../assets/11_figma/f01_popup_compacto.png)

**Objetivo do usuário:** acompanhar rapidamente o estado predominante do grupo sem interromper o treinamento.

**Descrição:** o pop-up apresenta uma visualização reduzida dos resultados, permitindo identificar o estado predominante e acessar informações mais detalhadas.

Na imagem fornecida, a interface apresenta:
- Identificação do MindFlow AI;
- Conta conectada e opção de sincronização;
- Estado predominante: "Confusão alto";
- Indicador visual circular amarelo;
- Confiança da estimativa: 30%;
- Quantidade de fontes: 1 fonte;
- Controle para expandir o pop-up.

**Signos principais:**
- Estado predominante;
- Confiança da estimativa;
- Participantes ou fontes contribuindo;
- Acompanhamento da reunião;
- Expandir pop-up.

**Origem no MoLIC:** M04 — cena "Acompanhar estado do grupo".

**Interações:**
- `u: expandir pop-up` → F02;
- `u: recolher/manter visualização compacta` → permanece em F01;
- O sistema atualiza os indicadores conforme novos resultados ficam disponíveis.

**Feedback:** o estado predominante, a confiança e a quantidade de fontes informam ao usuário o resultado atual da análise e sua base.

### F02 — Pop-up expandido com gráfico de indicadores

![F02 — Pop-up expandido](../assets/11_figma/f02_popup_expandido.png)

**Objetivo do usuário:** visualizar os indicadores completos e acompanhar suas variações durante o treinamento.

**Descrição:** ao expandir o pop-up, o instrutor tem acesso a informações detalhadas sobre os estados do grupo.

Na imagem fornecida, a interface apresenta:
- Estado predominante "Confusão alto";
- Confiança da estimativa: 33%;
- Quantidade de fontes: 1 fonte;
- Engajamento: 40%;
- Tédio: 55%;
- Confusão: 56%;
- Frustração: 49%;
- Gráfico de linhas com os quatro indicadores;
- Referência temporal dos últimos cinco minutos;
- Identificação "AO VIVO";
- Informações sobre fontes anônimas detectadas;
- Informações técnicas sobre o processamento e a conexão.

O indicador de confusão apresenta o maior valor (56%), enquanto o engajamento apresenta o menor (40%).

O gráfico permite observar a evolução dos quatro estados ao longo do período exibido.

**Signos principais:**
- Estado predominante;
- Valor dos indicadores;
- Engajamento;
- Tédio;
- Confusão;
- Frustração;
- Variação dos indicadores;
- Período analisado;
- Confiança da estimativa;
- Fontes contribuindo;
- Estado de atualização.

**Origem no MoLIC:** M04 — cena "Examinar todos os estados".

**Interações:**
- `u: recolher pop-up` → F01;
- O sistema atualiza os valores e o gráfico durante o acompanhamento.

**Feedback:** os cartões numéricos permitem comparar os indicadores, enquanto o gráfico apresenta sua evolução no tempo.

### F03 — Iniciando análise

**Objetivo do usuário:** compreender que o sistema está processando o início do acompanhamento.

**Descrição:** estado de carregamento proposto para o período entre o acionamento da análise e a apresentação dos primeiros resultados.

**Signos principais:**
- Estado da análise;
- Processamento;
- Disponibilidade de dados.

**Origem no MoLIC:** M04 — processo de início da análise.

**Interações:**
- `d: análise iniciada` → F01;
- `d: análise indisponível` → F04.

**Feedback:** mensagem indicando que o sistema está iniciando a análise.

**Estado:** proposto para o Figma, ainda não representado nas imagens fornecidas.

### F04 — Análise indisponível ou dados insuficientes

**Objetivo do usuário:** compreender por que não existem resultados e conseguir continuar a atividade.

**Descrição:** estado de erro ou indisponibilidade apresentado quando o sistema não consegue obter dados suficientes para realizar a análise.

**Signos principais:**
- Disponibilidade de dados;
- Estado da análise;
- Motivo da indisponibilidade;
- Fontes contribuindo.

**Origem no MoLIC:** M04 — cena de ruptura "Entender ausência de resultados".

**Interações:**
- `u: tentar novamente` → F03;
- `u: continuar sem análise` → encerra o acompanhamento, permitindo continuar o treinamento.

**Feedback:** mensagem informando que não foi possível apresentar os indicadores.

**Recuperação:** possibilidade de tentar iniciar novamente ou continuar o treinamento sem os resultados do MindFlow AI.

**Estado:** proposto para o Figma para cobrir a ruptura definida no MoLIC.

---

### F05 — Aviso de mudança no estado da turma

**Responsável:** Isabella Rosseto (M05)

**Objetivo do usuário:** perceber que o estado da turma mudou sem tirar a atenção da explicação.

**Descrição:** aviso discreto dentro do pop-up compacto, que aparece quando o estado predominante muda por tempo suficiente. Mostra o estado anterior, o atual, desde quando e a confiança. Não sugere o que a professora deve fazer (RC03), e aparece um aviso por vez, sem acumular avisos antigos (RC06).

**Signos principais:** mudança de estado; estado predominante; confiança da estimativa; participantes contribuindo.

**Origem no MoLIC:** M05 — cena "Examinar a mudança no estado".

**Interações:**
- `u: o que isso significa?` → F06;
- `u: marcar este momento` → confirmação "Momento marcado aos 23 min" → F01;
- `u: dispensar o aviso` → F01.

**Estado:** proposto para o Figma.

### F06 — Significado e confiança da estimativa

**Responsável:** Isabella Rosseto (M05)

**Objetivo do usuário:** entender o que o estado significa e quanto confiar nele.

**Descrição:** painel curto, aberto a partir do aviso ou pela ajuda, que explica o estado em linguagem simples ("parte da turma mostra sinais associados a dificuldade"), o que a estimativa não indica (não avalia alunos individualmente) e por que a confiança está alta, média ou baixa.

**Signos principais:** significado do indicador; confiança da estimativa; qualidade do sinal.

**Origem no MoLIC:** M05 — cena "Entender o significado da estimativa"; acesso ubíquo `u: ajuda`.

**Interações:**
- `u: voltar` → F05 (quando veio do aviso) ou F01 (quando veio da ajuda).

**Estado:** proposto para o Figma.

### F07 — Acompanhamento pausado

**Responsável:** Isabella Rosseto (M05)

**Objetivo do usuário:** interromper o acompanhamento rapidamente, sem sair da videochamada.

**Descrição:** o pop-up mostra que o acompanhamento está pausado desde determinado horário e que os participantes foram avisados. O botão "Pausar acompanhamento" fica visível em F01 e F02.

**Signos principais:** acompanhamento (ativo, pausado ou desligado); aviso aos participantes.

**Origem no MoLIC:** M05 — acesso ubíquo `u: pausar acompanhamento` e cena "Acompanhamento pausado".

**Interações:**
- `u: retomar o acompanhamento` → F03;
- `u: encerrar a aula` → F08.

**Estado:** proposto para o Figma.

### F08 — Encerramento da aula: resumo salvo ou falha ao salvar

**Responsável:** Isabella Rosseto (M05)

**Objetivo do usuário:** saber que a aula ficou registrada para revisar depois.

**Descrição:** ao encerrar, o pop-up confirma "Resumo salvo — disponível no Dashboard". Se o salvamento falhar, mostra o motivo, informa que os dados continuam no computador e oferece duas saídas.

**Signos principais:** resumo da aula; momento marcado.

**Origem no MoLIC:** M05 — processo de encerramento, fechamento da conversa (`gcc`) e cena de alerta "Salvar o registro da aula".

**Interações:**
- `d: resumo salvo` → fim do acompanhamento;
- `d: falha ao salvar` → `u: tentar novamente` (novo salvamento) ou `u: tentar mais tarde` (encerra sem perder os dados).

**Estado:** proposto para o Figma.

---

## Sistema visual e consistência

O sistema visual segue a identidade apresentada nas interfaces da extensão MindFlow AI, priorizando uma visualização compacta e objetiva para utilização durante videoconferências.

| Elemento | Regra adotada | Justificativa |
|---|---|---|
| Tipografia | Fonte sem serifa, com títulos em destaque e textos auxiliares menores. | Facilitar a leitura e organizar as informações em uma interface compacta. |
| Cores | Cabeçalho azul-escuro, fundo claro, cartões em tons suaves e cores distintas para os indicadores. | Criar hierarquia visual e permitir diferenciar os estados do grupo. |
| Componentes | Pop-up compacto, cartões de indicadores, botões, gráfico de linhas e mensagens de status. | Manter consistência entre a visualização resumida e a expandida. |
| Feedback | Estado predominante, confiança, fontes contribuindo e indicação de atualização ao vivo. | Comunicar o resultado e o contexto da estimativa durante o acompanhamento. |
| Navegação | Controle de expansão e recolhimento do pop-up. | Permitir alternar entre uma consulta rápida e uma visualização detalhada sem interromper o treinamento. |
| Gráficos | Linhas distintas para engajamento, tédio, confusão e frustração, acompanhadas de legenda. | Permitir acompanhar a evolução dos estados e comparar seus valores. |
| Mensagens de erro | Mensagem textual acompanhada de opção de recuperação. | Evitar que o usuário fique sem orientação quando a análise estiver indisponível. |

### Consistência entre os estados

- A visualização compacta e a expandida apresentam informações referentes à mesma análise.
- O estado predominante deve corresponder aos indicadores disponíveis no momento.
- Os nomes dos indicadores devem permanecer consistentes entre os cartões e o gráfico.
- O usuário pode expandir ou recolher o pop-up sem reiniciar a análise.
- As atualizações não devem alterar automaticamente o modo de visualização selecionado.
- A ausência de dados não deve ser apresentada como um indicador com valor zero.
- Os indicadores são estimativas do estado do grupo, não avaliações individuais de aprendizagem.

---

## Verificação de acessibilidade básica

A interface deve considerar critérios pertinentes da WCAG para melhorar a acessibilidade e a compreensão das informações.

| Critério | Aplicação no protótipo | Verificação |
|---|---|---|
| Contraste | Manter contraste adequado entre textos, cartões e fundo. | Pendente de validação das combinações de cores. |
| Uso de cores | Não depender exclusivamente de cores para diferenciar os indicadores. | Associar cores aos nomes e valores dos estados. |
| Legibilidade | Priorizar textos legíveis no tamanho reduzido do pop-up. | Verificar especialmente os textos auxiliares e informações técnicas. |
| Navegação por teclado | Permitir acessar os controles de iniciar, expandir e recolher. | Pendente de simulação e validação. |
| Foco visível | Destacar o controle selecionado durante a navegação por teclado. | Pendente de prototipação. |
| Identificação dos controles | Utilizar nomes compreensíveis para os botões e ações. | Verificar os controles de expansão, sincronização e início da análise. |
| Compreensão dos resultados | Apresentar nomes, valores e contexto das estimativas. | Parcialmente contemplado nas interfaces fornecidas. |

**Observação:** as imagens demonstram a organização visual da extensão, mas não comprovam, isoladamente, conformidade com os critérios de acessibilidade. A navegação e os estados de foco deverão ser verificados no protótipo.
---

## Checklist

- [ ] Link do Figma está acessível.
- [ ] Há screenshots representativos no repositório.
- [ ] As duas interfaces principais do acompanhamento foram identificadas.
- [ ] O fluxo principal do MoLIC M04 foi mapeado para as telas.
- [ ] Os estados de carregamento, erro e recuperação foram prototipados no Figma.
- [ ] A terminologia dos indicadores está relacionada à Entrega 9.
- [ ] A navegação entre pop-up compacto e expandido foi definida.
- [ ] Os fluxos críticos estão clicáveis do início ao fim no Figma.
- [ ] O protótipo está pronto para inspeção e testes sem links mortos.
- [ ] Os indicadores e o gráfico possuem justificativa relacionada ao objetivo do usuário.
- [ ] Os estados de processamento, indisponibilidade e recuperação foram considerados.
- [ ] Os resultados técnicos são apresentados por conceitos compreensíveis ao instrutor.
- [ ] Os estados propostos foram diferenciados das interfaces já apresentadas.
- [ ] A acessibilidade básica foi verificada no protótipo navegável.
- [ ] A cobertura dos demais diagramas MoLIC da equipe foi consolidada (M04 e M05 mapeados; faltam M01, M02 e M03).

**Observação final:** esta documentação representa a contribuição individual de Rafael para a Entrega 11. A conclusão da entrega depende da integração dos demais fluxos da equipe, da criação dos estados complementares no Figma e da validação dos links de acesso.
