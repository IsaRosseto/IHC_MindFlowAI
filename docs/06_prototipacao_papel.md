# Entrega 6 — Prototipação em papel

**Data:** {{18/10/2026}}  
**Status:** 🟩 Concluida
**Responsabilidade:** 1 solução integrada por equipe

## Objetivo da atividade

Externalizar rapidamente ideias de interação em baixa fidelidade para explorar alternativas antes de investir em detalhes visuais. O valor da atividade está no **ciclo construir → simular → observar → revisar**, não na beleza do desenho.


## 1. Escopo do protótipo

**Personas:** P01 – Karol Schrödinger, professora de ensino a distância, e P02 – Camila Duarte, professora de inglês em turmas pequenas.

**Cenários/tarefas cobertos:** o protótipo explora principalmente T01, relacionada à consulta e à personalização dos resultados de uma aula concluída. Esse recorte está associado à necessidade de revisão pós-aula derivada de C02, da persona P01. C05, da persona P02, também orienta a exploração da apresentação dos resultados.

As tarefas de acompanhamento durante a sessão, como T02, T03 e T05, ainda não possuem um fluxo completo representado. A configuração da extensão não substitui a prototipação do uso do indicador durante a videoconferência. T04, relacionada à participação e à transparência da análise, também não está coberta.

**Objetivos principais:**

- Explorar a localização de reuniões concluídas e o acesso aos seus resumos.
- Investigar a compreensão dos indicadores e gráficos apresentados.
- Experimentar alternativas de personalização das visualizações, cuja necessidade permanece como hipótese em investigação (H06).
- Explorar o acesso à ajuda e às explicações sobre os indicadores.

O acompanhamento em tempo real permanece como recorte principal do projeto, mas sua representação neste protótipo ainda é uma pendência.

## 1.1 Possíveis famílias de interface

Foram exploradas as seguintes famílias de interface:

- **Histórico:** localização de reuniões concluídas e acesso aos respectivos resumos.
- **Relatório/resultados:** apresentação dos indicadores e gráficos de uma reunião.
- **Dashboard:** visualização dos resultados de uma reunião e de informações consolidadas.
- **Configuração/personalização:** exploração da organização dos indicadores e das configurações da extensão.

O protótipo também contempla uma área de suporte. A ajuda contextual em pop-up é uma proposta de revisão decorrente do feedback recebido.

As interfaces de alertas durante a sessão e de participação na análise permanecem pendentes de prototipação.

## 2. Fluxos escolhidos

| Fluxo | Tarefa/objetivo | Por que foi priorizado |
|---|---|---|
| PF01 | Acompanhar os indicadores durante uma videoconferência. | Corresponde ao recorte central do projeto, mas ainda não está representado como fluxo completo. A tela de configuração da extensão oferece apenas cobertura preparatória. |
| PF02 | Localizar uma reunião concluída e consultar seus resultados. | Permite explorar o acesso ao resumo e a compreensão das informações apresentadas, apoiando a revisão pós-aula. |
| PF03 | Personalizar a apresentação dos indicadores e gráficos. | Permite investigar a hipótese H06. A existência dessa possibilidade no protótipo não confirma sua necessidade nem sua percepção como diferencial pelos usuários. |
| PF04 | Consultar o suporte e esclarecer o significado dos indicadores. | O participante relatou falta de explicação em alguns cards e sugeriu tornar a ajuda acessível nas diferentes telas. |

## 3. Telas e estados

O protótipo do MindFlow AI é composto por sete telas principais, que permitem ao usuário consultar reuniões, visualizar resultados, personalizar dashboards, configurar a extensão e acessar o suporte.

| Tela | Nome | Descrição | Controles e navegação |
|---|---|---|---|
| P01 | Home / Minhas Reuniões | Tela inicial que apresenta as reuniões do usuário e permite acessar os resultados de cada sessão. | Ao clicar em **Ver Resumo**, o usuário é direcionado para a tela P02. |
| P02 | Resumo da Reunião | Apresenta os resultados de uma reunião específica, incluindo gráficos e indicadores dos estados cognitivos dos participantes. | O botão **Nova Visualização** direciona o usuário para a tela P03. |
| P03 | Editar Resumo | Permite personalizar a visualização dos resultados de uma reunião específica, organizando as informações conforme as preferências do usuário. | O usuário pode realizar alterações na visualização e retornar ao resumo da reunião (P02). |
| P04 | Dashboard Geral | Apresenta uma visão consolidada dos indicadores e resultados das reuniões, permitindo acompanhar informações gerais. | O botão **Nova Visualização** direciona o usuário para a tela P05. |
| P05 | Edição do Dashboard Geral | Permite personalizar o Dashboard Geral, modificando a organização e a apresentação dos indicadores e gráficos. | O usuário pode realizar alterações e retornar ao Dashboard Geral (P04). |
| P06 | Editar Extensão | Permite acessar e modificar as configurações da extensão do MindFlow AI, adequando seu funcionamento às preferências do usuário. | Controles de configuração da extensão e navegação para as demais telas. |
| P07 | Suporte | Disponibiliza informações e orientações para auxiliar o usuário na utilização da plataforma. | Acesso às informações de ajuda e retorno às demais telas do sistema. |

### 3.1 Fluxos principais de navegação

**Fluxo 1 – Visualização e personalização do resumo de uma reunião**

P01 (Minhas Reuniões) → **Ver Resumo** → P02 (Resumo da Reunião) → **Nova Visualização** → P03 (Editar Resumo) → Retorno à P02.

**Fluxo 2 – Visualização e personalização do Dashboard Geral**

P04 (Dashboard Geral) → **Nova Visualização** → P05 (Edição do Dashboard Geral) → Retorno à P04.

**Fluxo 3 – Configuração da extensão**

P06 (Editar Extensão) → Acesso às opções de configuração → Alteração das preferências da extensão.

**Fluxo 4 – Acesso ao suporte**

P07 (Suporte) → Consulta às orientações e informações de ajuda → Retorno à navegação principal.

---

#### P01 – Home / Minhas Reuniões

Tela inicial do sistema, na qual o usuário visualiza suas reuniões e pode acessar os resultados de cada sessão por meio do botão **Ver Resumo**.

![P01 - Minhas Reuniões](../assets/06_prototipos/minhas%20reuni%C3%B5es.png)

*Figura 1 – Tela Home / Minhas Reuniões.*

#### P02 – Resumo da Reunião

Apresenta os indicadores e gráficos referentes a uma reunião específica, permitindo analisar os resultados e acessar a personalização por meio do botão **Nova Visualização**.

![P02 - Resumo da Reunião](../assets/06_prototipos/resumo%20reuni%C3%A3o.png)

*Figura 2 – Tela Resumo da Reunião.*

#### P03 – Editar Resumo

Permite personalizar a apresentação das informações de uma reunião, oferecendo ao usuário maior controle sobre a organização dos indicadores e gráficos.

![P03 - Editar Resumo](../assets/06_prototipos/edit%20resumo.png)

*Figura 3 – Tela de Edição do Resumo.*

#### P04 – Dashboard Geral

Apresenta uma visão consolidada dos resultados e indicadores das reuniões, facilitando o acompanhamento geral das informações.

![P04 - Dashboard Geral](../assets/06_prototipos/dash%20gerak.png)

*Figura 4 – Tela Dashboard Geral.*

#### P05 – Edição do Dashboard Geral

Permite modificar a organização e a apresentação dos indicadores do Dashboard Geral, destacando a personalização como um dos principais diferenciais do MindFlow AI.

![P05 - Edição do Dashboard Geral](../assets/06_prototipos/editar%20geral.png)

*Figura 5 – Tela de Edição do Dashboard Geral.*

#### P06 – Editar Extensão

Disponibiliza as opções de configuração e personalização da extensão utilizada pelo MindFlow AI durante as videoconferências.

![P06 - Editar Extensão](../assets/06_prototipos/extensao.png)

*Figura 6 – Tela de Edição da Extensão.*

#### P07 – Suporte

Apresenta informações de ajuda e orientações para auxiliar o usuário na utilização da plataforma e no esclarecimento de dúvidas.

![P07 - Suporte](../assets/06_prototipos/Captura%20de%20tela%202026-10-18%20210812.png)

*Figura 7 – Tela de Suporte.*
## 4. Simulação / walkthrough

A sessão formativa foi realizada presencialmente na faculdade com Beatriz Manaia, colega da equipe que não participou da elaboração das telas. Sua participação foi utilizada para identificar dúvidas e oportunidades de melhoria, sem substituir a avaliação posterior com os participantes finais do projeto. A data da sessão ainda precisa ser registrada.

Inicialmente, a equipe apresentou a finalidade do MindFlow AI e seu objetivo. Em seguida, a participante explorou livremente a interface. Durante a navegação, fez perguntas sobre a finalidade de elementos e funcionalidades, e a equipe respondeu às dúvidas conforme surgiam.

A sessão teve caráter exploratório, sem um roteiro estruturado de tarefas descrito no registro disponível. Não foram registrados o percurso completo, os tempos de execução ou as conclusões de tarefas sem ajuda. Também não foi detalhado o mecanismo utilizado 
Os achados abaixo correspondem aos comentários relatados e às dúvidas surgidas durante a exploração. As explicações fornecidas ppara representar as transições de tela e as respostas do sistema.
ela equipe devem ser consideradas na interpretação dos resultados, pois a compreensão após uma explicação não demonstra que a interface era compreensível de forma independente.

| Observação | Tela/ação | Evidência | Consequência para o design |
|---|---|---|---|
| A interface foi percebida como visualmente uniforme. | Cards dos dashboards e apresentação geral | A participante relatou pouca variedade de cores e uso de tons muito semelhantes. | Revisar a diferenciação e a hierarquia visual dos componentes, considerando cores, contraste e organização. |
| Algumas funções principais estavam pouco evidentes. | Acesso às ações nos dashboards | A participante relatou que determinados botões estavam escondidos ou pouco destacados. | Reorganizar os controles e destacar as ações necessárias para consultar e personalizar os resultados. |
| O significado de alguns cards não estava suficientemente explicado. | Leitura dos indicadores e exploração das funcionalidades | A participante perguntou sobre a finalidade de elementos da interface, e a equipe precisou explicar seus significados. | Acrescentar explicações nos cards e no suporte, reduzindo a dependência de orientação da equipe. |
| A ajuda poderia estar disponível durante a navegação. | Aba Suporte e demais telas | A participante sugeriu disponibilizar ajuda em formato de pop-up nas diferentes abas. | Permitir a consulta ao suporte sem abandonar a tela atual. |
| A possibilidade de personalizar os dashboards não estava suficientemente visível. | Acesso à edição das visualizações | A participante sugeriu destacar a possibilidade de modificar a apresentação dos dashboards conforme suas preferências. | Evidenciar os controles de personalização. Essa sugestão não confirma, por si só, a necessidade da funcionalidade ou a hipótese H06. |
| Faltava um recurso para registrar observações sobre as reuniões. | Revisão dos resultados após a aula | Foi sugerida a possibilidade de registrar anotações para evitar o esquecimento de acontecimentos relevantes. | Incluir anotações na revisão pós-aula, associadas à análise dos resultados. |
| A avaliação geral da proposta foi positiva. | Exploração geral da interface | A participante relatou ter gostado do sistema, apesar das sugestões de melhoria. | Preservar os elementos aproveitáveis e revisar os pontos identificados, sem interpretar a satisfação geral como comprovação de usabilidade. |

## 5. Alterações após a simulação

Conforme o relato da equipe, as melhorias planejadas após a sessão foram aplicadas ao protótipo. Para distinguir as etapas, a versão apresentada à participante é denominada V0, e a versão revisada após o feedback é denominada V1.

As alterações buscaram melhorar a compreensão das informações, a localização das funcionalidades e o apoio à análise dos resultados após a aula. Seus efeitos ainda precisam ser verificados em uma nova avaliação.

| Antes | Problema | Depois | Justificativa |
|---|---|---|---|
| Alguns cards apresentavam indicadores sem explicações complementares suficientes. | A participante precisava perguntar à equipe sobre o significado e a finalidade de determinados elementos. | Foram acrescentadas informações complementares no suporte e explicações resumidas ao passar o mouse sobre os cards. | Apoiar a compreensão dos indicadores durante a utilização, reduzindo a necessidade de explicações externas. |
| Os componentes utilizavam cores muito semelhantes. | A participante percebeu pouca diferenciação visual na interface. | As cores dos cards foram revisadas para diferenciar melhor as informações, respeitando o tema visual escolhido. | Explorar uma hierarquia visual mais clara. A adequação das cores e do contraste ainda deve ser avaliada. |
| Algumas ações principais estavam pouco destacadas. | As funcionalidades não eram facilmente percebidas. | A disposição e o destaque dos botões foram reformulados. | Facilitar a localização das ações necessárias ao objetivo do usuário. |
| A ajuda estava concentrada em uma aba específica. | A participante sugeriu consultar orientações sem precisar abandonar a tela atual. | Foi acrescentado suporte em formato de pop-up nas diferentes abas. | Disponibilizar ajuda durante a execução da atividade e preservar o contexto da navegação. |
| As opções de edição das visualizações tinham pouco destaque. | A possibilidade de modificar a apresentação dos resultados não estava clara. | Os controles de personalização e a apresentação das opções do dashboard foram reorganizados e destacados. | Tornar as possibilidades da interface mais compreensíveis. A necessidade de personalização permanece como hipótese em investigação (H06). |
| Não havia possibilidade de registrar anotações após a aula. | O usuário não dispunha desse recurso para registrar acontecimentos relevantes e consultá-los posteriormente. | Foi acrescentada a possibilidade de registrar anotações após a aula, no contexto da análise do gráfico temporal. | Apoiar a memória do docente e a contextualização dos resultados durante a revisão da sessão. |

## Checklist

- [ ] O protótipo cobre tarefas relevantes da Entrega 5 — cobre T01 e T02 (pós-sessão e personalização); T03/T05 (indicador durante a sessão) aparecem só na configuração da extensão e T04 (participante) ainda não tem tela.
- [x] Cada tela/estado pode ser justificado por uma tarefa, decisão ou informação necessária (T01 e T02; Suporte justificado pelo walkthrough).
- [x] O projeto não criou dashboard/CRUD/login apenas para parecer “completo” — os dashboards estão ligados a T01/T02 e à necessidade R03; a personalização segue como hipótese (H06).
- [x] Telas/estados estão numerados e navegáveis na documentação (P01–P07 e fluxos 1 a 4).
- [x] Há pelo menos uma simulação/walkthrough documentado (seção 4).
- [x] Críticas não foram apenas listadas: geraram decisão de revisão (seção 5).
- [ ] O protótipo continua em baixa fidelidade — as telas apresentadas são digitais e com acabamento visual próximo do final; a equipe deve registrar esse desvio ou anexar os esboços em papel usados antes.
