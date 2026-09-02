<!-- Entrega 2 consolidada em 02/09/2026 a partir das análises individuais commitadas nas branches de cada integrante (C01 Kayky, C02 Rafael, C03 Matheus, C04 Isabella, C05 Gustavo). -->

# Entrega 2 — Público-alvo e análise de concorrência

**Data:** 02/09/2026  
**Status:** 🟩 concluída — consolidação das análises individuais  
**Responsabilidade mínima:** cada integrante analisa pelo menos 1 concorrente/interface representativa; a equipe produz síntese comparativa.

## Objetivo da atividade

Compreender soluções do mesmo domínio **e também interfaces familiares ao público-alvo**. O objetivo não é copiar telas, mas identificar convenções, padrões, affordances percebidas, problemas recorrentes, expectativas e oportunidades de design.

## Entrada obrigatória da Entrega 1

| Item citado na Entrega 1 | Tipo | Por que foi citado | Status inicial | Decisão nesta entrega |
|---|---|---|---|---|
| Read AI | concorrente indireto | Já entrega análise de engajamento e resumo de reuniões nas mesmas plataformas-alvo | F | analisar (C01) |
| Noldus FaceReader | análogo (pesquisa) | Usa o rosto para inferir estados, como o MindFlow, mas em contexto de laboratório | F | analisar (C02) |
| Microsoft Teams Education Insights | concorrente indireto | Painel de engajamento para professores dentro da plataforma de aula | F | analisar (C03) |
| "Olhar a grade de câmeras" + reações/enquetes manuais (processo atual) | processo manual | É como o comunicador resolve o problema hoje | H | reações por emoji analisadas em C04; grade do Meet na Seção 3 |
| Slido / Mentimeter | análogo | Como comunicadores medem a audiência ativamente hoje (enquetes ao vivo) | — (novo) | coberto na Seção 3 (cotidiano) |
| Zoom AI Companion | análogo/cotidiano | Assistente de IA embutido na própria plataforma de reunião, sem bot visível | — (novo) | coberto na Seção 3 (cotidiano) |
| Adobe Connect Engagement Dashboard | análogo | Painel de engajamento em tempo real exclusivo do apresentador, dentro da plataforma | — (novo) | analisar (C05) — o análogo mais próximo do Semáforo |

> Atualizações de hipóteses decorrentes desta análise (H04 sustentada; ?01 respondida; H03 reforçada) — a registrar na [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md) na próxima atualização da matriz.

## 1. Público-alvo desta análise

O público é o **comunicador** definido na Entrega 1 (professor, instrutor ou palestrante que conduz sessões por videoconferência) — perfil priorizado no item 7.2 da Entrega 1. É um público que já vive dentro de Meet/Teams/Zoom, costuma apresentar com slides (PowerPoint/Slides) e conhece dashboards de métricas de forma superficial; durante a sessão está com a atenção dividida (item 2.4 da Entrega 1), o que torna "leitura de relance" o critério central desta análise. Secundariamente, olhamos o que essas ferramentas mostram (ou escondem) do ponto de vista do **participante**, por causa da hipótese H03 (desconforto de ser "lido").

## 2. Concorrentes diretos/indiretos

### Análise C01 — Read AI

**Autor(a):** Kayky Pires - 22.222.040-2  
**Tipo:** direto 
**Link oficial:** [Read AI](https://www.read.ai/pt) 
**Data de acesso:** 26/08/2026

#### Contexto e proposta

Read é o seu copiloto de IA — transformando reuniões, e-mails e mensagens em resumos, insights e respostas instantâneas em todos os dispositivos, onde quer que você trabalhe.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Transcrição da Reunião | O Read AI registra e transcreve automaticamente as falas da reunião, separando o conteúdo por participante. | [Trasncrição](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/02_concorrencia/Transcri%C3%A7%C3%A3o%20READIA.png) | A organização por participante facilita a compreensão de quem falou e permite consultar rapidamente partes específicas da reunião. |
|Resumo automático|Após a reunião, a IA gera um resumo com os principais assuntos discutidos, decisões, perguntas e pontos relevantes.|[Resumo](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/02_concorrencia/Resumo%20READIA.png)|Reduz a quantidade de informação que o usuário precisa analisar e apresenta uma visão geral da reunião de forma mais objetiva|
|Métricas da reunião|O sistema reúne diferentes indicadores de desempenho, como engajamento, sentimento e outras métricas relacionadas à participação e comunicação.|[Metrica](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/02_concorrencia/Dash%20READIA.png)|A centralização das métricas em um painel facilita a comparação das informações, mas exige boa hierarquia visual para não sobrecarregar o usuário|

#### Experiência do usuário e opiniões


#### Preço/modelo de negócio

Utiliza o modelo freemium, oferecendo um plano gratuito limitado a 5 reuniões por mês e planos pagos por usuário. Atualmente, o plano Pro custa a partir de US$ 15/mês por usuário no pagamento anual, enquanto os planos Enterprise e Enterprise+ oferecem recursos adicionais para equipes e organizações

#### Padrões e tendências percebidos

Apresenta tendência de centralizar, em um único painel, transcrição, resumo, métricas de engajamento, sentimento e destaques da reunião. Também se percebe forte uso de inteligência artificial para reduzir o esforço de análise do usuário e transformar reuniões longas em informações visuais e objetivas.

#### Pontos positivos, limitações e lições

| ID | Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|---|
|C01| Visualização de engajamento e sentimento da reunião. | Dashboard do Read AI. | Possui função semelhante ao MindFlow, sendo necessário diferenciar o projeto pelo foco educacional e pelos estados afetivo-cognitivos analisados. |

---

### Análise C02 — Noldus FaceReader

**Autor(a):** Rafael Dias - 22.222.039-4 <br>
**Tipo:** Análogo <br>
**Link oficial:** [Noldus FaceReader](https://noldus.com/facereader) <br>
**Data de acesso:** 26/08/2026

#### Contexto e proposta

Noldus FaceReader - É um produto que realiza a identificação das reações faciais dos usuarios capturando em tempo real ou por videos, demonstrando como as pessoas reagem ao seu produto

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Análise automática de expressões faciais | Detecta expressões como felicidade, tristeza, raiva, surpresa, medo, nojo, desprezo e estado neutro, indicando também a intensidade de cada expressão | [Identificação](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/02_concorrencia/evidencia_noldus.png) | ele Gera um indicador com o nivel de confiança para cada reação facilitando a demonstração a quem utiliza |

#### Experiência do usuário e opiniões


#### Preço/modelo de negócio

O Noldus FaceReader é um software comercial B2B, vendido a partir de licenças, principalmente para laboratorios, univesidades, empresas e instituições de pesquisa. O Noldus oferece 3 tipos de licenças: Essential - € 2000, Advanced - € 9000 e Premium - € 12500. Além dessas versões existe uma versão gratuita de 14 dias.

#### Padrões e tendências percebidos

Demonstra uma tendência para usos de estudo, para entender como os usuarios reagem a produtos ou areas de ensino. Tendo alto nivel de resultados para cada expressão.

#### Pontos positivos, limitações e lições

| ID | Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|---|
| C02 | Identificação da reação das pessoas | Graficos demonstrando o nivel de confiança da emoção (Execução do software) | Possui a funcionalidade parecida com a do nosso projeto de identificar a emoção dos usuarios, demonstrando um farol cognitivo captura em tempo real. |

---

### Análise C03 — Microsoft Teams Education Insights

**Autor(a):** Matheus Ferreira de Freitas — 22.125.085-5  
**Tipo:** concorrente indireto (analytics educacional dentro da plataforma de aula)  
**Link oficial:** https://support.microsoft.com/en-us/topic/educator-s-guide-to-insights-in-microsoft-teams-27b56255-90c0-47aa-bac3-1c9f50157181  
**Data de acesso:** 30/08/2026

#### Contexto e proposta

O Education Insights é o painel de dados do Teams for Education: dá ao docente uma visão por turma (e uma visão geral de todas as turmas) sobre **atividade digital** dos alunos — presença em reuniões, posts em canais, edição de arquivos de classe, entrega e notas de tarefas, progresso de leitura (Reading Progress) e check-ins emocionais autodeclarados (Reflect). A apresentação usa "spotlights": cartões que destacam pontos que merecem atenção ("aluno X sem atividade há N dias"), com visualizações de tendência (guia do educador, acesso 30/08/2026).

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Painel por turma + visão geral de todas as turmas | Dashboards nativos no Teams | guia do educador (link acima) | Padrão "resumo primeiro, detalhe depois" — bom para o nosso pós-sessão |
| Spotlights (destaques automáticos) | Cartões que apontam quem/o que precisa de atenção | guia do educador | Tradução de dado em **chamada para ação** — inspiração direta para as notificações do Semáforo |
| Métricas de engajamento por ações | Presença em reunião, posts, edição de arquivos, entregas | guia do educador | Mede **comportamento digital**, não estado cognitivo: presença ≠ atenção |
| Reflect (check-in emocional) | Aluno autodeclara como se sente, periodicamente | guia do educador | Estado emocional entra só por autodeclaração pontual — nada em tempo real durante a aula |
| Transparência para o aluno | Página oficial "quais dados o Insights coleta sobre você" | https://support.microsoft.com/en-us/teams/education/quick-start/student-transparency-in-insights-data-collected-to-support-you (acesso 30/08/2026) | Padrão de governança que o MindFlow deveria imitar para tratar a H03 |

#### Experiência do usuário e opiniões

**[F]** A própria documentação delimita o que **não** é coletado (chats privados, OneDrive pessoal, dados de login), e há uma página dedicada a explicar ao aluno o que é coletado — sinal de que vigilância percebida é uma preocupação real do produto. **[H]** Interpretação: para o nosso público (a professora que conduz a aula), o Insights responde "quem está participando das atividades?", mas não responde "a turma está me acompanhando **agora**?" — a decisão em sala continua às cegas.

#### Preço/modelo de negócio

**[F]** Incluído no Teams for Education (licenças A1/A3/A5 institucionais); dados de engajamento digital exportáveis na versão Premium (documentação Microsoft, acesso 30/08/2026). A adoção é decidida pela instituição, não pelo professor — padrão relevante para o perfil de coordenação/gestão, que é quem decide a adoção institucional.

#### Padrões e tendências percebidos

Spotlight cards; visões agregadas com drill-down; tendências temporais; linguagem de "apoio ao aluno" (não de vigilância); transparência documentada para o titular dos dados.

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| Spotlights transformam métrica em ação sugerida | guia do educador | Nosso alerta deve vir com sugestão de ação (pausa/enquete/reexplicar), como o Semáforo já prevê |
| Proxy de engajamento por ações digitais | guia do educador | Lacuna que o MindFlow ataca: estado cognitivo em tempo real vs. rastro de atividade (sustenta H04) |
| Nada de estado em tempo real durante a reunião | guia do educador | Confirma o espaço do trilho de tempo real |
| Página de transparência para o aluno | doc. de transparência | Criar equivalente no MindFlow: o participante vê o que é (e o que não é) processado — responde H03 (RC05) |

---

### Análise C04 — Reações por emoji manuais (Zoom / Google Meet / Teams)

**Autor(a):** Isabella Rosseto - 22.222.036-0
**Tipo:** análogo  
**Link oficial:** [Zoom Support](https://support.zoom.com/) e [Google Meet Help](https://support.google.com/meet/)  
**Data de acesso:** 27/08/2026

#### Contexto e proposta

> As reações por emoji são um recurso nativo das principais plataformas de videoconferência (Zoom, Google Meet, Microsoft Teams). A proposta é simples, o participante clica num ícone (aplausos, joinha, mão levantada etc.) e esse ícone aparece brevemente pra todo mundo ver, sem precisar interromper quem está falando. É a forma mais comum hoje de dar um sinal não verbal numa reunião online, e foi o que a equipe já tinha citado como alternativa atual na Entrega 1.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Reação temporária | No Zoom, o participante clica no botão Reactions e escolhe entre 11 emojis padrão. O ícone aparece do lado do nome do participante na lista e some sozinho depois de 10 segundos | <img width="760" height="403" alt="image" src="https://github.com/user-attachments/assets/4d31f18c-af59-4ecc-b870-219208295ba9" />| O tempo curto (10s) evita poluir a tela, mas também significa que se o comunicador não estiver olhando naquele instante, perde o sinal |
| Reação persistente | Ícones como "Levantar a mão" e "Sim/Não" ficam fixos até o próprio participante ou o host removerem manualmente | <img width="520" height="196" alt="image" src="https://github.com/user-attachments/assets/cb7e820a-3761-4ff0-b021-20d973e899f6" /> | Só esse tipo de reação dá um sinal confiável de estado sustentado, o resto é só um pulso rápido |
| Contagem agregada por ícone | O Zoom mostra, acima de cada ícone, o número total de pessoas que reagiram daquele jeito |<img width="306" height="470" alt="image" src="https://github.com/user-attachments/assets/ebfb6ffa-74d2-45fd-bc0a-79b7413002ea" /> | É o único lugar onde existe uma leitura agregada do grupo, mas só conta quem decidiu clicar, não reflete quem está de fato engajado ou confuso |
| Badge no vídeo + explosão de emoji na tela | No Google Meet, a reação aparece como um selo no canto do vídeo da pessoa e sobe flutuando pela tela, com várias reações ao mesmo tempo aparecendo como uma explosão de emojis | <img width="239" height="226" alt="image" src="https://github.com/user-attachments/assets/63039f19-0b4d-4582-9575-54e328c94cc6" /> | Reforça a reação como algo visual e rápido, mas ainda depende inteiramente de ação manual do participante |

#### Experiência do usuário e opiniões


> Segundo a própria documentação do Google Workspace, o objetivo declarado das reações é oferecer uma forma leve e não disruptiva de participar da reunião sem interromper quem está falando. Não achamos, nessa busca inicial, pesquisa de usuário publicada medindo se essa forma de sinal realmente ajuda o apresentador a perceber o clima do grupo, fica como uma lacuna a investigar melhor.


#### Padrões e tendências percebidos

> Ícone pequeno, temporário e não bloqueante é o padrão dominante. A diferença entre reação temporária (10 segundos, some sozinha) e persistente (fica até alguém remover) parece ser a única forma que essas plataformas já usam pra distinguir reação pontual de estado sustentado, o que é justamente o problema que o Semáforo Cognitivo do MindFlow tenta resolver de um jeito automático, sem depender do participante escolher manter o ícone ativo.

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| Reação some sozinha em poucos segundos, não polui a tela | Zoom, expiração de 10s | O Semáforo Cognitivo também deveria evitar acumular informação antiga na tela, sempre mostrar o estado mais recente |
| Contagem agregada acima de cada ícone já é um padrão aceito pra ler o grupo de relance | Zoom, contador por ícone | Reforça que um resumo agregado simples, tipo porcentagem do grupo em cada estado, é uma leitura que esse público já sabe interpretar |
| Depende inteiramente de ação manual do participante | Descrição de uso em ambas plataformas | É exatamente a limitação que o MindFlow resolve ao captar sinal passivo pela webcam, sem exigir clique de ninguém |
| Host pode ligar/desligar o recurso pra reunião inteira | Toggle de reações do Google Meet | O MindFlow provavelmente também vai precisar de um controle parecido, dar ao comunicador a opção de ativar ou não o Semáforo Cognitivo numa sessão específica |

---

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

## 3. Softwares que o público-alvo usa no cotidiano

| Software | Por que o público usa | Padrões relevantes | Prints | O que aprender |
|---|---|---|---|---|
| Google Meet | Plataforma padrão de aula/reunião | Grade de câmeras; reações (emoji); levantar a mão; contorno azul em quem fala | `../assets/02_concorrencia/meet.jpg` | A "interface do problema": a grade é o único lugar onde o comunicador lê a turma hoje — miniaturas pequenas, muitas câmeras fechadas |
| Microsoft Teams (reunião) | Padrão corporativo/educacional | Mesma lógica de grade + reações; integração com Insights | — | Qualquer indicador novo precisa competir por atenção com uma UI já densa |
| PowerPoint (modo apresentador) | É onde o comunicador vive durante a fala | Notas, cronômetro, próximo slide numa tela só do apresentador | — | Existe um "cockpit privado do apresentador" consolidado — lugar natural para um semáforo discreto |
| Slido / Mentimeter | Quando o comunicador quer medir a sala ativamente (enquetes/quiz ao vivo) | Overlay de resultados sobre os slides; agregação anônima; relatório pós-evento | — | Overlay simples durante a fala é absorvível; mede só nos momentos de enquete — o contínuo/passivo do MindFlow é o complemento (sustenta H04) |
| Zoom AI Companion | Assistente de IA nativo da plataforma de reunião | Resumo e capítulos automáticos; "catch me up"; aviso de IA ativa aos participantes | — | IA embutida sem bot visível virou padrão; o aviso de sistema ativo é referência de consentimento (H03, RC05) |

## 3.1 Padrões de interface relevantes ao escopo de IHC

| Padrão observado | Produto(s) | Para qual tarefa serve | Vantagem percebida | Risco/limitação | Aplicável ao nosso escopo? |
|---|---|---|---|---|---|
| Indicador de status por cor (semáforo) | Dashboards de monitoramento; Read AI (score); Adobe Connect (score por cor) | Perceber o estado geral de relance (T01) | Leitura em <2s | Cor sozinha exclui daltônicos; score sem explicação vira caixa-preta | sim — cor + ícone + rótulo (RC01) |
| Spotlight/cartão de atenção com ação sugerida | Teams Education Insights | Transformar dado em decisão (T02) | Diz "o que fazer", não só "o que houve" | Sugestão ruim mina confiança | sim — já previsto no Semáforo |
| Timeline com marcadores ancorados no conteúdo | Read AI (transcrição), Adobe Connect (minuto a minuto), FaceReader (curvas), Zoom (capítulos) | Revisar a sessão depois (T03) | Liga reação a momento/slide | Precisa de âncora de conteúdo confiável | sim — dashboard pós-sessão (RC04) |
| Overlay mínimo sobre a apresentação | Slido/Mentimeter, modo apresentador | Informar sem interromper a fala (T01) | Não rouba o palco | Espaço de tela disputado | sim — forma do Semáforo (RC01) |
| Indicador de qualidade/confiança do sinal | FaceReader | Calibrar confiança na estimativa (H02) | Honestidade epistêmica | Excesso de detalhe distrai | sim — versão simples ao vivo, detalhada no dashboard (RC02) |
| Página de transparência + aviso de IA ativa | Insights (aluno), Zoom AI Companion | Consentimento e confiança do participante (H03) | Reduz percepção de vigilância | Ninguém lê textão jurídico | sim — tela curta de consentimento/o-que-processamos (RC05) |
| Dashboard geral + drill-down | Insights, Read AI | Visão agregada → detalhe | Resumo primeiro | Tentação de mostrar tudo | sim, no pós-sessão |
| Score único agregado | Read AI | Comparar sessões | Simples | Esconde incerteza e composição | talvez — só com explicação junto (H02) |

## 4. Síntese comparativa da equipe

| Critério | C01 Read AI | C02 FaceReader | C03 Edu Insights | C04 Reações emoji | C05 Adobe Connect | Oportunidade para o projeto |
|---|---|---|---|---|---|---|
| Momento do feedback | pós (resumo/métricas) | pós (pesquisa) | pós/assíncrono | ao vivo, mas pontual e manual | ao vivo (score) + relatório pós | **Contínuo, passivo e ao vivo** é o espaço vazio |
| O que mede | fala/participação/sentimento | emoções individuais (face) | ações digitais | reações voluntárias clicadas | interações explícitas (enquete/chat/reação) | **Estado cognitivo agregado** ninguém entrega |
| Leitura de relance durante a fala | não | não | não | parcial (contador por emoji, efêmero) | sim (cor no pod do host) | Semáforo: relance + persistente + sem depender de clique |
| Explicabilidade/incerteza | métricas sem "porquê" | nível de confiança por expressão | métricas claras | n/a | faixas de score sem explicação | Mostrar confiança sem virar caixa-preta (H02) |
| Privacidade do participante | nuvem + gravação | vídeo identificado | transparência documentada | reação pública identificada | só interações, sem câmera | Local + agregado + transparência = diferencial comunicável |
| Fricção de adoção | bot precisa ser admitido | licença de pesquisa (€ 2.000+) | depende do Teams | nativo, zero fricção | plano corporativo (12.8+) | Rodar como camada do comunicador, sem depender da plataforma |

## 5. Recomendações derivadas

- **RC01:** O Semáforo deve ser um overlay mínimo de leitura em ≤2s, com **cor + ícone + rótulo curto** (nunca só cor), coexistindo com o modo apresentador — derivada de C05 (score por cor do Adobe), C04 (contadores agregados de relance) e Seção 3; acessibilidade para daltônicos.
- **RC02:** Exibir indicador simples de **confiança/qualidade do sinal** ao vivo (e detalhado no dashboard) — derivada de C02 (FaceReader expõe nível de confiança por expressão) e das métricas sem explicação de C01/C05; responde H02.
- **RC03:** Toda visualização em tempo real mostra **somente o agregado do grupo**, nunca indivíduos — C04 mostra que leitura agregada por contador já é padrão aceito pelo público, em contraste com a análise individual identificada de C02; coerente com a arquitetura do TCC.
- **RC04:** Dashboard pós-sessão organizado como **timeline com momentos críticos ancorados no conteúdo** — derivada de C05 (relatório minuto a minuto), C01 (transcrição temporal) e C02 (curvas por estado).
- **RC05:** Criar **tela curta de consentimento/transparência do participante** ("o que processamos, o que nunca sai do seu dispositivo") + aviso de sistema ativo — derivada de C03 (páginas de transparência do Insights) e do aviso de IA nativo (Zoom, Seção 3); responde H03.
- **RC06:** O MindFlow aparece como **recurso privado do comunicador** (sem bot/entidade visível na chamada), com **controle de ativar/desativar por sessão** — derivada de C05 (pod exclusivo do host) e C04 (toggle de reações do host).
- **RC07:** Alertas devem vir com **ação sugerida** ("considere uma pausa/enquete") — derivada de C03 (spotlights) e alinhada ao Semáforo já previsto no TCC.

## Referências

- Microsoft. *Educator's guide to Insights in Microsoft Teams* — acesso 30/08/2026 (C03).
- Microsoft. *Student transparency in Insights* — acesso 30/08/2026 (C03).
- Microsoft Learn. *IT Admin Guide to Education Insights* — acesso 30/08/2026 (C03).
- Adobe. *Viewing engagement data in Adobe Connect* (helpx.adobe.com) — acesso 27/08/2026 (C05).
- Noldus. *FaceReader* — acesso 26/08/2026 (C02).
- Read AI (read.ai/pt) — acesso 26/08/2026 (C01).
- Zoom Support · Google Meet Help (reações por emoji) — acesso 27/08/2026 (C04).
- Slido · Mentimeter · Zoom AI Companion (docs oficiais e institucionais, p.ex. Stanford UIT) — acesso 30/08/2026 (Seção 3).
- Prints e demais evidências referenciados inline em cada análise.

## Checklist

- [x] O mapa inicial de alternativas da Entrega 1 foi revisitado e aprofundado.
- [ ] Hipóteses relevantes sobre mercado/padrões foram atualizadas na rastreabilidade. *(H04 sustentada e ?01 respondida por este levantamento — registrar na matriz na próxima atualização)*
- [x] Há pelo menos uma análise completa por integrante (C01 Kayky, C02 Rafael, C03 Matheus, C04 Isabella, C05 Gustavo).
- [ ] Cada análise contém prints legíveis da interface. *(pendentes: print do Insights em C03 e o print de rastreamento por papel em C05)*
- [x] Prints mostram telas/estados relevantes, não apenas logos/homepage.
- [x] Foram analisados concorrentes e/ou interfaces representativas ao público.
- [x] Padrões como dashboard, relatório, filtros e CRUD foram analisados como soluções para tarefas, não como requisitos automáticos.
- [ ] Opiniões de UX têm fonte. *(pendente em C01 e C02 — seções "Experiência do usuário" ainda em aberto)*
- [x] A síntese compara critérios comuns e produz recomendações.
- [x] Não há "copiar porque o concorrente faz"; há justificativa de adequação ao público/contexto.
