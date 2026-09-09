# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** {{27/08/2026}} 
**Status:** 🟨 iniciada
**Responsabilidade:** 1 persona por integrante; 1 mapa de empatia, 1 contexto de uso consolidado e 1 jornada por equipe (salvo orientação diferente do docente).

## Objetivo da atividade

Representar grupos de usuários de forma útil para decisões de design. Persona não é personagem decorativo: suas características devem alterar requisitos, prioridades, linguagem, fluxos ou critérios de avaliação.

## Atenção a projetos técnicos

Em TCCs sem interface original, a persona pode representar um **profissional que se apropria da contribuição técnica**: DBA, analista, cientista de dados, administrador, pesquisador, técnico, operador, gestor ou especialista de domínio.

Não escolha um perfil apenas porque “parece combinar” com a tecnologia. Explique **qual objetivo esse perfil teria e qual parte da contribuição do TCC produziria valor para ele**. Se ainda for hipótese, mantenha como hipótese/proto-persona a validar.

Também considere papéis diferentes quando houver tarefas distintas, por exemplo:

- operador que executa análises;
- administrador que configura e gerencia permissões;
- especialista que interpreta resultados;
- gestor que consulta relatórios e decide;
- auditor que revisa histórico.

## Entradas da Entrega 1

Antes de criar personas, retome os tipos de usuários, características relevantes, objetivos e hipóteses registradas na Entrega 1. A persona **não deve transformar uma hipótese inicial em fato por meio de uma história fictícia**.

| Item da Entrega 1 | Status inicial | Evidência disponível agora | Como será tratado nesta entrega |
|---|---|---|---|
| {{usuário/objetivo/característica/H01...}} | F / H / ? | {{...}} | incorporar / manter como hipótese / descartar / investigar |

## 1. Personas

### Persona P01 — Karol

**Autor(a):** Kayky Pires — 22.222.040-2  
**Tipo:** primária  
**Base de evidências:** proto-persona baseada na Entrega 1  
**Hipóteses da Entrega 1 relacionadas:** H01

<img src="https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/03_personas/Karol.png" width="300">

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | 30–45 anos; professora que ministra aulas por videoconferência |
| Ocupação/papel | Professora de Filosofia no ensino a distância e responsável pela condução das aulas |
| Conhecimento do domínio | Alto domínio do conteúdo que ensina e 7 anos de experiência como professora |
| Experiência tecnológica | Familiaridade baixa a média com plataformas de videoconferência, ambientes virtuais de aprendizagem e compartilhamento de conteúdo |
| Objetivos | azer com que os alunos compreendam o conteúdo de Filosofia por meio de aulas didáticas, claras e facilitadoras, mesmo no ambiente de ensino a distância |
| Necessidades | Compreender como a turma está reagindo durante a aula e saber quando precisa mudar a forma de explicar o conteúdo |
| Dores/frustrações | Sente falta de observar as expressões e reações dos alunos como fazia presencialmente e se preocupa quando recebe pouco retorno da turma |
| Motivadores | Paixão por ensinar, ajudar os alunos a compreender conteúdos complexos e melhorar continuamente suas aulas |
| Restrições/acessibilidade | Possui mobilidade reduzida após um acidente, dificultando o deslocamento até a instituição; durante as aulas também precisa dividir a atenção entre conteúdo, chat, alunos e apresentação |
| Ambiente típico de uso | Pequena sala, iluminada em sua residência, utilizando notebook, webcam e internet para ministrar aulas online |
| Comportamentos relevantes | Observa câmeras e chat, pergunta se os alunos entenderam e, diante de pouca participação, utiliza resumos, tópicos nos slides e novos exemplos para tentar facilitar a compreensão |

**Decisões de design influenciadas por P01:**

- Priorizar informações simples e rápidas de interpretar durante a aula.
- Evitar excesso de elementos e interações que disputem a atenção da professora.
- Apresentar informações de forma clara, considerando sua familiaridade tecnológica baixa a média.
- Permitir que estimativas do sistema sejam apresentadas como apoio, sem transmitir certeza absoluta sobre o estado dos alunos.
> Repita para P02, P03... Cada integrante deve produzir ao menos uma persona.


### Persona P02 — Camila Duarte

**Autor(a):** Isabella Rosseto - 22.222.036-0
**Tipo:** primária  
**Base de evidências:** proto-persona a validar, construída a partir das hipóteses e do usuário definido na Entrega 1, ainda sem entrevista real  
**Hipóteses da Entrega 1 relacionadas:** H01, H02

<img width="512" height="279" alt="image" src="https://github.com/user-attachments/assets/7c55de54-a37e-44a8-a060-c40d44d79be6" />

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | 34 anos |
| Ocupação/papel | Professora de inglês, dá aula em uma escola de idiomas e também turmas particulares por conta própria |
| Conhecimento do domínio | Alta, é formada em Letras e tem certificação internacional de proficiência, domina bem o conteúdo que ensina |
| Experiência tecnológica | Mediana, usa bem o Zoom, Google Meet e ferramentas básicas de apresentação, mas não é alguém que acompanha lançamento de tecnologia por hobby |
| Objetivos | Manter a turma engajada durante a aula toda, mesmo sendo online, e perceber rápido quando algum aluno está se perdendo no conteúdo |
| Necessidades | Um sinal simples de como a turma está reagindo, sem precisar ficar checando rosto por rosto enquanto fala e compartilha slide |
| Dores/frustrações | Em turmas de 5 a 15 alunos, é fácil um ou dois alunos ficarem confusos sem avisar nada, e ela só percebe isso quando já é tarde, na correção do exercício ou na aula seguinte |
| Motivadores | Ver os alunos evoluindo de verdade no idioma, e sentir que a aula foi bem conduzida, não só que o conteúdo foi passado |
| Restrições/acessibilidade | Nenhuma restrição de acessibilidade conhecida, mas tem pouco tempo entre uma aula e outra, então qualquer ferramenta nova precisa ser rápida de entender |
| Ambiente típico de uso | Dá aula de casa, notebook com webcam, às vezes numa sala silenciosa, às vezes com alguma interrupção doméstica |
| Comportamentos relevantes | Fala bastante durante a aula, compartilha tela com exercícios e slides, e só consegue olhar rapidamente pra grade de vídeo entre uma atividade e outra |

**Decisões de design influenciadas por P02:**

- O Semáforo Cognitivo precisa ser lido de relance, já que Camila está com a atenção dividida entre falar, compartilhar tela e conduzir a aula.
- Como a turma é pequena (5 a 15 alunos), o indicador agregado por grupo precisa continuar fazendo sentido mesmo com poucas pessoas, diferente de uma sala de aula cheia com 40 ou 50 alunos.
- A linguagem da interface não pode usar termo técnico de IA, já que Camila tem experiência tecnológica mediana, não é especialista.
- O nível de confiança da classificação (ligado à H02) precisa aparecer de um jeito simples, porque ela não teria como validar sozinha se o sistema está certo ou errado numa aula de idioma.


### Persona P03 — Nathanael Lima

**Autor(a):** Rafael Dias - 22.222.039-4  
**Tipo:** Secundária  
**Base de evidências:** proto-persona a validar  
**Hipóteses da Entrega 1 relacionadas:** H01

![Persona P01](../assets/03_personas/persona_nathanael.png)

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | 25–30 anos; profissional de Treinamento e Desenvolvimento que conduz capacitações online para equipes de diferentes áreas da empresa |
| Ocupação/papel | Instrutor corporativo responsável por apresentar novos processos, ferramentas e procedimentos internos aos funcionários |
| Conhecimento do domínio | Alto conhecimento dos processos que ensina, mas normalmente trabalha com públicos de áreas e níveis de experiência diferentes |
| Experiência tecnológica | Familiaridade média a alta com videoconferência, apresentações, enquetes, formulários e plataformas corporativas |
| Objetivos | Fazer com que os participantes compreendam rapidamente o treinamento e consigam aplicar o conteúdo nas atividades do trabalho |
| Necessidades | Perceber durante o treinamento quando o grupo está com dificuldade e identificar posteriormente quais partes da apresentação precisam ser melhoradas |
| Dores/frustrações | Como frequentemente ministra treinamentos para pessoas que não conhece, tem dificuldade para interpretar silêncio ou pouca participação. Muitas vezes só descobre que um conteúdo não ficou claro quando surgem dúvidas ou erros depois do treinamento |
| Motivadores | Realizar capacitações objetivas, reduzir dúvidas posteriores e melhorar seus materiais para os próximos grupos |
| Restrições/acessibilidade | Trabalha com horários definidos e precisa cumprir uma pauta dentro de um tempo limitado. Também divide a atenção entre apresentação, chat, perguntas e controle do cronograma |
| Ambiente típico de uso | Escritório ou home office, utilizando notebook, headset e plataforma de videoconferência para treinamentos com funcionários de diferentes setores |
| Comportamentos relevantes | Costuma apresentar exemplos práticos, fazer perguntas rápidas e utilizar enquetes para verificar a compreensão. Após o treinamento, revisa feedbacks e ajusta os materiais antes de apresentá-los para outro grupo |

**Decisões de design influenciadas por P03:**

- Apresentar informações de forma objetiva durante a sessão, sem interromper o ritmo do treinamento.
- Permitir a consulta posterior dos momentos em que o grupo apresentou maior dificuldade.
- Facilitar a comparação entre diferentes sessões ou turmas de treinamento.
- Apresentar informações agregadas, sem identificar individualmente os funcionários.
> Repita para P02, P03... Cada integrante deve produzir ao menos uma persona.

### Persona P01 — {{nome fictício}}

**Autor(a):** {{nome — matrícula}}  
**Tipo:** primária / secundária  
**Base de evidências:** entrevista / questionário / literatura / observação / proto-persona a validar / combinação  
**Hipóteses da Entrega 1 relacionadas:** {{H01, H02 ou —}}

![Persona P01](../assets/03_personas/persona_p01.svg)

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | {{somente o que impacta o uso}} |
| Ocupação/papel | {{...}} |
| Conhecimento do domínio | {{...}} |
| Experiência tecnológica | {{...}} |
| Objetivos | {{...}} |
| Necessidades | {{...}} |
| Dores/frustrações | {{...}} |
| Motivadores | {{...}} |
| Restrições/acessibilidade | {{...}} |
| Ambiente típico de uso | {{...}} |
| Comportamentos relevantes | {{...}} |

**Decisões de design influenciadas por P01:**

- {{...}}

> Repita para P02, P03... Cada integrante deve produzir ao menos uma persona.

### Síntese das personas

Explique diferenças entre os perfis e qual persona é prioritária. Evite personas duplicadas que só mudam nome/foto.

## 2. Mapa de empatia — equipe

**Persona escolhida:** P02 (Camila Duarte)  
**Justificativa:** É a persona mais detalhada até agora e representa bem o comunicador em uma situação concreta e comum (aula de idioma em turma pequena), o que ajuda a equipe a validar decisões de design num cenário realista antes de generalizar pra outros contextos.

<img width="590" height="420" alt="image" src="https://github.com/user-attachments/assets/480fd080-5094-4bac-a365-f7f001a930d5" />

Documente também em texto: o que vê; ouve; diz/faz; pensa/sente; dores; ganhos. Diferencie **evidência** de **hipótese**.

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

**Persona:** P01 (Camila Duarte)  
**Objetivo da jornada:** Dar uma aula de inglês de 50 minutos pra uma turma de 12 alunos, percebendo a tempo se alguém está confuso ou desengajado, e revisando depois o que deu certo ou não.  
**Início e fim da jornada:** Começa alguns minutos antes da aula, quando ela abre a chamada e ativa o MindFlow, e termina depois da aula, quando ela revisa o Dashboard antes de planejar a próxima aula.

| Etapa | Situação/ação | Objetivo | Pensamento/emoção | Dor | Oportunidade de design | Evidência |
|---|---|---|---|---|---|---|
| 1 | Abre a videochamada alguns minutos antes e ativa o MindFlow | Deixar tudo pronto antes dos alunos entrarem | Tranquila, rotina já conhecida | Nenhuma até aqui | Ativação simples, poucos cliques | H |
| 2 | Começa a aula explicando um tópico novo de gramática | Passar o conteúdo com clareza | Focada na explicação, atenção dividida entre falar e compartilhar tela | Não consegue olhar a grade de vídeo com atenção | O Semáforo Cognitivo precisa ser visível sem que ela precise procurar por ele na tela | H |
| 3 | O indicador mostra sinal de confusão crescente no grupo | Perceber que algo não está sendo entendido | Alerta, mas ainda incerta se deve confiar no sinal | Medo de interromper a aula à toa por um alerta errado | Mostrar o nível de confiança da classificação, ligado à hipótese H02 | H |
| 4 | Ela para, dá um exemplo extra e pergunta se a turma entendeu | Resolver a confusão percebida antes de seguir em frente | Mais segura, sente que agiu a tempo | Nenhuma, esse é o momento em que a ferramenta cumpriu o propósito dela | Confirma o valor central do Semáforo Cognitivo, definido desde a Entrega 1 | H |
| 5 | Termina a aula e depois abre o Dashboard pra revisar | Entender quais momentos tiveram mais dificuldade, pra ajustar a próxima aula | Curiosa, quer aprender com a própria condução | Pode não ter tempo sobrando entre uma aula e outra pra revisar com calma | O Dashboard precisa ser rápido de ler, tipo um resumo, não um relatório longo | H |

> A jornada pode incluir etapas **antes, durante e depois** do uso do produto. Não transforme a jornada em lista de telas.

## Síntese

A partir da persona P01 e da jornada, alguns pontos precisam obrigatoriamente aparecer nos cenários e nas tarefas das próximas entregas: o Semáforo Cognitivo precisa ser lido sem esforço mesmo com a atenção da professora dividida, o nível de confiança da classificação precisa aparecer de forma simples (ligado à H02), o indicador agregado precisa fazer sentido mesmo em turmas pequenas de 5 a 15 alunos, e o Dashboard pós-sessão precisa ser rápido de consultar, dado o pouco tempo que a professora tem entre uma aula e outra.
## Checklist

- [ ] Existe pelo menos uma persona por integrante.
- [ ] As personas não são apenas diferenças demográficas superficiais.
- [ ] Está claro o que é dado real e o que é hipótese/proto-persona.
- [ ] A persona não “validou por ficção” uma hipótese da Entrega 1; afirmações continuam marcadas como hipótese quando não há evidência.
- [ ] Objetivos e dores têm consequência para o design.
- [ ] Contexto de uso está coerente com a Entrega 1.
- [ ] Em TCC sem interface original, a persona possui relação explícita com a contribuição técnica.
- [ ] Papéis administrativos, técnicos e decisórios só foram criados quando possuem objetivos/tarefas diferentes.
- [ ] Jornada possui etapas, dores e oportunidades e não é apenas wireflow.
- [ ] IDs das personas foram adicionados à rastreabilidade.
