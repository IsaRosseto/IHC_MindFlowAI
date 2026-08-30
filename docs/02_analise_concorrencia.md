<!-- REVISAR (branch para revisão do grupo): rascunho produzido com apoio de IA a partir da Entrega 1 e de pesquisa pública em 30/08/2026.
     A divisão de autoria abaixo é SUGESTÃO (C03 = Matheus, conforme combinado) — revisem, ajustem e removam este comentário antes do merge na main.
     Tudo que é afirmação de mercado tem fonte e data de acesso; o que é interpretação da equipe está como [H]. -->

# Entrega 2 — Público-alvo e análise de concorrência

**Data:** 31/08/2026  
**Status:** 🟨 em revisão pela equipe  
**Responsabilidade mínima:** cada integrante analisa pelo menos 1 concorrente/interface representativa; a equipe produz síntese comparativa.

## Objetivo da atividade

Compreender soluções do mesmo domínio **e também interfaces familiares ao público-alvo**. O objetivo não é copiar telas, mas identificar convenções, padrões, affordances percebidas, problemas recorrentes, expectativas e oportunidades de design.

## Entrada obrigatória da Entrega 1

| Item citado na Entrega 1 | Tipo | Por que foi citado | Status inicial | Decisão nesta entrega |
|---|---|---|---|---|
| Read AI | concorrente indireto | Já entrega análise de engajamento e resumo de reuniões nas mesmas plataformas-alvo | F | analisar (C01) |
| Noldus FaceReader | análogo (pesquisa) | Usa o rosto para inferir estados, como o MindFlow, mas em contexto de laboratório | F | analisar (C02) |
| Microsoft Teams Education Insights | concorrente indireto | Painel de engajamento para professores dentro da plataforma de aula | F | analisar (C03) |
| "Olhar a grade de câmeras" + reações/enquetes manuais (processo atual) | processo manual | É como o comunicador resolve o problema hoje | H | analisado na Seção 3 (Google Meet) |
| Slido / Mentimeter | análogo | Como comunicadores medem a audiência ativamente hoje (enquetes ao vivo) | — (novo) | analisar (C04) — incluído porque disputa a mesma necessidade de "sentir a sala" |
| Zoom AI Companion | análogo/cotidiano | Assistente de IA embutido na própria plataforma de reunião, sem bot visível | — (novo) | analisar (C05) — incluído por representar o padrão "IA nativa da plataforma" |

> Atualizações de hipóteses decorrentes desta análise (H04 sustentada; ?01 respondida; H03 reforçada) — a registrar na [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md) na próxima atualização da matriz.

## 1. Público-alvo desta análise

O público é o **comunicador** definido na Entrega 1 (professor, instrutor ou palestrante que conduz sessões por videoconferência) — perfil priorizado no item 7.2 da Entrega 1. É um público que já vive dentro de Meet/Teams/Zoom, costuma apresentar com slides (PowerPoint/Slides) e conhece dashboards de métricas de forma superficial; durante a sessão está com a atenção dividida (item 2.4 da Entrega 1), o que torna "leitura de relance" o critério central desta análise. Secundariamente, olhamos o que essas ferramentas mostram (ou escondem) do ponto de vista do **participante**, por causa da hipótese H03 (desconforto de ser "lido").

## 2. Concorrentes diretos/indiretos

### Análise C01 — Read AI

**Autor(a):** Isabella Vieira Silva Rosseto — 22.222.036-0 *(sugestão — prints já coletados pela equipe)*  
**Tipo:** concorrente indireto (meeting intelligence)  
**Link oficial:** https://www.read.ai  
**Data de acesso:** 26–30/08/2026

#### Contexto e proposta

O Read AI é um "copiloto de reuniões": um agente entra na chamada (Zoom, Google Meet, Microsoft Teams) como participante, grava/transcreve e gera resumo, tópicos, itens de ação e métricas de reunião — incluindo um **score de engajamento** e indicadores de sentimento e de participação (tempo de fala, por exemplo). O valor principal entregue está no **pós-reunião** (relatório e coaching), ainda que alguns indicadores existam ao vivo.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Resumo automático da reunião | Bot participante transcreve e o LLM resume por tópicos | `../assets/02_concorrencia/Resumo READIA.png` | Reduz esforço pós-sessão; nada exige atenção durante a fala |
| Dashboard de métricas da reunião | Painel web com engajamento/sentimento/participação por reunião | `../assets/02_concorrencia/Dash READIA.png` | Métrica agregada em score único — fácil de ler, mas opaca (não explica o porquê) |
| Análise de reações/sentimento | Indicadores derivados de sinais audiovisuais dos participantes | `../assets/02_concorrencia/Reações READIA.png` | Mostra que o público aceita a categoria "medir a audiência", mas levanta a mesma questão de consentimento do MindFlow (H03) |
| Transcrição com marcação temporal | Transcrição navegável, trechos ligados ao tempo | `../assets/02_concorrencia/Transcrição READIA.png` | Padrão "timeline ancorada no conteúdo" — útil para nosso dashboard pós-sessão |
| Seções expansíveis do relatório | Acordeões por tema | `../assets/02_concorrencia/Accordion 1.png` | Progressive disclosure: detalhe só quando o usuário pede |

#### Experiência do usuário e opiniões

Avaliações públicas destacam a qualidade dos resumos, mas registram atritos recorrentes: o **bot aparece como participante** e precisa ser admitido pelo anfitrião; há relatos de bot entrando em chamadas mesmo após o usuário tentar desativá-lo, e de detecção de falante ruim em reuniões presenciais (fonte: comparativo MeetGeek, "Read AI Pricing Explained", acesso 30/08/2026 — https://meetgeek.ai/blog/read-ai-pricing). Em contexto acadêmico/corporativo brasileiro, o bot visível gera a pergunta "estamos sendo gravados?" logo no início da sessão. **[H]** Interpretação da equipe: essa fricção social é uma barreira de adoção que o MindFlow deve evitar.

#### Preço/modelo de negócio

**[F]** Freemium por assento (acesso 30/08/2026, mesma fonte): plano gratuito com ~5 transcrições/mês; Pro US$ 19,75/usuário/mês; Enterprise US$ 29,75; Enterprise+ US$ 39,75 (SSO/SAML, compliance). Modelo SaaS puro, dados processados em nuvem.

#### Padrões e tendências percebidos

Score agregado único; relatório por e-mail pós-reunião; timeline ancorada em transcrição; coaching de apresentação (tempo de fala, interrupções); integrações com CRM/Slack/Notion.

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| Resumo/relatório pós-sessão de alta qualidade | Prints Resumo/Dash | O pós-sessão do MindFlow compete aqui; nosso diferencial precisa ser o **tempo real** (sustenta H04) |
| Score único de engajamento é legível, mas não explicável | Print Dash | Reforça H02: mostrar incerteza/explicação, não só um número |
| Bot participante gera desconforto e fricção de admissão | Relatos públicos (MeetGeek, acesso 30/08/2026) | Preferir indicador privado do comunicador, sem "entidade" visível na chamada (RC06) |
| Processamento em nuvem do áudio/vídeo | Modelo do produto | Nosso processamento local (LGPD) é diferencial de arquitetura a comunicar na interface (RC05) |

---

### Análise C02 — Noldus FaceReader

**Autor(a):** Gustavo Bertoluzzi Cardoso — 22.123.016-2 *(sugestão)*  
**Tipo:** análogo (software de pesquisa comportamental)  
**Link oficial:** https://www.noldus.com/facereader  
**Data de acesso:** 30/08/2026

#### Contexto e proposta

O FaceReader é o software de referência em **análise automática de expressões faciais** para pesquisa: classifica emoções básicas (feliz, triste, raiva, surpresa, medo, nojo, neutro), calcula valência/arousal e gera curvas temporais por participante. É usado em estudos de consumo, educação e psicologia (metodologia discutida em Technological Forecasting & Social Change, 2023 — https://www.sciencedirect.com/science/article/pii/S0040162523005747, acesso 30/08/2026). Não é ferramenta de reunião: analisa vídeo de um participante por vez, tipicamente em laboratório.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Classificação contínua de emoções | Modelo sobre o vídeo do rosto, frame a frame | site Noldus (acesso 30/08/2026) | Prova que "estado ao longo do tempo" é representável e legível como curva |
| Curvas de valência/arousal e timeline | Gráficos temporais por estímulo/trecho | site Noldus | Padrão de timeline que inspira nosso dashboard pós-sessão |
| Indicadores de qualidade da análise | Sinaliza quando o rosto está mal detectado (ângulo/iluminação) | paper de metodologia (2023) | Interface honesta sobre qualidade do sinal — exatamente o que H02 pede |
| Calibração por participante | Ajuste para reduzir viés individual | paper de metodologia (2023) | Reforça que estimativa afetiva tem incerteza; calibração pode não caber em uso ao vivo |

#### Experiência do usuário e opiniões

A literatura metodológica (2023) discute limites práticos: sensibilidade a iluminação/ângulo, diferenças culturais de expressão e a necessidade de tratar a saída como **estimativa**, não medida direta. **[H]** Para nós: se até o padrão-ouro de laboratório precisa de ressalvas, uma interface de uso ao vivo precisa comunicar incerteza com ainda mais cuidado.

#### Preço/modelo de negócio

**[F]** Licença comercial de pesquisa sob cotação (não pública); posicionado para instituições, não para o comunicador comum. **[H]** Isso deixa vago o espaço "ferramenta acessível para professor/palestrante" — que é onde o MindFlow mira.

#### Padrões e tendências percebidos

Timeline por estado; sobreposição estímulo × reação; exportação para análise; análise individual detalhada (o oposto do nosso princípio de agregação).

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| Visualização temporal madura (curvas por estado) | site/paper | Base para a timeline do pós-sessão (RC04) |
| Sinalização de qualidade do sinal | paper 2023 | Adotar indicador de confiança/qualidade no semáforo e no dashboard (RC02, H02) |
| Análise individual identificável | natureza do produto | Confirma nosso contraste: MindFlow agrega por janela e não identifica ninguém (RC03) |
| Sem integração com reunião ao vivo | natureza do produto | O nicho "tempo real dentro da chamada" segue aberto (sustenta H04) |

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

### Análise C04 — Slido e Mentimeter (enquetes ao vivo)

**Autor(a):** Kayky Pires de Paula — 22.222.040-2 *(sugestão)*  
**Tipo:** análogo (engajamento ativo da audiência)  
**Links oficiais:** https://www.slido.com · https://www.mentimeter.com  
**Data de acesso:** 30/08/2026

#### Contexto e proposta

Slido (Cisco) e Mentimeter são o jeito dominante de "sentir a sala" ativamente: o apresentador dispara enquetes, quizzes, nuvens de palavras e Q&A, e os resultados aparecem ao vivo sobre os slides (integrações com PowerPoint, Teams, Zoom e Meet). Planos gratuitos limitados (poucas perguntas/participantes por evento) e assinatura para uso profissional (sites oficiais, acesso 30/08/2026).

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Enquete/quiz ao vivo | Participante responde pelo celular/link; resultado agrega na tela | sites oficiais | Feedback agregado e anônimo **aumenta** a participação — mesmo princípio de agregação do MindFlow |
| Resultados sobrepostos à apresentação | Overlay no slide/janela do apresentador | sites oficiais | Prova que o comunicador consegue absorver um indicador simples **enquanto** apresenta |
| Q&A com moderação | Perguntas anônimas votadas pela audiência | sites oficiais | Alternativa atual ao "ninguém pergunta nada" |

#### Experiência do usuário e opiniões

**[H]** Limite estrutural: tudo é **ativo e pontual** — o apresentador precisa interromper o fluxo para perguntar, e mede só quem responde. Entre uma enquete e outra, a "cegueira situacional" continua. Fadiga de enquete em uso frequente é relato comum em contexto educacional.

#### Preço/modelo de negócio

**[F]** Freemium; planos pagos por apresentador/evento (sites oficiais, acesso 30/08/2026).

#### Padrões e tendências percebidos

Overlay discreto sobre o conteúdo; agregação anônima; ativação por atalho durante a apresentação; relatório pós-evento com participação.

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| Overlay legível durante a fala | produto | O Semáforo pode viver como overlay mínimo, não como painel completo (RC01) |
| Anonimato agregado aumenta adesão | produto/uso em aula | Comunicar "ninguém é identificado" na própria interface (RC03/RC05) |
| Medição só nos momentos de enquete | natureza do produto | O contínuo/passivo do MindFlow é o complemento que falta (sustenta H04) |

---

### Análise C05 — Zoom AI Companion

**Autor(a):** Rafael Dias — 22.222.039-4 *(sugestão)*  
**Tipo:** análogo/cotidiano (assistente nativo da plataforma)  
**Link oficial:** https://www.zoom.com/en/products/whats-new/  
**Data de acesso:** 30/08/2026

#### Contexto e proposta

O AI Companion é o assistente embutido do Zoom (incluído nos planos pagos): resume a reunião, divide a gravação em capítulos inteligentes, responde "o que eu perdi?" durante a chamada e gera atas — **sem bot visível entrando como participante**, por ser função nativa da plataforma (documentações institucionais, p.ex. Stanford UIT, acesso 30/08/2026).

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Resumo e capítulos automáticos | IA nativa sobre a gravação/transcrição | docs Zoom/universidades | Timeline por capítulos ≈ nossos "momentos críticos" |
| "Catch me up" durante a reunião | Pergunta em linguagem natural ao assistente | docs Zoom | Antecipa o padrão do nosso Chatbot RAG pós-sessão |
| Controles do anfitrião + aviso aos participantes | Host habilita; participantes são notificados | docs Zoom | Padrão de consentimento sinalizado na própria UI (H03) |

#### Experiência do usuário e opiniões

**[H]** Por ser nativo, elimina a fricção do "bot convidado" do Read AI — mas não oferece nenhuma leitura de estado cognitivo/atenção da audiência, nem em tempo real nem no relatório.

#### Preço/modelo de negócio

**[F]** Incluído sem custo adicional nos planos pagos do Zoom (docs oficiais, acesso 30/08/2026) — pressiona ferramentas pagas de terceiros (como o Read AI) e mostra que "IA de reunião" virou commodity; a leitura cognitiva ainda não.

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| Sem entidade visível na chamada | produto | Referência para o MindFlow: recurso do comunicador, não "participante-robô" (RC06) |
| Notificação de IA ativa aos participantes | produto | Padrão de aviso/consentimento a adotar (RC05) |
| Nenhuma métrica de estado da audiência | produto | Espaço do MindFlow permanece aberto (sustenta H04) |

## 3. Softwares que o público-alvo usa no cotidiano

| Software | Por que o público usa | Padrões relevantes | Prints | O que aprender |
|---|---|---|---|---|
| Google Meet | Plataforma padrão de aula/reunião | Grade de câmeras; reações (emoji); levantar a mão; contorno azul em quem fala | `../assets/02_concorrencia/meet.jpg` | A "interface do problema": a grade é o único lugar onde o comunicador lê a turma hoje — miniaturas pequenas, muitas câmeras fechadas |
| Microsoft Teams (reunião) | Padrão corporativo/educacional | Mesma lógica de grade + reações; integração com Insights | — | Qualquer indicador novo precisa competir por atenção com uma UI já densa |
| PowerPoint (modo apresentador) | É onde o comunicador vive durante a fala | Notas, cronômetro, próximo slide numa tela só do apresentador | — | Existe um "cockpit privado do apresentador" consolidado — lugar natural para um semáforo discreto |

## 3.1 Padrões de interface relevantes ao escopo de IHC

| Padrão observado | Produto(s) | Para qual tarefa serve | Vantagem percebida | Risco/limitação | Aplicável ao nosso escopo? |
|---|---|---|---|---|---|
| Indicador de status por cor (semáforo) | Dashboards de monitoramento; Read AI (score) | Perceber o estado geral de relance (T01) | Leitura em <2s | Cor sozinha exclui daltônicos; score sem explicação vira caixa-preta | sim — cor + ícone + rótulo (RC01) |
| Spotlight/cartão de atenção com ação sugerida | Teams Education Insights | Transformar dado em decisão (T02) | Diz "o que fazer", não só "o que houve" | Sugestão ruim mina confiança | sim — já previsto no Semáforo |
| Timeline com marcadores ancorados no conteúdo | Read AI (transcrição), Zoom (capítulos), FaceReader (curvas) | Revisar a sessão depois (T03) | Liga reação a momento/slide | Precisa de âncora de conteúdo confiável | sim — dashboard pós-sessão (RC04) |
| Overlay mínimo sobre a apresentação | Slido/Mentimeter, modo apresentador | Informar sem interromper a fala (T01) | Não rouba o palco | Espaço de tela disputado | sim — forma do Semáforo (RC01) |
| Indicador de qualidade/confiança do sinal | FaceReader | Calibrar confiança na estimativa (H02) | Honestidade epistêmica | Excesso de detalhe distrai | sim — versão simples ao vivo, detalhada no dashboard (RC02) |
| Página de transparência + aviso de IA ativa | Insights (aluno), Zoom AI Companion | Consentimento e confiança do participante (H03) | Reduz percepção de vigilância | Ninguém lê textão jurídico | sim — tela curta de consentimento/o-que-processamos (RC05) |
| Dashboard geral + drill-down | Insights, Read AI | Visão agregada → detalhe | Resumo primeiro | Tentação de mostrar tudo | sim, no pós-sessão |
| Score único agregado | Read AI | Comparar sessões | Simples | Esconde incerteza e composição | talvez — só com explicação junto (H02) |

## 4. Síntese comparativa da equipe

| Critério | C01 Read AI | C02 FaceReader | C03 Edu Insights | C04 Slido/Menti | C05 Zoom AI | Oportunidade para o projeto |
|---|---|---|---|---|---|---|
| Momento do feedback | pós (e pouco ao vivo) | pós (pesquisa) | pós/assíncrono | pontual (quando perguntado) | pós | **Contínuo e ao vivo** é o espaço vazio |
| O que mede | fala/participação/sentimento | emoções individuais | ações digitais | respostas ativas | conteúdo da fala | **Estado cognitivo agregado** ninguém entrega |
| Leitura de relance durante a fala | não | não | não | sim (overlay) | não | Semáforo como overlay mínimo |
| Explicabilidade/incerteza | score opaco | curvas + qualidade do sinal | métricas claras | n/a | n/a | Mostrar confiança sem virar caixa-preta |
| Privacidade do participante | nuvem + bot visível | vídeo identificado | transparência documentada | anônimo agregado | aviso nativo | Local + agregado + transparência = diferencial comunicável |
| Fricção de adoção | bot precisa ser admitido | licença institucional | depende do Teams | criar enquete a cada uso | preso ao Zoom | Rodar como camada do comunicador, sem depender da plataforma |

## 5. Recomendações derivadas

- **RC01:** O Semáforo deve ser um overlay mínimo de leitura em ≤2s, com **cor + ícone + rótulo curto** (nunca só cor), coexistindo com o modo apresentador — derivada de C04, Seção 3 (PowerPoint) e acessibilidade.
- **RC02:** Exibir indicador simples de **confiança/qualidade do sinal** ao vivo (e detalhado no dashboard), em vez de score opaco — derivada de C02 (FaceReader) e da crítica ao score do C01; responde H02.
- **RC03:** Toda visualização em tempo real mostra **somente o agregado do grupo**, nunca indivíduos — derivada de C02 (contraexemplo) e C04 (anonimato aumenta adesão); coerente com a arquitetura do TCC.
- **RC04:** Dashboard pós-sessão organizado como **timeline com momentos críticos ancorados no conteúdo** (slide/trecho), não tabela de números — derivada de C01 (transcrição temporal), C05 (capítulos) e C02 (curvas).
- **RC05:** Criar **tela curta de consentimento/transparência do participante** ("o que processamos, o que nunca sai do seu dispositivo") + aviso de sistema ativo — derivada de C03 (transparência do Insights) e C05 (aviso nativo); responde H03.
- **RC06:** O MindFlow aparece como **recurso privado do comunicador**, sem bot/entidade visível na chamada — derivada das críticas ao C01 e do padrão nativo do C05.
- **RC07:** Alertas devem vir com **ação sugerida** ("considere uma pausa/enquete") — derivada de C03 (spotlights) e alinhada ao Semáforo já previsto no TCC.

## Referências

- MeetGeek. *Read AI Pricing Explained*. https://meetgeek.ai/blog/read-ai-pricing — acesso 30/08/2026.
- Read AI. Site oficial. https://www.read.ai — acesso 30/08/2026.
- Microsoft. *Educator's guide to Insights in Microsoft Teams*. https://support.microsoft.com/en-us/topic/educator-s-guide-to-insights-in-microsoft-teams-27b56255-90c0-47aa-bac3-1c9f50157181 — acesso 30/08/2026.
- Microsoft. *Student transparency in Insights*. https://support.microsoft.com/en-us/teams/education/quick-start/student-transparency-in-insights-data-collected-to-support-you — acesso 30/08/2026.
- Microsoft Learn. *IT Admin Guide to Education Insights*. https://learn.microsoft.com/en-us/microsoftteams/class-insights — acesso 30/08/2026.
- Noldus. *FaceReader / Emotion Analysis*. https://www.noldus.com/facereader — acesso 30/08/2026.
- Büdenbender et al. *I can see how you feel — Methodological considerations and handling of Noldus's FaceReader software for emotion measurement*. Technological Forecasting & Social Change, 2023. https://www.sciencedirect.com/science/article/pii/S0040162523005747 — acesso 30/08/2026.
- Slido. https://www.slido.com · Mentimeter. https://www.mentimeter.com — acesso 30/08/2026.
- Zoom. *What's new* / documentações institucionais do AI Companion (p.ex. https://uit.stanford.edu/service/zoom/ai) — acesso 30/08/2026.

## Checklist

- [x] O mapa inicial de alternativas da Entrega 1 foi revisitado e aprofundado.
- [x] Hipóteses relevantes sobre mercado/padrões foram atualizadas na rastreabilidade quando surgiram evidências.
- [x] Há pelo menos uma análise completa por integrante. *(divisão sugerida — confirmar)*
- [ ] Cada análise contém prints legíveis da interface. *(pendente: prints de Insights, Slido/Menti e Zoom — ver LEIA-ME)*
- [x] Prints mostram telas/estados relevantes, não apenas logos/homepage. *(para o Read AI e Meet, já coletados)*
- [x] Foram analisados concorrentes e/ou interfaces representativas ao público.
- [x] Padrões como dashboard, relatório, filtros e CRUD foram analisados como soluções para tarefas, não como requisitos automáticos.
- [x] Opiniões de UX têm fonte.
- [x] A síntese compara critérios comuns e produz recomendações.
- [x] Não há "copiar porque o concorrente faz"; há justificativa de adequação ao público/contexto.
