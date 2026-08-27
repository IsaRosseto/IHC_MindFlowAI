# Entrega 2 — Público-alvo e análise de concorrência

**Data:** 26/08/2026  
**Status:** 🟨 em andamento  
**Responsabilidade mínima:** cada integrante analisa pelo menos 1 concorrente/interface representativa; a equipe produz síntese comparativa.

## Objetivo da atividade

Compreender soluções do mesmo domínio **e também interfaces familiares ao público-alvo**. O objetivo não é copiar telas, mas identificar convenções, padrões, affordances percebidas, problemas recorrentes, expectativas e oportunidades de design.

> **Concorrente não precisa ser idêntico ao produto.** Pode atuar na mesma área, resolver objetivo semelhante ou disputar a mesma necessidade. Quando não houver concorrente direto, use produtos análogos e softwares que o público já utiliza.

### Para TCCs que não previam interface

Não procure apenas um "concorrente do algoritmo". Investigue **interfaces profissionais que materializam atividades semelhantes** às que o usuário escolhido precisaria realizar.

Exemplos:

- TCC de banco de dados → consoles de administração, ferramentas para DBA, monitoramento e análise de consultas;
- TCC de LLM/ML → painéis de experimentos, gestão de modelos/datasets, comparação de métricas, revisão de resultados;
- TCC de análise de dados → dashboards, ferramentas de BI, filtros, relatórios e exploração;
- TCC de infraestrutura/API → portais administrativos, observabilidade, logs, gestão de credenciais e uso;
- TCC de cibersegurança → consoles de alertas, triagem, histórico e auditoria.

A pergunta é: **"que convenções esse perfil já conhece para executar tarefas equivalentes?"**

## Entrada obrigatória da Entrega 1

Retome o mapa inicial de alternativas e produtos citado na Entrega 1. Aqui a equipe deixa de trabalhar apenas com impressão inicial e passa a **investigar sistematicamente** cada solução.

| Item citado na Entrega 1 | Tipo | Por que foi citado | Status inicial | Decisão nesta entrega |
|---|---|---|---|---|
| {{...}} | concorrente / análogo / ferramenta cotidiana / processo manual | {{...}} | F / H / ? | analisar / descartar com justificativa |

Se uma hipótese da Entrega 1 for confirmada ou refutada durante esta análise, atualize `H01`, `H02`... em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

## 1. Público-alvo desta análise

O público-alvo é o **comunicador**: professor, instrutor, palestrante ou facilitador. É quem usa a interface — acompanha o Semáforo em tempo real e o Dashboard depois. O participante só fornece dado pela webcam, não vê tela nenhuma.

Por isso comparamos com ferramentas que servem esse mesmo perfil: alguém que precisa acompanhar o estado de um grupo, ao vivo ou depois, e decidir algo em cima disso.

## 2. Concorrentes diretos/indiretos

### Análise C05 — Adobe Connect Engagement Dashboard

**Autor(a):** Gustavo Bertoluzzi 22.123.016-2  
**Tipo:** análogo  
**Link oficial:** https://helpx.adobe.com/adobe-connect/using/viewing-data-meetings.html  
**Data de acesso:** 27/08/2026

#### Contexto e proposta

> [F] O Adobe Connect é uma plataforma de webinars, salas de aula virtuais e reuniões corporativas, mais voltada pra treinamento e apresentação do que pra reunião comum. Dentro dela existe um recurso chamado Engagement Dashboard, disponível como um "pod" que só o apresentador/host enxerga (fica numa área exclusiva do apresentador, os participantes não veem). Ele calcula um score de engajamento em tempo real a partir de interações mensuráveis, como resposta a enquete, uso do chat e reações, e mostra esse score com um indicador visual por cor.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Indicador de engajamento por cor, em tempo real | Score calculado a partir de interações (enquete, chat, reação); score maior ou igual a 60 é "alto engajamento", menor que 20 é "baixo engajamento" |<img width="841" height="901" alt="image" src="https://github.com/user-attachments/assets/f98167be-a169-4625-a440-e991abb71c0e" />|É praticamente o mesmo conceito do Semáforo Cognitivo, um número complexo por trás, traduzido em uma cor simples pra leitura rápida durante a sessão |
| Relatório minuto a minuto pós-sessão | Depois do evento, fica disponível um relatório detalhado mostrando a variação do engajamento ao longo do tempo, permitindo cruzar com o conteúdo apresentado em cada minuto |<img width="272" height="672" alt="image" src="https://github.com/user-attachments/assets/6e80d988-1006-41b6-99cd-da889413eebb" />| É praticamente o mesmo objetivo do Dashboard pós-sessão do MindFlow, achar qual trecho específico gerou queda de engajamento |
| Rastreamento por papel/função | O apresentador pode filtrar o engajamento por tipo de participante (todos, ou por papel específico) | `../assets/02_concorrencia/adobe-connect-tracking.png` (PENDENTE) | Mostra um nível de granularidade a mais que o MindFlow ainda não previu, pode virar uma possibilidade futura pra turmas grandes com subgrupos |

#### Experiência do usuário e opiniões

> [?] Não encontramos avaliação pública de usuário específica sobre esse recurso nesta busca inicial, a documentação consultada é oficial, da própria Adobe. Fica como uma lacuna a investigar melhor, talvez em fóruns de administradores de treinamento corporativo ou reviews do Adobe Connect como um todo.

#### Preço/modelo de negócio

> [F] O Engagement Dashboard só está disponível a partir da versão 12.8 do Adobe Connect, dentro do plano corporativo da ferramenta, não é um produto avulso, é um recurso dentro de uma licença maior.

#### Padrões e tendências percebidos

> [H] Uso de cor como atalho visual pra engajamento, sem precisar interpretar número, separação clara entre visão do apresentador e visão do participante, e relatório pós-sessão organizado por linha do tempo pra permitir cruzar engajamento com o conteúdo daquele momento específico.

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| Indicador por cor é exatamente o padrão que já tínhamos escolhido pro Semáforo Cognitivo | Faixas de score High/Low com cor associada | Valida a escolha de design feita na Entrega 1, esse padrão já é reconhecido no mercado de ferramentas de apresentação/treinamento |
| O engajamento é calculado a partir de interação explícita (enquete, chat, reação), não de sinal visual/facial | Descrição da métrica do Adobe Connect | Essa é a maior diferença real do MindFlow, ele não depende do participante agir, o que resolve exatamente a limitação que fez a equipe escolher captar sinal facial/postural pela webcam |
| Relatório organizado por linha do tempo pós-sessão | Minute-by-minute engagement report | Reforça que a timeline é um padrão esperado no Dashboard pós-sessão do MindFlow, não uma invenção sem precedente |
| Recurso só disponível em plano corporativo, dentro de uma versão específica | Requisito de versão 12.8+ | Vale considerar se o MindFlow vai ficar preso a um modelo de licença parecido ou se vai ser mais acessível, isso pode virar diferencial de adoção |

> Repita a subseção para C02, C03... até atender à quantidade da equipe.

## 3. Softwares que o público-alvo usa no cotidiano

Analise interfaces que moldam a expectativa do público, mesmo que não sejam concorrentes.

| Software | Por que o público usa | Padrões relevantes | Prints | O que aprender |
|---|---|---|---|---|
| Zoom | Ferramenta de videochamada mais usada em aula/reunião | Reactions agregadas pro host; "Attention Tracking" foi removido em 2020 por pressão de privacidade [F] | `../assets/02_concorrencia/zoom-reactions.png` (PENDENTE) | Público aceita feedback agregado, mas rejeita rastreamento individual explícito |
| Mentimeter | Engajar audiência com enquete/quiz ao vivo | Resultado em tempo real só na tela do apresentador [F] | `../assets/02_concorrencia/mentimeter-live-results.png` (PENDENTE) | Reforça a separação comunicador × participante |
| Kahoot! | Quiz gamificado de revisão em aula | Leaderboard ao vivo + relatório pós-jogo com erros da turma [F] | `../assets/02_concorrencia/kahoot-report.png` (PENDENTE) | Relatório pós-sessão já é familiar pro público |

## 3.1 Padrões de interface relevantes ao escopo de IHC

Registre somente padrões encontrados nas soluções analisadas e que possam ter relação com objetivos reais da equipe.

| Padrão observado | Produto(s) | Para qual tarefa serve | Vantagem percebida | Risco/limitação | Aplicável ao nosso escopo? |
|---|---|---|---|---|---|
| dashboard | Adobe Connect, Mentimeter, Kahoot! | Mostrar o estado do grupo em tempo real de forma rápida (cor/gráfico) | Leitura instantânea, sem interpretar número cru | Host pode confiar demais no indicador sem saber a confiança do dado por trás | sim |
| relatório | Adobe Connect (minuto a minuto), Kahoot! (pós-jogo) | Entender depois o que aconteceu e cruzar com o conteúdo | Vira ação pra próxima sessão, não só constatação | Se não for bem filtrado, gera dado demais sem direção clara | sim |
| histórico + filtros | Adobe Connect (filtro por papel/função, PENDENTE evidência) | Revisar engajamento por subgrupo/período | Granularidade pra achar quem/quando precisa de atenção | Individualizar dado tensiona com a decisão de privacidade do MindFlow | talvez, só agregado por tempo, não por pessoa |
| administração/CRUD | — | — | — | Não observado nos concorrentes analisados até agora | não (fora do escopo de IHC) |
| comparação de resultados | — | — | — | [?] Nenhum concorrente analisado mostrou comparação clara entre sessões | a investigar |

> O objetivo não é concluir "todo concorrente tem dashboard, então teremos um". O padrão só será adotado se apoiar uma tarefa rastreável.

## 4. Síntese comparativa da equipe

| Critério | C01 | C02 | C03 | C05 | Oportunidade para o projeto |
|---|---|---|---|---|---|
| Navegação |  |  |  | Indicador fica dentro do pod, na própria sala, sem precisar trocar de tela |  |
| Feedback/estado |  |  |  | Cor em tempo real (score ≥60 = alto, <20 = baixo engajamento) |  |
| Prevenção/recuperação de erro |  |  |  | [?] Não documentado nas fontes consultadas |  |
| Terminologia |  |  |  | "Engagement score", alto/baixo — linguagem simples, traduzida pra cor |  |
| Acessibilidade |  |  |  | [?] Não documentado nas fontes consultadas |  |
| Eficiência |  |  |  | Score calculado automaticamente a partir de interações que já existem (enquete, chat, reação), sem ação extra do host |  |

## 5. Recomendações derivadas

Liste recomendações com origem explícita.

- **RC01:** Usar um indicador de cor simples (sem exigir leitura de número) no Semáforo Cognitivo — derivada de C05.
- **RC02:** Manter o indicador visível só para o comunicador, sem expor nada aos participantes — derivada de C05.
- **RC03:** Estruturar o Dashboard pós-sessão como linha do tempo (minuto a minuto), pra permitir cruzar quedas de engajamento com o conteúdo apresentado naquele momento — derivada de C05.

## Referências

**Adobe Connect (C05)**
- Adobe. *Engagement dashboard pod.* https://helpx.adobe.com/adobe-connect/using/engagement-dashboard-pod.html
- Adobe. *View the session dashboard.* https://helpx.adobe.com/adobe-connect/using/session-dashboard.html
- Adobe. *Measurable business impact — Adobe Connect.* https://www.adobe.com/products/adobeconnect/measurable-business-impact
- Adobe. *What's new in Adobe Connect — Fall Release 2024* (PDF, com prints do dashboard). https://www.adobe.com/content/dam/cc/us/en/products/adobe-connect/fall-release-2024/Whats_new_in_Adobe_Connect_Fall_Release.pdf

**Zoom**
- Zoom. *A Message to Our Users* (CEO Eric Yuan, remoção do Attention Tracking). https://blog.zoom.us/wordpress/2020/04/01/a-message-to-our-users/
- Arizona State University. *April 1, 2020 - Zoom Update.* https://tech.asu.edu/april-1-2020-zoom-update
- University of Michigan. *Reactions in a Zoom Meeting.* https://teamdynamix.umich.edu/TDClient/30/Portal/KB/Article/3805/Reactions-in-a-Zoom-Meeting

**Mentimeter**
- Purdue University. *Mentimeter — Online Teaching Hub.* https://onlineteachinghub.education.purdue.edu/mentimeter/
- K20 Center. *Mentimeter — Authentic Lessons for 21st Century Learning.* https://learn.k20center.ou.edu/tech-tool/645

**Kahoot!**
- University of Colorado Boulder. *Kahoot! — Research & Innovation Office.* https://www.colorado.edu/researchinnovation/kahoot
- Purdue University. *Kahoot! — Online Teaching Hub.* https://onlineteachinghub.education.purdue.edu/kahoot/

## Checklist

- [ ] O mapa inicial de alternativas da Entrega 1 foi revisitado e aprofundado.
- [ ] Hipóteses relevantes sobre mercado/padrões foram atualizadas na rastreabilidade quando surgiram evidências.
- [ ] Há pelo menos uma análise completa por integrante.
- [ ] Cada análise contém prints legíveis da interface.
- [ ] Prints mostram telas/estados relevantes, não apenas logos/homepage.
- [ ] Foram analisados concorrentes e/ou interfaces representativas ao público.
- [ ] Em TCC sem interface original, foram investigadas ferramentas profissionais análogas às atividades do usuário escolhido.
- [ ] Padrões como dashboard, relatório, filtros e CRUD foram analisados como soluções para tarefas, não como requisitos automáticos.
- [ ] Opiniões de UX têm fonte.
- [ ] A síntese compara critérios comuns e produz recomendações.
- [ ] Não há "copiar porque o concorrente faz"; há justificativa de adequação ao público/contexto.
