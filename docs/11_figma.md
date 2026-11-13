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

**Protótipo:** {{URL}}  
**Arquivo editável:** {{URL}}  
**Última verificação de permissão:** {{dd/mm/aaaa}}

> Teste o link em janela anônima. O avaliador deve conseguir abrir o protótipo sem solicitar permissão.

## Cobertura MoLIC → Figma

| MoLIC | Objetivo | Fluxo/telas no Figma | Estados de erro/recuperação | Responsável |
|---|---|---|---|---|
| M01 — Consultar resumo da reunião | O03 — Analisar os resultados de uma aula concluída. | F01 — Minhas Reuniões → **Ver resumo** → F02 — Resumo da Reunião. A interface apresenta identificação da reunião, indicadores, gráficos e explicações dos cards. | F02V — Resumo sem dados: apresenta mensagens como “Sem leituras para esta reunião” e “Sem reações neste intervalo”. Estado registrado nas imagens. | Kayky Pires — 22.222.040-2 |
| M01 — Personalizar visualização | O01 — Personalizar a visualização do resumo da reunião. | F02 → **Organizar dashboard** → F03 — Editor de personalização. Permite nomear a visualização, selecionar blocos, reorganizar e redimensionar os elementos. Apresenta os controles **Cancelar** e **Salvar visualização**. | Os controles estão evidenciados. A confirmação de descarte de alterações não salvas e a recuperação de falha no salvamento ainda precisam ser verificadas e documentadas. | Kayky Pires — 22.222.040-2 |
| M01 — Conferir resumo personalizado | O05 — Avaliar a adequação da visualização personalizada. | Fluxo previsto: F03 → **Salvar visualização** → F02S — Resumo com a configuração aplicada. A conferência ocorre na própria tela de resumo, com possibilidade de acessar novamente **Organizar dashboard**. | A aplicação da configuração, a mensagem de sucesso e o retorno para novos ajustes ainda precisam de evidência após o salvamento. | Kayky Pires — 22.222.040-2 |

## Catálogo de telas/estados

## Catálogo de telas/estados

### F01 — Minhas Reuniões

![F01 — Minhas Reuniões e acesso ao resumo](../assets/11_figma/ver_resumo.png)

**Objetivo do usuário:** localizar uma reunião concluída e acessar seus resultados pelo botão **Ver resumo**.  
**Signos principais:** título, data, duração, quantidade de participantes, situação da reunião e indicador de engajamento.  
**Origem no MoLIC:** contexto de acesso anterior ao ponto de abertura do M01, correspondente à solicitação `u: abrir resumo da reunião`.

### F02 — Resumo da Reunião: estado sem dados (F02V)

![F02V — Resumo sem dados, explicação de card e acesso à personalização](../assets/11_figma/resumo%20inicial%20e%20organizar%20dash.png)

**Objetivo do usuário:** consultar os resultados da reunião, compreender os indicadores e identificar a possibilidade de personalizar sua apresentação.  
**Signos principais:** título e data da reunião, participantes, indicadores, explicações dos cards, disponibilidade de dados e visualização selecionada.  
**Origem no MoLIC:** M01 — cena **Consultar resumo da reunião**, relacionada a O03.

O registro apresenta as mensagens **“Sem reações neste intervalo”** e **“Sem leituras para esta reunião”**, além da explicação aberta do card de participantes. O botão **Organizar dashboard** permite iniciar a personalização.

### F03 — Personalizar visualização

![F03 — Editor de organização do dashboard](../assets/11_figma/organiza%C3%A7%C3%A3o%20do%20dash.png)

**Objetivo do usuário:** escolher os blocos apresentados no resumo, definir sua organização e atribuir um nome à visualização.  
**Signos principais:** nome da visualização, blocos disponíveis, seleção de blocos e ordem de apresentação.  
**Origem no MoLIC:** M01 — cena **Personalizar visualização**, relacionada a O01.

O editor apresenta caixas de seleção, controles de ordenação e orientações para arrastar e redimensionar os blocos. As ações disponíveis incluem **Cancelar** e **Salvar visualização**.

### F03E — Validação: tentativa de salvar sem nome

![F03E — Mensagem de validação ao salvar sem nome](../assets/11_figma/erro%20salvar%20sem%20nome.png)

**Objetivo do usuário:** identificar o dado necessário para concluir o salvamento e corrigir a entrada.  
**Signos principais:** nome da visualização, seleção de blocos e mensagem **“Dê um nome para a visualização.”**  
**Origem no MoLIC:** detalhamento da validação associada à cena **Personalizar visualização** e à solicitação `u: salvar alterações`, a incorporar na revisão do M01.

Após a tentativa de salvamento sem nome, o editor permanece aberto com a seleção visível. A recuperação consiste em preencher o nome e solicitar novamente **Salvar visualização**. Esse estado representa um erro de entrada, distinto de uma falha técnica no salvamento.

### F02S — Visualização salva e aplicada

![F02S — Resumo após o salvamento da visualização](../assets/11_figma/visualiza%C3%A7%C3%A3o%20salva.png)

**Objetivo do usuário:** reconhecer que a visualização foi salva e conferir a configuração apresentada no resumo.  
**Signos principais:** nome da visualização selecionada, blocos apresentados e mensagem **“Visualização ‘dsa’ salva na sua conta.”**  
**Origem no MoLIC:** M01 — retorno de sucesso do processo de salvamento e cena **Conferir resumo personalizado**, relacionada a O01 e O05.

O editor está fechado, a visualização nomeada aparece selecionada e a mensagem confirma o salvamento. O usuário pode solicitar novos ajustes pelo botão **Organizar dashboard**. A reunião utilizada neste registro permanece sem leituras; salvar a configuração não altera a disponibilidade dos dados.

### F03C — Confirmação de exclusão de uma visualização salva

![F03C — Confirmação antes de excluir uma visualização salva](../assets/11_figma/info%20excluir%20visualiza%C3%A7%C3%A3o.png)

**Objetivo do usuário:** confirmar ou cancelar a exclusão de uma visualização salva.  
**Signos principais:** nome da visualização, mensagem **“Excluir a visualização ‘dsa’?”** e opções **OK** e **Cancelar**.  
**Origem no MoLIC:** ação adicional de gerenciamento de visualizações, cuja conversa de exclusão ainda precisa ser incorporada ao modelo de interação.

A confirmação é apresentada antes da exclusão. O registro evidencia a solicitação de confirmação, mas não apresenta o resultado após sua aceitação.

> Documente também estados que muitas equipes esquecem: carregamento, vazio, confirmação, sucesso, erro, permissão negada, cancelamento, desfazer/voltar quando aplicável.

## Sistema visual e consistência

| Elemento | Regra adotada | Justificativa |
|---|---|---|
| Tipografia | {{...}} | {{legibilidade/contexto}} |
| Cores | {{...}} | {{hierarquia/contraste/semântica}} |
| Componentes | {{...}} | {{consistência}} |
| Feedback | {{...}} | {{status}} |

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
