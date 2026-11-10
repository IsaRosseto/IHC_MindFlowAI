# Entrega 7 — Coleta de dados, necessidades e aspectos éticos

**Data:** {{20/10/2026}}  
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

### A01 — Kayky Pires

**Autor(a):** {{Kayky Pires - 22.222.040-2}}

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Perfil principal e frequência de condução de atividades por videoconferência | ?02 / ?03 | Caracterizar quem respondeu e evitar tratar contextos diferentes como equivalentes | Delimitar o público prioritário e as variações de contexto a investigar |
| Sinais e estratégias atualmente utilizados para perceber se o público acompanha o conteúdo, e dificuldade percebida nessa atividade | H01 | Investigar a experiência existente antes de apresentar uma solução | Verificar em quais situações existe necessidade de apoio ao comunicador |
| Efeito esperado de um indicador automático sobre a tomada de decisão e a atenção | H01 | Investigar tanto a utilidade percebida quanto a possibilidade de distração | Explorar se, quando e como apresentar um indicador durante a sessão |
| Momentos em que informações sobre o grupo seriam úteis e ações que o comunicador consideraria tomar | H01 | Relacionar a informação a situações e decisões, e não apenas a uma preferência visual | Priorizar momentos de apresentação da informação, preservando a decisão com o comunicador |
| Informações que o comunicador consultaria após a sessão, incluindo a possibilidade de não consultar nenhuma | R03 / ?03 | Verificar necessidades pós-sessão sem pressupor dashboard, relatório ou exportação | Definir conteúdo essencial do resumo e necessidade de detalhamento |
| Necessidade atual de selecionar ou reorganizar informações ao revisar registros e relatórios | H06 | Investigar uma necessidade anterior à proposta de personalização do MindFlow | Definir se opções de personalização merecem investigação adicional e quais problemas devem resolver |
| Importância atribuída à informação de confiança e preferência de representação | H02 | Investigar interesse e compreensão declarados, sem confundi-los com eficácia demonstrada | Explorar alternativas de apresentação da incerteza em testes posteriores |
| Conforto do próprio comunicador ao imaginar-se no papel de participante de uma análise de imagens | H03, visão do respondente | Conhecer a percepção pessoal dos comunicadores, sem atribuí-la aos estudantes ou ao público em geral | Levantar questões para aprofundar na coleta com participantes da análise |
| Informações desejadas antes de autorizar uma análise e preferência sobre agregação dos resultados | H03 | Identificar preocupações e necessidades de transparência | Orientar alternativas de aviso, explicação, controle e apresentação agregada |
| Benefícios percebidos, preocupações e motivos para evitar a ferramenta | H01 / H02 / H03 / H06 | Registrar críticas, dúvidas e necessidades não previstas nas alternativas | Revisar prioridades, conteúdo e propostas de interação |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Professores e docentes | Já ter conduzido aulas síncronas por videoconferência | Público prioritário ligado a P01 e P02 |
| Instrutores e facilitadores | Já ter conduzido cursos ou treinamentos por videoconferência | Perfil de contraste para investigar semelhanças e diferenças em relação ao ensino |
| Palestrantes e apresentadores | Já ter conduzido apresentações remotas para grupos | Perfil de contraste para investigar variações de atividade e linguagem |
| Comunicadores que conduzem reuniões de trabalho | Já ter conduzido reuniões por videoconferência | Perfil de contraste; sua inclusão não pressupõe que compartilhe as necessidades dos docentes |

#### Aspectos éticos

- **Consentimento:** apresentar o [termo de consentimento do I01](../instrumentos/termo-consentimento.md) antes das perguntas. Quem não aceitar não acessará o questionário.
- **Voluntariedade:** a pessoa poderá interromper antes do envio e deixar questões opcionais sem resposta. Somente o aceite e a pergunta inicial de elegibilidade serão obrigatórios.
- **Dados coletados:** respostas de alternativas, respostas abertas e registro do aceite. Não haverá captura ou processamento de imagem, áudio, vídeo ou tela nesta coleta.
- **Privacidade:** não solicitar nome, e-mail, identificação de estudantes ou instituição de trabalho. Conferir a configuração do Forms antes da aplicação e ajustar o termo se houver alguma identificação obrigatória imposta pelo ambiente institucional.
- **Respostas abertas:** orientar a não identificar terceiros; remover informações identificáveis antes de qualquer divulgação.
- **Acesso e descarte:** acesso restrito à equipe. Descartar os registros individuais ao término da disciplina, preservando sínteses e trechos anonimizados. Não enviar respostas individuais ao GitHub.
- **Interpretação:** tratar estados afetivo-cognitivos como estimativas na descrição da ferramenta. Não utilizar respostas para avaliação profissional ou punitiva.
- **Limites da retirada:** esclarecer que, após o envio sem identificação nominal, pode não ser possível localizar uma resposta individual para excluí-la.

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

### A03 — Gustavo Bertoluzzi

**Autor(a):** Gustavo Bertoluzzi Cardoso — 22.123.016-2

**Foco desta solução:** o **participante** da videochamada (persona P05, Cenário C03 e tarefa T04). A01 e A02 investigam o comunicador; a A03 investiga quem tem a imagem analisada, principalmente a hipótese H03 e o que a interface de transparência e participação precisa comunicar.

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Como o aluno decide hoje se liga a câmera e se participa (fatores, momentos, regras percebidas) | H03 / C03 (Q4) | Mostra o comportamento atual antes de qualquer análise automática; se a câmera já é pouco usada, o sinal do MindFlow será fraco | Como a interface trata câmeras desligadas e quantos participantes contribuem para o agregado |
| Que regras e consequências o aluno acredita existir sobre câmera e participação, e de onde tira essa informação | C03 (Q1, Q2) | Separa medo baseado em regra real de medo por falta de informação | Conteúdo do aviso de análise ativa e das informações de transparência |
| Grau de conforto com a análise automática da própria imagem durante a aula, e o que aumenta ou reduz esse conforto (agregação, processamento local, quem vê o resultado) | H03 | É o núcleo da hipótese: pode tornar o produto inviável ou exigir controles adicionais | Requisitos de consentimento, transparência e controle do participante |
| O que o aluno precisa saber antes de aceitar participar da análise e em que momento quer saber | H03 / T04 | Define o conteúdo mínimo e o momento do aviso (ao entrar, antes da aula, no plano de ensino) | Texto e momento do aviso; nível de detalhe das informações completas |
| Se o aluno quer poder pausar ou recusar a análise sem desligar a câmera e se isso mudaria seu comportamento | H03 / T04 (tarefas marcadas como [H]) | T04 supõe essas opções; é preciso saber se são desejadas e se seriam usadas | Manter, alterar ou remover as opções de pausa/recusa |
| Se o aluno gostaria de conferir depois o que foi processado sobre a aula e o que esperaria ver | C03 (Q7) / T04 (tarefa 4) | Verifica se o resumo de transparência pós-aula tem valor ou é dispensável | Inclusão e conteúdo do resumo de transparência |
| Como o aluno interpreta resultados agregados da turma e se acredita que eles podem identificá-lo, principalmente em turmas pequenas | H03 / H05 | Agregação é a principal proteção prevista; se não for percebida como proteção, a transparência precisa explicar melhor | Número mínimo de participantes e explicação sobre agregação |
| Vocabulário que o aluno usa para falar de "estar sendo analisado" (monitorado, avaliado, observado) | ?04 / H03 | Evita termos que aumentem a sensação de vigilância | Rótulos e textos da interface do participante |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Alunos de graduação que assistem aulas síncronas por videoconferência | Maiores de 18 anos, com pelo menos uma disciplina on-line síncrona no último ano | Corresponde diretamente à persona P05 (Bruno) e ao Cenário C03 |
| Alunos de cursos livres on-line, como idiomas, em turmas pequenas | Maiores de 18 anos, em turmas de até 15 alunos | Liga o participante ao contexto de P02 (Camila) e à hipótese H05 |
| Participantes de treinamentos corporativos on-line (contraste) | Funcionários que participaram de treinamento síncrono por videoconferência | Liga ao contexto de P03 (Nathanael), em que hierarquia e avaliação de desempenho podem aumentar o desconforto |

Critério de exclusão: menores de 18 anos e alunos que nunca participaram de aula síncrona on-line. Os grupos serão formados por perfil (não misturar alunos com funcionários), para que ninguém se sinta constrangido diante de colegas de outro contexto.

**Limitação da amostra:** o acesso mais fácil é a colegas da própria instituição, o que tende a gerar uma amostra de estudantes de tecnologia, mais familiarizados com IA. Essa limitação será registrada, e os resultados não serão generalizados para todos os participantes de videoconferência.

#### Aspectos éticos

- **Sensibilidade do tema:** a coleta pede que os participantes falem sobre desconforto, vigilância e medo de avaliação. O roteiro não pede que ninguém revele notas, desempenho ou situações pessoais, e qualquer pergunta pode ser pulada.
- **Grupo focal e confidencialidade:** em grupo, o que um participante diz é ouvido pelos outros. No início, será combinado que nada do que for dito sai do grupo e que exemplos devem ser contados sem nomes de professores, colegas ou disciplinas. Mesmo assim, será informado que a equipe não consegue garantir a confidencialidade entre participantes.
- **Relação de poder:** os moderadores são estudantes da mesma instituição. Não serão convidados alunos de turmas em que um integrante da equipe seja monitor, e fica explícito que participar ou não, e o que se diz, não tem nenhuma consequência acadêmica.
- **Sem demonstração com câmera:** a sessão não usa nenhuma análise de imagem. A ideia do MindFlow é apresentada só por descrição e cartões de texto, e as câmeras dos participantes podem ficar desligadas.
- **Consentimento:** lido no início e registrado individualmente antes da discussão, conforme o [modelo de termo de consentimento](../instrumentos/termo_consentimento_modelo.md), incluindo autorização separada para gravação de áudio.
- **Minimização:** são registrados apenas curso/contexto em categoria ampla e faixa de experiência com aulas on-line. Não são coletados nome completo, RA, idade exata ou turma.
- **Gravação, anonimização e descarte:** somente áudio e somente se **todos** do grupo autorizarem; caso contrário, apenas anotações. Cada participante recebe um código (G1-P1, G1-P2...). O áudio é apagado após a transcrição revisada, as transcrições ao fim da disciplina, e no repositório entram só trechos anonimizados e a síntese.



### A04 — Rafael Dias

**Autor(a):** Rafael Dias — 22.222.039-4

**Foco desta solução:** o uso **após a aula** do MindFlow AI pelo docente EAD para revisar o resumo da reunião, interpretar os indicadores agregados, identificar momentos críticos e definir ajustes para aulas futuras. A A04 complementa as soluções anteriores ao investigar o valor do **dashboard histórico** e das **opções de personalização da visualização**.

A proposta está relacionada à tarefa de configurar o acompanhamento após uma aula, permitindo investigar se as necessidades de análise e personalização previstas no projeto correspondem às práticas reais dos docentes.

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Quais indicadores o docente considera mais úteis após a aula (engajamento, confusão, frustração, tédio e evolução ao longo do tempo) | H01 | Permite compreender quais informações são relevantes para a análise pós-sessão, sem pressupor que todos os indicadores tenham a mesma importância | Definir os indicadores principais do resumo e do dashboard histórico |
| Como o docente costuma avaliar uma aula após seu encerramento e quais ferramentas utiliza atualmente | H01 | Verifica se a revisão pós-aula já faz parte da rotina docente e quais necessidades não são atendidas pelas ferramentas existentes | Decidir se o dashboard histórico complementa práticas existentes e quais funcionalidades devem ser priorizadas |
| Em que nível de detalhe o docente deseja revisar a aula (resumo geral, intervalos de tempo ou momentos específicos) | H01 / H02 | Ajuda a compreender se um panorama geral é suficiente ou se existe necessidade de investigar acontecimentos específicos | Definir a granularidade da linha do tempo, dos gráficos e dos filtros |
| Como o docente identifica momentos críticos durante uma aula e quais evidências considera necessárias para interpretar esses acontecimentos | H02 | Permite entender quais informações tornam as classificações da IA compreensíveis e confiáveis | Definir se o sistema deve apresentar explicações, indicadores de incerteza e marcadores temporais |
| Que decisões o docente toma após identificar aumento de confusão, frustração ou queda de engajamento | H01 | Investiga se a análise posterior contribui para decisões pedagógicas concretas ou se os indicadores possuem apenas valor informativo | Definir funcionalidades de apoio à reflexão pedagógica e ao planejamento de aulas futuras |
| Se o docente considera útil comparar resultados de diferentes aulas, turmas ou períodos | H01 | Permite investigar se a comparação histórica representa uma necessidade real, em vez de presumir sua utilidade | Definir necessidade de comparações entre reuniões e filtros por período |
| Quais informações o docente gostaria de manter, ocultar ou reorganizar ao consultar o resumo de uma reunião | H01 / R03 | Investiga a necessidade de personalização prevista nas tarefas de IHC e verifica quais opções seriam utilizadas na prática | Definir o escopo da edição e personalização do resumo e do dashboard |
| Se o docente precisa registrar observações ou destacar acontecimentos específicos durante a análise | H01 | Permite compreender se a interpretação dos indicadores precisa ser associada a registros qualitativos do próprio docente | Definir necessidade de anotações, marcações e registros associados aos gráficos |
| Se o docente precisa exportar, compartilhar ou consultar posteriormente os resultados de uma aula | H01 | Verifica se a atividade de análise termina na consulta individual ou continua em processos de acompanhamento pedagógico | Definir necessidade de relatórios, exportação e compartilhamento |
| Como o docente interpreta os termos engajamento, tédio, confusão e frustração e quais considera mais claros | H02 | Permite verificar se o vocabulário técnico utilizado pelo sistema corresponde à linguagem e à compreensão do usuário | Refinar rótulos, descrições, legendas e explicações dos indicadores |
| Quais cuidados o docente considera necessários para evitar exposição individual dos estudantes | H03 | A análise histórica pode gerar riscos de identificação e utilização inadequada das informações | Definir nível de agregação, anonimização, transparência e regras de acesso aos resultados |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Docentes do ensino superior ou EAD | Conduzir aulas síncronas por videoconferência e possuir experiência com avaliação ou revisão de atividades após as aulas | Corresponde diretamente à persona P01, docente EAD, principal público da análise pós-sessão |
| Professores que utilizam dashboards ou relatórios educacionais | Ter experiência na consulta de indicadores de aprendizagem, participação ou desempenho de turmas | Permite compreender expectativas sobre apresentação de informações, filtros, gráficos e comparações |
| Docentes que não utilizam dashboards educacionais | Conduzir aulas on-line e realizar algum tipo de reflexão ou avaliação posterior, mesmo sem ferramentas específicas | Permite investigar se a ausência de dashboards decorre de falta de necessidade, dificuldade de uso ou desconhecimento das ferramentas |
| Instrutores corporativos ou facilitadores de treinamentos on-line | Conduzir treinamentos síncronos por videoconferência e revisar seus resultados após as sessões | Representa um público secundário e permite verificar se as necessidades de análise posterior também aparecem fora do contexto acadêmico |

**Critério de exclusão:** pessoas que nunca conduziram sessões síncronas por videoconferência ou que não possuem experiência com acompanhamento, reflexão ou avaliação de atividades realizadas após essas sessões.

**Limitação da amostra:** o acesso aos participantes tende a ocorrer por conveniência, principalmente entre docentes próximos à instituição e profissionais familiarizados com tecnologias educacionais. Essa característica pode favorecer respostas de pessoas com maior experiência em ferramentas digitais.

Para reduzir essa limitação, recomenda-se incluir docentes com diferentes níveis de familiaridade tecnológica e experiências variadas com análise de resultados educacionais.

As conclusões deverão considerar o perfil efetivamente alcançado, sem generalizar os resultados para todos os professores ou instrutores.

#### Aspectos éticos

- **Participação voluntária:** os participantes devem receber explicações claras sobre o objetivo da pesquisa, os dados coletados e sua utilização exclusivamente acadêmica. A participação poderá ser interrompida a qualquer momento, sem justificativa ou consequência.

- **Consentimento informado:** antes da coleta, deve ser apresentado o termo de consentimento previsto no projeto, esclarecendo os procedimentos da pesquisa, a finalidade das respostas e as condições de armazenamento das informações.

- **Privacidade dos estudantes:** como a investigação envolve relatos sobre aulas e indicadores de comportamento, os participantes devem ser orientados a não mencionar nomes de estudantes, turmas identificáveis ou informações que permitam reconhecer indivíduos.

- **Proteção dos docentes:** as respostas não devem ser utilizadas para avaliar ou comparar o desempenho profissional dos participantes. A pesquisa busca compreender necessidades de interação e não julgar práticas pedagógicas.

- **Interpretação dos indicadores:** os estados afetivo-cognitivos estimados pelo MindFlow AI não devem ser tratados como diagnósticos, avaliações definitivas ou medidas individuais de aprendizagem. Os indicadores representam estimativas que precisam ser interpretadas considerando o contexto da aula.

- **Minimização dos dados:** devem ser coletadas somente informações necessárias para compreender as necessidades dos usuários. Dados como nome completo, instituição, idade exata e identificação dos estudantes não são necessários para a análise.

- **Anonimização e armazenamento:** os participantes devem ser identificados por códigos, como R01, R02 e R03. As respostas devem permanecer em ambiente com acesso restrito à equipe responsável pelo estudo.

- **Gravações:** qualquer gravação de áudio deverá ocorrer somente com autorização específica. Caso o participante não autorize, a coleta poderá ser realizada exclusivamente por anotações.

- **Descarte das informações:** gravações devem ser excluídas após a transcrição e conferência. Os registros individuais deverão ser descartados ao final da disciplina ou quando deixarem de ser necessários, mantendo-se apenas resultados agregados e anonimizados.

- **Uso responsável dos resultados:** as descobertas deverão apoiar decisões de design relacionadas à compreensão, personalização e utilização dos indicadores, sem incentivar mecanismos de vigilância ou avaliação punitiva de estudantes e docentes.


## Parte B — ferramentas de coleta

> Cada integrante deve preparar uma técnica/instrumento completo. As técnicas devem ser diferentes entre si e **questionário deve estar entre as técnicas escolhidas**, conforme o enunciado da disciplina.

### Instrumento I01 — Questionário

**Autor(a):** Kayky Pires — 22.222.040-2  
**Técnica:** Questionário on-line  
**Objetivo:** Investigar como comunicadores percebem o estado do público durante videoconferências, quais informações consideram úteis durante e após a sessão e suas percepções sobre confiança da IA e privacidade.  
**Público:** Professores, instrutores, palestrantes e outros comunicadores que conduzem atividades por videoconferência.

#### Procedimento padronizado de aplicação

1. **Preparação:** configurar o formulário com o consentimento e as perguntas documentadas neste instrumento. Conferir se o registro de nome ou e-mail está desativado ou se corresponde às condições informadas no termo.

2. **Piloto:** realizar um preenchimento para verificar clareza, duração, alternativas e condições de navegação. Registrar eventuais ajustes antes da aplicação com o público definido.

3. **Recrutamento:** convidar pessoas com experiência na condução de atividades por videoconferência, priorizando docentes e incluindo outros comunicadores como perfis de contraste. Registrar os canais e o período de divulgação.

4. **Consentimento:** apresentar o [termo de consentimento do I01](../instrumentos/termo-consentimento.md) antes das perguntas. Se a pessoa não concordar em participar, encerrar o formulário.

5. **Elegibilidade:** apresentar a pergunta inicial sobre a experiência de condução. Se a pessoa nunca tiver conduzido uma atividade por videoconferência, agradecer e encerrar o preenchimento.

6. **Aplicação:** apresentar as perguntas na ordem documentada, sem orientar quais respostas escolher. Diferenciar questões de escolha única, seleção múltipla e resposta aberta. Apenas o consentimento e a identificação da elegibilidade serão obrigatórios.

7. **Encerramento:** agradecer e informar que as respostas serão utilizadas para fins acadêmicos. Manter disponível o contato da equipe indicado no termo.

8. **Registro e armazenamento:** registrar o número de respostas elegíveis e os perfis alcançados, separando eventuais respostas do piloto. Manter os registros individuais com acesso restrito à equipe e seguir o descarte previsto no termo.

#### Instrumento

[**Link do formulário I01**](https://forms.cloud.microsoft/r/fHf6y8q6ZK)

#### Como os dados serão analisados

1. **Organização da base:** separar as respostas do piloto das respostas da aplicação. Considerar na análise somente os registros de pessoas que aceitaram participar e atendem ao critério de experiência de condução. Registrar respostas ausentes por pergunta e remover informações identificáveis eventualmente mencionadas nos campos abertos.

2. **Caracterização dos respondentes:** utilizar Q1 e Q2 para descrever o perfil principal e a frequência de condução de atividades por videoconferência. Comparações entre perfis serão exploratórias e deverão informar a quantidade de respondentes de cada grupo.

3. **Perguntas fechadas:** apresentar contagens e proporções de cada alternativa, utilizando como referência o número de respostas válidas da pergunta. Nas questões de seleção múltipla, informar que a soma das proporções pode ultrapassar 100%. Respostas ausentes serão apresentadas separadamente.

4. **Perguntas abertas:** analisar Q15 e Q16 por codificação temática, agrupando conteúdos relacionados a benefícios, distração, confiança, privacidade, revisão pós-sessão e organização da informação. Preservar críticas e opiniões divergentes, utilizando apenas trechos sem identificação pessoal.

5. **Relação com as hipóteses e necessidades:**
   - **H01 — Q3 a Q7:** investigar sinais utilizados atualmente, dificuldade percebida, utilidade esperada, possíveis distrações e ações consideradas pelo comunicador.
   - **H02 — Q10 e Q11:** identificar a importância atribuída à informação de incerteza e as preferências de apresentação.
   - **H03 — Q12 a Q14:** investigar o conforto pessoal dos comunicadores ao imaginar-se como participantes, suas necessidades de informação e preferências sobre agregação.
   - **H06 — Q9:** investigar se existe uma necessidade atual de selecionar ou reorganizar informações durante a revisão de registros e relatórios.
   - **R03 e ?03 — Q6 e Q8:** identificar momentos de consulta e informações consideradas relevantes após a sessão.
   - As respostas abertas poderão complementar essas relações ou revelar necessidades não previstas.

6. **Interpretação:** distinguir relatos sobre práticas atuais de opiniões sobre uma ferramenta hipotética. Interesse declarado não comprova utilidade real ou ausência de distração. Preferência por um formato não demonstra sua compreensão, e a opinião dos comunicadores não substitui a coleta com alunos e demais participantes prevista em I03. As evidências serão confrontadas com os outros instrumentos antes de sustentar, contrariar ou refinar as hipóteses.

7. **Uso no design:** relacionar os achados às decisões sobre apresentação dos indicadores, explicações, ajuda, revisão pós-sessão e personalização. Registrar a origem da evidência, a interpretação e a decisão em `RASTREABILIDADE.md`, mantendo explícitas as questões ainda abertas.

8. **Limitações:** considerar a amostra por conveniência, o autorrelato e a influência da descrição da ferramenta. Os resultados não serão generalizados para todos os comunicadores. Caso sejam aplicadas versões diferentes do questionário, elas serão identificadas e analisadas separadamente.

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

### Instrumento I03 — Grupo focal com participantes de aulas on-line

**Autor(a):** Gustavo Bertoluzzi Cardoso — 22.123.016-2  
**Técnica:** grupo focal (discussão moderada em grupo, com cartões de texto como estímulo)  
**Objetivo:** entender como participantes de aulas e treinamentos on-line decidem sobre câmera e participação hoje, quanto conforto têm com a análise automática da própria imagem e o que precisariam saber e controlar para aceitá-la. Responde às questões Q1 a Q7 do Cenário C03 e investiga H03, H05 e o vocabulário do participante (?04).  
**Público:** perfis definidos na A03. Meta: 2 a 3 grupos de 4 a 6 participantes cada, um grupo por perfil (graduação; cursos livres; treinamento corporativo, se houver acesso).

**Por que grupo focal:** o tema (sentir-se observado, consentimento, privacidade) depende de normas sociais e de como as pessoas se comparam umas com as outras. A discussão em grupo revela concordâncias, divergências e argumentos que não aparecem em respostas individuais. É uma técnica diferente do questionário (I01) e da entrevista com comunicadores (I02), e ouve o outro lado da interação.

#### Procedimento padronizado de aplicação

1. **Preparação:** recrutar os participantes pelos critérios da A03 e formar grupos homogêneos por perfil. Agendar 60 minutos por videochamada, com câmera opcional. Definir um moderador (conduz) e um relator (anota falas, concordâncias e divergências). Preparar os quatro cartões de estímulo abaixo e testar a gravação de áudio. Atribuir códigos aos participantes.
2. **Apresentação e consentimento:** ler o texto de abertura sem alterações, combinar as regras do grupo, registrar o aceite de cada participante e perguntar se todos autorizam a gravação de áudio. Se alguém não autorizar, a sessão segue só com anotações.
3. **Aplicação:** seguir os blocos na ordem e com as mesmas perguntas em todos os grupos. O moderador garante que todos falem, não dá opinião, não defende o MindFlow e **só apresenta a ideia do sistema no Bloco 3**, depois de ouvir as experiências atuais. Os cartões são lidos em voz alta e mostrados como texto na tela.
4. **Encerramento:** fazer a pergunta final, agradecer, relembrar o uso dos dados e o combinado de confidencialidade.
5. **Armazenamento e anonimização:** no mesmo dia, moderador e relator preenchem a ficha de registro, revisam as anotações e transcrevem o áudio removendo nomes de pessoas, professores, disciplinas e instituições. Os arquivos ficam na pasta restrita da equipe com o código do grupo, e o áudio é apagado após a revisão.

#### Instrumento

**Texto de abertura (ler na íntegra)**

> Obrigado(a) por participar. Somos estudantes da FEI e, na disciplina de Interação Humano-Computador, estamos estudando como é participar de aulas e treinamentos on-line. Não existe resposta certa ou errada, e não estamos avaliando ninguém. Queremos ouvir opiniões diferentes, então sintam-se à vontade para discordar uns dos outros. A conversa dura cerca de 60 minutos e vocês podem deixar a câmera desligada. Por favor, não citem nomes de professores, colegas, disciplinas ou empresas. Combinamos que o que for dito aqui não sai do grupo, mas não conseguimos garantir isso entre os participantes, então compartilhem só o que se sentirem confortáveis. Qualquer pessoa pode não responder ou sair a qualquer momento, sem explicar o motivo. Todos autorizam a gravação apenas do áudio, que será apagado após a transcrição? [registrar a resposta de cada um] Todos concordam em participar? [registrar o aceite de cada um]

**Bloco 1 — Aquecimento (10 min)**

1. Cada um pode contar, em uma frase, que tipo de aula ou treinamento on-line costuma assistir e com que frequência?
2. Numa aula on-line típica, vocês costumam deixar a câmera ligada ou desligada? Do que isso depende?

**Bloco 2 — Experiência atual com câmera e participação (15 min) — Q1, Q2, Q4, Q5, Q6**

3. Que regras vocês conhecem sobre câmera e participação nas suas aulas ou treinamentos? Onde ficaram sabendo delas?
   - ↳ Alguma vez ficaram em dúvida se algo contava para a nota ou para a avaliação?
4. Quando vocês não querem aparecer ou falar, mas querem acompanhar, o que costumam fazer?
   - ↳ Chat, reações, microfone, perguntar depois: o que usam e o que evitam? Por quê?
5. Que situações durante a aula fazem vocês mudarem de ideia e ligarem a câmera ou se manifestarem?
6. Na opinião de vocês, quem fica sabendo de como cada um participou de uma aula on-line? O professor, a coordenação, a plataforma?

**Bloco 3 — Reação à ideia de análise automática (20 min) — H03, H05**

> Ler: "Agora vamos apresentar uma ideia que está sendo estudada. Comentários negativos ajudam tanto quanto os positivos, e não fomos nós que decidimos que ela vai existir." Mostrar um cartão de cada vez e perguntar: "O que vocês acham disso? Quem vê de outro jeito?"

- **Cartão A:** "Durante a aula, um programa estima a partir das câmeras se a turma, de forma geral, parece engajada, entediada, confusa ou frustrada. O professor vê só um resumo do grupo, não o resultado de cada aluno."
- **Cartão B:** "A análise da imagem acontece no computador de cada aluno; a imagem não é enviada para fora, só números do grupo."
- **Cartão C:** "Ao entrar na aula, aparece um aviso de que a análise está ativa, com a opção de ler mais sobre o que é e o que não é processado."
- **Cartão D:** "O aluno pode escolher não participar da análise, mesmo com a câmera ligada, e depois da aula pode ver um resumo do que foi processado."

7. (Cartão A) Como vocês se sentiriam numa aula com isso funcionando? O que mudaria no jeito de vocês participarem?
8. (Cartão A) Em uma turma pequena, de 5 a 10 pessoas, um "resumo do grupo" ainda protege cada aluno? E numa turma grande?
9. (Cartão B) Saber disso muda alguma coisa para vocês? Por quê?
10. (Cartão C) O que vocês gostariam de saber antes de a aula começar? E em que momento: no plano de ensino, ao entrar na aula, antes de ligar a câmera?
11. (Cartão D) Vocês usariam a opção de não participar? Em que situações? Ter essa opção muda a opinião sobre o Cartão A?
12. (Cartão D) Depois da aula, vocês teriam interesse em conferir o que foi processado? O que esperariam encontrar?
13. Que palavra vocês usariam para descrever estar numa aula com isso: acompanhado, observado, avaliado, monitorado, outra? Por quê?

**Bloco 4 — Fechamento (10 min) — Q3, Q7**

14. Para vocês, o que é "participar o suficiente" numa aula on-line?
15. Hoje, quando ficam em dúvida se foram mal avaliados por participar pouco, o que fazem? O que tranquilizaria vocês?
16. De tudo o que conversamos, o que seria indispensável para vocês aceitarem uma ferramenta assim? E o que faria vocês recusarem?

> Ler: "Muito obrigado(a). Lembrando: as respostas serão usadas só neste trabalho, identificadas por código, e o que foi dito aqui fica no grupo. Se alguém quiser retirar sua participação, basta nos avisar até o fim da disciplina."

**Ficha de registro (moderador e relator, logo após cada grupo)**

| Campo | Registro |
|---|---|
| Código do grupo e perfil | G__ — graduação / curso livre / treinamento corporativo |
| Data, duração e número de participantes | |
| Gravação de áudio autorizada por todos? | sim / não |
| Comportamento atual com câmera e participação (pontos de consenso) | |
| Regras e consequências percebidas | |
| Reação ao Cartão A (conforto, desconforto, condições) | |
| O que mudou com os Cartões B, C e D | |
| Opinião sobre turmas pequenas | |
| Palavras usadas para descrever a experiência | |
| Divergências relevantes dentro do grupo | |
| Trechos marcantes (citação literal, anonimizada, com código) | |
| Observações da dinâmica (alguém dominou a conversa, alguém ficou calado, temas evitados) | |

#### Como os dados serão analisados

1. **Codificação temática:** as transcrições ou anotações de cada grupo serão codificadas por dois integrantes da equipe, primeiro com códigos derivados das hipóteses (regras percebidas, estratégias de participação, conforto com a análise, efeito do processamento local, efeito do aviso, desejo de recusar, turma pequena, vocabulário) e depois com códigos novos que surgirem. Divergências serão discutidas até consenso.
2. **Análise por grupo e entre grupos:** para cada tema, registrar se houve consenso, divergência ou posição isolada dentro do grupo, e comparar os perfis (graduação, curso livre, corporativo). Uma opinião isolada não será tratada como posição do grupo.
3. **Efeito de cada cartão:** comparar a reação ao Cartão A com a reação depois dos Cartões B, C e D, para saber quais mecanismos (processamento local, aviso, recusa, resumo) realmente reduzem o desconforto e quais são indiferentes.
4. **Matriz de hipóteses:**
   - **H03** é **sustentada** se a maioria dos grupos expressar desconforto com o Cartão A que não desaparece com os Cartões B a D; é **refinada** se o desconforto diminuir com transparência e controle (indicando quais mecanismos são indispensáveis); é **refutada** se os grupos se mostrarem indiferentes à análise mesmo sem esses mecanismos.
   - **H05** é **sustentada** se os participantes considerarem o resumo do grupo protetor também em turmas pequenas, e **refutada** se disserem que, em poucos alunos, o resumo permitiria identificar quem está confuso.
   - **?04:** o vocabulário levantado orienta os rótulos da interface do participante.
5. **Uso no design:** os resultados alimentam a revisão da persona P05, do Cenário C03 (as hipóteses de refinamento Q1 a Q7 passam a fatos ou são reescritas), da tarefa T04 (manter ou remover as opções marcadas como [H]) e dos requisitos da interface de transparência (R04/F08). O resultado será registrado em `RASTREABILIDADE.md`.
6. **Limitações a relatar:** amostra pequena e por conveniência, efeito de conformidade em grupo (participantes acompanharem a opinião dominante), possível constrangimento em falar de desconforto diante de colegas e influência dos cartões, que descrevem uma solução. Por isso, o Bloco 2 (experiência atual) é analisado separadamente do Bloco 3.


### Instrumento I04 — Teste de usabilidade

**Autor(a):** Rafael Dias — 22.222.039-4  
**Técnica:** Teste de usabilidade moderado com protótipo.  
**Objetivo:** Verificar se os docentes conseguem consultar o resumo de uma aula, compreender os indicadores apresentados e personalizar a visualização sem dificuldades.  
**Público:** Professores e docentes que realizam aulas on-line por videoconferência. Meta: 5 participantes.

**Por que teste de usabilidade:** a técnica permite observar como os usuários interagem com o MindFlow AI e identificar dificuldades de navegação, compreensão dos indicadores e utilização das funcionalidades. Diferentemente das entrevistas e questionários, o teste avalia a execução prática das tarefas.

#### Procedimento padronizado de aplicação

1. **Preparação:** selecionar 5 docentes com experiência em aulas on-line e disponibilizar um protótipo do MindFlow AI com dados fictícios.
2. **Apresentação:** explicar o objetivo do teste, informar que a participação é voluntária e solicitar o consentimento.
3. **Execução:** apresentar as três tarefas abaixo, uma de cada vez, sem ensinar como realizá-las.
4. **Observação:** registrar se o participante conseguiu concluir cada tarefa, quais dificuldades encontrou e se precisou de ajuda.
5. **Encerramento:** fazer as perguntas finais e agradecer pela participação.
6. **Armazenamento:** identificar os participantes por códigos e manter os registros apenas para fins acadêmicos, com acesso restrito.

#### Instrumento

**Texto de abertura**

> Estamos realizando um teste para avaliar a facilidade de utilização do MindFlow AI. Você deverá realizar algumas tarefas em um protótipo do sistema.
>
> Não estamos avaliando seu desempenho, mas a facilidade de uso da interface. Sua participação é voluntária, e você pode interrompê-la quando desejar.
>
> Os resultados serão utilizados apenas para fins acadêmicos, sem identificação dos participantes.
>
> Você concorda em participar? [sim/não]

**Tarefa 1 — Consultar o resumo de uma aula**
> Imagine que você deseja revisar uma aula que já terminou. Encontre essa reunião no sistema e abra seu resumo.
**Observar:**
- Se encontra a reunião facilmente;
- Se consegue acessar o resumo;
- Se compreende os indicadores apresentados.

**Tarefa 2 — Personalizar a visualização**
> Imagine que você deseja modificar as informações exibidas no resumo. Encontre a opção de edição e realize uma alteração na visualização.
**Observar:**
- Se encontra a opção de editar;
- Se compreende as opções disponíveis;
- Se consegue realizar a alteração.

**Tarefa 3 — Salvar a personalização**
> Após modificar o resumo, salve suas alterações e confira se a visualização foi atualizada.
**Observar:**
- Se encontra o botão de salvar;
- Se compreende a confirmação do salvamento;
- Se identifica que as alterações foram mantidas.

#### Perguntas finais

1. Você achou fácil encontrar o resumo da aula?
2. Os indicadores apresentados foram claros?
3. Foi fácil encontrar e utilizar a opção de personalização?
4. Qual foi a maior dificuldade encontrada?
5. O que você melhoraria na interface?

#### Ficha de registro

| Campo | Registro |
|---|---|
| Código do participante | U__ |
| Data | |
| Experiência com aulas on-line | |
| Tarefa 1 — Consultar resumo | Sucesso / Com ajuda / Não concluiu |
| Tarefa 2 — Personalizar | Sucesso / Com ajuda / Não concluiu |
| Tarefa 3 — Salvar | Sucesso / Com ajuda / Não concluiu |
| Principais dificuldades | |
| Sugestões do participante | |

#### Como os dados serão analisados

1. **Conclusão das tarefas:** verificar quantos participantes conseguiram realizar cada atividade sem ajuda, com ajuda ou não conseguiram concluí-la.
2. **Dificuldades encontradas:** agrupar os problemas observados em navegação, interpretação dos indicadores e personalização da visualização.
3. **Avaliação das hipóteses:**
   - **H01:** investigar se o resumo apresenta informações consideradas úteis pelos docentes, como complemento à análise do uso em tempo real.
   - **H02:** identificar dificuldades na interpretação dos indicadores e na compreensão das classificações da IA.
   - **H03:** registrar eventuais preocupações espontâneas relacionadas à privacidade dos estudantes.
4. **Melhorias no design:** utilizar os resultados para ajustar a organização das telas, os indicadores apresentados e os controles de personalização.
5. **Limitações:** por envolver uma amostra pequena e um protótipo, os resultados servirão para identificar problemas de usabilidade, sem representar todos os possíveis usuários do MindFlow AI.
Os resultados serão registrados em `RASTREABILIDADE.md` para apoiar futuras melhorias na interface.


## Síntese

O conjunto de técnicas pretende reduzir quatro lacunas sobre os usuários, que até aqui só foram tratadas com evidência secundária (Entrega 2) e com artefatos de análise (personas, cenários e modelos de tarefa, Entregas 3 a 5):

1. **Se o problema do comunicador existe na prática:** se professores e instrutores realmente deixam de perceber dificuldades do grupo durante a sessão, que sinais usam hoje e como decidem reforçar ou seguir (I01 em escala; I02 em profundidade, a partir de aulas reais).
2. **Se o tipo de apoio imaginado faz sentido:** utilidade de um sinal durante a sessão, interesse por informação de confiança e o que de fato seria consultado depois da aula, sem pressupor dashboard, filtros ou relatórios (I01 e I02).
3. **Como o participante reage à análise da própria imagem:** conforto, regras percebidas, o que precisa saber e controlar, e se a agregação protege em turmas pequenas (I03, com apoio da A01).
4. **Se a interface proposta é fácil de utilizar:** verificar se docentes conseguem localizar uma reunião concluída, interpretar os indicadores, personalizar o resumo e salvar as alterações sem dificuldades, identificando problemas de navegação e compreensão (I04, por meio de teste de usabilidade).

| Técnica | Quem responde | Hipóteses/lacunas investigadas |
|---|---|---|
| I01 — Questionário (Kayky) | Comunicadores, em maior número | H01, H02, H03 (visão do comunicador), necessidades do Dashboard |
| I02 — Entrevista com incidente crítico (Isabella) | Professores, prioritariamente de idiomas com turmas pequenas | H01, H02, H05, ?02, ?04; questões Q1–Q7 do C05 |
| I03 — Grupo focal (Gustavo) | Participantes de aulas e treinamentos on-line | H03, H05, ?04; questões Q1–Q7 do C03 |
| I04 — Teste de usabilidade (Rafael Dias) | Docentes que realizam aulas on-line por videoconferência | H01, H02 e H03 (complementar); usabilidade do resumo, interpretação dos indicadores e personalização da visualização |

**O que se espera concluir após a análise dos dados:**

- **H01** deverá ficar **sustentada, refutada ou refinada** quanto à utilidade de um sinal durante a sessão; o resultado mais provável a testar é o refinamento para momentos específicos (conteúdo novo com a tela compartilhada). O I04 complementará essa análise verificando se o resumo pós-aula apresenta informações úteis e acessíveis aos docentes. Decide se o Semáforo continua como recorte principal e quais informações devem ser priorizadas no resumo.
- **H02** deverá ficar **sustentada ou refinada** quanto a mostrar a confiança durante a sessão ou só depois dela. O I04 permitirá identificar dificuldades na compreensão dos indicadores e de suas classificações. Decide a forma de comunicar incerteza e melhorar a clareza das informações apresentadas.
- **H03** deverá ficar **sustentada, refinada ou refutada**, incluindo quais mecanismos (processamento local, aviso, recusa, resumo) são indispensáveis. Decide o escopo da interface do participante (T04). O I04 poderá contribuir de forma complementar, caso sejam identificadas preocupações com privacidade durante o teste.
- **H05** (turmas pequenas) deverá ficar **sustentada ou refutada**, a partir da visão de professores (I02) e de participantes (I03).
- **?02, ?03 e ?04** deverão ser **parcialmente respondidas**: se professores, instrutores e apresentadores compartilham as mesmas tarefas e se os rótulos engajamento, tédio, confusão e frustração fazem sentido para eles. O I04 também contribuirá para avaliar a compreensão desses rótulos na interface.
- **Usabilidade do resumo e da personalização (I04):** deverá ser verificado se os docentes conseguem localizar uma reunião concluída, compreender os indicadores, personalizar a visualização e salvar as alterações sem dificuldades. Os problemas identificados orientarão melhorias na navegação, organização das informações e controles de edição.
- **H04** e **?01** não dependem desta coleta (foram tratadas na Entrega 2).

Quando os dados forem coletados e analisados, o histórico será atualizado em `RASTREABILIDADE.md` (seções 2 e 5), e as personas, cenários, tarefas e elementos da interface afetados serão revisados.

## Checklist

- [x] Hipóteses/lacunas prioritárias da Entrega 1 foram revisitadas (tabela inicial e Síntese).
- [x] Se o escopo de IHC foi derivado de TCC técnico, a coleta investiga a plausibilidade do usuário, tarefa e contexto adotados — o TCC já previa interface, mas I02 e I03 verificam se as situações de C05 e C03 acontecem na prática.
- [x] Perguntas não pressupõem que dashboard, CRUD, filtros ou relatórios sejam necessários; investigam a necessidade (I02, pergunta 19; I03, perguntas 10 a 12).
- [x] Cada dado a coletar responde uma dúvida concreta do projeto ou justifica outra necessidade de informação (colunas de hipótese e decisão em A01–A03).
- [x] Parte A identifica dados e perfis de coleta de forma específica (A01–A03).
- [x] Aspectos éticos são contextualizados para o projeto (A01–A03).
- [ ] Há uma técnica completa por integrante e técnicas distintas — três técnicas distintas prontas (questionário, entrevista e grupo focal); faltam as de Rafael e Matheus.
- [x] Questionário está incluído entre as técnicas (I01).
- [ ] Cada instrumento possui objetivo, público, procedimento e conteúdo integral — I02 e I03 têm o conteúdo integral no repositório; I01 tem apenas o link do formulário e precisa da cópia textual.
- [x] Perguntas evitam indução e coletam apenas dados necessários (I02 e I03 apresentam a ideia do sistema só no fim, com convite a críticas).
- [x] Está claro como os dados serão analisados e usados no design (seções de análise de I01–I03 e Síntese).
