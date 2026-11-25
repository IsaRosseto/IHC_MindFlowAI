# Entrega 9 — Modelo conceitual e design centrado na comunicação

**Data:** {{dd/mm/aaaa}}  
**Status:** 🟨 em andamento  
**Responsabilidade:** soluções individuais, com consolidação da equipe para mapa de objetivos e esquema de signos.

## Objetivo da atividade

Passar do cenário de problema para uma concepção da interação, explicitando objetivos, tópicos de conversa, falas e signos que a interface deverá comunicar/manipular.

## Transformando resultados técnicos em conceitos compreensíveis

Em TCCs algorítmicos ou orientados a dados, esta entrega deve evitar que a interface exponha apenas estruturas internas do código. Identifique os **conceitos e signos que fazem sentido para o usuário**.

Exemplos:

- `query plan`, custo estimado, recomendação e impacto para um DBA;
- modelo, dataset, versão, execução e métrica para engenheiro de IA;
- período, indicador, grupo, tendência e filtro para gestor/analista;
- alerta, severidade, evidência, responsável e status para analista de segurança.

Se um termo técnico for necessário, modele como será comunicado, explicado e relacionado à tarefa.

Dashboards, relatórios, filtros e CRUDs devem aparecer no modelo conceitual por meio dos **objetivos, signos e conversas** que justificam sua existência.

## 1. Cenários de interação

Para cada cenário de problema, produza uma versão em que a solução já pode ser descrita. **Destaque claramente o texto alterado** em relação ao cenário original.

### CI01 — Manoel percebe a reação dos clientes durante a apresentação comercial e decide como prosseguir

**Autor(a):** Matheus Ferreira de Freitas — 22.125.085-5  
**Origem:** cenário problema C01 — Dificuldade em interpretar a reação do cliente durante uma apresentação comercial on-line (versão refinada da Entrega 4), tarefa T05 (Entrega 5) e persona P04 — Manoel Gomes

> Os trechos marcados com **[ACRÉSCIMO: ...]** e **[ALTERADO: ...]** mostram o que mudou em relação ao cenário problema C01; o restante do texto foi mantido. A interação descrita é uma proposta de design: a utilidade de um sinal durante a reunião (H01), a forma de comunicar a confiança (H02), o aviso a clientes de outra empresa (H03) e o uso em grupos pequenos (H05) continuam como hipóteses, a verificar com o estudo de campo I05 (diário de atividades, Entrega 7).

Durante uma reunião comercial pelo Microsoft Teams, Manoel apresenta uma proposta para um grupo de clientes enquanto compartilha sua tela. **[ACRÉSCIMO: Antes de iniciar o compartilhamento, Manoel ativa o acompanhamento da reunião na extensão do MindFlow e informa que os participantes são de outra empresa. A extensão gera o aviso padrão, com o que é e o que não é processado e como não participar, que Manoel envia no chat da reunião com um clique; a estimativa só começa depois do aviso. O painel mostra que 3 dos 4 clientes estão com a câmera ligada e contribuindo para a estimativa.]** Ao mesmo tempo, tenta acompanhar as reações dos participantes para entender se eles estão compreendendo e demonstrando interesse no que está sendo apresentado. **[ALTERADO: Ao lado da grade de vídeo reduzida fica o Semáforo Cognitivo, um indicador pequeno que permanece visível durante o compartilhamento e mostra, com cor, ícone e rótulo, o estado predominante do grupo ("acompanhando", no verde), a confiança da estimativa e há quanto tempo ela foi atualizada. Ele mostra o grupo, nunca a reação de um cliente específico.]**

Como a tela compartilhada reduz a visualização dos participantes, Manoel nem sempre consegue observar todos os clientes. Para tentar confirmar a compreensão, ele faz perguntas curtas, como "esse ponto ficou claro?" ou "faz sentido para a operação de vocês?". **[ACRÉSCIMO: Ao soltar a pílula de dúvida sobre as condições comerciais, Manoel marca o momento na extensão, com o rótulo "condições comerciais", para saber depois como o grupo reagiu naquele trecho.]** Porém, nem todos respondem, e o silêncio pode significar compreensão, dúvida, desinteresse ou até uma objeção não verbalizada. **[ACRÉSCIMO: Poucos segundos depois, o Semáforo indica uma mudança de estado: de "acompanhando" para "possível confusão", em amarelo, com confiança média e a observação "3 de 4 contribuindo". Ao passar o mouse sobre o indicador, Manoel vê desde quando a mudança começou e que a estimativa considera só os clientes com câmera ligada. O sistema não diz quem está confuso nem o que fazer.]**

Com pouco tempo disponível e sem querer constranger os clientes com perguntas repetidas, Manoel precisa decidir se continua a apresentação, explica novamente algum ponto ou muda seu discurso com base em sinais incompletos. **[ALTERADO: Agora o silêncio e o sinal apontam na mesma direção. A decisão continua sendo dele: como o ponto é central para a proposta e ainda há tempo, ele reexplica as condições com um exemplo ligado à operação do cliente e faz uma nova pílula de dúvida; o responsável técnico responde, e o indicador volta a "acompanhando". Quando o decisor faz uma pergunta inesperada, Manoel dispensa o aviso e responde; o Semáforo continua mostrando apenas o estado atual. Se o tempo estivesse curto, ele anotaria no momento marcado "retomar no follow-up" e seguiria para o próximo bloco.]**

Em alguns casos, ele interpreta a falta de reação como concordância e só descobre posteriormente, durante o follow-up ou após a recusa da proposta, que determinados pontos não haviam sido compreendidos ou aceitos pelo cliente. **[ALTERADO: Ao encerrar a chamada, a extensão avisa que o resumo da reunião foi salvo. Logo depois, Manoel abre o resumo no Dashboard, vê a linha do tempo da reunião com os momentos marcados e o estado do grupo em cada trecho, e anota suas percepções nos pontos em que ficou em dúvida. Dias depois, quando chega o e-mail do cliente, ele registra em cada momento marcado se o retorno confirmou a leitura feita na reunião. A comparação, que antes dependia da memória, fica registrada junto da reunião.]**

**[ACRÉSCIMO — ruptura considerada: em outra reunião, só um dos três clientes liga a câmera. Ao ativar o acompanhamento, a extensão informa que não há participantes suficientes para estimar o estado do grupo sem expor uma pessoa e explica o motivo. Manoel segue a apresentação sem o acompanhamento, conduzindo como fazia antes, e ainda pode marcar momentos e anotar no resumo.]**

### Diferenças relevantes

| Alteração | Por que foi necessária | Evidência/artefato que justifica |
|---|---|---|
| Ativar o acompanhamento informando que os participantes são de outra empresa, com o aviso enviado no chat antes da primeira estimativa | Clientes externos não têm a extensão nem a página de transparência da aula; o aviso precisa chegar pelo canal da reunião e antes do processamento | H03; RC04 e RC09; F08; T04 (aviso ao participante); A05 e I05 (consentimento com participantes externos) |
| Semáforo Cognitivo visível ao lado da grade reduzida, com cor, ícone e rótulo, mostrando só o grupo | Na T05, perceber a reação acontece ao mesmo tempo que explicar (CTT 2.1.1 `\|\|\|` 2.1.2); a grade reduzida só mostra quem tem câmera ligada; R04 impede mostrar reação individual | T05 (HTA 3.1, CTT 2.1); R01, R02, R04; RC08; F01 |
| Marcar o momento ao soltar a pílula de dúvida | As pílulas de dúvida são planejadas (T05, operação 1.2) e são o ponto em que Manoel mais precisa da reação; marcar liga a reação ao trecho da proposta | T05 (HTA 1.2 e 2.2); C01 (Q1: trechos de preço e condições); RC10 |
| Mudança de estado com confiança, participantes contribuindo e desde quando | Manoel precisa julgar quanto confiar na leitura (T05, operação 4.3), etapa que hoje não tem apoio | T05 (HTA 4.3, CTT 2.3); H02; RC02; F04 |
| O sistema não diz quem está confuso nem o que fazer; a decisão continua de Manoel | A reação que importa pode ser a do decisor (C01, Q2), mas o agregado não identifica pessoas; o sistema indica sem prescrever | RC03; R04; C01 (Q2 e Q4); T05 (objetivo 5) |
| Aviso dispensado quando um cliente pergunta; o indicador mostra só o estado atual | Perguntas inesperadas e objeções competem com a observação (C01, Q6); avisos antigos não devem se acumular | C01 (Q6); T05 (CTT 2.2 `\|>`); RC06 |
| Anotar "retomar no follow-up" no momento marcado | É a alternativa 5.3 da T05, hoje feita de memória ou em papel | T05 (HTA 5.3 e 6.2); C01 (Q4) |
| Resumo salvo ao encerrar, com linha do tempo, momentos marcados, percepções e retorno do cliente no mesmo lugar | A avaliação do que funcionou só acontece dias depois (T05, operação 6.3) e depende de comparar anotações com o e-mail do cliente (C01, Q7) | T05 (HTA 6.2 e 6.3); C01 (Q7); R03 e R05; F02 e F03; RC10 |
| Ruptura: participantes insuficientes | Em grupos de 2 a 6 clientes, o agregado pode expor uma pessoa ou não ter base | H05; R04; A05 (dado sobre papéis e tamanho do grupo) |

---

### CI02 — Bruno entende o que acontece com a própria imagem e escolhe como participar da aula

**Autor(a):** Gustavo Bertoluzzi Cardoso — 22.123.016-2  
**Origem:** cenário problema C03 — Aluno que não sabe como está sendo percebido numa aula online (Entrega 4), tarefa T04 (Entrega 5) e persona P05 — Bruno D. Roger  
**Objetivos:** O18 a O23 (dicionário na seção 3)

> Os trechos marcados com **[ACRÉSCIMO: ...]** e **[ALTERADO: ...]** mostram o que mudou em relação ao cenário problema C03; o restante do texto foi mantido. Bruno é persona secundária: não usa o Semáforo Cognitivo nem o Dashboard, só a interface de transparência e participação (F08). A interação descrita é uma proposta de design. A opção de ligar a câmera sem participar da análise, a pausa só da análise e o resumo de transparência continuam como hipóteses (H03; tarefas marcadas com [H] na T04), a verificar com o grupo focal I03 (Entrega 7).

Bruno é aluno do segundo ano de Ciência da Computação e tem duas disciplinas EAD nesse semestre. Numa segunda de manhã ele entra na aula de Cálculo pelo Teams um pouco atrasado, ainda terminando o café, e decide deixar a câmera desligada porque o quarto tá bagunçado e ele não quer aparecer assim pros colegas. **[ACRÉSCIMO: Como a aula já começou, ele fecha o aviso de entrada sem ler. Ao lado dos controles da chamada continua um indicador pequeno do MindFlow: "análise da turma ativa · você: não participando". Bruno clica no indicador e o aviso abre de novo, em poucas linhas e sem termos de IA: o que a webcam capta (sinais do rosto, da postura e do olhar, processados no próprio computador dele), o que a professora recebe (só um estado geral da turma, nunca o de um aluno) e o que não é feito com os dados (o vídeo não é guardado e não existe resultado individual).]**

A professora começa a explicar um assunto novo e, no meio da aula, comenta que gostaria que mais gente ligasse a câmera, porque assim ela consegue perceber se a turma tá acompanhando. Bruno fica na dúvida se liga ou não, porque não sabe se isso vai pesar de alguma forma na nota de participação dele, mas também não quer ficar exposto justo num dia que ele não entendeu direito o conteúdo da aula passada. **[ACRÉSCIMO: Ele abre as informações completas a partir do aviso. Elas estão organizadas por perguntas com as palavras de um aluno, e ele lê "Isso conta na minha nota?": o MindFlow não gera nenhum resultado por aluno, então não há nada dele para entrar na nota; as regras de participação continuam sendo as da disciplina. Logo abaixo aparece o contato para dúvidas sobre os dados.]** **[ALTERADO: Antes ele decidia no escuro. Agora sabe o que acontece com a imagem e que a professora vê só a turma, mas a decisão continua sendo dele, e o sistema não recomenda nenhuma opção. Ele mantém a câmera desligada, porque o que o incomoda hoje é o quarto, e não a análise, e o indicador confirma "você: não participando".]**

Em um momento a professora pede pra alguém responder rápido uma pergunta no chat, Bruno demora pra digitar porque ainda tá processando o que foi perguntado, e três colegas respondem antes dele. **[ACRÉSCIMO: Mais tarde, a professora avisa que a próxima atividade vale participação, e Bruno decide ligar a câmera para não parecer ausente. Ao ligar, o MindFlow pergunta se ele quer participar da análise. Como ainda está inseguro com o conteúdo, ele escolhe "câmera ligada, sem participar da análise", e o indicador mostra "você: câmera ligada · análise pausada". Ele aparece para a turma sem que a imagem dele entre na estimativa. Quando a professora pausa o acompanhamento para uma atividade em grupo, o indicador mostra "análise da turma pausada pela professora", sem que Bruno precise fazer nada. Dez minutos depois, já mais seguro, ele retoma a própria participação pelo mesmo indicador, sem mexer na câmera, e o indicador volta para "você: participando".]**

Depois da aula ele fica sem saber se a professora reparou que ele participou pouco, se isso ficou só na impressão dela ou se tem algum jeito disso voltar contra ele de algum modo, e não tem com quem tirar essa dúvida. **[ALTERADO: Quando a professora encerra a aula, o indicador avisa que a análise terminou junto com a aula. Depois, Bruno abre o resumo de transparência da aula, que só ele vê: por quanto tempo a imagem dele contribuiu para a estimativa da turma, que o vídeo não foi guardado e que nenhum resultado individual foi gerado ou enviado. O que a professora achou da participação dele continua sendo impressão dela, mas Bruno sabe que o MindFlow não registrou nada sobre ele. Se ainda tiver dúvida, já sabe a quem perguntar.]**

**[ACRÉSCIMO — ruptura considerada: em outra aula, Bruno assiste pelo celular, que não consegue fazer o processamento no próprio aparelho. Ao entrar, o indicador informa "este aparelho não faz a análise: sua imagem não será analisada, mesmo com a câmera ligada". Bruno segue a aula normalmente, e a professora continua vendo só o número de participantes que contribuem, sem saber quem está fora.]**

### Diferenças relevantes

| Alteração | Por que foi necessária | Evidência/artefato que justifica |
|---|---|---|
| Indicador pequeno e permanente que reabre o aviso a qualquer momento | Bruno entra atrasado e pode fechar o aviso de entrada sem ler; o aviso não pode existir só na entrada | C03 (entrada atrasada); T04 (HTA 1.2; GOMS METHOD 1.B); RC04 |
| Aviso em três blocos curtos: o que é captado, o que a professora recebe e o que não é feito com os dados | São as três dúvidas de Bruno no C03; dizer o que **não** acontece responde ao medo dele de forma mais direta | T04 (HTA 2.1, 2.2 e 2.3); P05 (decisões de design); H03; RC04; página de transparência do Education Insights (Entrega 2) |
| Informações completas organizadas por perguntas do aluno, com o contato para dúvidas | As dúvidas são concretas ("isso conta na nota?") e hoje não existe canal para perguntar | T04 (HTA 3.2 e 3.3); C03 (Q1, Q2 e Q7) |
| A escolha de como participar é de Bruno, e o sistema não recomenda nenhuma opção | A relação de poder entre professora e aluno pode deixá-lo sem jeito de recusar | T04 (HTA 4 e 4.1); Entrega 3 (contexto de uso, ambiente social/organizacional); RC05 |
| Câmera ligada sem participar da análise e pausa só da análise **[H]** | Separa aparecer para a turma de ser analisado; sem isso, a única forma de não ser analisado é desligar a câmera, que é o conflito do C03 | T04 (HTA 4.3 e 5.3; GOMS METHODS 2.B e 4.B); H03; A03 (dado sobre pausar ou recusar sem desligar a câmera) |
| Indicador da própria participação: participando, câmera ligada com análise pausada, não participando | Sem confirmação, Bruno não sabe se a escolha foi aplicada | T04 (HTA 4.5 e 5.4; CTT 2.2) |
| Pausa feita pela professora aparece no indicador do aluno | O acompanhamento pausado pela comunicadora precisa chegar aos participantes | CI05 (O16); RC07; RC09 |
| A análise termina junto com a aula, e o resumo de transparência só é visto por Bruno | Responde à última ruptura do C03: depois da aula, ele não sabe se algo pode voltar contra ele | T04 (HTA 6; CTT 3 `[>` e tarefa 4); C03 (Q7); RC09 |
| Ruptura: aparelho que não faz o processamento local | Bruno também assiste pelo celular; a análise não pode acontecer fora do aparelho dele | P05 (ambiente típico de uso); T04 (HTA 4.5); R04 |

---

### CI03 — Acompanhar os estados da turma e revisar os resultados da aula

**Autor(a):** Kayky Pires — 22.222.040-2  
**Origem:** cenário problema C02 — Dificuldade de Karol em perceber se a turma está acompanhando a aula on-line.

Karol, professora de Filosofia na modalidade EAD, precisa apresentar o conteúdo durante a videoconferência e, ao mesmo tempo, perceber como os alunos estão reagindo.

O professor tende a considerar principalmente a participação no chat, as perguntas realizadas e as expressões visíveis dos alunos como sinais de acompanhamento da aula.

Porém, muitos participantes permanecem em silêncio, apresentam poucas reações ou mantêm a câmera desligada. Essa dificuldade aumenta principalmente durante momentos em que o professor está explicando conteúdos mais complexos ou precisa dividir sua atenção entre apresentação, chat e participantes.

Quando os sinais são pouco claros ou contraditórios, o professor pode ter dificuldade para identificar se a turma está concentrada, desinteressada, confusa ou com dificuldade para acompanhar o conteúdo.

**[ACRÉSCIMO: O professor consulta os indicadores de engajamento, tédio, confusão e frustração apresentados pelo MindFlow AI, considerando os participantes para os quais existem dados disponíveis. Os indicadores são comunicados como estimativas que complementam os sinais observados na videoconferência.]**

Nesses momentos, o professor costuma fazer perguntas diretamente à turma, solicitar alguma interação ou repetir parte da explicação para tentar confirmar se o conteúdo foi compreendido.

Em turmas maiores, acompanhar individualmente os participantes se torna ainda mais difícil, aumentando a quantidade de informações que o professor precisa observar simultaneamente.

**[ALTERADO: Com o apoio dos indicadores e dos demais sinais observados, o professor avalia se deve continuar a explicação, reduzir o ritmo, repetir um conteúdo ou alterar a dinâmica da aula. A decisão permanece sob sua responsabilidade.]**

**[ACRÉSCIMO: Após o encerramento da aula, o professor acessa suas reuniões, identifica a aula pelo título e pela data e consulta o resumo. Examina os indicadores apresentados e identifica quais informações deseja destacar em sua análise.]**

**[ACRÉSCIMO: Para modificar a apresentação do resumo, o professor acessa a personalização, consulta os indicadores disponíveis e seleciona aqueles que deseja exibir. Ao salvar, recebe a confirmação de que a configuração foi salva e aplicada. Em seguida, confere o resumo personalizado e pode retornar à edição para realizar novos ajustes.]**

**[ACRÉSCIMO: Se cancelar a personalização, o professor retorna à consulta sem aplicar as alterações. Se ocorrer uma falha no salvamento, o sistema informa o problema e preserva as seleções para permitir uma nova tentativa.]**

### Diferenças relevantes

| Alteração | Por que foi necessária | Evidência/artefato que justifica |
|---|---|---|
| Inclusão da consulta aos indicadores durante a aula. | Descrever como a solução pode complementar os sinais utilizados pelo professor para interpretar o estado da turma. | C01 e hipótese H01, relacionada à utilidade de um indicador discreto do estado do grupo em tempo real. |
| Comunicação dos indicadores como estimativas, considerando a disponibilidade de dados. | Evitar que os resultados sejam interpretados como certezas ou como informações disponíveis para todos os participantes. | Proposta de comunicação derivada do funcionamento da classificação, a validar no protótipo. |
| Uso dos indicadores como apoio à decisão do professor. | Relacionar as informações apresentadas à necessidade de manter ou adaptar a condução da aula. | Objetivo e consequências descritos no C01. |
| Extensão do cenário para a revisão após a aula. | Contemplar a consulta e a personalização dos resultados de uma aula concluída, ampliando o contexto original do C01. | T01 — Configurar o acompanhamento de uma aula concluída no MindFlow AI. |
| Seleção dos indicadores exibidos no resumo. | Permitir que o docente adapte a visualização às suas necessidades de análise. | T01 e cena Personalizar visualização do M01. |
| Inclusão de feedback de salvamento, cancelamento e recuperação de falha. | Informar o resultado das ações e permitir que o docente ajuste ou retome a personalização. | Caminho principal e alternativas do M01. |


### CI04 — Acompanhar a compreensão e o engajamento dos participantes durante o treinamento on-line

**Autor(a):** Rafael Dias — 22.222.039-4  
**Origem:** cenário problema C04 — Dificuldade em identificar a compreensão e o aprendizado durante treinamento on-line.  
**Persona relacionada:** P03 — Nathanael Lima.

Nathanael, profissional de Treinamento e Desenvolvimento, conduz capacitações on-line para colaboradores de diferentes áreas e níveis de experiência. Durante o treinamento, precisa apresentar os conteúdos e, ao mesmo tempo, identificar se os participantes estão acompanhando e compreendendo as explicações.

Normalmente, utiliza as câmeras, o chat e as perguntas dos participantes para interpretar suas reações. Entretanto, em ambientes corporativos, o uso da câmera nem sempre é obrigatório e muitos participantes não interagem durante a apresentação.

Em treinamentos com grande número de participantes, essa dificuldade aumenta, pois Nathanael não consegue acompanhar individualmente todas as pessoas. Assim, sua percepção sobre o grupo pode ficar limitada aos participantes que demonstram alguma reação, dificultando a identificação de momentos de confusão, desinteresse ou perda de atenção.

**[ACRÉSCIMO: Durante o treinamento, Nathanael utiliza o MindFlow AI para consultar os indicadores de engajamento, tédio, confusão e frustração do grupo, apresentados de maneira objetiva para não interromper o ritmo da capacitação.]**

**[ACRÉSCIMO: Os indicadores são apresentados como estimativas calculadas a partir dos participantes para os quais existem dados disponíveis. O sistema informa quando não há dados suficientes e comunica que os resultados não representam uma confirmação do aprendizado ou da compreensão do conteúdo.]**

**[ALTERADO: Ao observar possíveis alterações nos indicadores, Nathanael considera também as manifestações no chat, as perguntas e as demais reações disponíveis para decidir se deve manter a explicação, reduzir o ritmo, apresentar outro exemplo ou solicitar uma interação dos participantes.]**

**[ACRÉSCIMO: Após o encerramento do treinamento, Nathanael pode acessar o resumo da sessão e consultar os indicadores registrados ao longo da apresentação, identificando períodos em que houve maior estimativa de confusão, tédio ou redução do engajamento.]**

**[ACRÉSCIMO: Com essas informações, Nathanael consegue revisar os momentos que merecem atenção e avaliar possíveis melhorias no conteúdo e na condução dos próximos treinamentos, sem utilizar os indicadores como avaliação individual dos participantes.]**

Dessa forma, Nathanael passa a contar com informações complementares às interações convencionais da videoconferência, utilizando os resultados como apoio à interpretação do comportamento do grupo e às decisões durante e após o treinamento.

### Diferenças relevantes

| Alteração | Por que foi necessária | Evidência/artefato que justifica |
|---|---|---|
| Inclusão da consulta aos indicadores durante o treinamento. | Permitir que o instrutor acompanhe possíveis sinais de engajamento e dificuldade mesmo quando existem poucas interações no chat. | C04, necessidade R01 e hipótese H01. |
| Apresentação dos indicadores como estimativas e comunicação da disponibilidade de dados. | Evitar que o instrutor interprete resultados da classificação como confirmação de compreensão ou aprendizado. | Hipótese H02 e necessidade de comunicar as limitações dos resultados técnicos. |
| Utilização dos indicadores como apoio à tomada de decisão. | Relacionar os resultados à necessidade de adaptar o ritmo, repetir explicações ou solicitar interações. | Objetivos e ações identificados no C04. |
| Consulta posterior aos resultados do treinamento. | Permitir que o instrutor identifique períodos que merecem revisão e avalie possíveis melhorias nos materiais. | Necessidades e objetivos da persona P03. |
| Apresentação de informações agregadas do grupo. | Evitar a interpretação dos resultados como avaliação individual dos colaboradores. | Decisões de design da P03 e hipótese H03. |
| Apresentação objetiva dos indicadores. | Reduzir a sobrecarga de informações durante a capacitação. | Restrições da P03 e problemas identificados no C04. |
---

### CI05 — Camila percebe, ainda na aula, que a turma pode não ter acompanhado a estrutura nova

**Autor(a):** Isabella Vieira Silva Rosseto — 22.222.036-0  
**Origem:** cenário problema C05 (versão refinada da Entrega 4), tarefa T03 (Entrega 5) e persona P02  
**Objetivos:** O11 a O17 (dicionário na seção 3)

> Os trechos marcados com **[ALTERADO]** ou **[NOVO]** mostram o que mudou em relação ao cenário problema C05. O restante do texto foi mantido. A interação descrita é uma proposta de design: a utilidade do indicador (H01), a forma de mostrar a confiança (H02), o aviso aos alunos (H03) e o uso em turma pequena (H05) continuam como hipóteses a validar com os instrumentos da Entrega 7.

Camila dá aula particular de inglês para uma turma de oito alunos, pelo Google Meet. **[NOVO: Antes de começar, ela ativa o acompanhamento da turma pela extensão do MindFlow. A extensão mostra que 4 de 8 alunos estão com a câmera ligada e contribuindo para a estimativa, e os alunos recebem na chamada o aviso de que o acompanhamento está ativo, com o que é e o que não é processado.]** Na metade da aula, ela compartilha a tela com um exercício de conversação e, ao mesmo tempo, tenta acompanhar a grade de vídeo reduzida que fica num cantinho da tela. **[ALTERADO: Ao lado da grade, fica o Semáforo Cognitivo, um indicador pequeno que continua visível durante o compartilhamento. Ele mostra o estado predominante da turma com cor, ícone e rótulo ("acompanhando", no verde), a confiança da estimativa e há quanto tempo foi atualizado.]** Metade da turma está com a câmera desligada.

Ela introduz uma estrutura gramatical nova, um pouco mais complexa que o normal. Nota um silêncio maior que o de costume, mas não sabe se é porque estão concentrados ouvindo ou porque não entenderam. **[NOVO: Poucos minutos depois, o indicador muda para "possível confusão", em amarelo, com confiança média e a observação "4 de 8 contribuindo". Camila passa o mouse sobre o indicador e vê desde quando a mudança aconteceu e que a estimativa considera só os alunos com câmera ligada.]** Pergunta "entenderam?" e alguns alunos respondem "sim" rapidamente, sem muita convicção. **[ALTERADO: Antes, a falta de tempo e de outro sinal a levava a seguir em frente. Agora, o indicador e o "sim" pouco convicto apontam na mesma direção. Ela não segue automaticamente o que o sistema mostra: usa o exemplo de reserva que tinha preparado e pede que um aluno forme uma frase com a estrutura. A resposta confirma a dúvida, e ela reforça o conteúdo por mais cinco minutos.]** **[NOVO: Antes de retomar o plano, ela clica em "marcar este momento" para registrar o trecho na linha do tempo da aula e dispensa o aviso. O indicador volta a "acompanhando" alguns minutos depois.]** Como o tempo de aula é curto e o plano prevê ainda mais dois tópicos, ela segue em frente **[ALTERADO: com um dos tópicos encurtado, e não mais sem saber se a turma tinha acompanhado]**.

**[ALTERADO: Ao encerrar a chamada, a extensão avisa que o resumo da aula foi salvo no Dashboard. Na aula seguinte]**, ao corrigir o exercício de casa, ela **[ALTERADO: confere se a turma ainda erra os exemplos com a estrutura nova e compara com o momento que tinha marcado]**. **[ALTERADO: Em vez de gastar parte da aula seguinte revisando um conteúdo que já devia ter sido reforçado, ela usa poucos minutos para retomar só o que ainda apareceu nos erros.]**

**[NOVO — ruptura considerada: em outra aula, só dois alunos ligam a câmera. Ao ativar o acompanhamento, a extensão informa que não há participantes suficientes para estimar o estado da turma e explica o motivo. Camila escolhe continuar a aula sem o acompanhamento, conduzindo como fazia antes.]**

### Diferenças relevantes

| Alteração | Por que foi necessária | Evidência/artefato que justifica |
|---|---|---|
| Ativar o acompanhamento antes da aula, vendo quantos alunos contribuem | Camila precisa saber se o indicador terá base antes de confiar nele; os alunos precisam ser avisados | RC07 (controle de ativação), H03, H05; T04 (aviso ao participante) |
| Indicador visível durante o compartilhamento de tela, com cor, ícone e rótulo | Na T03, observar a turma concorre com explicar (`\|\|\|` no CTT); a grade reduzida não basta | T03 (CTT tarefa 2), RC08 (não depender só da cor), F01 |
| Mudança de estado com confiança e número de participantes | A professora precisa avaliar quanto confiar no sinal, etapa que hoje não tem apoio | T03 (HTA 3.2, CTT 3.2), H02, RC02, F04 |
| Camila confirma a dúvida por conta própria antes de reforçar | O sistema indica que algo merece atenção, mas não decide a ação | RC03; T03 (decisão é tarefa do usuário); C05 (Q4, Q5) |
| Marcar o momento da aula | Ligar o que aconteceu durante a aula à revisão posterior, sem exigir anotação manual | Jornada de Camila, etapa 8 (Entrega 3); R03; RC10 |
| Resumo salvo ao encerrar | Permite comparar a percepção da aula com o exercício corrigido depois | C05 (Q7), R03, F02/F03 |
| Ruptura: poucos alunos com câmera | Em turma pequena, o agregado pode não ter base ou expor alunos | H05; contexto de uso (Entrega 3) |
| Aviso que some depois de dispensado e indicador que volta ao estado atual | Não acumular alertas antigos na tela | RC06 |

---

## 2. Design centrado na comunicação

**Autor(a):** Matheus Ferreira de Freitas — 22.125.085-5  
**Origem:** cenário problema C01 — Dificuldade em interpretar a reação do cliente durante uma apresentação comercial on-line (versão refinada da Entrega 4), tarefa T05 (Entrega 5) e persona P04 — Manoel Gomes

| Tópico > subtópico | Falas e signos envolvidos | Intenção/efeito esperado |
|---|---|---|
| **O01 Ativar o acompanhamento em uma reunião com clientes** | `U: quero acompanhar esta reunião; os participantes são de outra empresa` / `D: aviso pronto para enviar no chat; a estimativa começa depois do aviso` / `D: acompanhamento ativo; 3 de 4 participantes contribuindo`. Signos: acompanhamento da reunião, aviso aos participantes, participantes contribuindo. | Manoel só passa a receber estimativas depois de os clientes serem avisados e sabe, antes de começar, se o sinal terá base. |
| > Não há participantes suficientes | `D: não há câmeras ligadas suficientes para estimar o estado do grupo sem expor uma pessoa (mínimo: 3)` / `U: continuar sem acompanhamento` ou `U: tentar novamente`. Signos: mínimo de participantes. | Evitar um sinal sem base, explicar o motivo e não bloquear a reunião. |
| **O02 Perceber o estado do grupo enquanto apresenta** | `D: o grupo parece estar acompanhando` (verde, ícone e rótulo) / `D: confiança alta; 3 de 4 contribuindo; atualizado há 15 s`. Signos: estado predominante, confiança da estimativa, participantes contribuindo, atualizado há. | Leitura de relance, sem tirar a atenção da tela compartilhada nem interromper a fala. |
| **O03 Marcar o momento da pílula de dúvida** | `U: marcar este momento: "condições comerciais"` / `D: momento marcado aos 12 min`. Signos: momento marcado. | Ligar a reação do grupo ao trecho da proposta, para a decisão na hora e para a revisão depois. |
| **O04 Verificar a reação depois da pílula de dúvida** | `D: o estado mudou de "acompanhando" para "possível confusão" há 20 s` / `U: o que mudou?` / `D: desde a pergunta sobre condições comerciais; confiança média; 3 de 4 contribuindo`. Signos: mudança de estado, confiança da estimativa, participantes contribuindo. | Chamar a atenção para o trecho sem dizer quem está em dúvida nem o que fazer (RC03, R04). |
| > Entender o significado e a confiança | `U: o que significa "possível confusão"?` / `D: parte do grupo mostra sinais associados a dificuldade; é uma estimativa do grupo, não de cada pessoa, e pode errar` / `D: a confiança está média porque um dos quatro está sem câmera`. Signos: estado predominante, qualidade do sinal. | Evitar confiança excessiva na estimativa (H02) e deixar claro que ninguém é avaliado individualmente (H03). |
| > Dispensar o aviso | `U: entendi, pode esconder` / `D: aviso dispensado; o indicador segue mostrando o estado atual`. Signos: mudança de estado. | Não acumular avisos quando um cliente pergunta ou o tempo aperta (RC06). |
| **O05 Anotar um ponto para o follow-up** | `U: anotar neste momento: "retomar no follow-up"` / `D: anotação salva no momento marcado`. Signos: anotação, momento marcado. | Registrar a dúvida sem interromper a reunião, no lugar da memória ou do papel (T05, operação 5.3). |
| **O06 Encerrar a reunião com o resumo salvo** | `U: encerrar a reunião` / `D: resumo salvo; disponível no Dashboard`. Signos: resumo da reunião. | Garantir que a reunião possa ser revisada depois. |
| > Falha ao salvar | `D: não foi possível salvar o resumo agora; os dados continuam no seu computador` / `U: tentar novamente` ou `U: tentar mais tarde`. Signos: resumo da reunião. | Recuperar de uma falha sem perder a reunião. |
| **O07 Revisar a reunião e registrar o retorno do cliente** | `U: abrir o resumo da reunião` / `D: linha do tempo com os momentos marcados e o estado do grupo em cada trecho` / `U: anotar minha percepção neste momento` / dias depois: `U: registrar o retorno do cliente neste momento: "em parte"` / `D: retorno registrado ao lado da leitura feita na reunião`. Signos: resumo da reunião, momento marcado, anotação, retorno do cliente. | Comparar, no mesmo lugar, a leitura feita na reunião com o que o cliente respondeu (T05, operação 6.3; C01, Q7). |

Decidir se avança, reforça ou reexplica um ponto **não é um tópico de conversa com o sistema**: é uma decisão de Manoel, tomada fora da interface. O sistema oferece o sinal, a confiança e a explicação para apoiar essa decisão, sem prescrever a ação (RC03).

---

**Autor(a):** Gustavo Bertoluzzi Cardoso — 22.123.016-2  
**Origem:** CI02 — Bruno entende o que acontece com a própria imagem e escolhe como participar da aula (cenário problema C03, tarefa T04), persona P05 — Bruno D. Roger.

| Tópico > subtópico | Falas e signos envolvidos | Intenção/efeito esperado |
|---|---|---|
| **O18 Entender o que acontece com a própria imagem nesta aula** | `D: a análise da turma está ativa nesta aula` / `D: a webcam capta sinais do rosto, da postura e do olhar, processados no seu computador` / `D: a professora recebe só o estado geral da turma, nunca o de um aluno` / `D: o vídeo não é guardado e não existe resultado individual`. Signos: análise da turma, aviso aos participantes. | Bruno sabe, em poucos segundos e sem termos de IA, o que acontece com a imagem dele antes de decidir como participar (RC04, H03). |
| > Reabrir o aviso com a aula em andamento | `U: o que é isso?` (clica no indicador) / `D: (o mesmo aviso, de novo)`. Signos: análise da turma, participação na análise. | Quem entra atrasado ou fecha o aviso sem ler não perde a informação (T04, HTA 1.2). |
| **O19 Tirar uma dúvida específica sobre os dados** | `U: ler mais` / `D: perguntas e respostas com as palavras do aluno` / `U: isso conta na minha nota?` / `D: o MindFlow não gera resultado por aluno; as regras de participação são as da disciplina`. Signos: informações completas. | Responder às dúvidas concretas do C03 sem exigir que Bruno pergunte à professora. |
| > Não encontrar a resposta | `D: não achou sua resposta? fale com: (contato para dúvidas sobre os dados)`. Signos: contato para dúvidas. | Dar um canal claro, que hoje não existe (C03, Q7; T04, HTA 3.3). |
| **O20 Escolher como participar da aula** | `D: como você quer participar? participar com câmera / câmera ligada, sem participar da análise [H] / câmera desligada` / `D: em todas as opções, a professora vê só a turma` / `U: (escolhe uma opção)` / `D: você: participando` ou `D: você: câmera ligada · análise pausada` ou `D: você: não participando`. Signos: participação na análise. | A decisão é de Bruno, e nenhuma opção é apresentada como a certa (T04, HTA 4). |
| **O21 Conferir se está contribuindo para a análise agora** | `U: (olha o indicador)` / `D: você: participando · análise da turma ativa`. Signos: participação na análise, análise da turma. | Confirmar de relance que a escolha foi aplicada, sem tirar a atenção da aula (T04, CTT 2.1 `\|\|\|` 2.2). |
| **O22 Mudar a participação durante a aula** | `U: pausar minha participação` / `D: análise pausada; sua câmera continua como estava` / `U: retomar minha participação` / `D: você: participando`. Signos: participação na análise. | Parar de ser analisado sem sumir da turma, sempre que a situação mudar (T04, HTA 5.3) [H]. |
| > Mudar a câmera na plataforma | `U: (desliga ou religa a câmera no Teams)` / `D: câmera religada; sua participação continua pausada, como você deixou`. Signos: participação na análise. | Deixar claro se a análise acompanha a câmera ou mantém a escolha anterior (T04, HTA 5.2). |
| > Pausa feita pela professora | `D: análise da turma pausada pela professora` / `D: análise da turma retomada`. Signos: análise da turma. | Bruno sabe que, enquanto estiver pausada, a imagem dele não é analisada, mesmo com a câmera ligada (ligação com O16 da CI05; RC07). |
| > Aparelho sem processamento local | `D: este aparelho não faz a análise; sua imagem não será analisada, mesmo com a câmera ligada`. Signos: participação na análise. | Não deixar Bruno achar que está participando quando não está, nem bloquear a aula (R04). |
| **O23 Conferir depois da aula o que foi processado** | `D: a análise terminou junto com a aula` / `U: abrir o resumo de transparência da aula` / `D: sua imagem contribuiu para a estimativa da turma por 32 min; o vídeo não foi guardado; nenhum resultado individual foi gerado ou enviado`. Signos: resumo de transparência. | Confirmar que nada foi registrado sobre ele, que é a informação que tranquiliza Bruno no C03 (Q7) [H]. |
| > Aula em que ele não participou da análise | `D: nesta aula sua imagem não foi analisada (câmera desligada o tempo todo)`. Signos: resumo de transparência, participação na análise. | O resumo vazio também precisa explicar o motivo, e não aparecer como erro. |

Decidir se liga a câmera ou se participa da análise **não é um tópico de conversa com o sistema** no sentido de uma recomendação: Bruno pesa o próprio conforto e a aula (T04, HTA 4.1) fora da interface. O sistema informa o que acontece em cada opção e confirma a escolha, sem sugerir qual é a melhor. A estimativa da turma não aparece em nenhuma fala para Bruno: o Semáforo e o Dashboard são só da professora (RC09).

---

**Autor(a):** Rafael Dias — 22.222.039-4  
**Origem:** cenário problema C04 — Dificuldade em identificar a compreensão e o aprendizado durante treinamento on-line.  
**Persona relacionada:** P03 — Nathanael Lima.

| Tópico > subtópico | Falas e signos envolvidos | Intenção/efeito esperado |
|---|---|---|
| Acompanhar o estado do grupo durante o treinamento | `U: consultar os indicadores do grupo` / `D: apresentar as estimativas de engajamento, tédio, confusão e frustração`. Signos: indicadores cognitivos, valores dos indicadores. | Permitir que o instrutor acompanhe possíveis alterações no estado do grupo durante a apresentação. |
| > Compreender os indicadores apresentados | `U: consultar o significado dos indicadores` / `D: explicar o significado de cada estado e informar que os resultados são estimativas`. Signos: descrição dos indicadores, escala dos valores. | Evitar interpretações incorretas sobre o comportamento e a aprendizagem dos participantes. |
| > Verificar a disponibilidade dos dados | `D: informar a disponibilidade de dados para a análise do grupo`. Signos: disponibilidade de dados, estado da análise. | Permitir que o instrutor reconheça as limitações das informações apresentadas. |
| Interpretar alterações no estado do grupo | `U: observar os indicadores durante a apresentação` / `D: apresentar os valores atualizados dos estados estimados`. Signos: engajamento, tédio, confusão, frustração e período analisado. | Auxiliar na identificação de possíveis momentos de dificuldade ou perda de atenção. |
| > Decidir sobre a condução do treinamento | `U: avaliar os indicadores e decidir se deve manter ou adaptar a explicação`. Signos: indicadores apresentados e período atual. | Apoiar a decisão de repetir um conteúdo, modificar o ritmo ou solicitar uma interação, mantendo a decisão sob responsabilidade do instrutor. |
| Revisar os resultados após o treinamento | `U: consultar os treinamentos concluídos` / `D: apresentar as sessões disponíveis`. Signos: título da reunião, data do treinamento. | Permitir que Nathanael identifique o treinamento que deseja analisar. |
| > Consultar o resumo do treinamento | `U: abrir o resumo do treinamento` / `D: apresentar os resultados e indicadores registrados durante a sessão`. Signos: identificação da reunião, indicadores cognitivos e valores estimados. | Permitir a revisão dos resultados apresentados ao longo do treinamento. |
| > Identificar períodos de maior dificuldade | `U: examinar os períodos do treinamento` / `D: apresentar a variação dos indicadores ao longo da sessão`. Signos: período analisado, indicadores e valores. | Auxiliar na identificação de momentos que merecem atenção na revisão dos conteúdos. |
| > Interpretar ausência de resultados | `D: informar que não existem dados suficientes para determinado período` / `U: consultar os demais períodos disponíveis`. Signos: disponibilidade de dados, período analisado. | Evitar que a ausência de informação seja interpretada como ausência de dificuldades. |
| Avaliar melhorias para próximos treinamentos | `U: analisar os períodos identificados e decidir quais conteúdos precisam ser revisados`. Signos: período analisado, indicadores cognitivos e resultados do treinamento. | Apoiar a avaliação de melhorias na apresentação e nos materiais utilizados em futuras capacitações. |

---

**Autor(a):** Isabella Vieira Silva Rosseto — 22.222.036-0  
**Origem:** CI05 — Camila percebe, ainda na aula, que a turma pode não ter acompanhado a estrutura nova (cenário problema C05, tarefa T03).

| Tópico > subtópico | Falas e signos envolvidos | Intenção/efeito esperado |
|---|---|---|
| **O11 Ativar o acompanhamento da turma** | `U: quero acompanhar a turma nesta aula` / `D: o acompanhamento está ativo; 4 de 8 alunos estão contribuindo` | Camila sabe, antes de começar, se o indicador terá base suficiente |
| > Avisar os participantes | `D: (para os alunos) o acompanhamento da turma está ativo; veja o que é e o que não é processado` | Os alunos não são surpreendidos; ligação com a interface do participante (T04) |
| > Não há participantes suficientes | `D: não há câmeras ligadas suficientes para estimar o estado da turma (mínimo: 3)` / `U: continuar sem acompanhamento` ou `U: tentar novamente` | Evitar um indicador sem base e explicar o motivo, sem bloquear a aula |
| **O12 Perceber o estado da turma** | `D: a turma parece estar acompanhando` (verde, ícone e rótulo) / `D: confiança alta; 4 de 8 contribuindo; atualizado há 20 s` | Leitura de relance durante a explicação, sem tirar a atenção da aula |
| **O13 Examinar uma mudança no estado** | `D: o estado mudou de "acompanhando" para "possível confusão" há 2 min` / `U: o que mudou?` | Chamar a atenção sem prescrever o que fazer (RC03) |
| > Dispensar o aviso | `U: entendi, pode esconder` / `D: aviso dispensado; o indicador continua mostrando o estado atual` | Não acumular avisos antigos (RC06) |
| **O14 Entender o significado e a confiança** | `U: o que significa "possível confusão"?` / `D: parte da turma mostra sinais associados a dificuldade; é uma estimativa do grupo, não de cada aluno, e pode errar` / `D: a confiança está média porque só metade da turma está com câmera` | Evitar confiança excessiva na estimativa (H02) e reforçar que o resultado não avalia alunos (H03) |
| **O15 Marcar o momento para revisar depois** | `U: marcar este momento` / `D: momento marcado aos 23 min na linha do tempo da aula` | Ligar a aula ao Dashboard sem anotação manual (R03) |
| **O16 Pausar ou retomar o acompanhamento** | `U: pausar o acompanhamento` / `D: acompanhamento pausado; os alunos foram avisados` / `U: retomar` | Dar controle à professora a qualquer momento (RC07) |
| **O17 Encerrar a aula com o resumo salvo** | `U: encerrar a aula` / `D: resumo salvo; disponível no Dashboard` | Garantir que a aula possa ser revisada depois |
| > Falha ao salvar | `D: não foi possível salvar o resumo agora; os dados continuam no seu computador` / `U: tentar novamente` ou `U: tentar mais tarde` | Recuperar de uma falha sem perder a aula |

Decidir se reforça o conteúdo **não é um tópico de conversa com o sistema**: é uma decisão de Camila, feita fora da interface. O sistema só oferece o sinal e a explicação para apoiar essa decisão.

**Nome do cenário:** CI03 — Acompanhar os estados da turma e revisar os resultados da aula.

| Tópico > subtópico | Falas e signos envolvidos | Intenção/efeito esperado |
|---|---|---|
| Acompanhar os estados da turma durante a aula | `U: consultar os indicadores da turma` / `D: apresentar estimativas dos estados cognitivos`. Signos: engajamento, tédio, confusão e frustração. | Complementar os sinais observados na videoconferência e apoiar a decisão do docente sobre a condução da aula. |
| > Compreender os indicadores | `D: explicar o significado dos indicadores e sua relação com os dados disponíveis`. Signos: significado dos estados e disponibilidade de dados. | Permitir a interpretação das informações sem apresentar as estimativas como certezas sobre os participantes. |
| Revisar os resultados após a aula | `U: consultar uma aula concluída` / `D: apresentar as reuniões disponíveis`. Signos: título e data da reunião. | Permitir que o docente identifique a aula que deseja analisar. |
| > Consultar o resumo da reunião | `U: abrir resumo da reunião` / `D: apresentar a identificação da reunião e seus indicadores`. Signos: título, data, estados cognitivos e indicadores exibidos. | Permitir que o docente examine os resultados e identifique suas necessidades de personalização. |
| > Personalizar a visualização | `U: personalizar visualização` / `D: apresentar os indicadores disponíveis` / `U: selecionar os indicadores desejados`. Signos: indicadores disponíveis e seleção de indicadores para exibição. | Adequar as informações apresentadas às necessidades de análise do docente. |
| > Salvar a personalização | `U: salvar alterações` / `D: configuração salva e aplicada`. Signos: configuração selecionada e situação do salvamento. | Confirmar que as alterações foram salvas e aplicadas ao resumo. |
| > Recuperar uma falha no salvamento | `D: não foi possível salvar; seleções preservadas` / `U: tentar salvar novamente, modificar a seleção ou cancelar`. Signos: mensagem de falha e seleção preservada. | Comunicar o problema e permitir a continuidade da tarefa sem refazer toda a seleção. |
| > Cancelar a personalização | `U: cancelar alterações` / `D: apresentar o resumo com a configuração anterior`. Signos: configuração anterior e indicadores exibidos. | Permitir o retorno à consulta sem aplicar as alterações não salvas. |
| > Conferir o resumo personalizado | `D: apresentar o resumo personalizado e a configuração aplicada`. Signos: indicadores exibidos, dados dos indicadores e seleção salva. | Permitir que o docente verifique se a visualização atende às suas necessidades. |
| > Revisar a personalização | `U: editar novamente` / `D: apresentar as opções de personalização`. Signos: indicadores disponíveis e seleção de indicadores. | Permitir novos ajustes quando o resultado ainda não atender às necessidades de análise. |


---

**Convenção:** `U` = usuário; `D` = preposto do designer/sistema, conforme a abordagem de Engenharia Semiótica adotada na disciplina.

## 3. Mapa de objetivos

Cada integrante apresenta seu mapa e a equipe cria um **mapa consolidado**, eliminando duplicidades e resolvendo conflitos de nomenclatura.

![Mapa consolidado](../assets/09_modelo_conceitual/mapa_objetivos.svg)

### Mapa individual 

**Autor(a):** Matheus Ferreira de Freitas — 22.125.085-5  
**Origem:** cenário problema C01 — Dificuldade em interpretar a reação do cliente durante uma apresentação comercial on-line (versão refinada da Entrega 4), tarefa T05 (Entrega 5) e persona P04 — Manoel Gomes

```mermaid
flowchart TD
    GERAL["`Conduzir a apresentação
    comercial percebendo a reação
    dos clientes e decidindo
    como prosseguir`"]

    O01["`**O01**
    Ativar o acompanhamento
    em uma reunião com clientes`"]

    O02["`**O02**
    Perceber o estado do grupo
    enquanto apresenta`"]

    O03["`**O03**
    Marcar o momento
    da pílula de dúvida`"]

    O04["`**O04**
    Verificar a reação depois
    da pílula de dúvida e
    quanto confiar nela`"]

    DEC["`Decidir se avança, reforça
    ou reexplica o ponto
    (fora do sistema)`"]

    O05["`**O05**
    Anotar um ponto
    para o follow-up`"]

    O06["`**O06**
    Encerrar a reunião
    com o resumo salvo`"]

    O07["`**O07**
    Revisar a reunião e registrar
    o retorno do cliente`"]

    GERAL --> O01
    GERAL --> O06
    O01 --> O02
    O02 --> O03
    O03 --> O04
    O04 --> DEC
    DEC -->|"quando o tempo está curto"| O05
    O06 --> O07
    O05 -.->|"anotações aparecem no resumo"| O07

    style DEC stroke-dasharray: 6 4
```
*A caixa tracejada é um objetivo de Manoel que acontece fora do sistema: a decisão de avançar, reforçar ou reexplicar continua sendo dele (RC03).*

### Dicionário de objetivos

| ID | Objetivo | Persona(s) | Cenário(s) | Prioridade |
|---|---|---|---|---|
| O01 | Ativar o acompanhamento em uma reunião com participantes de outra empresa, com o aviso enviado antes da primeira estimativa | P04 (também P01, P02 e P03) | CI01 | alta |
| O02 | Perceber o estado do grupo de clientes enquanto apresenta com a tela compartilhada | P04 (também P01, P02 e P03) | CI01 | alta |
| O03 | Marcar o momento da pílula de dúvida, ligando a reação ao trecho da proposta | P04 | CI01 | alta |
| O04 | Verificar a reação do grupo depois da pílula de dúvida e quanto confiar nela | P04 | CI01 | alta |
| O05 | Anotar um ponto para retomar no follow-up, sem interromper a reunião | P04 | CI01 | média |
| O06 | Encerrar a reunião com o resumo salvo | P04 | CI01 | média |
| O07 | Revisar a reunião e registrar, no momento marcado, se o retorno do cliente confirmou a leitura feita na reunião | P04 | CI01 | média |

---

**Autor(a):** Gustavo Bertoluzzi Cardoso — 22.123.016-2  
**Origem:** CI02 (cenário problema C03, tarefa T04), persona P05 — Bruno D. Roger.

```mermaid
flowchart TD
    G["<b>Participar da aula sabendo o que acontece<br/>com a própria imagem e decidindo como participar</b><br/>(P05 — Bruno, CI02)"]
    D1["<b>Ao entrar e durante a aula</b><br/>(interface do participante)"]
    D2["<b>Depois da aula</b>"]
    DEC["<b>Pesar o próprio conforto e a aula</b><br/>fora do sistema: decisão do aluno"]
    O18["<b>O18</b><br/>Entender o que acontece<br/>com a própria imagem"]
    O19["<b>O19</b><br/>Tirar uma dúvida<br/>específica sobre os dados"]
    O20["<b>O20</b><br/>Escolher como<br/>participar da aula"]
    O21["<b>O21</b><br/>Conferir se está<br/>contribuindo agora"]
    O22["<b>O22</b><br/>Mudar a participação<br/>durante a aula"]
    O23["<b>O23</b><br/>Conferir o que<br/>foi processado"]

    G --> D1
    G --> D2
    G --> DEC
    D1 --> O18
    O18 -->|"se ainda tiver dúvida"| O19
    DEC -.->|"orienta"| O20
    O18 --> O20
    O20 --> O21
    D1 --> O22
    O22 --> O21
    D2 --> O23
    O23 -.->|"se ainda tiver dúvida"| O19

    style DEC stroke-dasharray: 6 4
    style G fill:#eef2ff
    style D1 fill:#f3f4f6
    style D2 fill:#f3f4f6
```

*A caixa tracejada é um objetivo de Bruno que acontece fora do sistema: a decisão de ligar a câmera e de participar da análise é dele, e o sistema não recomenda nenhuma opção. O22 pode acontecer várias vezes, sempre que a situação mudar (T04, Plano 5).*

#### Dicionário de objetivos — CI02

| ID | Objetivo | Persona(s) | Cenário(s) | Prioridade |
|---|---|---|---|---|
| O18 | Entender o que acontece com a própria imagem nesta aula: o que é captado, o que a professora recebe e o que não é feito com os dados | P05 | CI02 | alta |
| O19 | Tirar uma dúvida específica sobre os dados e saber a quem perguntar quando a resposta não bastar | P05 | CI02 | média |
| O20 | Escolher como participar da aula (participar com câmera, câmera ligada sem participar da análise [H] ou câmera desligada) | P05 | CI02 | alta |
| O21 | Conferir se está contribuindo para a análise naquele momento | P05 | CI02 | alta |
| O22 | Mudar a participação durante a aula, pela câmera ou pausando só a análise [H] | P05 | CI02 | alta |
| O23 | Conferir depois da aula o que foi processado e que nada foi registrado sobre ele [H] | P05 | CI02 | média |

Os IDs O18 a O23 continuam a numeração depois de O17 (CI05). Eles não se fundem com os objetivos dos comunicadores, porque o ator é outro: Bruno é participante, não usa o Semáforo nem o Dashboard. Há duas ligações a manter na consolidação: o aviso de O18 é o mesmo **aviso aos participantes** gerado quando o comunicador ativa o acompanhamento (O01 e O11), e a pausa feita pelo comunicador (O16) aparece para o participante como estado da **análise da turma**, sem se confundir com a pausa da própria participação (O22).

---
**Autor(a):** Kayky Pires — 22.222.040-2   
**Origem:** cenário problema C02 — Dificuldade de Karol em perceber se a turma está acompanhando a aula on-line. 
**Persona relacionada:** P02 — Karol.
```mermaid
flowchart TD
    GERAL["`Analisar os estados
    da turma para apoiar
    decisões pedagógicas`"]

    O04["`**O04**
    Decidir se deve manter
    ou adaptar a condução
    da aula`"]

    O03["`**O03**
    Analisar os resultados
    de uma aula concluída`"]

    O02["`**O02**
    Interpretar os estados
    da turma durante a aula`"]

    O01["`**O01**
    Personalizar a visualização
    do resumo da reunião`"]

    O05["`**O05**
    Avaliar a adequação
    da visualização
    personalizada`"]

    GERAL --> O04
    GERAL --> O03

    O04 --> O02

    O03 -->|"quando necessário"| O01
    O01 --> O05
```

### Dicionário de objetivos

| ID | Objetivo | Persona(s) | Cenário(s) | Prioridade |
|---|---|---|---|---|
| O01 | Personalizar a visualização do resumo da reunião, selecionando os indicadores que deseja exibir. | P01 — Karol | CI01 | Alta |
| O02 | Interpretar os estados de engajamento, tédio, confusão e frustração durante a aula, considerando o significado dos indicadores, suas escalas e a disponibilidade dos dados. | P01 — Karol | CI01 | Alta |
| O03 | Analisar os resultados de uma aula concluída, identificando as informações relevantes para sua revisão e considerando os limites das estimativas apresentadas. | P01 — Karol | CI01 | Alta |
| O04 | Decidir se deve manter ou adaptar a condução da aula, utilizando os indicadores como apoio e considerando os demais sinais observados na videoconferência. | P01 — Karol | CI01 | Alta |
| O05 | Avaliar se a seleção de indicadores foi aplicada e se a visualização personalizada apresenta as informações necessárias à análise. | P01 — Karol | CI01 | Alta |

---

**Autor(a):** Rafael Dias — 22.222.039-4  
**Origem:** cenário problema C04 — Dificuldade em identificar a compreensão e o aprendizado durante treinamento on-line.  
**Persona relacionada:** P03 — Nathanael Lima.

```mermaid
flowchart TD
    GERAL["Acompanhar e analisar os estados do grupo para melhorar a condução dos treinamentos"]

    O06["O06 - Interpretar os estados do grupo durante o treinamento"]
    O07["O07 - Decidir se deve adaptar a condução do treinamento"]
    O08["O08 - Analisar os resultados de um treinamento concluído"]
    O09["O09 - Identificar períodos do treinamento que precisam de atenção"]
    O10["O10 - Avaliar melhorias para os próximos treinamentos"]

    GERAL --> O07
    GERAL --> O08

    O07 --> O06
    O08 --> O09
    O09 --> O10
```

### Dicionário de objetivos

| ID | Objetivo | Persona(s) | Cenário(s) | Prioridade |
|---|---|---|---|---|
| O06 | Interpretar os estados de engajamento, tédio, confusão e frustração durante o treinamento, considerando o significado dos indicadores e a disponibilidade dos dados. | P03 — Nathanael | CI04 | Alta |
| O07 | Decidir se deve manter ou adaptar a condução do treinamento, considerando os indicadores e as demais interações dos participantes. | P03 — Nathanael | CI04 | Alta |
| O08 | Analisar os resultados de um treinamento concluído, consultando os indicadores apresentados durante a sessão. | P03 — Nathanael | CI04 | Alta |
| O09 | Identificar períodos com possíveis sinais de confusão, tédio ou redução do engajamento que merecem atenção. | P03 — Nathanael | CI04 | Alta |
| O10 | Avaliar possíveis melhorias nos conteúdos e na condução dos próximos treinamentos com base na análise dos resultados. | P03 — Nathanael | CI04 | Média |

Os objetivos O06 e O07 correspondem ao acompanhamento durante o treinamento. Os objetivos O08, O09 e O10 correspondem à análise posterior da sessão.

---

**Autor(a):** Isabella Vieira Silva Rosseto — 22.222.036-0  
**Origem:** CI05 (cenário problema C05, tarefa T03), persona P02 — Camila Duarte.

```mermaid
flowchart TD
    G["<b>Conduzir a aula de inglês percebendo se a turma<br/>acompanha o conteúdo novo</b><br/>(P02 — Camila, CI05)"]
    D1["<b>Durante a aula</b><br/>(Semáforo Cognitivo)"]
    D2["<b>Ao fim da aula</b>"]
    DEC["<b>Decidir se reforça o conteúdo</b><br/>fora do sistema: decisão da professora"]
    O11["<b>O11</b><br/>Ativar o acompanhamento"]
    O12["<b>O12</b><br/>Perceber o estado da turma"]
    O16["<b>O16</b><br/>Pausar ou retomar<br/>o acompanhamento"]
    O13["<b>O13</b><br/>Examinar uma<br/>mudança no estado"]
    O14["<b>O14</b><br/>Entender o significado<br/>e a confiança"]
    O15["<b>O15</b><br/>Marcar o momento<br/>para revisar depois"]
    O17["<b>O17</b><br/>Encerrar a aula com<br/>o resumo salvo"]

    G --> D1
    G --> D2
    G --> DEC
    D1 --> O11
    D1 --> O12
    D1 --> O16
    O12 --> O13
    O12 --> O14
    O13 --> O15
    D2 --> O17

    style DEC stroke-dasharray: 6 4
    style G fill:#eef2ff
    style D1 fill:#f3f4f6
    style D2 fill:#f3f4f6
```

*A caixa tracejada é um objetivo de Camila que acontece fora do sistema. Versão em imagem: [PNG](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/09_modelo_conceitual/mapa_objetivos_ci05.png) · [SVG editável](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/09_modelo_conceitual/mapa_objetivos_ci05.svg).*

#### Dicionário de objetivos — CI05

| ID | Objetivo | Persona(s) | Cenário(s) | Prioridade |
|---|---|---|---|---|
| O11 | Ativar o acompanhamento da turma | P02 (também P01, P03, P04) | CI05 | alta |
| O12 | Perceber o estado da turma durante a explicação | P02 (também P01, P03, P04) | CI05 | alta |
| O13 | Examinar uma mudança no estado da turma | P02 | CI05 | alta |
| O14 | Entender o significado e a confiança da estimativa | P02 | CI05 | alta |
| O15 | Marcar um momento da aula para revisar depois | P02 | CI05 | média |
| O16 | Pausar ou retomar o acompanhamento | P02 | CI05 | média |
| O17 | Encerrar a aula com o resumo salvo | P02 | CI05 | média |

Os IDs O11 a O17 foram escolhidos para não repetir os IDs já usados na CI01 (O01 a O07) e na CI04 (O06 a O10). Alguns objetivos são equivalentes entre os cenários e devem virar um só na consolidação: O11 corresponde a O01 (ativar o acompanhamento), O12 a O02 e O06 (perceber/interpretar o estado do grupo), O14 a O04 (entender o significado e a confiança), O15 a O03 (marcar o momento) e O17 a O06 da CI01 (encerrar com o resumo salvo).

---

Os IDs O01 a O07 vêm da CI01. Na consolidação, a equipe junta os objetivos iguais dos outros cenários (ativar o acompanhamento, perceber o estado do grupo e encerrar com o resumo salvo também aparecem para Karol, Camila e Nathanael) e mantém um único ID para cada objetivo.

## 4. Esquema conceitual de signos

O esquema conceitual reúne os signos identificados nos cenários CI01, CI02, CI04 e CI05, considerando as necessidades das personas P04 — Manoel Gomes, P05 — Bruno D. Roger, P03 — Nathanael Lima e P02 — Camila Duarte.

Os signos compartilhados entre os cenários foram unificados, mantendo a mesma nomenclatura para garantir consistência nas próximas entregas.

| Grupo | Signo | Origem | Observações/semântica | Tipo de conteúdo | Restrição | Valor padrão | Prevenção | Recuperação |
|---|---|---|---|---|---|---|---|---|
| Acompanhamento | acompanhamento da reunião | sistema | Indica se a estimativa está ativa, pausada ou desligada na reunião ou treinamento atual. Em reuniões com participantes externos, só fica ativa depois do aviso. | estado: ativo / pausado / desligado | só o comunicador altera; não ativa antes do aviso obrigatório | desligado | PE: exigir o envio do aviso antes da ativação | RE: permitir pausar ou desligar a qualquer momento (RC07) |
| Acompanhamento | aviso aos participantes | sistema | Texto padrão informando o que é processado, quais informações não são coletadas e como não participar. Em reuniões com clientes externos, é enviado no chat com o link da página de transparência (T04). | texto + registro do envio (hora) | obrigatório antes da primeira estimativa | — | PE: impedir o início da estimativa antes do aviso | RE: permitir reenviar o aviso caso o envio falhe |
| Acompanhamento | participantes contribuindo | sistema | Quantidade de participantes com câmera ligada que contribuem para a estimativa em relação ao total da reunião, por exemplo, "3 de 4", sem identificar individualmente os participantes. | número inteiro "n de N" | n ≤ N; sem identificação individual | — | PP: apresentar a quantidade junto aos indicadores para contextualizar os resultados | — |
| Acompanhamento | mínimo de participantes | domínio | Quantidade mínima de participantes necessária para produzir uma estimativa agregada sem comprometer a privacidade. Aplica-se também a treinamentos com poucos participantes. | número inteiro | valor a validar na coleta da Entrega 7 (I05 e demais instrumentos pertinentes) | 3 (provisório) | PE: impedir a apresentação de estados estimados abaixo do mínimo | RE: explicar o motivo e permitir continuar sem acompanhamento |
| Estado do grupo | estado predominante | sistema | Estimativa agregada do grupo: acompanhando, possível tédio, possível confusão, possível frustração ou sem estimativa. Permite ao apresentador acompanhar possíveis mudanças durante a sessão. | lista fixa de estados, com cor + ícone + rótulo | nunca utilizar apenas cor (RC08); sempre representar o grupo, nunca um indivíduo (R04) | sem estimativa | PP: utilizar "possível" para comunicar a incerteza e oferecer explicação sob demanda | — |
| Estado do grupo | confiança da estimativa | sistema | Indica o grau de confiança da estimativa apresentada, considerando a qualidade dos dados disponíveis. Ajuda o apresentador a interpretar os resultados sem tratá-los como certezas. | faixa: alta / média / baixa | não utilizar percentual durante a reunião | — | PP: explicar os motivos de uma confiança média ou baixa | RE: permitir consultar a explicação do indicador |
| Estado do grupo | atualizado há | sistema | Tempo decorrido desde a última atualização da estimativa, permitindo identificar se o estado apresentado ainda corresponde ao momento atual. | segundos/minutos | deve corresponder à última atualização válida | — | PP: destacar quando a informação estiver desatualizada | — |
| Estado do grupo | mudança de estado | sistema | Comunica discretamente uma alteração no estado predominante do grupo, indicando o estado anterior, o atual e desde quando ocorreu. Pode ser associada ao trecho da apresentação ou treinamento. | estado anterior → estado atual + desde quando + trecho | um aviso por vez (RC06); não determinar ações ao comunicador (RC03) | — | PP: apresentar a mudança como estimativa, sem prescrever decisões | RE: permitir dispensar o aviso |
| Estado do grupo | qualidade do sinal | sistema | Explica possíveis limitações da estimativa, como câmeras desligadas, iluminação inadequada ou problemas de conexão. | texto curto | apresentar apenas informações que o sistema consegue identificar | — | PP: informar limitações que podem afetar a interpretação | RE: orientar a continuar a reunião normalmente quando não houver estimativa confiável |
| Estado do grupo | significado do indicador | domínio | Explica os estados de engajamento, tédio, confusão e frustração. Esclarece que representam estimativas afetivo-cognitivas e não comprovam diretamente a compreensão ou aprendizagem. | texto explicativo | utilizar linguagem compreensível e manter consistência com os indicadores apresentados | — | PP: disponibilizar explicações para evitar interpretações incorretas | RE: permitir consultar novamente o significado dos indicadores |
| Estado do grupo | disponibilidade de dados | sistema | Informa se existem dados suficientes para estimar o estado do grupo. Considera apenas os participantes que contribuem para a análise, sem identificá-los individualmente. | estado: disponível / insuficiente / indisponível | ausência de dados não pode ser representada como valor zero ou como ausência de dificuldade | indisponível antes da análise | PP: comunicar quando não existem dados suficientes para interpretar o grupo | RE: explicar a indisponibilidade e permitir continuar a reunião sem acompanhamento |
| Linha do tempo | momento marcado | usuário | Ponto da reunião identificado pelo apresentador para revisão posterior. Pode representar uma pílula de dúvida, um trecho da proposta ou um conteúdo importante do treinamento. | minuto da reunião + rótulo | deve estar dentro da duração da reunião | rótulo vazio | — | RE: permitir editar ou desmarcar o momento no resumo |
| Linha do tempo | anotação | usuário | Texto associado a um momento marcado, utilizado para registrar dúvidas, percepções ou assuntos que precisam ser retomados posteriormente. | texto | vinculada a um momento marcado | vazio | — | RE: permitir editar ou apagar a anotação |
| Linha do tempo | retorno do cliente | usuário | Registro posterior indicando se a resposta do cliente confirmou a interpretação realizada durante a reunião comercial. Específico da CI01. | confirmou / em parte / não / sem retorno | somente em momentos marcados | sem retorno | PP: mostrar junto ao estado e à anotação correspondente | RE: permitir atualizar o retorno registrado |
| Linha do tempo | resumo da reunião | sistema | Registro agregado da sessão concluída, contendo identificação, data, duração, indicadores ao longo do tempo, momentos marcados e anotações. Em reuniões comerciais, também pode conter retornos dos clientes. | registro com data, duração e linha do tempo | não armazenar imagens nem apresentar dados individuais | — | PE: salvar os dados localmente antes da sincronização, conforme o fluxo previsto | RE: permitir tentar salvar novamente ou posteriormente |
| Linha do tempo | período analisado | sistema | Identifica o intervalo da reunião ou treinamento ao qual os resultados correspondem. Permite relacionar os indicadores aos diferentes momentos da apresentação. | horário ou intervalo de tempo | deve corresponder aos dados efetivamente registrados na sessão | período atual durante o acompanhamento | PP: apresentar a referência temporal junto aos indicadores | RE: permitir consultar outros períodos disponíveis no resumo |
| Linha do tempo | variação dos indicadores | sistema | Representa as alterações das estimativas de engajamento, tédio, confusão e frustração ao longo da sessão. Ajuda a identificar momentos que merecem revisão após o treinamento. | série temporal ou gráfico | utilizar apenas resultados disponíveis e escalas consistentes | — | PP: identificar os indicadores e períodos apresentados e esclarecer que variações não comprovam aprendizagem | RE: informar períodos sem dados e permitir consultar os demais resultados |
| Linha do tempo | data da reunião | domínio | Identifica quando ocorreu a reunião ou treinamento, permitindo diferenciar sessões realizadas em momentos distintos. | data | deve corresponder à reunião selecionada | — | PP: apresentar junto à identificação da reunião | RE: permitir retornar à lista e selecionar outra reunião |
| Linha do tempo | título da reunião | domínio | Nome utilizado para identificar a reunião comercial ou treinamento corporativo que será analisado. | texto | deve corresponder à reunião selecionada | — | PP: apresentar junto à data para evitar confusão entre sessões semelhantes | RE: permitir retornar à lista e selecionar a reunião correta |
| Transparência | análise da turma | sistema | Estado do acompanhamento visto pelo participante, num indicador pequeno e permanente que também reabre o aviso. É o mesmo signo "acompanhamento", com rótulo do ponto de vista de quem é analisado. Específico da CI02. | estado: ativa / pausada pela professora / encerrada | só o comunicador altera; o participante apenas vê | — (só aparece quando o comunicador ativa) | PP: manter o indicador visível durante toda a aula e reabrir o aviso com um clique | RE: permitir reabrir o aviso a qualquer momento |
| Transparência | participação na análise | usuário | Escolha do participante sobre a própria imagem, separada de ligar ou desligar a câmera. Específico da CI02. | estado: participando / câmera ligada com análise pausada [H] / não participando | só o próprio participante altera; nunca é mostrada ao comunicador individualmente, só entra na contagem de participantes contribuindo | não participando até o participante escolher | PE: não começar a analisar a imagem sem uma escolha do participante; PP: confirmar no indicador cada mudança | RE: permitir mudar a escolha a qualquer momento da aula |
| Transparência | informações completas | domínio | Perguntas e respostas sobre os dados, escritas com as palavras do aluno ("isso conta na minha nota?", "a professora vê o meu rosto?"). Específico da CI02. | lista de perguntas e respostas | não usar termos técnicos de IA (RC04); dizer também o que não é feito com os dados | — | PP: organizar por dúvida do participante, e não por função do sistema | RE: indicar o contato para dúvidas quando a resposta não bastar |
| Transparência | contato para dúvidas | domínio | Pessoa ou canal indicado para perguntas sobre os dados da análise. Específico da CI02. | texto (nome do canal e forma de contato) | definido pela instituição ou pelo comunicador | — | PP: mostrar junto às informações completas e ao resumo de transparência | — |
| Transparência | resumo de transparência | sistema | Resumo, visto só pelo próprio participante, do que aconteceu com a imagem dele na aula: por quanto tempo contribuiu para a estimativa da turma e o que não foi guardado. Específico da CI02 [H]. | tempo de contribuição + lista do que não foi guardado | nunca mostra a estimativa da turma nem resultado individual (RC09); fica no aparelho do participante | — | PP: explicar o motivo quando a imagem não foi analisada na aula | RE: indicar o contato para dúvidas |

**Signos da CI05 (Isabella):** a CI05 usa os mesmos signos desta tabela, sem criar novos: acompanhamento, aviso aos participantes, participantes contribuindo, mínimo de participantes, estado predominante, confiança da estimativa, atualizado há, mudança de estado, qualidade do sinal, significado do indicador, momento marcado e resumo. No contexto de aula, "reunião" corresponde a "aula" e "grupo" a "turma"; o rótulo exibido muda, mas o conceito é o mesmo. A pausa do acompanhamento é um dos valores do signo "acompanhamento" (ativo, pausado ou desligado).

**Signos da CI02 (Gustavo):** a CI02 reusa **aviso aos participantes** e **participantes contribuindo** e acrescenta o grupo **Transparência** (análise da turma, participação na análise, informações completas, contato para dúvidas e resumo de transparência), que é o lado do participante. "Análise da turma" não é um conceito novo: é o signo "acompanhamento" visto por quem é analisado, com os mesmos valores. A **participação na análise** de cada pessoa nunca chega ao comunicador individualmente; ela só muda o número em "participantes contribuindo" (R04). Nenhum signo do grupo Estado do grupo aparece para o participante.

### Regras para os signos

- Os signos utilizam conceitos compreensíveis para as personas, como reunião, treinamento, estado do grupo, indicador, período e resumo.
- Signos compartilhados entre os cenários CI01 e CI04 foram unificados, evitando duplicações conceituais.
- Os signos `estado predominante`, `confiança da estimativa`, `participantes contribuindo` e `disponibilidade de dados` são utilizados para comunicar os resultados e suas limitações durante o acompanhamento.
- Os signos `momento marcado`, `anotação`, `período analisado` e `variação dos indicadores` permitem relacionar os resultados aos acontecimentos da reunião e apoiar a análise posterior.
- Os signos de origem **usuário** representam informações fornecidas ou registradas pelo apresentador.
- Os signos de origem **sistema** representam informações produzidas, registradas ou organizadas pelo MindFlow AI.
- Os signos de origem **domínio** representam conceitos e regras pertencentes ao contexto das reuniões e treinamentos.
- Os indicadores apresentados são estimativas de estados afetivo-cognitivos e não devem ser interpretados como comprovação de compreensão ou aprendizagem.
- As informações devem permanecer agregadas, respeitando a privacidade dos participantes e evitando a identificação individual.
- A ausência de dados deve ser diferenciada de resultados válidos, evitando interpretações equivocadas.
- O sistema deve comunicar os resultados e suas limitações, mantendo as decisões sobre a condução da reunião ou treinamento sob responsabilidade do apresentador.

**Siglas:**
- **PE:** prevenção de erro, mecanismo que impede a ocorrência de uma situação inadequada.
- **PP:** prevenção passiva, informação ou explicação que ajuda a evitar interpretações incorretas.
- **RE:** recuperação de erro, ação que permite ao usuário continuar ou corrigir uma situação problemática.
- **—:** indica que não existe valor padrão fixo ou que o campo não se aplica.
  
## Síntese

Quais objetivos/tópicos/signos deverão necessariamente aparecer nos diagramas MoLIC?

### Contribuição da CI01 — Matheus

**Contribuição da CI01 (Matheus):** os objetivos O01 a O07, os tópicos da tabela da seção 2 e os signos dos grupos "Acompanhamento", "Estado do grupo" e "Linha do tempo" devem aparecer no diagrama MoLIC da CI01 (Entrega 10). Os pontos que não podem faltar são:

- o **aviso aos participantes de outra empresa** antes da primeira estimativa, com a ruptura de **participantes insuficientes** e a saída para continuar sem acompanhamento;
- o **momento marcado** na pílula de dúvida, ligado à **mudança de estado** que vem em seguida, com a confiança e uma cena para entender o significado do estado;
- a decisão de avançar, reforçar ou reexplicar como algo **fora do sistema**, sem uma fala do sistema que diga a Manoel o que fazer;
- a **anotação** "retomar no follow-up" feita sem sair da apresentação;
- o **resumo da reunião** com o **retorno do cliente** registrado no mesmo momento marcado, e a **falha ao salvar** com recuperação.


### Contribuição da CI02 — Gustavo

**Contribuição da CI02 (Gustavo):** os objetivos O18 a O23, os tópicos da tabela da seção 2 e os signos do grupo "Transparência", junto com "aviso aos participantes" e "participantes contribuindo", devem aparecer no MoLIC M02 (Entrega 10), que é a conversa do participante. Os pontos que não podem faltar são:

- o **aviso de análise ativa** ao entrar e a forma de **reabri-lo pelo indicador** com a aula em andamento;
- as **informações completas** organizadas por perguntas do aluno, com o **contato para dúvidas** quando a resposta não bastar;
- a **escolha da participação** com as três opções, sem nenhuma fala do sistema que recomende uma delas, e o indicador confirmando a escolha;
- a **pausa só da análise** sem desligar a câmera e o que acontece quando a câmera é desligada ou religada na plataforma;
- a **pausa feita pela professora** chegando ao participante como estado da análise da turma;
- o **encerramento da análise junto com a aula** e o **resumo de transparência**, inclusive quando a imagem não foi analisada;
- a ruptura do **aparelho sem processamento local**, com saída para seguir a aula sem participar da análise.

**Contribuição da CI04 (Rafael):** os objetivos O06 a O10 do mapa individual, os tópicos da tabela da seção 2 e os signos dos grupos "Acompanhamento", "Estado do grupo" e "Linha do tempo" devem aparecer no diagrama MoLIC da CI04 (Entrega 10). Os pontos que não podem faltar são:

- o **acompanhamento do estado do grupo durante o treinamento**, apresentando as estimativas de engajamento, tédio, confusão e frustração, junto à quantidade de **participantes contribuindo** e à **disponibilidade de dados**;
- a possibilidade de **compreender o significado dos indicadores**, consultando a **confiança da estimativa** e a **qualidade do sinal**, para evitar que Nathanael interprete os resultados como uma confirmação do aprendizado dos participantes;
- a **mudança de estado do grupo** durante a apresentação, permitindo identificar possíveis momentos de confusão, tédio ou perda de engajamento, sem interromper o ritmo do treinamento;
- a decisão de **manter ou adaptar a condução do treinamento** como uma responsabilidade de Nathanael, tomada **fora do sistema**, sem uma fala que determine se ele deve repetir o conteúdo, modificar o ritmo ou solicitar uma interação;
- o **resumo da reunião** após o encerramento do treinamento, apresentando o **período analisado** e a **variação dos indicadores** ao longo da sessão, permitindo identificar momentos que merecem revisão;
- a possibilidade de **avaliar melhorias para os próximos treinamentos**, utilizando os resultados disponíveis como apoio para revisar conteúdos e estratégias de apresentação, sem tratar as estimativas como medidas diretas de aprendizagem;
- a **ruptura de dados insuficientes ou indisponíveis**, com uma explicação clara sobre a ausência de resultados e a possibilidade de continuar o treinamento normalmente, sem depender do acompanhamento pelo sistema.

### Contribuição da CI05 — Isabella

**Contribuição da CI05 (Isabella):** os objetivos O11 a O17, os tópicos da tabela da seção 2 e os signos do grupo "Acompanhamento", "Estado da turma", "Linha do tempo" e "Transparência" devem aparecer no MoLIC M05 (Entrega 10). Os pontos que não podem faltar são:

- a ruptura de **participantes insuficientes** ao ativar e durante a aula, com saída para continuar sem acompanhamento;
- a **confiança da estimativa** junto do estado, com uma cena para entender o significado e o motivo da confiança;
- o **acesso ubíquo** para pausar e para abrir a ajuda;
- a **falha ao salvar** o resumo, com recuperação;
- a decisão de reforçar como algo **fora do sistema**, sem uma fala do sistema que diga à professora o que fazer.

## Checklist

- [ ] Cenários de interação mostram alterações em relação aos cenários de problema.
- [ ] Cada solução individual identifica autor e cenário de origem.
- [ ] Tópicos/falas/signos são coerentes com objetivos do usuário.
- [ ] Mapas individuais foram consolidados.
- [ ] O esquema de signos está em uma tabela única e sem duplicações conceituais.
- [ ] Nomes de objetivos/signos serão reutilizados na Entrega 10.
- [ ] Em TCC técnico, signos representam conceitos do domínio compreensíveis ao usuário, não apenas variáveis/estruturas internas.
- [ ] Padrões como dashboard, relatório, filtros, administração e CRUD possuem objetivos e signos correspondentes.
- [ ] A interface comunica não só o resultado técnico, mas também seu significado para a tarefa.
