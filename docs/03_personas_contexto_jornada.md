# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** 27/08/2026  
**Status:** 🟨 iniciada  
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
| Restrições/acessibilidade | Possui mobilidade reduzida após um acidente, o que dificulta o deslocamento até a instituição; durante as aulas, divide a atenção entre conteúdo, chat, alunos e apresentação |
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

### Síntese das personas

As quatro personas são classificadas como **primárias** porque representam usuários diretos do MindFlow AI: todas conduzem sessões por videoconferência, consultam o Semáforo Cognitivo durante a apresentação e podem utilizar o Dashboard após a sessão. Embora atuem em contextos diferentes, compartilham o objetivo central de perceber a reação do grupo sem perder o foco na própria condução.

Karol representa o ensino a distância de conteúdo conceitual, com menor familiaridade tecnológica e necessidade de baixa carga de atenção. Camila representa aulas de idioma mais interativas, turmas pequenas e pouco tempo disponível entre sessões. Nathanael representa treinamentos corporativos, nos quais precisa cumprir uma pauta, trabalhar com públicos heterogêneos e evitar que dados agregados sejam interpretados como avaliação individual de funcionários. Manoel representa apresentações comerciais B2B, em que o comunicador precisa interpretar rapidamente a reação de clientes, ajustar o discurso e lidar com exigências ainda mais sensíveis de transparência e consentimento.

As diferenças entre elas não são apenas demográficas: cada persona introduz condições de uso e necessidades que influenciam o design. Mesmo sendo todas primárias, a equipe adotará **P02 — Camila Duarte** como persona de referência para o mapa de empatia e a jornada desta entrega. Essa escolha serve apenas para consolidar os artefatos coletivos exigidos pelo modelo e não estabelece hierarquia entre as personas primárias.

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
| Usuários | Comunicador (professor/instrutor/palestrante/facilitador), com a persona P01 representando especificamente professora de idioma em turma pequena (5 a 15 alunos) | A interface precisa funcionar bem tanto pra grupos pequenos quanto pra turmas maiores, sem perder a leitura de "clima do grupo" quando há poucos alunos |
| Tarefas | Perceber o estado do grupo em tempo real durante a aula, e revisar depois quais momentos tiveram mais dificuldade | Justifica o Semáforo Cognitivo (tempo real) e o Dashboard pós-sessão, já definidos na Entrega 1 |
| Equipamentos | Notebook ou desktop com webcam, conexão de internet doméstica, às vezes instável | A interface do tempo real precisa ser leve, sem exigir muito processamento nem depender de conexão perfeita |
| Ambiente físico | Geralmente a casa da professora, nem sempre um espaço silencioso ou bem iluminado | Reforça a decisão já tomada na Entrega 1, de que iluminação ruim pode prejudicar a extração de sinal facial |
| Ambiente social/organizacional | Aula particular ou de escola de idiomas, sem estrutura de TI dedicada por trás | A ferramenta precisa ser simples de configurar sozinha, sem depender de suporte técnico |
| Papéis/permissões/governança | Só a professora vê o Semáforo Cognitivo e o Dashboard, os alunos não têm acesso a nenhuma tela do sistema | Confirma a decisão de privacidade já definida na Entrega 1, indicador visível só pro comunicador |
| Volume de dados/histórico | Turma pequena, poucas aulas por semana, histórico relevante seria por turma ou por aluno ao longo do curso | Levanta uma dúvida nova pra investigar, se faz sentido comparar o engajamento da mesma turma entre aulas diferentes |


## 4. Jornada do usuário — equipe

**Persona:** P02 — Camila Duarte  
**Objetivo da jornada:** conduzir uma aula de inglês por videoconferência, perceber a tempo mudanças no estado geral da turma e revisar posteriormente os momentos que podem exigir melhoria.  
**Início e fim da jornada:** começa antes da aula, quando Camila prepara a videoconferência e verifica o MindFlow AI, e termina depois da sessão, quando consulta o Dashboard para planejar uma aula futura.


| Etapa | Situação/ação | Objetivo | Pensamento/emoção | Dor | Oportunidade de design | Evidência |
|---|---|---|---|---|---|---|
| 1 | Abre a videochamada alguns minutos antes e ativa o MindFlow | Deixar tudo pronto antes dos alunos entrarem | Tranquila, rotina já conhecida | Nenhuma até aqui | Ativação simples, poucos cliques | H |
| 2 | Começa a aula explicando um tópico novo de gramática | Passar o conteúdo com clareza | Focada na explicação, atenção dividida entre falar e compartilhar tela | Não consegue olhar a grade de vídeo com atenção | O Semáforo Cognitivo precisa ser visível sem que ela precise procurar por ele na tela | H |
| 3 | O indicador mostra sinal de confusão crescente no grupo | Perceber que algo não está sendo entendido | Alerta, mas ainda incerta se deve confiar no sinal | Medo de interromper a aula à toa por um alerta errado | Mostrar o nível de confiança da classificação, ligado à hipótese H02 | H |
| 4 | Ela para, dá um exemplo extra e pergunta se a turma entendeu | Resolver a confusão percebida antes de seguir em frente | Mais segura, sente que agiu a tempo | Nenhuma, esse é o momento em que a ferramenta cumpriu o propósito dela | Confirma o valor central do Semáforo Cognitivo, definido desde a Entrega 1 | H |
| 5 | Termina a aula e depois abre o Dashboard pra revisar | Entender quais momentos tiveram mais dificuldade, pra ajustar a próxima aula | Curiosa, quer aprender com a própria condução | Pode não ter tempo sobrando entre uma aula e outra pra revisar com calma | O Dashboard precisa ser rápido de ler, tipo um resumo, não um relatório longo | H |

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

- [ ] Existe pelo menos uma persona por integrante — atualmente existem 4 personas para 5 integrantes.
- [x] As personas existentes não são apenas diferenças demográficas superficiais.
- [x] Está claro que as quatro personas são proto-personas e que seus dados precisam ser validados.
- [x] As personas não transformam as hipóteses da Entrega 1 em fatos comprovados.
- [x] Objetivos e dores têm consequência para o design.
- [x] O contexto de uso está coerente com a Entrega 1.
- [x] O TCC já possui interface prevista; portanto, o item destinado a TCCs sem interface original não se aplica.
- [x] Os papéis existentes foram diferenciados por contexto, objetivos e tarefas.
- [x] A jornada possui etapas, dores e oportunidades e não é apenas um wireflow.
- [ ] Os IDs das personas ainda não foram adicionados à matriz de rastreabilidade.
