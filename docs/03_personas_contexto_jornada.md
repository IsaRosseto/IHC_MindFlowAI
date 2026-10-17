# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** 27/08/2026  
**Status:** 🟩 concluído  
**Responsabilidade:** 1 persona por integrante; 1 mapa de empatia, 1 contexto de uso consolidado e 1 jornada por equipe (salvo orientação diferente do docente).

## Objetivo da atividade

Representar grupos de usuários de forma útil para decisões de design. Persona não é personagem decorativo: suas características devem alterar requisitos, prioridades, linguagem, fluxos ou critérios de avaliação.

## Relação com o projeto de IHC

O MindFlow AI já prevê uma interface como parte do TCC. Conforme a Entrega 1 e a matriz de rastreabilidade, o projeto de IHC prioriza o **comunicador** — como professor, instrutor, palestrante ou apresentador comercial — que precisa perceber em tempo real o estado afetivo-cognitivo agregado do grupo sem tirar a atenção da condução da sessão.

O recorte principal é o **Semáforo Cognitivo em tempo real**. O **Dashboard pós-sessão** é o recorte secundário para revisão da linha temporal e dos momentos de maior dificuldade. Como ainda não há pesquisa com usuários reais registrada, as personas desta entrega são **proto-personas a validar**.

## Entradas da Entrega 1

| Item da Entrega 1 | Status inicial | Evidência disponível agora | Como será tratado nesta entrega |
|---|---|---|---|
| Comunicador — professor, instrutor, palestrante ou apresentador — como usuário prioritário | H | Entrega 1, itens 2.2 e 7.2; matriz de rastreabilidade, seção 1 | Incorporar nas personas e manter como hipótese até a validação com usuários |
| Objetivo de perceber o estado do grupo em tempo real sem tirar a atenção da condução | H | Entrega 1, itens 3.1, 7.3 e 9.1 | Incorporar nos objetivos, necessidades, contexto e jornada |
| A01 — perceber o estado do grupo durante a sessão | H | Entrega 1, item 3.2 | Representar na jornada e nas decisões de design |
| A02 — ajustar a condução da sessão em resposta ao estado percebido | H | Entrega 1, item 3.2 | Representar como objetivo do comunicador, sem transformar a ação em resposta automática do sistema |
| A03 — revisar após a sessão os momentos de maior confusão ou desengajamento | H | Entrega 1, item 3.2 | Representar na etapa pós-sessão da jornada |
| H01 — o comunicador considera útil um indicador discreto durante a própria sessão | H, aberta | Matriz de rastreabilidade, seção 2 | Manter como hipótese central a ser validada |
| H02 — o nível de confiança deve aparecer para evitar confiança cega na classificação | H, aberta | Matriz de rastreabilidade, seção 2 | Incorporar como necessidade e oportunidade de design, ainda sem tratá-la como requisito validado |
| H03 — o participante pode sentir desconforto com a classificação de seu comportamento | H, aberta | Matriz de rastreabilidade, seção 2 | Considerar no contexto social, na transparência e na privacidade |
| Turmas pequenas, de 5 a 15 alunos, como recorte específico de P02 | H nova | Informação introduzida nesta entrega; não constava na Entrega 1 | Investigar se o indicador agregado continua representativo em grupos pequenos |

## 1. Personas

### Persona P01 — Karol Schrödinger

**Autor:** Kayky Pires de Paula — 22.222.040-2  
**Tipo:** primária  
**Base de evidências:** proto-persona baseada na Entrega 1; ainda sem entrevista ou observação com usuários reais  
**Hipóteses da Entrega 1 relacionadas:** H01 e H02

<img src="https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/03_personas/Karol.png" width="300" alt="Persona P01 — Karol">

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | 35 anos; professora que ministra aulas por videoconferência |
| Ocupação/papel | Professora de Filosofia no ensino a distância e responsável pela condução das aulas |
| Conhecimento do domínio | Alto domínio do conteúdo que ensina e sete anos de experiência como professora |
| Experiência tecnológica | Familiaridade baixa a média com plataformas de videoconferência, ambientes virtuais de aprendizagem e compartilhamento de conteúdo |
| Objetivos | Fazer com que os alunos compreendam o conteúdo de Filosofia por meio de aulas didáticas, claras e facilitadoras, mesmo no ensino a distância |
| Necessidades | Compreender como a turma está reagindo durante a aula e saber quando pode ser necessário mudar a forma de explicar o conteúdo |
| Dores/frustrações | Sente falta de observar as expressões e reações dos alunos como fazia presencialmente e se preocupa quando recebe pouco retorno da turma |
| Motivadores | Paixão por ensinar, ajudar os alunos a compreender conteúdos complexos e melhorar continuamente suas aulas |
| Restrições/acessibilidade | Possui baixa a média familiaridade com ferramentas digitais e, durante as aulas, divide a atenção entre apresentação, chat, alunos e conteúdo. Por isso, precisa de uma interface simples, com poucas informações simultâneas e leitura rápida. |
| Ambiente típico de uso | Pequena sala iluminada em sua residência, utilizando notebook, webcam e internet para ministrar aulas on-line |
| Comportamentos relevantes | Observa câmeras e chat, pergunta se os alunos entenderam e, diante de pouca participação, utiliza resumos, tópicos e novos exemplos |

> Os dados específicos de Karol são características da proto-persona e ainda precisam ser validados. Eles não constituem evidência sobre todos os professores.

**Decisões de design influenciadas por P01:**

- Priorizar informações simples e rápidas de interpretar durante a aula.
- Evitar elementos e interações que disputem a atenção da professora.
- Utilizar linguagem clara, considerando sua familiaridade tecnológica baixa a média.
- Apresentar as classificações como estimativas de apoio, sem transmitir certeza absoluta.

### Persona P02 — Camila Duarte

**Autora:** Isabella Vieira Silva Rosseto — 22.222.036-0  
**Tipo:** primária  
**Base de evidências:** proto-persona construída a partir das hipóteses e do usuário definido na Entrega 1; ainda sem entrevista ou observação com usuários reais  
**Hipóteses da Entrega 1 relacionadas:** H01 e H02; inclui a hipótese nova sobre turmas pequenas

<img src="https://github.com/user-attachments/assets/7c55de54-a37e-44a8-a060-c40d44d79be6" width="300" alt="Persona P02 — Camila Duarte">

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | 34 anos; ministra aulas por videoconferência para turmas pequenas, de 5 a 15 alunos |
| Ocupação/papel | Professora de inglês em uma escola de idiomas e em turmas particulares |
| Conhecimento do domínio | Alto; formada em Letras e com certificação internacional de proficiência |
| Experiência tecnológica | Média; utiliza Zoom, Google Meet e ferramentas básicas de apresentação, mas não é especialista em tecnologia |
| Objetivos | Manter a turma engajada e perceber rapidamente quando os alunos estão encontrando dificuldade no conteúdo |
| Necessidades | Receber um sinal simples do estado geral da turma sem precisar verificar cada rosto enquanto fala e compartilha a tela |
| Dores/frustrações | Pode perceber somente na correção de um exercício ou na aula seguinte que parte da turma não compreendeu o conteúdo |
| Motivadores | Ver os alunos evoluindo no idioma e sentir que a aula produziu compreensão, não apenas exposição de conteúdo |
| Restrições/acessibilidade | Nenhuma restrição de acessibilidade conhecida; possui pouco tempo entre uma aula e outra, portanto uma nova ferramenta precisa ser rápida de compreender |
| Ambiente típico de uso | Ministra aulas de casa, com notebook e webcam, em um ambiente que pode sofrer interrupções domésticas |
| Comportamentos relevantes | Compartilha exercícios e slides, fala durante grande parte da aula e consulta rapidamente a grade de vídeo entre as atividades |

> Os dados específicos de Camila são características da proto-persona. O recorte de 5 a 15 alunos é uma hipótese nova e deve ser investigado.

**Decisões de design influenciadas por P02:**

- Permitir que o Semáforo Cognitivo seja interpretado de relance.
- Avaliar se o indicador agregado continua significativo em grupos pequenos.
- Evitar terminologia técnica de inteligência artificial.
- Representar o nível de confiança de maneira simples, conforme H02.

### Persona P03 — Nathanael Lima

**Autor:** Rafael Dias — 22.222.039-4  
**Tipo:** primária  
**Base de evidências:** proto-persona a validar, construída a partir do contexto de treinamento corporativo previsto na Entrega 1  
**Hipóteses da Entrega 1 relacionadas:** H01, H02 e H03


<img src="https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/03_personas/persona_nathanael.png" width="300" alt="Persona P03 — Nathanael Lima">

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | 25–30 anos; profissional de Treinamento e Desenvolvimento que conduz capacitações on-line para equipes de diferentes áreas |
| Ocupação/papel | Instrutor corporativo responsável por apresentar processos, ferramentas e procedimentos internos |
| Conhecimento do domínio | Alto conhecimento dos processos que ensina, mas trabalha com públicos de áreas e níveis de experiência variados |
| Experiência tecnológica | Familiaridade média a alta com videoconferência, apresentações, enquetes, formulários e plataformas corporativas |
| Objetivos | Fazer com que os participantes compreendam o treinamento e consigam aplicar o conteúdo nas atividades de trabalho |
| Necessidades | Perceber durante o treinamento quando o grupo encontra dificuldade e identificar posteriormente partes da apresentação que precisam ser melhoradas |
| Dores/frustrações | Tem dificuldade para interpretar silêncio ou pouca participação de pessoas que não conhece; muitas vezes descobre falhas de compreensão somente após o treinamento |
| Motivadores | Realizar capacitações objetivas, reduzir dúvidas posteriores e melhorar seus materiais para os próximos grupos |
| Restrições/acessibilidade | Nenhuma restrição de acessibilidade conhecida; precisa cumprir uma pauta em tempo limitado e divide a atenção entre apresentação, chat, perguntas e cronograma |
| Ambiente típico de uso | Escritório ou home office, utilizando notebook, headset e plataforma de videoconferência |
| Comportamentos relevantes | Apresenta exemplos práticos, faz perguntas rápidas, utiliza enquetes e revisa feedbacks para ajustar os materiais |

> Os dados específicos de Nathanael são características da proto-persona e devem ser validados com profissionais de treinamento corporativo.

**Decisões de design influenciadas por P03:**

- Apresentar informações objetivas sem interromper o ritmo do treinamento.
- Permitir a consulta posterior dos períodos em que o grupo apresentou maior dificuldade.
- Investigar a comparação entre sessões ou turmas, atualmente registrada apenas como possibilidade na Entrega 1.
- Manter os resultados agregados e considerar o receio de uso para avaliação individual, relacionado a H03.

### Persona P04 — Manoel Gomes

**Autor(a):** Matheus Ferreira de Freitas — RA 22.125.085-5  
**Tipo:** primária  
**Base de evidências:** proto-persona a validar, construída a partir das hipóteses da Entrega 1, estendendo o perfil do comunicador para o contexto comercial  
**Hipóteses da Entrega 1 relacionadas:** H01, H03, H04

<img src="https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/03_personas/persona_manoel_gomes.png" width="300" alt="Persona P04 — Manoel Gomes">


| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | 38–45 anos; vendedor que apresenta propostas e demonstrações por videoconferência (Microsoft Teams) para clientes de outras empresas |
| Ocupação/papel | Executivo de vendas B2B, responsável por conduzir reuniões comerciais com grupos de 3 a 10 participantes do lado do cliente |
| Conhecimento do domínio | Alto no produto e no discurso de venda, com anos de experiência em reunião presencial, onde lia o cliente pelo olhar e pela postura |
| Experiência tecnológica | Média; usa Teams, CRM e slides todos os dias, mas não tem paciência para ferramenta complicada — precisa funcionar sem atrapalhar a reunião |
| Objetivos | Saber, ainda durante a fala, se o cliente está compreendendo e comprando a ideia, para ajustar o discurso na hora e aumentar a chance de fechar a venda |
| Necessidades | Um sinal em tempo real da reação do grupo enquanto apresenta, principalmente logo depois das "pílulas de dúvida" — perguntas curtas que ele solta de propósito para testar se o cliente entendeu e se interessou |
| Dores/frustrações | Hoje, sem a ferramenta, ele tem dificuldade de entender os clientes no mundo virtual: não consegue ver todos na grade do Teams (ainda mais compartilhando tela) e não sabe se estão de fato compreendendo o discurso; muitas vezes interpreta o silêncio como acordo e só descobre a objeção dias depois, quando a proposta é recusada por e-mail |
| Motivadores | Bater meta, encurtar o ciclo de venda e chegar no follow-up sabendo exatamente qual parte da proposta precisa reforçar |
| Restrições/acessibilidade | Apresenta quase sempre com tela compartilhada, o que esconde a grade de vídeo; o tempo da reunião é definido pelo cliente e costuma ser curto; não pode constranger o cliente com cobrança direta de atenção |
| Ambiente típico de uso | Home office ou mesa do escritório, notebook com headset, várias reuniões comerciais por dia no Teams |
| Comportamentos relevantes | Sem a ferramenta, ele conduz assim: apresenta compartilhando a tela, tenta espiar a grade reduzida de vídeo enquanto fala, solta as pílulas de dúvida ("faz sentido para a operação de vocês?", "esse ponto ficou claro?") e, como nem todos aparecem ou respondem, anota o que conseguiu captar e manda e-mail de follow-up tentando adivinhar onde perdeu o cliente |

**Decisões de design influenciadas por P04:**

- O Semáforo Cognitivo precisa ser legível de relance com a tela compartilhada, sem cobrir o material da apresentação — a mesma atenção dividida das demais personas, agora em reunião com cliente.
- O sinal em tempo real precisa reagir rápido o suficiente para mostrar a reação do grupo logo após uma pílula de dúvida, que é o momento em que Manoel decide se avança ou reexplica (H01, H04).
- O sistema deve indicar quantos participantes estão contribuindo para o sinal (câmeras abertas ou não), para Manoel saber o quanto pode confiar no agregado antes de mudar o discurso por causa dele.
- Como os participantes são clientes de outra empresa, o aviso e o consentimento sobre a classificação ficam ainda mais sensíveis (H03) — o uso comercial não pode acontecer sem transparência para os convidados.

### Persona P05 — Bruno D. Roger

**Autor(a):** Gustavo Bertoluzzi Cardoso - 22.123.016-2  
**Tipo:** secundária  
**Base de evidências:** proto-persona a validar. A gente já tinha percebido lá na Entrega 1 que o aluno que participa da chamada é afetado pelo sistema mas não chega a usar a interface, então essa persona vem daí  
**Hipóteses da Entrega 1 relacionadas:** H03

<img width="450" alt="Gemini_Generated_Image_nocb3hnocb3hnocb" src="https://github.com/user-attachments/assets/1ea7d2ce-5920-4bab-874f-091bec03ca7a" />

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | 20 anos, aluno de graduação que assiste aula por videoconferência como parte de uma disciplina EAD |
| Ocupação/papel | Participante da chamada, ele que fornece os dados captados pela webcam, mas quem usa a tela do MindFlow é o professor, não ele |
| Conhecimento do domínio | Conhecimento baixo ou médio do conteúdo da matéria, afinal ele tá ali pra aprender |
| Experiência tecnológica | Usa Zoom, Meet e vídeo chamada o tempo todo no celular, mas nunca ouviu falar de um sistema que analisa expressão facial durante aula |
| Objetivos | Acompanhar a aula, entender o conteúdo e conseguir tirar dúvida quando precisa |
| Necessidades | Saber o que é feito com a imagem dele captada pela câmera e sentir que assistir aula não é a mesma coisa que estar sendo vigiado |
| Dores/frustrações | Fica incomodado de pensar que o rosto dele pode estar sendo analisado por um sistema sem saber direito o que tá sendo medido. Tem medo de que parecer confuso ou parecer desatento vire algum tipo de avaliação sobre ele, mesmo sabendo que o resultado é só um número agregado da turma inteira |
| Motivadores | Aprender direito o conteúdo e ter a privacidade dele respeitada durante a aula |
| Restrições/acessibilidade | Pode escolher deixar a câmera desligada, mas às vezes isso depende da regra do professor ou da instituição |
| Ambiente típico de uso | Assiste aula de casa, no quarto ou num espaço dividido com a família, usando notebook ou até celular |
| Comportamentos relevantes | Liga e desliga a câmera dependendo de como tá se sentindo naquele dia, fica mais retraído quando sabe que tem algo analisando ele e provavelmente nunca ouviu falar do Semáforo Cognitivo, porque essa tela é só do professor |

**Decisões de design influenciadas por P05:**

- Reforça que precisa existir algum aviso pro aluno de que a aula está sendo classificada, mesmo que ele nunca veja o resultado
- Confirma que o resultado do sistema tem que ficar agregado, sem apontar aluno específico, pra não virar avaliação individual
- Ajuda a justificar o processamento local no próprio dispositivo, não só pela LGPD, mas também pra diminuir a sensação de estar sendo vigiado
- Levanta uma dúvida pra investigar depois, se desligar a câmera pode prejudicar o aluno de alguma forma


### Síntese das personas

As personas P01, P02, P03 e P04 foram mantidas como **personas primárias** porque todas utilizam diretamente o Semáforo Cognitivo e o Dashboard, mas possuem necessidades, prioridades e contextos de uso que geram diferenças importantes para o design da interface.

**P01 — Karol Schrödinger** representa o contexto de ensino a distância com menor familiaridade tecnológica. Para ela, a interface precisa ser simples, direta e fácil de interpretar, com o mínimo possível de elementos que disputem sua atenção durante a aula.

**P02 — Camila Duarte** representa aulas mais interativas e turmas pequenas. Nesse caso, além da leitura rápida durante a aula, é importante entender se o indicador agregado continua útil quando poucos participantes contribuem para o sinal e permitir que ela organize rapidamente quais informações deseja acompanhar no dashboard.

**P03 — Nathanael Lima** representa o contexto de treinamento corporativo, em que existe maior necessidade de revisar resultados depois da sessão, comparar treinamentos e identificar partes do conteúdo que precisam ser melhoradas. Seu contexto também traz uma preocupação maior com o uso dos dados, já que as informações não devem ser interpretadas como avaliação individual dos funcionários.

**P04 — Manoel Gomes** representa apresentações comerciais para clientes externos. Ele costuma trabalhar com tela compartilhada, reuniões curtas e pouco espaço disponível na interface, o que exige indicadores ainda mais rápidos e discretos. Nesse cenário, transparência e privacidade também ganham maior peso por envolver pessoas externas à organização.

Apesar de compartilharem o objetivo geral de acompanhar melhor a reação do grupo durante uma apresentação, essas personas possuem necessidades que alteram prioridades da interface, como nível de simplicidade, quantidade de informação exibida, personalização do dashboard, comparação entre sessões, uso durante compartilhamento de tela e cuidados com privacidade.

Por isso, uma interface projetada pensando apenas em uma dessas personas poderia não atender completamente às necessidades das demais.

A **P02 — Camila Duarte** será utilizada como persona de referência principal para o mapa de empatia e para a jornada desta entrega, por representar de forma clara o uso do MindFlow durante uma aula on-line. Essa escolha não elimina as demais personas primárias, que continuam sendo consideradas nas decisões de design e nas próximas etapas do projeto.

**P05 — Bruno D. Roger** é classificado como **persona secundária**. Ele não utiliza o Semáforo Cognitivo nem o Dashboard, mas possui interação própria com o MindFlow por meio das informações de transparência e participação. Suas necessidades influenciam principalmente decisões relacionadas à privacidade, clareza sobre o processamento dos dados e controle do participante.


## 2. Mapa de empatia — equipe

**Persona escolhida:** P02 — Camila Duarte  
**Justificativa:** Camila foi escolhida como referência por representar diretamente o comunicador definido na Entrega 1 em uma situação concreta de aula on-line. Sua atenção dividida entre explicação, compartilhamento de tela e observação dos alunos permite explorar a hipótese H01. O recorte de turma pequena também introduz uma questão relevante para validação: se um indicador agregado continua útil quando o grupo possui poucos participantes.


<img src="https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/03_personas/mapa_empatia_camila.png" width="590" alt="Mapa de empatia da persona P02 — Camila Duarte">

**O que vê [H]:** a própria tela de compartilhamento, uma grade pequena de vídeo no canto, alguns alunos com câmera desligada.

**O que ouve [H]:** os alunos respondendo os exercícios em voz alta, silêncio quando ninguém entende a pergunta, às vezes o próprio som da casa.

**O que diz e faz [H]:** explica a matéria, faz perguntas pra turma, tenta puxar quem está mais quieto, compartilha exercício na tela.

**O que pensa e sente [H]:** preocupação de estar falando sozinha sem saber se a turma está acompanhando, ansiedade de não ter feedback claro durante a aula.

**Dores [H]:** perceber tarde demais que um aluno específico ficou perdido num tópico, não ter como saber se o silêncio da turma é atenção ou desânimo.

**Ganhos/necessidades [H]:** um sinal rápido e confiável do clima da turma, que não a distraia da própria condução da aula.




## 3. Contexto de uso — consolidação

| Dimensão | Descrição | Implicação de design |
|---|---|---|
| Usuários | Os usuários principais são professores, instrutores e apresentadores que conduzem sessões por videoconferência. P01 — Karol representa o ensino a distância, P02 — Camila representa aulas de idioma em turmas pequenas, P03 — Nathanael representa treinamentos corporativos e P04 — Manoel representa apresentações comerciais para clientes externos. P05 — Bruno participa da sessão e utiliza apenas as informações de transparência e participação do MindFlow, não o Semáforo Cognitivo ou o Dashboard. | A interface principal precisa atender diferentes contextos de comunicação sem exigir mudanças grandes no fluxo. O Semáforo e o Dashboard devem ser voltados ao comunicador, enquanto o participante precisa ter acesso somente às informações necessárias para compreender o processamento realizado. |
| Tarefas | Durante a sessão, o comunicador apresenta conteúdo, pode compartilhar a tela, acompanhar chat e participantes e tentar perceber se o grupo está acompanhando. O MindFlow funciona como apoio nessa percepção, sem substituir a avaliação do próprio comunicador. Após a sessão, o usuário pode revisar momentos importantes e utilizar essas informações para melhorar aulas, treinamentos ou apresentações futuras. | O Semáforo Cognitivo deve oferecer uma leitura rápida e discreta durante a sessão. As inferências não devem ser apresentadas como certezas nem determinar automaticamente qual ação o comunicador deve tomar. O Dashboard deve permitir uma revisão posterior simples e útil. |
| Equipamentos | O uso ocorre principalmente em notebook ou desktop com webcam, podendo envolver headset, monitor adicional e ferramentas de apresentação. O comunicador também pode estar compartilhando a tela durante grande parte da sessão. Os participantes podem utilizar notebook, computador ou celular e nem sempre manter a câmera ligada. | O indicador precisa ocupar pouco espaço, permanecer legível mesmo durante o compartilhamento de tela e funcionar em diferentes configurações de equipamento. Também deve considerar situações em que nem todos os participantes estejam contribuindo para a análise. |
| Ambiente físico | O uso pode acontecer em casa, escola, escritório ou ambiente corporativo. Condições como iluminação, ruído, conexão com a internet, posição da webcam e presença de outras pessoas no ambiente podem variar e interferir na qualidade dos sinais analisados. | O sistema deve considerar variações na qualidade da captura e evitar apresentar inferências de baixa qualidade como certezas. Quando necessário, deve informar de maneira simples que a qualidade ou confiança da análise está reduzida. |
| Ambiente social/organizacional | O MindFlow pode ser utilizado em relações diferentes, como professor e aluno, instrutor e funcionário ou apresentador comercial e cliente. Esses contextos possuem diferentes níveis de autoridade, expectativa de privacidade e liberdade para participar. O uso também pode ser definido pelo próprio comunicador ou por uma escola, empresa ou instituição. | A interface deve considerar que os participantes podem se sentir monitorados ou pouco à vontade para recusar o uso da câmera. Os resultados devem permanecer agregados e servir como apoio ao comunicador, sem serem utilizados como avaliação individual. O sistema também precisa apresentar de forma clara sua finalidade e os limites das inferências realizadas. |
| Papéis/permissões/governança | O Semáforo Cognitivo e o Dashboard são destinados ao comunicador. Os participantes não visualizam esses painéis, mas possuem uma interação própria com o MindFlow por meio das informações de transparência sobre o processamento realizado. Devem conseguir saber que o sistema está sendo utilizado, quais informações são processadas e qual é a finalidade da análise. A forma de consentimento ou possibilidade de recusa ainda precisa ser investigada. | O sistema deve separar claramente a interface analítica do comunicador da interface de transparência destinada aos participantes. As informações apresentadas ao participante devem ser simples e explicar o que é processado e o que é disponibilizado ao comunicador, sem dar acesso ao Semáforo ou ao Dashboard. |
| Volume de dados/histórico | O número de participantes pode variar de pequenos grupos a turmas maiores. Após as sessões, pode existir interesse em consultar momentos anteriores e comparar diferentes aulas, treinamentos ou apresentações. Neste momento, o projeto trabalha com informações agregadas do grupo e não assume a existência de histórico individual por participante. | O Dashboard deve organizar o histórico principalmente por sessão e por grupo, permitindo comparar momentos e sessões quando isso for útil. Qualquer acompanhamento individual deve permanecer como hipótese futura e só poderá ser incluído se houver necessidade de usuário, justificativa de privacidade e validação nas próximas etapas. |




## 4. Jornada do usuário — equipe

**Persona:** P02 — Camila Duarte  
**Objetivo da jornada:** conduzir uma aula de inglês por videoconferência, acompanhar possíveis mudanças no estado geral da turma sem perder o foco da explicação e utilizar as informações obtidas para melhorar aulas futuras.  
**Início e fim da jornada:** começa antes da interação com o MindFlow, quando Camila prepara a aula e pensa em dificuldades percebidas em encontros anteriores, e termina depois do uso do sistema, quando decide se e como vai adaptar uma próxima aula com base nas informações observadas.

| Etapa | Situação/ação | Objetivo | Pensamento/emoção | Dor | Oportunidade de design | Evidência |
|---|---|---|---|---|---|---|
| 1 | Antes da aula, Camila prepara o conteúdo e relembra pontos em que os alunos tiveram dificuldade em encontros anteriores | Planejar uma aula clara e tentar evitar que as mesmas dúvidas se repitam | Quer preparar uma aula melhor, mas nem sempre sabe quais momentos realmente foram mais difíceis para a turma | O feedback que recebe normalmente é limitado e pode aparecer somente durante exercícios ou em aulas posteriores | O MindFlow pode apoiar a preparação futura ao permitir consultar informações de sessões anteriores sem substituir a percepção da professora | H |
| 2 | Pouco antes da aula, abre a videoconferência e prepara as ferramentas que vai utilizar | Deixar a aula pronta sem gastar muito tempo com configurações | Quer começar a aula sem precisar aprender ou configurar várias coisas | Possui pouco tempo entre aulas e uma ferramenta complexa pode atrapalhar sua rotina | Permitir ativação rápida e configurações simples, deixando informações mais avançadas como opcionais | H |
| 3 | Começa a aula, compartilha a tela e explica um novo conteúdo | Ensinar o conteúdo com clareza e manter o ritmo da aula | Focada na explicação e dividindo a atenção entre slides, chat e participantes | Não consegue acompanhar continuamente as câmeras e reações dos alunos enquanto apresenta | O Semáforo Cognitivo deve permanecer visível de forma discreta e permitir leitura rápida sem disputar atenção com a aula | H |
| 4 | Durante a explicação, o MindFlow apresenta uma mudança no indicador, sugerindo possível aumento de confusão no grupo | Perceber que pode existir alguma dificuldade naquele momento | Fica atenta ao sinal, mas ainda não sabe se ele representa corretamente o que está acontecendo | Pode confiar demais em uma inferência errada ou ignorar um alerta que seria útil | Mostrar a inferência de forma clara e, quando necessário, indicar qualidade ou confiança do sinal para apoiar a interpretação | H |
| 5 | Camila decide confirmar o sinal fazendo uma pergunta, retomando um exemplo ou observando a resposta da turma | Verificar se a dificuldade indicada pelo sistema também aparece na interação com os alunos | Usa o indicador como apoio, mas combina essa informação com sua própria percepção da aula | Pode modificar a explicação sem necessidade ou interpretar uma reação pontual como dificuldade geral | O sistema não deve determinar automaticamente qual ação deve ser tomada; deve apoiar a decisão do comunicador | H |
| 6 | Depois da aula, Camila abre o Dashboard e revisa os principais momentos da sessão | Entender em quais partes da aula ocorreram mudanças nos indicadores | Curiosa para comparar sua percepção com o que foi registrado pelo sistema | Pode não ter tempo ou interesse em analisar um relatório longo e cheio de métricas | Apresentar primeiro um resumo simples e uma linha do tempo, permitindo abrir mais detalhes somente quando necessário | H |
| 7 | Ao preparar uma aula futura, Camila utiliza o que observou no Dashboard junto com sua própria experiência para decidir se vai revisar um conteúdo, trocar um exemplo ou manter a aula como estava | Melhorar as próximas aulas com base em diferentes fontes de informação | Avalia se os dados realmente fazem sentido dentro do contexto que conhece da turma | O sistema pode apontar um momento como relevante, mas isso não significa que Camila precise obrigatoriamente alterar seu planejamento | Permitir que os resultados sirvam como apoio à reflexão e comparação entre sessões, sem transformar as inferências em recomendações obrigatórias | H |

## Síntese

As próximas entregas devem contemplar:

- a percepção rápida do estado agregado do grupo durante a sessão, relacionada a A01 e H01;
- a decisão do comunicador de verificar ou adaptar a condução, relacionada a A02;
- a comunicação da confiança e dos limites da classificação, relacionada a H02;
- a transparência sobre processamento local, agregação e ausência de avaliação individual, relacionada a H03;
- a revisão da timeline e dos momentos críticos após a sessão, relacionada a A03 e R03;
- a validação da utilidade do Semáforo Cognitivo em turmas pequenas, treinamentos corporativos e apresentações comerciais;
- a confirmação, por pesquisa com usuários, das características atribuídas às proto-personas.

## Checklist

- [x] Existe pelo menos uma persona por integrante ]]
- [x] As personas existentes não são apenas diferenças demográficas superficiais.
- [x] Está claro que as quatro personas são proto-personas e que seus dados precisam ser validados.
- [x] As personas não transformam as hipóteses da Entrega 1 em fatos comprovados.
- [x] Objetivos e dores têm consequência para o design.
- [x] O contexto de uso está coerente com a Entrega 1.
- [x] O TCC já possui interface prevista; portanto, o item destinado a TCCs sem interface original não se aplica.
- [x] Os papéis existentes foram diferenciados por contexto, objetivos e tarefas.
- [x] A jornada possui etapas, dores e oportunidades e não é apenas um wireflow.
- [x] Os IDs das personas ainda não foram adicionados à matriz de rastreabilidade.
