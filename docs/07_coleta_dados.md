# Entrega 7 — Coleta de dados, necessidades e aspectos éticos

**Data:** {{dd/mm/aaaa}}  
**Status:** ⬜ não iniciada

## Objetivo da atividade

Planejar dados necessários para compreender usuários e requisitos de IHC, escolher técnicas adequadas e documentar instrumentos de modo que a aplicação possa ser reproduzida por pessoas diferentes.

## Para escopos de IHC derivados de TCC técnico

Quando o usuário e a interface foram propostos pela disciplina, uma prioridade da coleta é investigar se esse **cenário de uso realmente faz sentido**. Não trate o exercício de comercialização da Entrega 1 como validação de mercado.

Perguntas úteis incluem:

- esse perfil realmente realiza a atividade imaginada?
- quais ferramentas usa hoje?
- quais informações consulta?
- quais decisões toma?
- que vocabulário utiliza?
- quais parâmetros compreende e quais deveriam ser abstraídos?
- precisa de dashboard, histórico, filtros, relatórios ou comparação? Por quê?
- quais erros são frequentes e quais são críticos?
- existem papéis/permissões diferentes?
- que resultados do algoritmo/modelo seriam úteis ou difíceis de interpretar?

Quando o acesso ao perfil profissional for difícil, discuta com o docente alternativas metodológicas (especialistas próximos, dados secundários, literatura, participantes proxy) e registre as limitações. **Não esconda a limitação da amostra.**

## Hipóteses e lacunas prioritárias herdadas da Entrega 1

Antes de decidir “que dados coletar”, retome os itens `[H]` e `[?]` da Entrega 1 e o registro de hipóteses em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md). A coleta deve responder perguntas reais do projeto, e não apenas produzir um formulário porque a técnica foi solicitada.

| ID | Hipótese/lacuna | Evidência atual | Decisão que depende da resposta | Prioridade |
|---|---|---|---|---|
| H01 | Comunicadores consideram útil acompanhar, durante a própria sessão, um indicador discreto do estado do grupo sem que ele se torne uma nova fonte de distração. | Personas, cenários e análise de tarefas indicam a dificuldade de perceber o estado do público durante videoconferências. A análise de concorrência também identificou ferramentas com indicadores e feedback em tempo real, porém ainda não há evidência coletada diretamente com usuários do MindFlow sobre a utilidade e o nível de distração desse recurso. | Manter o Semáforo Cognitivo em tempo real como principal recorte de interação ou priorizar apenas análises e informações pós-sessão. | alta |
| H02 | O comunicador precisa visualizar alguma indicação de confiança ou incerteza da classificação para evitar confiança excessiva em uma previsão incorreta da IA. | A análise do Noldus FaceReader mostrou o uso de níveis de confiança associados às classificações e reforçou que resultados de reconhecimento devem ser tratados como estimativas. Ainda falta compreender quanto dessa informação os usuários desejam ou conseguem interpretar durante uma sessão. | Definir se a confiança do modelo será exibida e, caso seja, se aparecerá como percentual, faixa, indicação visual simplificada ou apenas em uma visualização detalhada. | média |
| H03 | Participantes podem sentir desconforto ao saber que suas expressões e comportamentos estão sendo processados para classificação de estados afetivo-cognitivos, mesmo quando o processamento ocorre localmente. | A análise de concorrência identificou preocupações com percepção de invasão em ferramentas de reunião e mecanismos explícitos de transparência sobre dados. Entretanto, ainda não há evidência direta de participantes sobre sua aceitação do funcionamento proposto pelo MindFlow. | Definir necessidade e forma de consentimento e transparência, quais informações devem ser apresentadas ao participante e se será necessário incluir interfaces específicas para esse público. | alta |
| H04 | O uso de informações em tempo real constitui um diferencial relevante do MindFlow em relação às soluções existentes. | A análise de concorrência refinou a hipótese: algumas ferramentas também possuem recursos em tempo real, enquanto outras trabalham principalmente com dados pós-sessão, atividade digital ou feedback explícito. Assim, tempo real isoladamente não parece ser um diferencial suficiente. | Refinar a proposta de valor do MindFlow, considerando como diferenciais a combinação entre análise em tempo real, estados afetivo-cognitivos, apoio imediato ao comunicador e contexto de videoconferência. | baixa |
| ?01 | Quais ferramentas existentes realizam análise de engajamento, comportamento ou estados dos participantes e quais informações disponibilizam em tempo real? | A lacuna foi parcialmente respondida na Entrega 2 com a análise de Read AI, Noldus FaceReader, Microsoft Teams Education Insights, reações manuais de plataformas de videoconferência, Adobe Connect Engagement Dashboard e outras ferramentas relacionadas. | Determinar quais funcionalidades já são padrões do domínio, quais não representam diferenciais do MindFlow e quais oportunidades ainda permanecem abertas para o projeto. | baixa |

## Parte A — necessidades e requisitos de IHC

> **Responsabilidade:** solução individual por integrante.

### A01 — Isabella Vieira Silva Rosseto

**Autor(a):** Isabella Vieira Silva Rosseto — 22.222.036-0

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Como professores de turmas pequenas (aproximadamente 5 a 15 alunos) percebem hoje, durante a aula, se a turma está acompanhando uma explicação nova | H01 / hipótese de turmas pequenas (Entrega 3) | O Cenário C05 assume que a professora só descobre a dificuldade da turma depois da aula. É preciso confirmar se isso realmente acontece e se o tamanho reduzido da turma já resolve o problema sozinho | Definir se o indicador em tempo real é necessário também para turmas pequenas ou se o foco deve ser outro perfil de uso |
| Quais sinais o professor usa (grade de vídeo, chat, respostas verbais, silêncio) e quanto confia em cada um | H01 | Permite saber quais sinais já são usados e quais são considerados pouco confiáveis, evitando criar um indicador que repita o que o professor já vê | Definir quais informações o indicador precisa trazer e quais seriam redundantes |
| Quanto tempo se passa entre a dificuldade da turma acontecer e o professor perceber que ela existiu | H01 | Dimensiona o atraso real descrito no Cenário C05 e mostra se existe ganho em perceber a dificuldade ainda durante a aula | Definir a frequência de atualização do indicador e a urgência do alerta |
| Como o compartilhamento de tela e as câmeras desligadas afetam a capacidade do professor de observar a turma | H01 | Verifica se a atenção dividida entre explicar, compartilhar e observar é o principal obstáculo, como sugerido na tarefa T04 | Definir posição, tamanho e nível de discrição do indicador durante o compartilhamento de tela |
| Quanta atenção o professor consegue dedicar a uma informação extra enquanto explica, e o que seria considerado distração | H01 | A hipótese H01 depende de o indicador ser discreto; só o professor pode dizer o que atrapalha uma aula em andamento | Definir forma do alerta (visual, sonoro ou ambos), tamanho, cor e frequência de mudança |
| O que o professor faz ao suspeitar que a turma não entendeu e o que o faz seguir em frente em vez de parar | H01 | Mostra o custo de parar a aula e o nível de certeza que o professor precisa ter para agir | Definir a partir de qual nível de indício o indicador deve chamar atenção e se deve sugerir alguma ação |
| Como o professor reagiria a uma indicação automática que contradiz o que ele está percebendo da turma | H02 | Permite verificar se o professor confiaria na indicação e que informação o ajudaria a decidir | Definir se a confiança da classificação será exibida e em que formato |
| Como alunos de turmas pequenas se sentiriam com a análise de sua imagem para estimar o acompanhamento da aula, e se o número reduzido de alunos muda essa percepção | H03 / hipótese de turmas pequenas (Entrega 3) | Em turma pequena, um resultado "do grupo" pode revelar facilmente o comportamento de cada aluno, o que aumenta o risco de exposição | Definir o número mínimo de participantes para exibir resultados agregados e o conteúdo do aviso de transparência |
| Como o professor revisa a aula depois que ela termina e que informações usaria nessa revisão | H01 / H02 | Evita incluir no Dashboard pós-sessão informações que não apoiem nenhuma decisão real do professor | Definir o conteúdo e o nível de detalhe do Dashboard pós-sessão |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Professores de idiomas ou de aulas particulares que lecionam on-line para turmas pequenas | Ter mais de 18 anos e conduzir aulas por videoconferência para grupos de aproximadamente 5 a 15 alunos, de forma recorrente | Representam diretamente a persona P02 (Camila Duarte) e o Cenário C05 |
| Tutores, monitores e professores de reforço ou de cursos livres que atendem pequenos grupos on-line | Ter mais de 18 anos e conduzir sessões on-line com poucos participantes, mesmo fora do ensino de idiomas | Permitem verificar se a dificuldade descrita no Cenário C05 aparece também em outras áreas |
| Alunos adultos de turmas pequenas on-line | Ter mais de 18 anos e já ter participado de aulas on-line com poucos colegas e uso de câmera | São afetados pelo processamento de imagem e são relevantes para investigar privacidade e transparência em turmas pequenas (H03) |

#### Aspectos éticos

A participação deve ser **voluntária**, e o participante deve ser informado, antes de a entrevista começar, sobre o objetivo do estudo, a duração estimada, o fato de poder interromper ou deixar de responder qualquer pergunta a qualquer momento e quais dados serão registrados. O consentimento deve ser obtido de forma explícita e registrado antes de qualquer gravação.

A coleta deve ser feita apenas com **adultos**, pois turmas pequenas on-line podem incluir menores de idade e o estudo não prevê coletar dados desse público. Ao relatar situações vividas, o professor não deve citar nomes, imagens ou informações que identifiquem seus alunos, e a entrevistadora deve interromper e reorientar caso isso ocorra.

As respostas devem ser **pseudonimizadas**, com códigos (por exemplo, E01, E02) no lugar de nomes. As gravações, quando autorizadas, devem ser usadas apenas para transcrição ou conferência das anotações e descartadas depois da análise.

Como o MindFlow envolve análise de imagens da webcam e inferência de estados afetivo-cognitivos, as perguntas sobre privacidade podem causar desconforto. O participante deve poder pular essas perguntas, e os resultados não devem ser tratados como diagnósticos ou avaliações definitivas sobre qualquer pessoa. A entrevistadora não deve apresentar o MindFlow como solução pronta, para não induzir aprovação.

A amostra será de **conveniência**, formada por professores e alunos de acesso próximo à equipe, e será pequena. Por isso, os resultados indicam tendências e não permitem generalizar para todos os professores de turmas pequenas, e essa limitação deve constar na análise.

> Repita A02, A03...

## Parte B — ferramentas de coleta

> Cada integrante deve preparar uma técnica/instrumento completo. As técnicas devem ser diferentes entre si e **questionário deve estar entre as técnicas escolhidas**, conforme o enunciado da disciplina.

### Instrumento I01 — Entrevista semiestruturada

**Autor(a):** Isabella Vieira Silva Rosseto — 22.222.036-0  
**Técnica:** Entrevista semiestruturada individual por videoconferência  
**Objetivo:** Compreender, a partir de situações reais vividas, como professores de turmas pequenas percebem hoje se a turma está acompanhando uma explicação, em que momento descobrem as dificuldades e que informações consideram úteis, confiáveis e aceitáveis em termos de privacidade, para verificar se o cenário do Cenário C05 faz sentido.  
**Público:** Professores, tutores e instrutores adultos que conduzem aulas on-line para turmas pequenas (aproximadamente 5 a 15 alunos). Pode ser aplicada, com os blocos 1 e 5 adaptados, a alunos adultos de turmas pequenas.

#### Procedimento padronizado de aplicação

1. **Preparação:** convidar o participante informando o tema, a duração estimada (cerca de 30 minutos) e que a participação é voluntária; agendar a entrevista por videoconferência, no horário escolhido por ele, com uma entrevistadora e, se possível, uma pessoa da equipe apenas para anotar; realizar uma entrevista-piloto com alguém próximo à equipe para ajustar clareza das perguntas e tempo.
2. **Apresentação/consentimento:** ler o texto de abertura e obter o consentimento verbal explícito, inclusive para gravar. Se o participante não autorizar a gravação, registrar apenas anotações.
3. **Aplicação:** conduzir as perguntas na ordem dos blocos, usando o aprofundamento somente quando a resposta for vaga e pedindo sempre exemplos de situações reais recentes. Não sugerir respostas, não corrigir o participante e não apresentar o MindFlow nem o Semáforo Cognitivo antes de concluir os blocos 2 e 3.
4. **Encerramento:** perguntar se o participante deseja acrescentar algo, ler o texto de encerramento, agradecer e informar como os dados serão usados.
5. **Armazenamento/anonimização:** em até 24 horas, organizar as anotações (e a transcrição, quando houver gravação), substituir o nome do participante por um código (E01, E02...), guardar o material em local de acesso restrito à equipe e apagar as gravações depois da análise.

#### Instrumento

O roteiro tem **20 perguntas em 5 blocos**, aplicadas nesta ordem. A coluna "Aprofundamento" só deve ser usada se a resposta for vaga. A coluna "Hipótese" é de uso interno da equipe e **não** deve ser lida ao participante.

**Texto de abertura (lido pela entrevistadora antes da pergunta 1):**

> Olá, obrigada por participar. Eu faço parte de um grupo de estudantes que está estudando como professores percebem se a turma está acompanhando a aula durante videoconferências. Não existe resposta certa ou errada: o objetivo é entender como as coisas acontecem na prática.
>
> A conversa dura cerca de 30 minutos. Sua participação é voluntária, você pode deixar de responder qualquer pergunta e pode parar a qualquer momento. Gostaria de gravar a conversa apenas para conferir minhas anotações; a gravação será usada só pela nossa equipe e apagada depois da análise, e seu nome não aparecerá em nenhum resultado. Por favor, não cite nomes nem dados que identifiquem seus alunos.
>
> Você concorda em participar? Você autoriza a gravação?

**Bloco 1 — Perfil e contexto (aquecimento)**

| # | Pergunta | Aprofundamento | Hipótese |
|---|---|---|---|
| 1 | Que tipo de aulas você ministra on-line e há quanto tempo? | — | contexto |
| 2 | Quantos alunos costuma ter em cada turma e com que frequência vocês se encontram? | — | contexto |
| 3 | Quais ferramentas de videoconferência você usa? Você costuma compartilhar a tela durante a explicação? | — | contexto |
| 4 | Os alunos costumam abrir a câmera? Como isso varia entre as aulas? | — | contexto |

**Bloco 2 — Percepção da turma durante a aula**

| # | Pergunta | Aprofundamento | Hipótese |
|---|---|---|---|
| 5 | Pense na última vez em que você explicou um conteúdo novo. Como você ficou sabendo se a turma estava acompanhando? | O que você olhava ou ouvia naquele momento? | H01 |
| 6 | Que sinais da turma você considera mais confiáveis para saber se entenderam? E quais considera menos confiáveis? Por quê? | — | H01 |
| 7 | Já aconteceu de você achar que a turma tinha entendido e depois perceber que não? Conte como foi. | Quando e como você descobriu? O que mudou na aula seguinte? | H01 |
| 8 | Enquanto você explica e compartilha a tela, como é acompanhar a turma ao mesmo tempo? | — | H01 |
| 9 | Quando você desconfia que parte da turma não entendeu, o que costuma fazer? O que pesa na sua decisão de parar para reforçar ou de seguir em frente? | — | H01 |
| 10 | O fato de a sua turma ter poucos alunos facilita ou dificulta perceber como cada um está? Por quê? | — | H01 (turmas pequenas) |

**Bloco 3 — Informação durante e depois da aula**

| # | Pergunta | Aprofundamento | Hipótese |
|---|---|---|---|
| 11 | Existe algum momento da aula em que você sente falta de informações sobre a turma? E algum momento em que qualquer informação extra atrapalharia? | — | H01 |
| 12 | Se, durante a aula, você pudesse receber alguma informação adicional sobre a turma, em qualquer formato, o que seria útil saber? O que seria inútil ou atrapalharia? | — | H01 |
| 13 | Depois que a aula termina, você revisa algo para avaliar como ela foi? O quê e como? | — | H01 |

**Bloco 4 — Confiança em informações automáticas**

| # | Pergunta | Aprofundamento | Hipótese |
|---|---|---|---|
| 14 | Imagine que uma ferramenta automática indicasse que a turma está com dificuldade, mas o que você está vendo na tela parece diferente. No que você confiaria? Por quê? | — | H02 |
| 15 | Que informação ajudaria você a decidir se acredita ou não nessa indicação? | — | H02 |

**Bloco 5 — Privacidade e transparência**

| # | Pergunta | Aprofundamento | Hipótese |
|---|---|---|---|
| 16 | Como você imagina que seus alunos se sentiriam se soubessem que a imagem da câmera deles poderia ser analisada por um programa para estimar o quanto estão acompanhando a aula? | — | H03 |
| 17 | O que você acharia aceitável e o que não acharia aceitável nesse tipo de análise? Há diferença entre ver o resultado do grupo e ver o resultado de cada aluno? | — | H03 |
| 18 | O número de alunos da turma muda algo na sua opinião sobre isso? O quê? | — | H03 (turmas pequenas) |
| 19 | O que você sentiria necessidade de explicar aos alunos antes de usar algo assim? | — | H03 |

**Fechamento**

| # | Pergunta | Aprofundamento | Hipótese |
|---|---|---|---|
| 20 | Há algo importante sobre esse assunto que eu não perguntei? | — | — |

**Texto de encerramento (lido pela entrevistadora):**

> Muito obrigada. Vou organizar as anotações sem identificar você e usar o que conversamos apenas neste trabalho acadêmico.

#### Como os dados serão analisados

As anotações e transcrições serão analisadas por **codificação temática**: cada resposta será associada a categorias como sinais usados para perceber a turma, momento e atraso na descoberta da dificuldade, efeito do compartilhamento de tela e das câmeras desligadas, critérios para parar ou seguir, informações desejadas durante e após a aula, confiança em indicações automáticas e privacidade em turmas pequenas.

As perguntas serão relacionadas às hipóteses: as perguntas 5 a 13 fornecem evidências sobre **H01** e sobre o recorte de turmas pequenas, as perguntas 14 e 15 sobre **H02**, e as perguntas 16 a 19 sobre **H03**. Os relatos serão comparados com o Cenário C05, a persona P02 e a tarefa T04, para verificar se a situação descrita é plausível e o que precisa ser corrigido.

Como a amostra será pequena e de conveniência, a análise considerará a **recorrência dos relatos** entre os participantes e registrará também os casos que contradizem o cenário. Ao final, cada hipótese será classificada como sustentada, refutada ou refinada, e o resultado será registrado em `RASTREABILIDADE.md`.

## Síntese

Explique quais lacunas de conhecimento sobre usuários o conjunto de técnicas pretende reduzir. Indique explicitamente quais hipóteses da Entrega 1 deverão ficar **sustentadas, refutadas ou refinadas** após a análise dos dados. Quando os dados forem coletados/analisados, atualize o histórico em `RASTREABILIDADE.md`.

## Checklist

- [ ] Hipóteses/lacunas prioritárias da Entrega 1 foram revisitadas.
- [ ] Se o escopo de IHC foi derivado de TCC técnico, a coleta investiga a plausibilidade do usuário, tarefa e contexto adotados.
- [ ] Perguntas não pressupõem que dashboard, CRUD, filtros ou relatórios sejam necessários; investigam a necessidade.
- [ ] Cada dado a coletar responde uma dúvida concreta do projeto ou justifica outra necessidade de informação.
- [ ] Parte A identifica dados e perfis de coleta de forma específica.
- [ ] Aspectos éticos são contextualizados para o projeto.
- [ ] Há uma técnica completa por integrante e técnicas distintas.
- [ ] Questionário está incluído entre as técnicas.
- [ ] Cada instrumento possui objetivo, público, procedimento e conteúdo integral.
- [ ] Perguntas evitam indução e coletam apenas dados necessários.
- [ ] Está claro como os dados serão analisados e usados no design.
