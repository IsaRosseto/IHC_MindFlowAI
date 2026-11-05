# Entrega 7 — Coleta de dados, necessidades e aspectos éticos

**Data:** {{dd/mm/aaaa}}  
**Status:** 🟨 em andamento

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

### A01 — {{autor}}

**Autor(a):** {{nome — matrícula}}

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Como o comunicador percebe atualmente se o público está engajado, confuso, entediado ou frustrado durante uma videoconferência | H01 | Permite compreender quais sinais e estratégias já são usados e se existe realmente dificuldade em acompanhar o estado do grupo durante a sessão | Definir se o Semáforo Cognitivo em tempo real é necessário e quais informações deve apresentar |
| Em quais momentos da sessão o comunicador sente maior necessidade de receber informações sobre o estado do público | H01 | Ajuda a entender quando o feedback seria útil e quando poderia gerar distração | Definir frequência de atualização, destaque visual e momento de exibição dos indicadores |
| Quais ações o comunicador tomaria ao perceber aumento de confusão, tédio, frustração ou queda de engajamento | H01 | Permite verificar se os dados gerados pelo sistema podem apoiar decisões reais durante a apresentação | Definir quais estados devem receber maior destaque e se o sistema deve apresentar sugestões de ação |
| Preferência entre informação em tempo real e análise após o término da sessão | H01 | Permite identificar qual dos dois momentos possui maior valor para o usuário | Priorizar o Semáforo em tempo real, o Dashboard histórico ou ambos |
| Nível de compreensão e interesse do comunicador sobre a confiança das classificações realizadas pela IA | H02 | É necessário verificar se apresentar a confiança melhora a interpretação ou apenas aumenta a carga cognitiva | Definir se a confiança será exibida e se aparecerá como percentual, faixa ou indicador simplificado |
| Forma considerada mais clara para indicar que uma classificação da IA possui incerteza | H02 | Diferentes formas de representação podem gerar interpretações distintas | Definir a representação visual da confiança ou incerteza do modelo |
| Grau de conforto dos participantes com o processamento de imagem da webcam para identificação de estados afetivo-cognitivos | H03 | O funcionamento do sistema pode ser percebido como invasivo ou gerar resistência ao uso | Definir requisitos de consentimento, transparência e controle do participante |
| Quais informações os participantes gostariam de receber antes de autorizar o uso da câmera para análise | H03 | Permite identificar quais explicações são necessárias para garantir uma decisão consciente | Definir o conteúdo da tela ou aviso de consentimento e transparência |
| Grau de aceitação do uso de dados agregados do grupo em comparação com resultados individuais | H03 | Informações individuais apresentam maior risco de exposição, vigilância e constrangimento | Definir se os resultados serão exclusivamente agregados ou se haverá algum nível de detalhamento individual |
| Quais informações do Dashboard são consideradas úteis após uma sessão | H01 / H02 | Permite evitar a inclusão de gráficos, filtros e métricas que não apoiem nenhuma tarefa real | Definir KPIs, gráficos, histórico, filtros e nível de detalhamento do Dashboard |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Professores e docentes que realizam aulas on-line | Ter experiência conduzindo aulas por videoconferência, preferencialmente de forma recorrente | Representam diretamente parte do público prioritário do MindFlow |
| Instrutores e facilitadores de treinamentos on-line | Conduzir apresentações, cursos ou treinamentos por videoconferência | Representam usuários com necessidades semelhantes às personas definidas no projeto |
| Palestrantes ou outros comunicadores que utilizam videoconferência | Ter experiência conduzindo sessões para grupos remotamente | Permitem verificar se as necessidades identificadas também aparecem fora do contexto estritamente educacional |
| Participantes de aulas, palestras ou treinamentos on-line | Ter participado de sessões por videoconferência com uso de câmera | São afetados pelo processamento das imagens e são relevantes principalmente para investigar privacidade, transparência e aceitação relacionadas à H03 |

#### Aspectos éticos

A participação deve ser **voluntária**, com consentimento claro sobre o objetivo da pesquisa e sobre quais dados serão coletados. Devem ser solicitadas apenas as informações necessárias, evitando dados pessoais sem relação com o estudo.

As respostas devem ser preferencialmente **anônimas ou pseudonimizadas**, e qualquer gravação deve ocorrer somente com autorização do participante.

Como o MindFlow envolve análise de imagens da webcam e inferência de estados afetivo-cognitivos, é necessário considerar riscos de **privacidade, sensação de vigilância e interpretações incorretas**. Os resultados não devem ser tratados como diagnósticos ou avaliações definitivas sobre os participantes.

Os dados coletados devem ter acesso restrito, ser utilizados apenas para o projeto e descartados quando não forem mais necessários.

### A02 — Isabella Rosseto

**Autor(a):** Isabella Vieira Silva Rosseto — 22.222.036-0

**Foco desta solução:** o momento **durante a aula** em que o comunicador introduz um conteúdo novo com a tela compartilhada e precisa decidir se reforça ou segue (persona P02, Cenário C05 e tarefa T03). A A01 investiga o comunicador de forma ampla; a A02 aprofunda essa decisão e verifica se a situação descrita nas Entregas 3 a 5 acontece de fato, já que foi construída sem contato com usuários reais.

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Se o comunicador realmente deixa de perceber dificuldades da turma durante a aula e com que frequência isso acontece | H01 | O Cenário C05 e a jornada de Camila supõem esse problema; se ele for raro ou pouco relevante, o recorte em tempo real perde força | Manter o Semáforo Cognitivo como recorte principal ou priorizar o pós-sessão |
| Quais sinais o comunicador usa hoje para perceber se a turma entendeu (rostos, silêncio, chat, respostas, exercícios) e qual considera mais confiável | H01 / H02 | Mostra o que o sistema precisaria complementar, e não substituir, e qual vocabulário o usuário usa para descrever esses sinais | Rótulos dos estados, linguagem da interface e quais estados merecem destaque |
| Como a tela compartilhada afeta a observação da turma (onde fica a grade de vídeo, quantos monitores usa, quando deixa de olhar os alunos) | H01 / C05 (Q1) | Define o espaço e o momento em que um indicador poderia ser visto sem atrapalhar a explicação | Posição, tamanho e discrição do indicador durante o compartilhamento de tela |
| Critério usado para decidir entre seguir o plano e reforçar o conteúdo, e o custo percebido de cada opção | H01 / C05 (Q4) | A T03 mostra que a decisão é tomada com sinais fracos e tende a favorecer seguir em frente; é preciso confirmar se isso acontece | Se o sistema deve apenas indicar que algo merece atenção ou também oferecer apoio à decisão (sem prescrever a ação, conforme RC03) |
| Alternativas que o comunicador já usa ou evita para checar a compreensão (chamar pelo nome, pedir um exemplo, enquete, chat) e por quê | C05 (Q5) | Mostra estratégias atuais e o receio de expor alunos, que pode tornar um sinal agregado mais aceitável | Se o indicador deve ser agregado e discreto, e se precisa conviver com ferramentas já usadas |
| Quanto o comunicador confiaria em um sinal externo que contradiz sua própria percepção e o que precisaria saber para confiar | H02 | Verifica se mostrar confiança/qualidade da inferência ajuda ou apenas aumenta a carga durante a aula | Exibir ou não a confiança, e de que forma (percentual, faixa, ícone ou só no pós-sessão) |
| Se o tamanho da turma muda a dificuldade de perceber a compreensão (turma pequena x turma grande) | Hipótese nova sobre turmas pequenas (Entrega 3) | O recorte de 5 a 15 alunos da persona P02 nunca foi verificado; em turma pequena, um indicador agregado pode ser pouco útil ou expor alunos | Número mínimo de participantes para exibir o indicador agregado e como tratar turmas muito pequenas |
| Percepção do comunicador sobre como os alunos reagiriam a ter a câmera analisada e o que ele se sentiria confortável em explicar a eles | H03 | O comunicador é quem ativa a ferramenta e responde aos alunos; se ele próprio se sentir desconfortável, não a usará | Conteúdo do aviso aos participantes, controle de ativar/desligar (RC07) e materiais de explicação para o comunicador |
| Como e quando o comunicador descobre depois que a turma não entendeu e o que faz com essa informação | H01 / C05 (Q7) / R03 | Mostra se uma revisão pós-sessão teria utilidade real ou se o exercício corrigido já cumpre esse papel | Necessidade, conteúdo e nível de detalhe do Dashboard pós-sessão |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Professores de idiomas que dão aula on-line para turmas pequenas | Ministrar aulas síncronas por videoconferência para turmas de até 15 alunos, há pelo menos 6 meses, usando compartilhamento de tela | Corresponde diretamente à persona P02 (Camila) e ao Cenário C05 |
| Professores de outras disciplinas com aulas on-line síncronas (ensino superior, cursos livres ou EAD) | Ministrar aulas síncronas por videoconferência com turmas de tamanhos variados, preferencialmente acima de 15 alunos | Permite comparar com P01 (Karol) e verificar se o problema depende do tamanho da turma |
| Instrutores de treinamento corporativo on-line (participante de contraste) | Conduzir treinamentos síncronos por videoconferência | Ligado a P03 (Nathanael); serve para verificar se as necessidades da A02 aparecem fora do ensino |

Critério de exclusão: pessoas que nunca conduziram sessões síncronas por videoconferência. Não serão entrevistados alunos menores de idade.

**Limitação da amostra:** o acesso a professores de idiomas pode ser difícil; nesse caso, serão usados professores da própria instituição ou conhecidos da equipe como participantes proxy, por conveniência. Essa limitação será registrada junto aos resultados, que não serão generalizados para todos os comunicadores.

#### Aspectos éticos

- **Dados envolvidos neste projeto:** relatos sobre a própria prática docente e, de forma indireta, sobre alunos e situações de sala de aula. O MindFlow analisa imagens de webcam, mas **esta coleta não usa câmera, imagem ou qualquer classificação de estados**: apenas conversa.
- **Voluntariedade e relação de poder:** se o entrevistado for professor da própria instituição da equipe, deve ficar claro que recusar ou desistir não traz consequência alguma, inclusive acadêmica. A participação pode ser interrompida a qualquer momento, sem justificativa.
- **Consentimento:** o objetivo, a duração (cerca de 40 minutos) e o uso dos dados serão lidos no início (texto do roteiro I02), com aceite registrado antes de qualquer pergunta, seguindo o [modelo de termo de consentimento](../instrumentos/termo_consentimento_modelo.md).
- **Risco de constrangimento:** falar de aulas em que "a turma não entendeu" pode soar como avaliação da didática do professor. O roteiro deixa explícito que se investiga a situação, e não o desempenho dele, e permite pular qualquer pergunta.
- **Terceiros citados:** o professor pode mencionar alunos. Será pedido que não use nomes; se aparecerem, serão removidos na transcrição. Nenhum dado de aluno será solicitado.
- **Minimização:** não serão coletados nome completo, instituição, idade exata ou contato além do necessário para agendar. O perfil é registrado por faixas (tempo de docência, tamanho da turma).
- **Gravação:** somente áudio, e somente com autorização específica. Sem autorização, a entrevista ocorre com anotações. Não haverá gravação de vídeo.
- **Anonimização, armazenamento e descarte:** cada participante recebe um código (E01, E02...). Áudios e transcrições ficam em pasta de acesso restrito à equipe; os áudios são apagados após a transcrição revisada e as transcrições, ao final da disciplina. No repositório entram apenas trechos anonimizados e a síntese.
- **Uso dos resultados:** os relatos servem para decisões de design e para confirmar ou refutar hipóteses; não serão usados para avaliar professores ou instituições.

> Repita A03, A04...

## Parte B — ferramentas de coleta

> Cada integrante deve preparar uma técnica/instrumento completo. As técnicas devem ser diferentes entre si e **questionário deve estar entre as técnicas escolhidas**, conforme o enunciado da disciplina.

### Instrumento I01 — Questionário

**Autor(a):** Kayky Pires — 22.222.040-2  
**Técnica:** Questionário on-line  
**Objetivo:** Investigar como comunicadores percebem o estado do público durante videoconferências, quais informações consideram úteis durante e após a sessão e suas percepções sobre confiança da IA e privacidade.  
**Público:** Professores, instrutores, palestrantes e outros comunicadores que conduzem atividades por videoconferência.

#### Procedimento padronizado de aplicação

1. Preparar o questionário em uma plataforma de formulários on-line.
2. Apresentar, no início do formulário, o objetivo da pesquisa e informar que a participação é voluntária.
3. Solicitar o consentimento do participante antes do início das perguntas.
4. Aplicar o questionário sem solicitar dados pessoais desnecessários.
5. Encerrar agradecendo a participação e informando que os dados serão utilizados apenas para fins acadêmicos.
6. Armazenar as respostas de forma restrita à equipe do projeto e analisar os resultados de forma agregada e anônima.

#### Instrumento

[**Link do formulário I01**](https://forms.cloud.microsoft/r/fHf6y8q6ZK)

#### Como os dados serão analisados

As questões fechadas serão analisadas por meio da **distribuição e frequência das respostas**, identificando padrões de percepção, necessidades e preferências dos participantes.

As respostas abertas serão analisadas por **codificação temática**, agrupando conteúdos semelhantes em categorias como utilidade do feedback em tempo real, confiança na IA, privacidade e informações desejadas no dashboard.

Ao final, os resultados serão relacionados às hipóteses **H01, H02 e H03**, permitindo verificar se elas foram sustentadas, refutadas ou precisam ser refinadas.

### Instrumento I02 — Entrevista semiestruturada com técnica de incidente crítico

**Autor(a):** Isabella Vieira Silva Rosseto — 22.222.036-0  
**Técnica:** entrevista semiestruturada individual, com técnica de incidente crítico (o entrevistado relata uma aula real e recente, em vez de opinar sobre situações hipotéticas)  
**Objetivo:** verificar se a situação descrita para Camila (P02, C05, T03) acontece com professores reais: como percebem, durante a aula on-line, se a turma acompanha um conteúdo novo, que sinais usam, como decidem entre reforçar e seguir e o que precisariam para confiar em um sinal externo. Responde às questões Q1 a Q7 do Cenário C05 e investiga H01, H02, H03 e a hipótese sobre turmas pequenas.  
**Público:** perfis definidos na A02 — prioritariamente professores de idiomas com turmas pequenas on-line; professores de outras disciplinas e instrutores corporativos como contraste. Meta: 5 a 8 entrevistas, com pelo menos 3 do perfil principal.

**Por que entrevista e não questionário:** o questionário (I01) mede a distribuição de opiniões em mais pessoas; a entrevista permite reconstruir, passo a passo, uma situação concreta, com os critérios e as dúvidas do professor no momento da decisão, o que um formulário fechado não captura.

#### Procedimento padronizado de aplicação

1. **Preparação:** agendar 40 a 45 minutos por videochamada (ou presencialmente), confirmar o perfil pelos critérios de inclusão da A02 e enviar com antecedência um resumo do objetivo. Atribuir o código do participante (E01, E02...). Preparar a ficha de registro abaixo e testar a gravação de áudio.
2. **Apresentação e consentimento:** ler o texto de abertura do roteiro sem alterações, perguntar se há dúvidas e registrar o aceite e a autorização (ou não) da gravação de áudio antes de iniciar.
3. **Aplicação:** seguir os blocos na ordem, fazendo as perguntas principais com as mesmas palavras para todos os participantes. Os aprofundamentos (↳) são usados somente quando a resposta não cobrir o ponto. O entrevistador **não apresenta o MindFlow nem sugere soluções antes do Bloco 6**, para não induzir respostas. Um segundo integrante, quando possível, faz as anotações.
4. **Encerramento:** fazer as perguntas finais, agradecer, explicar como os dados serão usados e perguntar se o participante deseja receber a síntese dos resultados.
5. **Armazenamento e anonimização:** no mesmo dia, preencher a ficha de registro, transcrever ou resumir a entrevista removendo nomes de pessoas e instituições, salvar na pasta restrita da equipe com o código do participante e apagar o áudio após a revisão da transcrição.

#### Instrumento

**Texto de abertura (ler na íntegra)**

> Obrigado(a) por aceitar participar. Sou estudante da FEI e, na disciplina de Interação Humano-Computador, estamos estudando como professores acompanham a turma durante aulas on-line. Não estamos avaliando você nem sua forma de dar aula: queremos entender a situação e as dificuldades que ela traz. A conversa dura cerca de 40 minutos. Você pode pular qualquer pergunta ou parar a qualquer momento, sem precisar explicar o motivo. Por favor, não cite nomes de alunos. Seus dados serão identificados apenas por um código, e os trechos usados no trabalho não vão identificar você nem sua instituição. Você autoriza a gravação apenas do áudio, que será apagado depois da transcrição? [registrar sim/não] Você concorda em participar? [registrar aceite]

**Bloco 1 — Perfil (registrar por faixa)**

1. Há quanto tempo você dá aulas on-line síncronas? (menos de 1 ano / 1 a 3 anos / mais de 3 anos)
2. O que você ensina e para que público, de forma geral?
3. Quantos alunos costumam participar de cada aula? (até 5 / 6 a 15 / 16 a 40 / mais de 40)
4. Que plataforma você usa e quem escolheu essa plataforma?

**Bloco 2 — Contexto da aula (Q1, Q2)**

5. Me descreva como é o seu espaço e o seu equipamento quando você dá uma aula on-line.
   - ↳ Você usa um ou mais monitores? Onde fica a imagem dos alunos quando você compartilha a tela?
6. Em uma aula típica, quantos alunos ficam com a câmera ligada? Na sua opinião, por que os demais desligam?
7. Além de você, alguém acompanha o resultado das suas turmas (coordenação, empresa, responsáveis)? De que forma?

**Bloco 3 — Incidente crítico: a última aula com conteúdo novo (Q3, Q4, Q6)**

8. Pense na última vez em que você apresentou um conteúdo novo ou mais difícil em uma aula on-line. Pode me contar como foi, do começo ao fim?
   - ↳ O que você estava fazendo na tela naquele momento?
   - ↳ Aconteceu alguma coisa que interrompeu ou mudou o rumo da aula (atraso, conexão, mensagem, interrupção em casa)?
9. Enquanto explicava, como você tentava saber se a turma estava acompanhando?
   - ↳ O que você olhava, ouvia ou lia? Em que momentos?
10. Em algum momento você ficou em dúvida se a turma tinha entendido? O que gerou essa dúvida?
11. O que você decidiu fazer naquele momento e por quê?
    - ↳ Que outras opções você considerou? O que pesou na escolha (tempo, plano de aula, os alunos)?
12. Para você, o que torna uma aula bem-sucedida? Isso mudou o que você fez naquele momento?

**Bloco 4 — Estratégias e sinais (Q5, H02)**

13. Quando você não tem certeza se a turma entendeu, o que costuma fazer?
    - ↳ Há alguma estratégia que você evita? Por quê?
14. Dos sinais que você usa, qual você considera mais confiável? E qual costuma enganar?
15. Já aconteceu de você achar que a turma tinha entendido e depois descobrir que não? Como descobriu e quanto tempo depois?
16. Já aconteceu o contrário: achar que não tinham entendido, parar para reforçar, e perceber que não era necessário? Como foi?

**Bloco 5 — Depois da aula (Q7, R03)**

17. Depois que a aula termina, como você avalia se aquele conteúdo funcionou?
    - ↳ Você anota algo para a próxima aula? Onde e como?
18. Quanto tempo você costuma ter entre uma aula e outra para revisar ou replanejar?
19. Se você pudesse saber algo sobre a aula depois que ela termina, o que gostaria de saber? Por quê? (não sugerir formatos como gráfico ou relatório)

**Bloco 6 — Reação a um apoio durante a aula (H01, H02, H03 e turma pequena)**

> Ler: "Agora vou descrever uma ideia ainda em estudo. Não há resposta certa: comentários negativos ajudam tanto quanto os positivos. Imagine um programa que, durante a aula, mostra a você um sinal resumido do estado geral da turma, por exemplo se o grupo parece atento ou confuso, estimado a partir das câmeras dos alunos. O programa não mostra resultados individuais."

20. Em que situações algo assim poderia ajudar você, se puder? E em que situações poderia atrapalhar?
21. Se o sinal indicasse que a turma está confusa, mas você achasse que ela está acompanhando, o que você faria?
    - ↳ O que você precisaria saber sobre esse sinal para decidir se confia nele?
22. Pensando no tamanho das suas turmas, um resumo do grupo faria sentido? A partir de quantos alunos?
23. Como você imagina que seus alunos reagiriam a isso? O que você precisaria explicar a eles antes de usar?
24. Você usaria algo assim nas suas aulas? Em que condições não usaria?

**Encerramento**

25. Há algo sobre acompanhar a turma em aulas on-line que eu não perguntei e que você acha importante?
26. Você gostaria de receber a síntese dos resultados? [registrar sim/não]

> Ler: "Muito obrigado(a) pela participação. Suas respostas serão usadas apenas neste trabalho, identificadas por código. Se quiser retirar sua participação, basta nos avisar até o fim da disciplina."

**Ficha de registro (preencher logo após cada entrevista)**

| Campo | Registro |
|---|---|
| Código do participante | E__ |
| Data e duração | |
| Perfil (faixas do Bloco 1) | |
| Autorizou gravação de áudio? | sim / não |
| Situação relatada no incidente crítico (resumo em 3 a 5 linhas, sem nomes) | |
| Sinais usados para perceber a turma | |
| Decisão tomada e critério declarado | |
| Momento em que descobriu se a decisão funcionou | |
| Reação à ideia do Bloco 6 (pontos positivos, negativos e condições) | |
| Trechos marcantes (citação literal, anonimizada) | |
| Observações do entrevistador (o que surpreendeu, dúvidas para a próxima entrevista) | |

#### Como os dados serão analisados

1. **Transcrição e codificação temática:** as transcrições anonimizadas serão codificadas por dois integrantes da equipe, primeiro com códigos definidos a partir das hipóteses (sinais usados, critério de decisão, custo de reforçar, confiança em sinal externo, tamanho da turma, privacidade dos alunos, uso pós-aula) e depois com códigos novos que surgirem das falas. Divergências de codificação serão discutidas até consenso.
2. **Reconstrução dos incidentes:** cada relato do Bloco 3 será organizado nos sete elementos do cenário (contexto, atores, objetivos, planejamento, ações, eventos, avaliação) e comparado com o Cenário C05 e com a T03, indicando o que se confirmou, o que mudou e o que não apareceu.
3. **Matriz de hipóteses:** para cada hipótese, será registrado quantos participantes trouxeram evidência a favor, contra ou com nuance, com trechos de apoio:
   - **H01** é **sustentada** se a maioria relatar dificuldade real de perceber a turma durante a aula e descrever situações em que um sinal no momento teria mudado a decisão; é **refutada** se os relatos mostrarem que o problema é raro ou que o exercício posterior já resolve; é **refinada** se a necessidade aparecer só em certos momentos (conteúdo novo, tela compartilhada).
   - **H02** é **sustentada** se os participantes disserem que precisariam de alguma indicação de confiança para decidir diante de um sinal contrário à própria percepção; é **refinada** se preferirem essa informação só depois da aula.
   - **H03** (visão do comunicador) é **sustentada** se os professores anteciparem desconforto dos alunos ou disserem que precisariam explicar o funcionamento antes de usar; a visão dos próprios participantes depende dos demais instrumentos.
   - **Hipótese sobre turmas pequenas** é **refutada** se professores de turmas pequenas afirmarem que já percebem bem a turma ou que um resumo do grupo não faz sentido nesse tamanho.
4. **Uso no design:** os achados alimentam a atualização da persona P02, do Cenário C05 (as hipóteses de refinamento Q1 a Q7 passam a fatos ou são reescritas), da T03 e dos requisitos do Semáforo Cognitivo (posição durante o compartilhamento, exibição de confiança, número mínimo de participantes, aviso aos alunos). O resultado será registrado em `RASTREABILIDADE.md`.
5. **Limitações a relatar:** amostra pequena e por conveniência, possível viés de memória no relato do incidente e influência do Bloco 6, que apresenta uma ideia de solução; por isso, ele vem por último e suas respostas são analisadas separadamente das necessidades relatadas nos Blocos 2 a 5.

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
