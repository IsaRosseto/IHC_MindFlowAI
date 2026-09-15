# Entrega 4 — Cenários de análise/problema

**Data:** {{30/08/2026}}  
**Status:** 🟨 iniciada  
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
**Necessidade relacionada:** Perceber durante a reunião se o cliente está compreendendo e demonstrando interesse pela proposta, para ajustar o discurso quando necessário.  
**Situação concreta da Entrega 1 relacionada:** H01, H03 e H04, estendidas ao contexto de reuniões comerciais por videoconferência.  
**Hipóteses ainda presentes:** H01, H03 e H04  

### 1. Cenário inicial

Durante uma reunião comercial pelo Microsoft Teams, Manoel apresenta uma proposta para um grupo de clientes enquanto compartilha sua tela. Ao mesmo tempo, tenta acompanhar as reações dos participantes para entender se eles estão compreendendo e demonstrando interesse no que está sendo apresentado.

Como a tela compartilhada reduz a visualização dos participantes, Manoel nem sempre consegue observar todos os clientes. Para tentar confirmar a compreensão, ele faz perguntas curtas, como “esse ponto ficou claro?” ou “faz sentido para a operação de vocês?”. Porém, nem todos respondem, e o silêncio pode significar compreensão, dúvida, desinteresse ou até uma objeção não verbalizada.

Com pouco tempo disponível e sem querer constranger os clientes com perguntas repetidas, Manoel precisa decidir se continua a apresentação, explica novamente algum ponto ou muda seu discurso com base em sinais incompletos.

Em alguns casos, ele interpreta a falta de reação como concordância e só descobre posteriormente, durante o follow-up ou após a recusa da proposta, que determinados pontos não haviam sido compreendidos ou aceitos pelo cliente.

### 2. Questões de refinamento

| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Quais sinais Manoel considera mais confiáveis para identificar interesse, dúvida ou resistência do cliente durante a reunião? | Ajuda a entender como ele interpreta as informações disponíveis e quais sinais orientam suas decisões. | Entrevista com profissionais de vendas B2B e observação de reuniões comerciais. |
| Q2 | Em quais momentos da apresentação Manoel sente maior dificuldade para acompanhar a reação dos participantes? | Permite identificar situações de maior carga de atenção e disputa entre tarefas, especialmente durante o compartilhamento de tela. | Entrevista e observação contextual de reuniões on-line. |
| Q3 | Como Manoel interpreta situações em que alguns clientes respondem positivamente e outros permanecem em silêncio? | Ajuda a compreender como sinais diferentes ou contraditórios são transformados em significado durante a negociação. | Entrevista semiestruturada com vendedores. |
| Q4 | Que estratégias Manoel utiliza quando percebe pouca participação, mas não pode interromper constantemente a apresentação para perguntar ao cliente? | Revela práticas atuais usadas para contornar a falta de retorno sem constranger os participantes. | Observação de reuniões e entrevistas com profissionais da área comercial. |
| Q5 | Como o número de participantes e o tempo disponível para a reunião influenciam a capacidade de Manoel de acompanhar as reações do grupo? | Ajuda a identificar limites de atenção, tempo e quantidade de informação que precisam ser considerados na atividade.| Comparação entre reuniões com diferentes tamanhos de grupo e duração. |


### 3. Cenário refinado

Durante uma reunião comercial pelo Microsoft Teams, Manoel apresenta uma proposta para um grupo de clientes enquanto compartilha sua tela. Ao mesmo tempo, tenta acompanhar as reações dos participantes para entender se eles estão compreendendo e demonstrando interesse no que está sendo apresentado.

Como a tela compartilhada reduz a visualização dos participantes, Manoel nem sempre consegue observar todos os clientes. Para tentar confirmar a compreensão, ele faz perguntas curtas, como “esse ponto ficou claro?” ou “faz sentido para a operação de vocês?”.

**[NOVO: Manoel costuma considerar respostas verbais, perguntas espontâneas, expressões faciais visíveis e mudanças no nível de participação como os sinais mais úteis para interpretar a reação do cliente.]**

Porém, nem todos respondem, e o silêncio pode significar compreensão, dúvida, desinteresse ou até uma objeção não verbalizada. **[NOVO: Quando alguns participantes respondem positivamente e outros permanecem em silêncio, Manoel tem dificuldade para saber se aquela resposta representa realmente a percepção do grupo.]**

**[NOVO: A dificuldade aumenta principalmente enquanto ele compartilha a tela, explica pontos mais complexos da proposta ou precisa controlar o tempo restante da reunião, pois sua atenção fica dividida entre apresentação, clientes e cronograma.]**

Com pouco tempo disponível e sem querer constranger os clientes com perguntas repetidas, Manoel precisa decidir se continua a apresentação, explica novamente algum ponto ou muda seu discurso com base em sinais incompletos.

**[NOVO: Quando percebe pouca participação, ele costuma fazer perguntas rápidas, apresentar exemplos ou reforçar algum benefício da proposta, tentando obter uma reação sem interromper excessivamente o ritmo da reunião.]**

**[NOVO: Em reuniões com mais participantes ou duração reduzida, acompanhar individualmente as reações se torna ainda mais difícil, aumentando a incerteza sobre a percepção geral do grupo.]**

Em alguns casos, Manoel interpreta a falta de reação como concordância e só descobre posteriormente, durante o follow-up ou após a recusa da proposta, que determinados pontos não haviam sido compreendidos ou aceitos pelo cliente.



### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Manoel, executivo de vendas B2B, e os clientes participantes da reunião comercial. |
| Objetivo(s) | Entender se os clientes estão compreendendo e demonstrando interesse na proposta para ajustar sua apresentação quando necessário. |
| Contexto | Reunião comercial on-line pelo Microsoft Teams, geralmente com compartilhamento de tela e tempo limitado. |
| Recursos/informações | Câmeras dos participantes, respostas verbais, perguntas, expressões faciais, nível de participação e tempo restante da reunião. |
| Ações | Apresentar a proposta, observar os participantes, fazer perguntas curtas, interpretar reações, apresentar exemplos e reforçar pontos da proposta. |
| Problemas/rupturas | Visualização limitada dos participantes, silêncio ambíguo, sinais contraditórios, atenção dividida e dificuldade maior em reuniões com mais pessoas ou pouco tempo. |
| Consequências | Incerteza sobre a compreensão e o interesse dos clientes, podendo levar Manoel a continuar a apresentação sem perceber dúvidas ou objeções que surgem apenas posteriormente. |



### 5. Implicações para as próximas entregas

**Quais tarefas merecem análise?**

- Conduzir a apresentação enquanto acompanha as reações dos clientes.
- Identificar sinais de dúvida, interesse ou resistência durante a reunião.
- Fazer perguntas curtas para verificar compreensão e interesse.
- Interpretar respostas, silêncio e sinais contraditórios do grupo.
- Decidir quando continuar, reforçar ou reexplicar um ponto da proposta.
- Registrar percepções importantes para utilizar no follow-up.

**Quais informações precisam ser coletadas?**

- Quais sinais os vendedores consideram mais confiáveis para avaliar a reação dos clientes.
- Em quais momentos da reunião ocorre maior dificuldade de acompanhamento.
- Como o compartilhamento de tela afeta a observação dos participantes.
- Como o vendedor interpreta silêncio, pouca participação e respostas contraditórias.
- Quais estratégias utiliza atualmente para confirmar compreensão sem constranger o cliente.
- Como o número de participantes e o tempo disponível influenciam essa percepção.
- Como essas dificuldades afetam decisões durante a reunião e o follow-up posterior.


## Cenário C02 — Dificuldade em perceber o estado dos participantes durante uma aula on-line

**Autor(a):** {{Kayky Pires — 22.222.040-2}}  
**Persona(s) relacionada(s):** P01 - Karol 
**Necessidade relacionada:** {{R01}}  
**Situação concreta da Entrega 1 relacionada:** H01 — Utilidade de um indicador discreto do estado do grupo em tempo real 
**Hipóteses ainda presentes:** H01, H03

### 1. Cenário inicial

Durante uma aula por videoconferência, o professor precisa apresentar o conteúdo e, ao mesmo tempo, perceber como os alunos estão reagindo. Para isso, observa câmeras, chat, perguntas e reações da plataforma.

Porém, muitos participantes permanecem em silêncio, com poucas reações ou com a câmera desligada. Assim, o professor pode ter dificuldade para identificar se a turma está concentrada, desinteressada, confusa ou com dificuldade para acompanhar o conteúdo.

Essa incerteza dificulta a decisão sobre continuar a explicação, reduzir o ritmo, repetir um conteúdo ou mudar a dinâmica da aula.


### 2. Questões de refinamento

Use os tipos de questões/taxonomia definidos na aula. As perguntas devem revelar informações **ainda ausentes** do cenário, não repetir o que já foi respondido.


| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Quais informações o professor considera mais importantes para perceber se a turma está acompanhando a aula? | Ajuda a identificar quais sinais recebem maior atenção e como ocorre a tomada de decisão do docente. | Entrevista com professores e observação de aulas on-line. |
| Q2 | Em quais momentos da aula o professor sente maior dificuldade para acompanhar as reações dos participantes? | Permite compreender quando há maior sobrecarga de atenção e quais tarefas competem entre si. | Entrevista e observação contextual. |
| Q3 | Como o professor interpreta sinais diferentes ou contraditórios, como silêncio no chat e alunos aparentemente atentos pela câmera? | Ajuda a entender como os docentes atribuem significado aos sinais disponíveis e quais interpretações podem gerar dúvidas. . | Entrevista semiestruturada com docentes. |
| Q4 | Que estratégias o professor utiliza quando não consegue identificar se os alunos compreenderam o conteúdo? | Revela práticas reais adotadas para contornar a falta de informação durante a aula.| Observação de aulas e entrevista com professores. |
| Q5 | Como o número de participantes interfere na capacidade do professor de acompanhar a turma? | Permite compreender como o aumento de informações disponíveis influencia o esforço cognitivo e a atenção do docente. | Entrevista e comparação entre aulas com turmas de tamanhos diferentes. |

### 3. Cenário refinado

Reescreva o cenário incorporando as respostas. Marque o conteúdo novo de forma consistente (por exemplo, `**[NOVO: ...]**`).

Durante uma aula por videoconferência, o professor precisa apresentar o conteúdo e, ao mesmo tempo, perceber como os alunos estão reagindo. Para isso, observa câmeras, chat, perguntas e reações da plataforma.

`**[NOVO: O professor tende a considerar principalmente a participação no chat, as perguntas realizadas e as expressões visíveis dos alunos como sinais de acompanhamento da aula.]**`

Porém, muitos participantes permanecem em silêncio, apresentam poucas reações ou mantêm a câmera desligada. `**[NOVO: Essa dificuldade aumenta principalmente durante momentos em que o professor está explicando conteúdos mais complexos ou precisa dividir sua atenção entre apresentação, chat e participantes.]**`

Quando os sinais são pouco claros ou contraditórios, o professor pode ter dificuldade para identificar se a turma está concentrada, desinteressada, confusa ou com dificuldade para acompanhar o conteúdo.

`**[NOVO: Nesses momentos, o professor costuma fazer perguntas diretamente à turma, solicitar alguma interação ou repetir parte da explicação para tentar confirmar se o conteúdo foi compreendido.]**`

`**[NOVO: Em turmas maiores, acompanhar individualmente os participantes se torna ainda mais difícil, aumentando a quantidade de informações que o professor precisa observar simultaneamente.]**`

Essa incerteza dificulta a decisão sobre continuar a explicação, reduzir o ritmo, repetir um conteúdo ou alterar a dinâmica da aula.

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Professor responsável pela aula e alunos participantes da videoconferência. |
| Objetivo(s) | Compreender como os alunos estão reagindo e se estão acompanhando o conteúdo. |
| Contexto | Aula realizada por videoconferência, com o professor apresentando o conteúdo enquanto acompanha a participação da turma. |
| Recursos/informações | Câmeras, chat, perguntas, reações da plataforma e expressões dos participantes. |
| Ações | Observar os participantes, acompanhar o chat, fazer perguntas, solicitar interação e repetir explicações quando necessário. |
| Problemas/rupturas | Pouca participação, câmeras desligadas, sinais contraditórios, excesso de informações simultâneas e dificuldade maior em turmas grandes. |
| Consequências | Incerteza sobre o estado da turma e dificuldade para decidir se deve continuar, repetir, reduzir o ritmo ou alterar a dinâmica da aula. |

### 5. Implicações para as próximas entregas

Quais tarefas merecem análise? Quais informações precisam ser coletadas? **Não desenhe a solução ainda.**

**Quais tarefas merecem análise?** 
- Acompanhar as reações dos participantes enquanto conduz a aula. 
- Identificar sinais de dúvida, desinteresse, confusão ou dificuldade. 
- Observar simultaneamente chat, câmeras, perguntas e reações. 
- Decidir quando continuar, repetir ou adaptar a explicação. 
- Verificar se a turma compreendeu o conteúdo. 

**Quais informações precisam ser coletadas?** 
- Quais sinais os professores mais utilizam para avaliar a turma. 
- Em quais momentos da aula há maior dificuldade de acompanhamento. 
- Como o professor interpreta silêncio, pouca participação e sinais contraditórios. 
- Quais estratégias utiliza atualmente quando não consegue compreender o estado da turma. 
- Como essas dificuldades influenciam suas decisões durante a aula.

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


## Checklist

- [ ] Há um cenário completo por integrante.
- [ ] Cada cenário tem título, ator, objetivo, contexto e problema.
- [ ] O cenário possui origem rastreável na Entrega 1 ou justifica claramente a inclusão de uma nova situação.
- [ ] O texto descreve a situação atual, sem antecipar a solução.
- [ ] Para TCC sem interface original, o cenário descreve uma prática humana plausível relacionada à contribuição técnica, e não “a falta de uma tela”.
- [ ] Questões de refinamento acrescentam informação nova.
- [ ] O refinamento mostra claramente o que foi adicionado/alterado.
- [ ] Cenários são diferentes o suficiente para cobrir objetivos/problemas relevantes.
- [ ] Cada cenário está ligado a persona/necessidade na matriz de rastreabilidade.
