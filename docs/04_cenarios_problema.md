# Entrega 4 — Cenários de análise/problema

**Data:** {{30/08/2026}}  
**Status:** ✅ Concluido 
**Responsabilidade:** 1 solução completa por integrante

## Objetivo da atividade

Descrever situações atuais em que o usuário tenta alcançar um objetivo e encontra dificuldades. O cenário de análise/problema deve tornar visível **o contexto, os atores, as ações e as rupturas**, sem antecipar a interface que será projetada.

> **Regra central:** cenário de problema é a “história do problema”. Se o texto já diz “o sistema mostra”, “o aplicativo resolve” ou descreve botões/telas futuras, provavelmente está misturando problema com solução.

Sempre que possível, o cenário deve aprofundar uma **situação concreta já registrada na Entrega 1**.

### Quando o TCC não possuía interface

O cenário continua sendo uma história de **problema/atividade humana**, não uma história do futuro sistema. Descreva como o profissional realiza hoje uma atividade semelhante ou como lida atualmente com dados, resultados, configurações, logs, decisões e limitações que o tema do TCC pretende apoiar.

Exemplo: em vez de “o DBA abre o novo dashboard e executa o algoritmo”, descreva “o DBA precisa investigar uma consulta lenta, reúne informações em ferramentas distintas, compara planos manualmente e tem dificuldade para estimar o impacto de uma mudança”.

A interface da disciplina aparecerá somente depois, nos cenários de interação.

Se o integrante escolher um novo problema/situação, explique por que ele passou a ser relevante e indique a evidência que motivou sua inclusão.

## Cenário C01 — Dificuldade em interpretar a reação do cliente durante uma apresentação comercial on-line

**Autor(a):** Matheus Ferreira de Freitas — RA 22.125.085-5  
**Persona(s) relacionada(s):** P04 — Manoel Gomes  
**Necessidade relacionada:** R01 e R02 da matriz de rastreabilidade: perceber durante a reunião se o cliente está compreendendo e demonstrando interesse pela proposta, para ajustar o discurso quando necessário.  
**Origem do cenário:** a reunião comercial B2B **não** consta como situação concreta na Entrega 1, cujo relato principal (item 4.5) é uma aula por videoconferência. O cenário aprofunda a situação introduzida pela persona P04 na Entrega 3, estendendo o papel de "palestrante/apresentador" citado nos itens 2.2 e 7.2 da Entrega 1. Trata-se, portanto, de uma **nova situação cuja relevância para o projeto ainda precisa ser investigada** (dúvidas ?02 e ?03 da Entrega 1). O que ele compartilha com a situação da Entrega 1 é a atenção dividida durante o compartilhamento de tela (itens 4.2 e 5.3) e a ambiguidade do silêncio do grupo (itens 4.4 e 4.5).  
**Hipóteses ainda presentes:** H01 (utilidade de um sinal durante a própria sessão), H02 (quanto confiar em um sinal incompleto), H03 (clientes externos sendo classificados) e H04, já refinada na Entrega 2 (a diferenciação não está em "ter tempo real", e sim no tipo de sinal e de inferência).

### 1. Cenário inicial

Durante uma reunião comercial pelo Microsoft Teams, Manoel apresenta uma proposta para um grupo de clientes enquanto compartilha sua tela. Ao mesmo tempo, tenta acompanhar as reações dos participantes para entender se eles estão compreendendo e demonstrando interesse no que está sendo apresentado.

Como a tela compartilhada reduz a visualização dos participantes, Manoel nem sempre consegue observar todos os clientes. Para tentar confirmar a compreensão, ele faz perguntas curtas, como “esse ponto ficou claro?” ou “faz sentido para a operação de vocês?”. Porém, nem todos respondem, e o silêncio pode significar compreensão, dúvida, desinteresse ou até uma objeção não verbalizada.

Com pouco tempo disponível e sem querer constranger os clientes com perguntas repetidas, Manoel precisa decidir se continua a apresentação, explica novamente algum ponto ou muda seu discurso com base em sinais incompletos.

Em alguns casos, ele interpreta a falta de reação como concordância e só descobre posteriormente, durante o follow-up ou após a recusa da proposta, que determinados pontos não haviam sido compreendidos ou aceitos pelo cliente.

### 2. Questões de refinamento

Antes de formular as perguntas, o cenário inicial foi separado pelos sete elementos característicos (Barbosa e Silva, 2010) para verificar o que ele já informa e o que ainda falta:

| Elemento | O que o cenário inicial já informa | Lacuna que a questão investiga |
|---|---|---|
| Ambiente/contexto | Reunião no Teams, tela compartilhada, grupo de clientes, pouco tempo | Pressões e recursos que condicionam a condução (quem define o tempo, apoio de colegas, segundo monitor, momento da pauta) |
| Atores | Manoel e "um grupo de clientes" | Quem são os participantes do lado do cliente, de quem depende a decisão e quem mais acompanha a reunião |
| Objetivos | Saber se o cliente compreende e demonstra interesse para ajustar o discurso | Subobjetivos e informações que Manoel usa para julgar se a reunião foi bem-sucedida |
| Planejamento | Precisa decidir entre continuar, reexplicar ou mudar o discurso | Com base em quê decide, que alternativas pesa e o que faz diante de sinais contraditórios |
| Ações | Apresenta compartilhando a tela e faz perguntas curtas | Outras ações usadas para obter reação e a ordem em que acontecem |
| Eventos | Silêncio após a pergunta; recusa descoberta no follow-up | Acontecimentos durante a reunião que mudam o rumo da apresentação |
| Avaliação | Às vezes interpreta a falta de reação como concordância | Como julga, ainda na reunião, se a decisão funcionou e como compara depois com o resultado |

Cada questão investiga uma informação **ainda ausente** do cenário inicial. Nenhuma delas foi respondida até o momento: as fontes indicadas são formas futuras de obtenção.

| # | Elemento | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|---|
| Q1 | Ambiente/contexto | Quais pressões (tempo definido pelo cliente, meta do período, concorrência) e quais recursos (segundo monitor, colega de pré-vendas na reunião, material de apoio) estão presentes na reunião, e em que momentos da pauta a dificuldade de observar o grupo pesa mais? | Define as condições sob as quais qualquer apoio à percepção do grupo teria de funcionar, sem supor que toda reunião comercial é igual. | Entrevista com vendedores B2B e observação de reuniões comerciais gravadas, com autorização. |
| Q2 | Atores | Quem participa do lado do cliente (decisor, usuário técnico, comprador), de quem depende a decisão de compra e alguém do lado de Manoel acompanha a reunião ajudando a observar os participantes? | A reação que importa pode ser a de uma pessoa específica, e não a média do grupo; isso muda o que precisa ser percebido. | Entrevista com vendedores e levantamento da composição típica das reuniões no CRM da empresa. |
| Q3 | Objetivos | Além de verificar compreensão e interesse, que resultados Manoel persegue na reunião (identificar objeções, avançar para a próxima etapa, cumprir a pauta) e que informações ele precisa ter em mãos para considerar a reunião bem-sucedida? | Separa a necessidade de "ler a reação" de outros objetivos que competem pela atenção dele durante a fala. | Entrevista semiestruturada com vendedores B2B. |
| Q4 | Planejamento | Com base em quê Manoel decide, no momento, entre continuar, reexplicar ou mudar o discurso? Quais alternativas considera, que critério usa para não interromper a reunião e o que faz quando alguns clientes reagem bem e outros ficam em silêncio? | Torna visível o raciocínio que transforma o objetivo em ação, que é justamente o que um apoio à decisão precisaria respeitar. | Entrevista com vendedores a partir de exemplos de reuniões reais (técnica de incidentes críticos). |
| Q5 | Ações | Além das perguntas curtas, que outras ações Manoel realiza para obter reação do cliente (pausar o compartilhamento de tela, chamar alguém pelo nome, pedir que o cliente descreva a própria operação, propor uma demonstração) e em que ordem elas costumam ocorrer? | Revela o repertório atual de estratégias e seu custo em tempo e constrangimento, antes de qualquer solução nova. | Observação de reuniões comerciais e entrevista com vendedores. |
| Q6 | Eventos | Quais acontecimentos durante a reunião fazem Manoel mudar o rumo da apresentação (pergunta inesperada, participante que sai ou desliga a câmera, objeção explícita, aviso de que o tempo está acabando, resposta no chat) e como ele reage a cada um? | Eventos externos competem com a observação do grupo e definem quando a decisão precisa ser tomada. | Observação de reuniões e entrevista com vendedores. |
| Q7 | Avaliação | Como Manoel avalia, ainda na reunião, se a decisão de reforçar ou seguir funcionou? Que sinais considera como confirmação de que o cliente entendeu e como registra as percepções para compará-las depois com o resultado do follow-up? | Mostra como ele julga o próprio desempenho e onde a avaliação atual falha, o que explica a descoberta tardia das objeções. | Entrevista com vendedores e análise de registros de follow-up (e-mails e anotações no CRM), com autorização. |

### 3. Cenário refinado

> Como ainda não foram realizadas entrevistas ou observações com vendedores reais, os trechos acrescentados abaixo são **hipóteses de refinamento**, identificadas pela questão e pelo elemento a que respondem. Eles não devem ser lidos como fatos sobre usuários reais; quando a investigação for feita, cada hipótese será confirmada, refutada ou reformulada. O texto do cenário inicial foi mantido.

Durante uma reunião comercial pelo Microsoft Teams, Manoel apresenta uma proposta para um grupo de clientes enquanto compartilha sua tela. **[HIPÓTESE DE REFINAMENTO — Q1 / Ambiente-contexto: o tempo da reunião costuma ser definido pelo cliente e ficar entre 30 e 45 minutos; Manoel pode usar apenas a tela do notebook, sem segundo monitor, e quase sempre está sozinho do lado da empresa, de modo que a dificuldade de observar o grupo pesa mais nos trechos de preço e condições comerciais, quando ele mais precisa da reação do cliente.]** Ao mesmo tempo, tenta acompanhar as reações dos participantes para entender se eles estão compreendendo e demonstrando interesse no que está sendo apresentado. **[HIPÓTESE DE REFINAMENTO — Q2 / Atores: do lado do cliente podem participar um decisor, um responsável técnico e um comprador, nem sempre apresentados no início; a decisão tende a depender do decisor, que pode ser justamente quem menos se manifesta durante a reunião.]**

**[HIPÓTESE DE REFINAMENTO — Q3 / Objetivos: além de verificar compreensão e interesse, Manoel pode estar tentando identificar objeções antes que elas se consolidem e garantir um próximo passo (uma visita, uma prova de conceito ou uma proposta formal); para considerar a reunião bem-sucedida, ele precisaria saber quais pontos geraram dúvida e quem precisa ser convencido.]**

Como a tela compartilhada reduz a visualização dos participantes, Manoel nem sempre consegue observar todos os clientes. Para tentar confirmar a compreensão, ele faz perguntas curtas, como “esse ponto ficou claro?” ou “faz sentido para a operação de vocês?”. **[HIPÓTESE DE REFINAMENTO — Q5 / Ações: quando a pergunta curta não traz resposta, ele pode chamar uma pessoa pelo nome, pedir que o cliente descreva como faz aquilo hoje na própria operação ou oferecer uma demonstração; interromper o compartilhamento de tela para olhar a grade de vídeo tende a ser a última opção, por quebrar o ritmo da apresentação.]** Porém, nem todos respondem, e o silêncio pode significar compreensão, dúvida, desinteresse ou até uma objeção não verbalizada. **[HIPÓTESE DE REFINAMENTO — Q6 / Eventos: acontecimentos como uma pergunta inesperada, um participante que desliga a câmera ou sai da chamada, uma objeção dita abertamente, uma mensagem no chat ou o aviso de que faltam poucos minutos podem fazer Manoel abandonar a sequência prevista e reorganizar o restante da apresentação.]**

Com pouco tempo disponível e sem querer constranger os clientes com perguntas repetidas, Manoel precisa decidir se continua a apresentação, explica novamente algum ponto ou muda seu discurso com base em sinais incompletos. **[HIPÓTESE DE REFINAMENTO — Q4 / Planejamento: a decisão pode se apoiar em quem reagiu (se o decisor demonstrou interesse, ele avança mesmo com os demais em silêncio), no tempo restante da pauta e na importância do ponto em questão; diante de sinais contraditórios, ele tende a seguir em frente e anotar o ponto para retomá-lo no follow-up, porque interromper a reunião tem custo imediato e a dúvida só tem custo depois.]**

Em alguns casos, ele interpreta a falta de reação como concordância e só descobre posteriormente, durante o follow-up ou após a recusa da proposta, que determinados pontos não haviam sido compreendidos ou aceitos pelo cliente. **[HIPÓTESE DE REFINAMENTO — Q7 / Avaliação: durante a reunião, Manoel pode considerar como confirmação uma resposta verbal, uma pergunta de detalhe ou um aceno visível na grade; depois, ele compara as anotações feitas ao final da reunião com o que o cliente escreve no e-mail de resposta, e é nessa comparação, dias depois, que percebe os pontos que interpretou errado.]**

### 4. Elementos extraídos

Os sete elementos característicos aparecem primeiro; recursos, problemas e consequências foram mantidos como complemento.

| Elemento | Evidência no cenário |
|---|---|
| Ambiente/contexto | Reunião comercial on-line pelo Microsoft Teams, com tela compartilhada durante quase toda a apresentação, tempo definido pelo cliente e Manoel sozinho do lado da empresa (parte hipotética: Q1). |
| Atores | Manoel, executivo de vendas B2B, e os clientes participantes; hipoteticamente um decisor, um responsável técnico e um comprador, com pesos diferentes na decisão (Q2). |
| Objetivos | Entender se os clientes estão compreendendo e demonstrando interesse para ajustar o discurso; hipoteticamente, também identificar objeções cedo e garantir um próximo passo (Q3). |
| Planejamento | Decidir entre continuar, reexplicar ou mudar o discurso com sinais incompletos; hipoteticamente, pesando quem reagiu, o tempo restante e a importância do ponto, e preferindo seguir em frente quando os sinais se contradizem (Q4). |
| Ações | Apresentar compartilhando a tela, observar os participantes visíveis, fazer perguntas curtas; hipoteticamente, chamar alguém pelo nome, pedir que o cliente descreva a própria operação, oferecer demonstração (Q5). |
| Eventos | Silêncio após a pergunta; recusa descoberta no follow-up; hipoteticamente, perguntas inesperadas, câmera desligada ou saída de participante, objeção explícita, mensagem no chat, aviso de tempo (Q6). |
| Avaliação | Interpretar a falta de reação como concordância; hipoteticamente, tratar resposta verbal, pergunta de detalhe ou aceno como confirmação e só comparar as anotações com o retorno do cliente dias depois (Q7). |
| Recursos/informações (complemento) | Câmeras dos participantes em miniatura, respostas verbais, perguntas, chat, tempo restante da reunião, anotações próprias e e-mail de follow-up. |
| Problemas/rupturas (complemento) | Visualização limitada dos participantes, silêncio ambíguo, sinais contraditórios, atenção dividida entre apresentação, clientes e cronograma, custo de interromper a reunião. |
| Consequências (complemento) | Incerteza sobre a compreensão e o interesse dos clientes, decisões de ritmo tomadas com pouca informação e objeções percebidas tarde demais, já no follow-up ou na recusa da proposta. |

### 5. Implicações para as próximas entregas

**Quais tarefas merecem análise?** Formuladas a partir do objetivo humano, e não de uma funcionalidade:

- Conduzir a apresentação enquanto percebe os sinais disponíveis sobre a reação dos clientes.
- Interpretar silêncio, respostas parciais e sinais contraditórios, decidindo o quanto confiar neles.
- Decidir, com pouco tempo e sem constranger o cliente, se continua, reforça ou reexplica um ponto da proposta (planejamento).
- Verificar, ainda na reunião, se a decisão tomada funcionou (avaliação).
- Registrar as percepções da reunião e revisá-las depois, comparando com o retorno do cliente no follow-up.

Na Entrega 5, a modelagem das tarefas deve incluir os passos de planejamento e de avaliação do Manoel, e não apenas as ações observáveis.

**Quais informações precisam ser coletadas?**

- Pressões e recursos presentes nas reuniões comerciais e em que trechos da pauta a observação do grupo é mais difícil (Q1).
- Composição do grupo do lado do cliente e de quem depende a decisão (Q2).
- Objetivos que competem com a leitura da reação durante a fala e critérios de sucesso da reunião (Q3).
- Critérios usados para decidir entre continuar, reforçar ou mudar o discurso, inclusive diante de sinais contraditórios (Q4).
- Repertório atual de ações para obter reação e seu custo em tempo e constrangimento (Q5).
- Eventos que alteram o rumo da reunião e como o vendedor reage a eles (Q6).
- Sinais considerados como confirmação de compreensão e forma de registro e comparação posterior (Q7).
- Se vendedores B2B, professores e instrutores compartilham as mesmas tarefas ou exigem recortes diferentes (dúvidas ?02 e ?03 da Entrega 1), o que decide se este cenário permanece no escopo prioritário.


## Cenário C02 — Dificuldade de Karol em perceber se a turma está acompanhando a aula on-line

**Autor(a):** Kayky Pires — 22.222.040-2  
**Persona(s) relacionada(s):** P01 — Karol Schrödinger  
**Necessidade relacionada:** Perceber, durante a aula, possíveis sinais de dificuldade da turma sem aumentar ainda mais sua carga de atenção.  
**Origem do cenário:** Situação derivada do contexto de ensino a distância já considerado na Entrega 1 e detalhada pela persona P01 na Entrega 3.  
**Hipóteses ainda presentes:** H01 e H02  

### 1. Cenário inicial

Karol é professora de Filosofia no ensino a distância e conduz suas aulas por videoconferência. Durante a explicação, precisa apresentar o conteúdo, acompanhar os slides, observar o chat e tentar perceber se os alunos estão acompanhando.

Como possui baixa a média familiaridade com ferramentas digitais, Karol procura manter sua atenção principalmente na explicação e utiliza os recursos básicos da plataforma. Em alguns momentos, observa a grade de vídeos e verifica o chat para tentar perceber como a turma está reagindo.

Porém, parte dos alunos permanece em silêncio, alguns deixam a câmera desligada e nem sempre surgem perguntas quando existe uma dificuldade. Isso faz com que Karol tenha dificuldade para distinguir se a turma está acompanhando, se está confusa ou se simplesmente não está participando.

Quando recebe poucos sinais dos alunos, ela precisa decidir se continua o conteúdo, repete uma explicação, utiliza outro exemplo ou faz uma pergunta para verificar a compreensão. Essa decisão acontece enquanto ainda precisa manter o ritmo da aula e cumprir o conteúdo planejado.

### 2. Questões de refinamento

| # | Elemento | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|---|
| Q1 | Ambiente/contexto | Em quais situações da aula Karol encontra maior dificuldade para observar os alunos enquanto explica o conteúdo? | Ajuda a entender quando a divisão de atenção se torna mais crítica e quais condições do ambiente interferem na percepção da turma. | Entrevista com professores de EAD e observação de aulas on-line. |
| Q2 | Atores | Como o comportamento dos alunos, como câmera desligada, silêncio ou pouca participação, influencia a forma como Karol interpreta a situação da turma? | Permite compreender como as ações dos demais participantes alteram a percepção da professora. | Entrevista com professores e observação de aulas. |
| Q3 | Objetivos | O que Karol considera mais importante descobrir quando tenta observar a reação da turma durante uma explicação? | Ajuda a separar necessidades diferentes, como verificar compreensão, atenção, participação ou necessidade de repetir um conteúdo. | Entrevista semiestruturada com docentes. |
| Q4 | Planejamento | Quando percebe poucos sinais da turma, quais alternativas Karol considera antes de decidir se continua ou modifica sua explicação? | Permite compreender o raciocínio utilizado para transformar a dúvida em uma decisão durante a aula. | Entrevista com professores utilizando exemplos de situações reais. |
| Q5 | Ações | O que Karol costuma fazer atualmente para verificar se os alunos compreenderam quando não consegue interpretar as reações disponíveis? | Revela as estratégias já utilizadas antes da introdução de qualquer nova solução. | Entrevista e observação contextual. |
| Q6 | Eventos | Quais acontecimentos durante a aula costumam fazer Karol reconsiderar se deve continuar o conteúdo, como uma pergunta inesperada, silêncio prolongado ou erro em uma atividade? | Ajuda a identificar eventos externos que alteram sua decisão durante a aula. | Observação de aulas e entrevistas com professores. |
| Q7 | Avaliação | Como Karol avalia se a decisão de repetir, continuar ou mudar a explicação realmente ajudou a turma? | Permite entender quais sinais ela utiliza depois de agir para julgar se a intervenção funcionou. | Entrevista e observação de momentos posteriores à intervenção. |

### 3. Cenário refinado

> Como ainda não foram realizadas entrevistas ou observações com usuários reais, os trechos acrescentados abaixo representam **hipóteses de refinamento** que deverão ser investigadas posteriormente.

Karol é professora de Filosofia no ensino a distância e conduz suas aulas por videoconferência. Durante a explicação, precisa apresentar o conteúdo, acompanhar os slides, observar o chat e tentar perceber se os alunos estão acompanhando.

Como possui baixa a média familiaridade com ferramentas digitais, Karol procura manter sua atenção principalmente na explicação e utiliza os recursos básicos da plataforma.

**[HIPÓTESE DE REFINAMENTO — Q1 / Ambiente-contexto: a dificuldade de acompanhar a turma pode aumentar principalmente quando Karol está compartilhando a tela ou explicando conteúdos mais complexos, pois sua atenção já está dividida entre apresentação, fala e chat.]**

Em alguns momentos, observa a grade de vídeos e verifica o chat para tentar perceber como a turma está reagindo. Porém, parte dos alunos permanece em silêncio, alguns deixam a câmera desligada e nem sempre surgem perguntas quando existe uma dificuldade.

**[HIPÓTESE DE REFINAMENTO — Q2 / Atores: Karol pode interpretar câmera desligada, silêncio ou pouca participação de maneiras diferentes, sem conseguir saber com segurança se esses comportamentos representam atenção, dúvida, desinteresse ou apenas preferência do aluno por participar menos.]**

Isso faz com que Karol tenha dificuldade para distinguir se a turma está acompanhando, se está confusa ou se simplesmente não está participando.

**[HIPÓTESE DE REFINAMENTO — Q3 / Objetivos: ao observar a turma, Karol pode estar principalmente tentando descobrir se precisa mudar sua explicação naquele momento, e não necessariamente identificar exatamente o estado de cada aluno.]**

Quando recebe poucos sinais dos alunos, ela precisa decidir se continua o conteúdo, repete uma explicação, utiliza outro exemplo ou faz uma pergunta para verificar a compreensão.

**[HIPÓTESE DE REFINAMENTO — Q4 / Planejamento: antes de mudar a explicação, Karol pode considerar fatores como dificuldade do conteúdo, tempo restante da aula, quantidade de perguntas recebidas e necessidade de cumprir o planejamento previsto.]**

**[HIPÓTESE DE REFINAMENTO — Q5 / Ações: quando permanece em dúvida, ela pode utilizar estratégias como fazer uma pergunta para a turma, pedir um exemplo, retomar brevemente o conteúdo ou aguardar uma atividade para observar se os alunos conseguem aplicar o que foi explicado.]**

Essa decisão acontece enquanto ainda precisa manter o ritmo da aula e cumprir o conteúdo planejado.

**[HIPÓTESE DE REFINAMENTO — Q6 / Eventos: acontecimentos como uma pergunta inesperada, várias respostas erradas em sequência ou um período prolongado sem interação podem fazer Karol interromper o plano inicial e reconsiderar sua condução.]**

**[HIPÓTESE DE REFINAMENTO — Q7 / Avaliação: depois de modificar sua explicação, Karol pode avaliar se a intervenção ajudou observando novas perguntas, respostas dos alunos ou o desempenho deles em uma atividade posterior.]**

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ambiente/contexto | Aula de Filosofia realizada por videoconferência, com compartilhamento de conteúdo e atenção dividida entre apresentação, chat e participantes. |
| Atores | Karol, professora responsável pela aula, e os alunos participantes da videoconferência. |
| Objetivos | Compreender se a turma está acompanhando o conteúdo e decidir se é necessário modificar a explicação. |
| Planejamento | Karol precisa considerar alternativas como continuar, repetir, usar outro exemplo ou verificar a compreensão, levando em conta o tempo e o conteúdo previsto. |
| Ações | Explicar o conteúdo, observar a grade de vídeos, acompanhar o chat, fazer perguntas e eventualmente repetir ou adaptar a explicação. |
| Eventos | Silêncio prolongado, câmera desligada, perguntas inesperadas, respostas erradas ou pouca interação podem alterar a condução da aula. |
| Avaliação | Karol precisa interpretar se os sinais disponíveis indicam necessidade de mudança e, depois de agir, avaliar se a intervenção ajudou a turma. |

### 5. Implicações para as próximas entregas

**Quais tarefas merecem análise?**

- Acompanhar sinais disponíveis enquanto conduz a aula.
- Interpretar se esses sinais indicam uma possível dificuldade da turma.
- Decidir se deve continuar, repetir ou mudar a explicação.
- Escolher uma forma de verificar a compreensão sem interromper excessivamente a aula.
- Avaliar se a ação tomada ajudou os alunos.

**Quais informações precisam ser coletadas?**

- Em quais momentos a atenção dividida mais prejudica a percepção da turma.
- Quais sinais professores de EAD consideram mais úteis ou confiáveis.
- Como interpretam silêncio, câmera desligada e pouca participação.
- Que alternativas consideram antes de modificar uma explicação.
- Que estratégias já utilizam para confirmar se houve compreensão.
- Quais acontecimentos fazem o professor mudar o planejamento durante a aula.
- Como avaliam se uma intervenção realmente funcionou.


## Cenário C03 — Aluno que não sabe como está sendo percebido numa aula online

**Autor(a):** Gustavo Bertoluzzi Cardoso - 22.123.016-2  
**Persona(s) relacionada(s):** P05 - Bruno D. Roger  
**Necessidade relacionada:** saber o que é feito com a imagem dele captada pela câmera e sentir que assistir aula não é a mesma coisa que estar sendo vigiado (necessidade registrada na persona P05)  
**Situação concreta da Entrega 1 relacionada:** seção 2.3, onde o participante da videochamada já tinha sido apontado como alguém que é afetado pela ferramenta mas não usa a interface  
**Hipóteses ainda presentes:** H03

### 1. Cenário inicial

Bruno é aluno do segundo ano de Ciência da Computação e tem duas disciplinas EAD nesse semestre. Numa segunda de manhã ele entra na aula de Cálculo pelo Teams um pouco atrasado, ainda terminando o café, e decide deixar a câmera desligada porque o quarto tá bagunçado e ele não quer aparecer assim pros colegas. A professora começa a explicar um assunto novo e, no meio da aula, comenta que gostaria que mais gente ligasse a câmera, porque assim ela consegue perceber se a turma tá acompanhando. Bruno fica na dúvida se liga ou não, porque não sabe se isso vai pesar de alguma forma na nota de participação dele, mas também não quer ficar exposto justo num dia que ele não entendeu direito o conteúdo da aula passada. Ele decide manter a câmera desligada e tentar acompanhar calado. Em um momento a professora pede pra alguém responder rápido uma pergunta no chat, Bruno demora pra digitar porque ainda tá processando o que foi perguntado, e três colegas respondem antes dele. Depois da aula ele fica sem saber se a professora reparou que ele participou pouco, se isso ficou só na impressão dela ou se tem algum jeito disso voltar contra ele de algum modo, e não tem com quem tirar essa dúvida.

### 2. Questões de refinamento

| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Por que Bruno decide manter a câmera desligada mesmo sabendo que a professora prefere que esteja ligada? | Revela o conflito real entre privacidade/constrangimento e medo de ser mal avaliado, que é o núcleo do problema | Entrevista com alunos reais de disciplinas EAD |
| Q2 | Como a professora hoje registra ou lembra quem participou pouco numa aula? | Mostra se já existe algum tipo de registro informal que afeta o aluno, ou se é só impressão subjetiva sem consequência real | Entrevista com professores, observação de uma aula |
| Q3 | O que Bruno considera "participar o suficiente" pra não se sentir mal avaliado? | Ajuda a entender se a ansiedade dele é proporcional a algum critério real ou só uma sensação sem base concreta | Entrevista com Bruno ou aluno equivalente |
| Q4 | Além da professora, quem mais poderia saber como Bruno se saiu naquela aula? | Revela o alcance real da exposição, coordenação do curso, colegas, sistema da instituição | Levantamento de política institucional da EAD |
| Q5 | Existe hoje algum canal pra Bruno perguntar depois como ele foi percebido na aula? | Mostra se a falta de transparência é total ou se já existe algum canal pouco usado | Entrevista com Bruno, checagem da plataforma usada pela instituição |

### 3. Cenário refinado

Bruno é aluno do segundo ano de Ciência da Computação e tem duas disciplinas EAD nesse semestre. Numa segunda de manhã ele entra na aula de Cálculo pelo Teams um pouco atrasado, ainda terminando o café, e decide deixar a câmera desligada porque o quarto tá bagunçado e ele não quer aparecer assim pros colegas. **[NOVO: Além disso, ele não teve tempo de estudar o conteúdo da aula passada direito, e prefere não se expor justo num dia que sabe que vai entender menos do que o normal (Q1)]**. A professora começa a explicar um assunto novo e, no meio da aula, comenta que gostaria que mais gente ligasse a câmera, porque assim ela consegue perceber se a turma tá acompanhando. **[NOVO: Hoje, quando isso acontece, o que a professora faz é só uma anotação mental, ela não usa nenhuma planilha ou sistema pra registrar quem participou pouco, mas às vezes comenta informalmente com a coordenação quando um aluno some da aula com frequência (Q2)]**. Bruno fica na dúvida se liga ou não a câmera, porque não sabe se isso vai pesar de alguma forma na nota de participação dele. **[NOVO: Pra ele, participar o suficiente seria pelo menos responder uma pergunta por aula ou reagir de alguma forma no chat, mas como isso nunca foi dito claramente por nenhum professor, é só uma régua que ele mesmo criou (Q3)]**. Ele decide manter a câmera desligada e tentar acompanhar calado. Em um momento a professora pede pra alguém responder rápido uma pergunta no chat, Bruno demora pra digitar porque ainda tá processando o que foi perguntado, e três colegas respondem antes dele. **[NOVO: Nenhum outro aluno vê isso diretamente, a única pessoa que teria essa percepção é a própria professora, mas a coordenação do curso pode ficar sabendo de forma indireta se a professora relatar baixa participação recorrente (Q4)]**. Depois da aula ele fica sem saber se a professora reparou que ele participou pouco, se isso ficou só na impressão dela ou se tem algum jeito disso voltar contra ele de algum modo. **[NOVO: Não existe nenhum canal formal pra ele perguntar isso depois, a única forma seria mandar e-mail direto pra professora perguntando como ele está indo, o que ele nunca fez porque acha que ia parecer estranho (Q5)]**, e segue pra próxima aula com a mesma dúvida de sempre.

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Bruno D. Roger (aluno), a professora da disciplina de Cálculo |
| Objetivo(s) | Acompanhar a aula e não ser mal interpretado por participar pouco ou manter a câmera desligada |
| Contexto | Aula EAD de graduação, câmera opcional, ambiente doméstico da manhã, plataforma Teams |
| Recursos/informações | Chat da plataforma, câmera, percepção subjetiva e informal da professora |
| Ações | Decidir ligar ou não a câmera, acompanhar a aula calado, responder devagar no chat |
| Problemas/rupturas | Bruno não sabe se sua baixa participação vai ser interpretada contra ele, e não existe nenhum canal claro pra saber como ele foi percebido depois |
| Consequências | Ansiedade durante a aula, incerteza que persiste depois dela, e possível tendência de evitar interação por medo de se expor |

### 5. Implicações para as próximas entregas

Precisa validar com alunos reais de disciplinas EAD se essa ansiedade sobre "como estou sendo percebido" é algo comum ou só uma impressão de Bruno. Também vale investigar com professores se realmente existe algum registro informal de participação que pode afetar o aluno, mesmo sem virar nota oficial. Isso tem relação direta com H03, porque reforça que qualquer ferramenta que classifique o comportamento da turma precisa pensar em transparência pro lado do participante, não só em utilidade pro lado do comunicador. Ainda não é hora de desenhar como essa transparência apareceria numa tela, isso fica pras próximas entregas.

## Cenário C04 — Dificuldade em identificar a compreenção e aprendizado durante treinamento online.

**Autor(a):** {{Rafael Dias - 22.222.039-4}}  
**Persona(s) relacionada(s):** P03 - Nathanael  
**Necessidade relacionada:** {{R01,R02}}  
**Situação concreta da Entrega 1 relacionada:** H01 - Tem necessidade de identificar como os grupos estão se sentindo durante os treinamentos.
**Hipóteses ainda presentes:** H01

### 1. Cenário inicial

Enquanto acontece um treinamento on-line, o profissional necessita identificar durante o treinamento como os demais membros do treinamento/video-conferencia estão conseguindo entender e aprender sobre o tema apresentado, nisso ele verifica suas cameras e chat da chamada.

Em diversos ambientes coorporativos o uso da camera não é obrigatorio e sem interações no chat, assim dificultando a identificação e analise so apresentador, sem conseguir identificar se estão prestando atenção ou confusos com o treinamento, impossibilitando uma ação imediata para repetir ou modificar o ritmo do treinamento.

### 2. Questões de refinamento

Use os tipos de questões/taxonomia definidos na aula. As perguntas devem revelar informações **ainda ausentes** do cenário, não repetir o que já foi respondido.

| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | O que o profissional considera importante para perceber a perca do engejamento do publico? | Ajuda identificar em quais pontos publico perde atenção assim facilitando a tomada de decição | Realizar conversa com os profissionais de treinamento para obter essas informação |
| Q2 | O que dificulta o profissional para entender o sentimento do publico durante o treinamento? | Vamos poder identificar qual maior bloqueio para o profissional e quais interpretações e ações a serem tomadas | Acompanhar os treinamentos on-line junto ao profissional |
| Q3 | Qual principal meio para o profissional utiliza para perceber se o publico esta acompanhando e entendendo o treinamento? | Ajuda entender quais informações são mais importantes e como extrair essas informações | Entrevista ao profissional e acompanhamento do treinamento on-line |
| Q4 | A quantidade de participantes dificulta a compreensão de como esta o publico? | Ajuda identificar melhor forma de demonstrar ao profissional como o publico esta durante o treinamento | Entrevista ao profissional e acompanhamento do treinamento on-line |

### 3. Cenário refinado

Reescreva o cenário incorporando as respostas. Marque o conteúdo novo de forma consistente (por exemplo, `**[NOVO: ...]**`).

Enquanto acontece um treinamento on-line, o profissional necessita identificar durante o treinamento como os demais membros do treinamento/video-conferencia estão conseguindo entender e aprender sobre o tema apresentado, nisso ele verifica suas cameras e chat da chamada, `**[NOVO: mas proprio publico não faz o uso desses meios durante o treinamento]**`. 

Em diversos ambientes coorporativos o uso da camera não é obrigatorio e sem interações no chat,`**[NOVO: esses são os principais meios que o profissional usa como para entender as reações do publico para cada tema e momento do treinamento]**`, assim dificultando a identificação e analise do apresentador, sem conseguir identificar se estão prestando atenção ou confusos com o treinamento, impossibilitando uma ação imediata para repetir ou modificar o ritmo do treinamento.

`**[NOVO: A falta de interação do publico com o profissional faz com que ele possa perder a atenção e engajamento durante o treinamento, gerando uma perca de aprendizado para o publico.]**`

`**[NOVO: E quando o volume do publico é muito grando, dificulta ainda mais para o profissional por não conseguir visualizar a camera de todos os membros da reunião, gerando um entendimento errado para o profissional sendo enviesado por uma pequena parcela que consegue visualizar.]**`

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Profissional de treinamento e treineiros |
| Objetivo(s) | Identificar perda de atenção e confusão durante o treinamento |
| Contexto | Treinamento realizado de forma online, com profissional de treinamento explicando e apresentando o tema enquanto consegue acompanhar a participação dos membros |
| Recursos/informações | Câmeras, chat, perguntas, reações da plataforma e expressões dos participantes. |
| Ações | Visualizar os membros, acompanhamento do chat, realizar perguntas, tira duvidas, explicar assuntos novamente quando necessario. |
| Problemas/rupturas | Cameras desligadas, pouca interação, grandes publicos no treinamento, e excesso de informação desnecessaria para o momento |
| Consequências | Inconsistencia com o resultado do modelo e duvida de qual ação tomar durante o treinamento. |

### 5. Implicações para as próximas entregas

Quais tarefas merecem análise? Quais informações precisam ser coletadas? **Não desenhe a solução ainda.**

**Quais tarefas merecem analise:**
 - Visualizar o engajamento dos participantes do treinamento.
 - Identificar momentos de alto nivel de duvida, confusão e desinteresse
 - Decisão para a tomada de ações durante o treinamento, como repetir, tirar duvidas, etc...

**Quais informações precisam ser coletadas:**
 - Reações que o profissional utiliza como meio de identificação para avaliação
 - Quais ações o profissional toma durante momentos de silencio e pouca interação dos membros
 - Quais impactos são gerados com a faltas de interação e engajamento do publico

## Cenário C05 — Perceber tarde demais que a turma pequena não acompanhou uma estrutura nova da aula de inglês

**Autor(a):** Isabella Vieira Silva Rosseto — 22.222.036-0  
**Persona(s) relacionada(s):** P02 — Camila Duarte  
**Necessidade relacionada:** R01, R02 — receber um sinal do estado geral da turma em tempo real, sem precisar checar cada rosto enquanto fala e compartilha a tela (necessidade registrada na persona P02)  
**Situação concreta da Entrega 1 relacionada:** itens 4.4 e 4.5, estendidos ao recorte de turma pequena (5 a 15 alunos) introduzido na Entrega 3 como hipótese nova a validar  
**Hipóteses ainda presentes:** H01, H02

### 1. Cenário inicial

Camila dá aula particular de inglês para uma turma de oito alunos, pelo Google Meet. Na metade da aula, ela compartilha a tela com um exercício de conversação e, ao mesmo tempo, tenta acompanhar a grade de vídeo reduzida que fica num cantinho da tela. Metade da turma está com a câmera desligada.

Ela introduz uma estrutura gramatical nova, um pouco mais complexa que o normal. Nota um silêncio maior que o de costume, mas não sabe se é porque estão concentrados ouvindo ou porque não entenderam. Pergunta "entenderam?" e alguns alunos respondem "sim" rapidamente, sem muita convicção. Como o tempo de aula é curto e o plano prevê ainda mais dois tópicos, ela segue em frente.

Só na aula seguinte, ao corrigir o exercício de casa, ela percebe que boa parte da turma errou justamente os exemplos que usavam aquela estrutura nova. Acaba gastando parte da aula seguinte revisando um conteúdo que já devia ter sido reforçado no momento em que a dificuldade apareceu.

### 2. Questões de refinamento

| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | O que leva Camila a interpretar aquele silêncio como "provavelmente entenderam" em vez de dúvida, no momento da aula? | Revela o critério informal que ela usa hoje pra decidir se segue em frente ou reforça o conteúdo | Entrevista com Camila ou professora de idiomas equivalente |
| Q2 | Mesmo numa turma pequena (5 a 15 alunos), por que ainda é difícil perceber a reação individual de cada aluno enquanto a tela está compartilhada? | Testa se o tamanho pequeno da turma realmente resolveria o problema sozinho, ou se o compartilhamento de tela é a barreira principal | Observação de uma aula com tela compartilhada |
| Q3 | O que Camila faz hoje, na prática, quando desconfia que alguém não entendeu mas não tem nenhuma confirmação clara? | Mostra a estratégia de contorno já usada, antes de qualquer ferramenta nova | Entrevista semiestruturada com Camila |
| Q4 | Quanto tempo, em média, passa entre o momento em que a dificuldade acontece na aula e o momento em que Camila descobre que ela existiu? | Dimensiona o atraso real entre o problema e a percepção dele, que é o núcleo da situação | Entrevista com Camila, comparando com o cronograma real das aulas |
| Q5 | Como o pouco tempo disponível entre uma aula e outra influencia a chance de Camila revisar o conteúdo antes do próximo encontro? | Relaciona a restrição de tempo já registrada na persona P02 com a consequência prática do atraso na percepção | Entrevista com Camila sobre a rotina entre aulas |

### 3. Cenário refinado

Camila dá aula particular de inglês para uma turma de oito alunos, pelo Google Meet. Na metade da aula, ela compartilha a tela com um exercício de conversação e, ao mesmo tempo, tenta acompanhar a grade de vídeo reduzida que fica num cantinho da tela. Metade da turma está com a câmera desligada.

**[NOVO: Mesmo pra quem está com a câmera ligada, a tela compartilhada reduz o vídeo de todo mundo a miniaturas pequenas, então Camila não consegue de fato ler a expressão de cada aluno enquanto explica. O problema não é só o tamanho da turma, é dividir atenção entre explicar, compartilhar e observar ao mesmo tempo (Q2)]**.

Ela introduz uma estrutura gramatical nova, um pouco mais complexa que o normal. Nota um silêncio maior que o de costume, mas não sabe se é porque estão concentrados ouvindo ou porque não entenderam. **[NOVO: Na falta de outro sinal, ela usa o silêncio "calmo" e a ausência de perguntas como indício de que entenderam, um critério que ela mesma reconhece como frágil, mas é o único que tem disponível na hora (Q1)]**. Pergunta "entenderam?" e alguns alunos respondem "sim" rapidamente, sem muita convicção. Como o tempo de aula é curto e o plano prevê ainda mais dois tópicos, ela segue em frente.

**[NOVO: Quando desconfia de algum aluno específico, hoje ela só tem como recurso perguntar diretamente pra pessoa ou esperar a próxima atividade prática pra ver se ele erra, mas fazer isso toda vez atrasa a aula e pode constranger quem realmente não entendeu (Q3)]**.

Só na aula seguinte, ao corrigir o exercício de casa, ela percebe que boa parte da turma errou justamente os exemplos que usavam aquela estrutura nova. **[NOVO: Entre o momento em que a dificuldade realmente aconteceu e o momento em que ela descobre isso, se passam de três a sete dias, o intervalo até a próxima aula daquela turma (Q4)]**. Acaba gastando parte da aula seguinte revisando um conteúdo que já devia ter sido reforçado no momento em que a dificuldade apareceu. **[NOVO: Como o intervalo entre as aulas já é curto e dividido entre preparar material novo e revisar o anterior, esse retrabalho de última hora reduz ainda mais o tempo que ela teria pra planejar a aula seguinte com calma (Q5)]**.

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Camila, professora de inglês, e os alunos da turma pequena |
| Objetivo(s) | Perceber, ainda durante a aula, se a turma está acompanhando uma estrutura nova, pra poder reforçar o conteúdo na hora certa |
| Contexto | Aula particular de inglês por videoconferência (Google Meet), turma pequena de 5 a 15 alunos, com tela compartilhada na maior parte do tempo |
| Recursos/informações | Grade de vídeo reduzida, câmeras parcialmente desligadas, respostas verbais rápidas e pouco convictas, exercício de casa corrigido na aula seguinte |
| Ações | Compartilhar tela, explicar o conteúdo, checar a grade de vídeo, perguntar "entenderam?", seguir o plano de aula, corrigir exercício na aula seguinte |
| Problemas/rupturas | Silêncio ambíguo, atenção dividida entre explicar e observar, resposta verbal pouco confiável, dificuldade só descoberta dias depois |
| Consequências | Retrabalho na aula seguinte, tempo de preparação reduzido, estrutura gramatical não reforçada no momento em que fazia mais diferença |

### 5. Implicações para as próximas entregas

**Quais tarefas merecem análise?**
- Perceber, durante a explicação de um tópico novo, se a turma está acompanhando.
- Decidir, com base em sinais incompletos, se reforça o conteúdo na hora ou segue o plano.
- Revisar, numa aula posterior, o que não ficou claro na aula anterior.

**Quais informações precisam ser coletadas?**
- Que critérios professores de turma pequena usam hoje pra interpretar silêncio como compreensão ou dúvida.
- Se a divisão de atenção entre compartilhar tela e observar a turma é, de fato, o gargalo principal, mais do que o tamanho da turma em si (ligado à hipótese nova sobre turmas pequenas, registrada na Entrega 3).
- Qual é, na prática, o intervalo entre o momento da dificuldade e o momento em que o professor descobre que ela existiu, e o quanto isso poderia ser antecipado (relacionado a H01).
- Como um sinal de confiança baixa ou alta nessa percepção mudaria a decisão do professor de parar ou seguir em frente (relacionado a H02).

## Checklist

- [x] Há um cenário completo por integrante.
- [x] Cada cenário tem título, ator, objetivo, contexto e problema.
- [x] O cenário possui origem rastreável na Entrega 1 ou justifica claramente a inclusão de uma nova situação.
- [x] O texto descreve a situação atual, sem antecipar a solução.
- [ ] Para TCC sem interface original, o cenário descreve uma prática humana plausível relacionada à contribuição técnica, e não “a falta de uma tela”.
- [x] Questões de refinamento acrescentam informação nova.
- [x] O refinamento mostra claramente o que foi adicionado/alterado.
- [x] Cenários são diferentes o suficiente para cobrir objetivos/problemas relevantes.
- [x] Cada cenário está ligado a persona/necessidade na matriz de rastreabilidade.

## Histórico de revisões

| Data | O que mudou | Motivação | Responsável |
|---|---|---|---|
| 16/10/2026 | C01: refinamento refeito pelos sete elementos característicos (uma questão por elemento, identificada), com tabela prévia do que o cenário inicial já informava; trechos novos do cenário refinado marcados como hipóteses de refinamento com o número da questão e o elemento; elementos extraídos reorganizados nos sete elementos formais (recursos, problemas e consequências mantidos como complemento); origem rastreável corrigida (P04/Entrega 3 e dúvidas ?02 e ?03, em vez de hipóteses); tarefas para a Entrega 5 formuladas a partir do objetivo humano, com planejamento e avaliação | Feedback do professor na Entrega 4 (itens 1 a 6, 8, 9 e 11) | Matheus Ferreira de Freitas |
