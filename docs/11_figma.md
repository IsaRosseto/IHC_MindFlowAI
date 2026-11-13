# Entrega 11 — Protótipo no Figma

**Data:** {{dd/mm/aaaa}}  
**Status:** ⬜ não iniciada  
**Responsabilidade:** 1 protótipo integrado por equipe cobrindo os fluxos MoLIC. Se a turma exigir divisão individual, identifique o responsável por cada fluxo/tela.

## Objetivo da atividade

Materializar o modelo de interação em um protótipo navegável, preservando a lógica dos objetivos, tópicos, signos, feedbacks, alternativas e recuperações definidos anteriormente.

## Biblioteca de possibilidades para projetos técnicos

O protótipo deve materializar os fluxos definidos nas entregas anteriores. Dependendo do escopo, podem fazer sentido:

1. **Dashboard:** indicadores, alertas, estado, tendências e atalhos para tarefas frequentes.
2. **Configuração/parametrização:** escolhas, presets, validação e explicação de opções técnicas.
3. **Entrada de dados:** upload, conexão, seleção, pré-visualização e validação.
4. **Processamento:** fila, status, progresso, cancelamento, falha e reexecução.
5. **Relatório/resultados:** síntese, métricas, gráficos, explicação, exportação e compartilhamento.
6. **Histórico:** busca, filtros, ordenação, paginação, detalhes e repetição de execução.
7. **Comparação:** antes/depois, modelo A/B, execução A/B, baseline ou períodos.
8. **Explicabilidade:** confiança, fatores, evidências, limitações e correção/contestação.
9. **Administração:** usuários, grupos, perfis, permissões, integrações e políticas.
10. **CRUDs de domínio:** somente quando criar/consultar/editar/excluir representa tarefa real.
11. **Auditoria/logs:** histórico de alterações e eventos em linguagem adequada.
12. **Alertas/ocorrências:** severidade, impacto, ação, responsável e resolução.
13. **Ajuda/documentação:** apoio contextual a tarefas complexas.

### Estados que não podem ser esquecidos

Quando aplicável, considere: vazio/sem dados; carregamento/processamento; sucesso; erro de entrada; erro de processamento; filtro sem resultados; permissão insuficiente; confirmação de ação destrutiva; cancelamento/desfazer/recuperação; dados desatualizados/conflito.

> Esta lista é repertório de design, **não uma exigência de quantidade de telas**. A rastreabilidade deve explicar por que cada tela existe.

## Link do Figma

**Protótipo:** [{{MINDFLOW SITE}}](https://mindflowiaa.netlify.app/)  
**Arquivo editável:** {{URL}}  
**Última verificação de permissão:** {{dd/mm/aaaa}}

> Teste o link em janela anônima. O avaliador deve conseguir abrir o protótipo sem solicitar permissão.


## Cobertura MoLIC → Figma

| MoLIC | Objetivo | Fluxo/telas no Figma | Estados de erro/recuperação | Responsável |
|---|---|---|---|---|
| M01 — Selecionar, consultar e avaliar o resumo | O03 — Analisar os resultados de uma aula concluída. | F01 — Minhas Reuniões → Ver resumo → F02 — Resumo da Reunião. | F02V documenta o resumo sem leituras e as explicações dos cards. O usuário pode retornar a Minhas Reuniões. | Kayky Pires — 22.222.040-2 |
| M01 — Personalizar visualização | O01 — Personalizar a visualização do resumo da reunião. | F02 → Organizar dashboard → F03 — Editor de personalização → Salvar visualização. | F03E apresenta a validação do nome não preenchido. O cancelamento retorna diretamente ao resumo. F03C registra a confirmação de exclusão de uma visualização já salva. | Kayky Pires — 22.222.040-2 |
| M01 — Conferir resumo personalizado | O05 — Avaliar a adequação da visualização personalizada. | Após o salvamento, F02S apresenta a visualização selecionada e a confirmação de sucesso. Organizar dashboard permite acessar novamente o editor F03. | F02S documenta o retorno de sucesso. A reunião utilizada no print permanece sem leituras, independentemente do salvamento da configuração. | Kayky Pires — 22.222.040-2 |


## Catálogo de telas/estados

### F01: M01 — Minhas Reuniões

![F01 — Minhas Reuniões e acesso ao resumo](../assets/11_figma/ver_resumo.png)

**Objetivo do usuário:** localizar uma reunião concluída e acessar seus resultados pelo botão **Ver resumo**.  
**Signos principais:** título, data, duração, quantidade de participantes, situação da reunião e indicador de engajamento.  
**Origem no MoLIC:** contexto de acesso anterior ao ponto de abertura do M01, correspondente à solicitação `u: abrir resumo da reunião`.

### F02: M01 — Resumo da Reunião: estado sem dados (F02V)

![F02V — Resumo sem dados, explicação de card e acesso à personalização](../assets/11_figma/resumo%20inicial%20e%20organizar%20dash.png)

**Objetivo do usuário:** consultar os resultados da reunião, compreender os indicadores e identificar a possibilidade de personalizar sua apresentação.  
**Signos principais:** título e data da reunião, participantes, indicadores, explicações dos cards, disponibilidade de dados e visualização selecionada.  
**Origem no MoLIC:** M01 — cena **Consultar resumo da reunião**, relacionada a O03.

O registro apresenta as mensagens **“Sem reações neste intervalo”** e **“Sem leituras para esta reunião”**, além da explicação aberta do card de participantes. O botão **Organizar dashboard** permite iniciar a personalização.

### F03: M01 — Personalizar visualização

![F03 — Editor de organização do dashboard](../assets/11_figma/organiza%C3%A7%C3%A3o%20do%20dash.png)

**Objetivo do usuário:** escolher os blocos apresentados no resumo, definir sua organização e atribuir um nome à visualização.  
**Signos principais:** nome da visualização, blocos disponíveis, seleção de blocos e ordem de apresentação.  
**Origem no MoLIC:** M01 — cena **Personalizar visualização**, relacionada a O01.

O editor apresenta caixas de seleção, controles de ordenação e orientações para arrastar e redimensionar os blocos. As ações disponíveis incluem **Cancelar** e **Salvar visualização**.

### F03E: M01 — Validação: tentativa de salvar sem nome

![F03E — Mensagem de validação ao salvar sem nome](../assets/11_figma/erro%20salvar%20sem%20nome.png)

**Objetivo do usuário:** identificar o dado necessário para concluir o salvamento e corrigir a entrada.  
**Signos principais:** nome da visualização, seleção de blocos e mensagem **“Dê um nome para a visualização.”**  
**Origem no MoLIC:** detalhamento da validação associada à cena **Personalizar visualização** e à solicitação `u: salvar alterações`, a incorporar na revisão do M01.

Após a tentativa de salvamento sem nome, o editor permanece aberto com a seleção visível. A recuperação consiste em preencher o nome e solicitar novamente **Salvar visualização**. Esse estado representa um erro de entrada, distinto de uma falha técnica no salvamento.

### F02S: M01 — Visualização salva e aplicada

![F02S — Resumo após o salvamento da visualização](../assets/11_figma/visualiza%C3%A7%C3%A3o%20salva.png)

**Objetivo do usuário:** reconhecer que a visualização foi salva e conferir a configuração apresentada no resumo.  
**Signos principais:** nome da visualização selecionada, blocos apresentados e mensagem **“Visualização ‘dsa’ salva na sua conta.”**  
**Origem no MoLIC:** M01 — retorno de sucesso do processo de salvamento e cena **Conferir resumo personalizado**, relacionada a O01 e O05.

O editor está fechado, a visualização nomeada aparece selecionada e a mensagem confirma o salvamento. O usuário pode solicitar novos ajustes pelo botão **Organizar dashboard**. A reunião utilizada neste registro permanece sem leituras; salvar a configuração não altera a disponibilidade dos dados.

### F03C: M01 — Confirmação de exclusão de uma visualização salva

![F03C — Confirmação antes de excluir uma visualização salva](../assets/11_figma/info%20excluir%20visualiza%C3%A7%C3%A3o.png)

**Objetivo do usuário:** confirmar ou cancelar a exclusão de uma visualização salva.  
**Signos principais:** nome da visualização, mensagem **“Excluir a visualização ‘dsa’?”** e opções **OK** e **Cancelar**.  
**Origem no MoLIC:** ação adicional de gerenciamento de visualizações, cuja conversa de exclusão ainda precisa ser incorporada ao modelo de interação.

A confirmação é apresentada antes da exclusão. O registro evidencia a solicitação de confirmação, mas não apresenta o resultado após sua aceitação.

> Documente também estados que muitas equipes esquecem: carregamento, vazio, confirmação, sucesso, erro, permissão negada, cancelamento, desfazer/voltar quando aplicável.

## Sistema visual e consistência

| Elemento | Regra adotada | Justificativa |
|---|---|---|
| Tipografia | Uso de fonte sem serifa, títulos destacados e hierarquia entre nomes das telas, seções, rótulos e textos explicativos. | Facilitar a identificação das informações e a leitura dos resultados e das opções de personalização. |
| Cores | Tons de roxo destacam ações principais, como Organizar dashboard e Salvar visualização. A exclusão utiliza vermelho. Os indicadores e gráficos combinam cores com nomes, valores e legendas. | Diferenciar ações e informações, oferecendo identificação textual além da cor. A adequação do contraste ainda precisa ser verificada. |
| Componentes | Reutilização de menu lateral, cards, botões, campos de texto, seletores e caixas de seleção. O editor mantém os controles Cancelar e Salvar visualização próximos entre si e oferece botões de ordenação além da interação por arraste. | Preservar padrões reconhecíveis durante a navegação e facilitar a localização das ações de personalização. |
| Feedback | Mensagens textuais comunicam nome não preenchido, salvamento concluído e ausência de leituras. A exclusão de uma visualização salva apresenta uma confirmação. O cancelamento da edição retorna diretamente ao resumo. | Informar o resultado das ações, orientar a correção de entradas e permitir que o usuário confirme uma exclusão antes de realizá-la. |

## Verificação de acessibilidade básica

Para produto Web, considere critérios pertinentes da WCAG vigente (por exemplo, contraste, foco, tamanho de alvo, texto alternativo e navegação por teclado quando aplicáveis). Para outras plataformas, use as recomendações adequadas ao contexto.

## Checklist

- [ ] Link do Figma está acessível.
- [ ] Há screenshots representativos no repositório.
- [ ] Todos os MoLIC relevantes estão cobertos.
- [ ] Estados de erro, feedback e recuperação foram prototipados.
- [ ] Terminologia/signos são consistentes com Entrega 9.
- [ ] Componentes equivalentes se comportam de forma consistente.
- [ ] Fluxos críticos são clicáveis do início ao fim.
- [ ] O protótipo está pronto para inspeção e testes, sem “links mortos” nas tarefas avaliadas.
- [ ] Dashboards, relatórios, históricos, filtros, administração e CRUDs presentes possuem justificativa rastreável.
- [ ] Estados de vazio, processamento, erro e recuperação foram considerados quando pertinentes.
- [ ] Resultados técnicos são apresentados de forma interpretável para o perfil de usuário.
- [ ] A equipe distingue no protótipo o que é interação simulada e o que é funcionalidade técnica realmente integrada, quando necessário.
