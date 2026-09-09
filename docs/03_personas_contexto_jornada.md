# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** 27/08/2026  
**Status:** 🟨 iniciada  
**Responsabilidade:** 1 persona por integrante; 1 mapa de empatia, 1 contexto de uso consolidado e 1 jornada por equipe (salvo orientação diferente do docente).

## Objetivo da atividade

Representar grupos de usuários de forma útil para decisões de design. Persona não é personagem decorativo: suas características devem alterar requisitos, prioridades, linguagem, fluxos ou critérios de avaliação.

## Relação com o projeto de IHC

O MindFlow AI já prevê uma interface como parte do TCC. Conforme a Entrega 1 e a matriz de rastreabilidade, o projeto de IHC prioriza o **comunicador** — professor, instrutor ou palestrante — que precisa perceber em tempo real o estado afetivo-cognitivo agregado do grupo sem tirar a atenção da condução da sessão.

O recorte principal é o **Semáforo Cognitivo em tempo real**. O **Dashboard pós-sessão** é o recorte secundário para revisão da linha temporal e dos momentos de maior dificuldade. Como ainda não há pesquisa com usuários reais registrada, as personas desta entrega são **proto-personas a validar**.

## Entradas da Entrega 1

| Item da Entrega 1 | Status inicial | Evidência disponível agora | Como será tratado nesta entrega |
|---|---|---|---|
| Comunicador — professor, instrutor ou palestrante — como usuário prioritário | H | Entrega 1, itens 2.2 e 7.2; matriz de rastreabilidade, seção 1 | Incorporar nas personas e manter como hipótese até a validação com usuários |
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
**Tipo:** secundária  
**Base de evidências:** proto-persona a validar, construída a partir do contexto de treinamento corporativo previsto na Entrega 1  
**Hipóteses da Entrega 1 relacionadas:** H01, H02 e H03

<img src="../assets/03_personas/persona_nathanael.png" width="300" alt="Persona P03 — Nathanael Lima">

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
**Tipo:** secundária  
**Base de evidências:** proto-persona a validar, construída a partir das hipóteses da Entrega 1, estendendo o perfil do comunicador para o contexto comercial  
**Hipóteses da Entrega 1 relacionadas:** H01, H03, H04

![Persona P04](../assets/03_personas/persona_manoel_gomes.png)

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

Karol e Camila são personas primárias porque representam variações centrais do usuário priorizado no projeto de IHC: professoras responsáveis por conduzir aulas por videoconferência e interpretar o Semáforo Cognitivo enquanto ensinam. Karol representa o ensino a distância de conteúdo conceitual, com menor familiaridade tecnológica e necessidade de baixa carga de atenção. Camila representa aulas de idioma mais interativas, turmas pequenas e pouco tempo disponível entre sessões.

Nathanael é uma persona secundária porque leva a mesma contribuição técnica para o contexto corporativo. Suas tarefas incluem cumprir uma pauta, treinar públicos heterogêneos e revisar sessões futuras, além de lidar com uma preocupação organizacional maior sobre o possível uso dos dados para avaliação de funcionários.

Para os artefatos consolidados desta entrega, a equipe adotará **P02 — Camila Duarte** como persona de referência. Essa escolha não torna Karol a única ou a principal persona e não altera a classificação de P01 e P02 como personas primárias.

## 2. Mapa de empatia — equipe

**Persona escolhida:** P02 — Camila Duarte  
**Justificativa:** Camila representa diretamente o comunicador definido na Entrega 1 em uma situação concreta de aula on-line. Sua atenção dividida entre explicação, compartilhamento de tela e observação dos alunos permite explorar a hipótese H01. O recorte de turma pequena também introduz uma questão relevante para validação: se um indicador agregado continua útil quando o grupo possui poucos participantes.

<img src="https://github.com/user-attachments/assets/480fd080-5094-4bac-a365-f7f001a930d5" width="590" alt="Mapa de empatia da persona P02 — Camila Duarte">

**O que vê [H]:** a própria tela compartilhada, uma pequena grade de vídeo, o chat e alguns alunos com a câmera desligada.

**O que ouve [H]:** respostas durante os exercícios, dúvidas pontuais, períodos de silêncio e, eventualmente, ruídos do ambiente doméstico.

**O que diz e faz [H]:** explica a matéria, propõe exercícios, faz perguntas, tenta envolver os alunos mais quietos e compartilha materiais na tela.

**O que pensa e sente [H]:** preocupa-se em não perceber quando a turma deixou de acompanhar a explicação e sente insegurança quando não recebe retorno claro.

**Dores [H]:** perceber tarde que parte da turma ficou confusa; dividir a atenção entre a aula e a grade de participantes; não distinguir se o silêncio significa atenção, dúvida ou desengajamento.

**Ganhos esperados [H]:** perceber rapidamente mudanças no estado geral da turma, verificar a compreensão enquanto ainda pode agir e revisar depois os pontos que precisam ser melhorados.

> Todos os elementos do mapa de empatia são hipóteses da proto-persona e ainda precisam ser validados com usuários reais.

## 3. Contexto de uso — consolidação

O contexto é consolidado porque representa o escopo do projeto de IHC e as três personas existentes. P02 — Camila é utilizada como referência principal para manter coerência com o mapa de empatia e a jornada.

| Dimensão | Descrição | Implicação de design |
|---|---|---|
| Usuários | Comunicadores — professores, instrutores ou palestrantes — que conduzem sessões por videoconferência. Camila representa especificamente uma professora de idiomas com turma pequena | Priorizar a visão do comunicador e validar se o mesmo indicador atende grupos de tamanhos e contextos diferentes |
| Tarefas | A01: perceber o estado do grupo; A02: ajustar a condução quando considerar necessário; A03: revisar posteriormente os momentos de dificuldade | Manter o Semáforo Cognitivo como foco principal e o Dashboard pós-sessão como recorte secundário |
| Equipamentos | Notebook ou desktop com webcam; o processamento ocorre no dispositivo do participante, conforme a arquitetura definida no TCC | A interface deve indicar o estado de funcionamento e considerar os limites de hardware e captura sem exigir celular, que ainda não faz parte do escopo |
| Ambiente físico | Aula remota ou híbrida em ambiente doméstico ou institucional; iluminação, enquadramento e conexão podem afetar os sinais capturados | Comunicar quando a qualidade do sinal ou da classificação for insuficiente, sem apresentar a estimativa como certeza |
| Ambiente social/organizacional | Existe assimetria entre o participante, que fornece os sinais, e o comunicador, que recebe o resultado; em instituições de ensino ou empresas pode haver exigências de consentimento e LGPD | Investigar transparência e consentimento, conforme H03, e evitar uso dos dados para avaliação individual |
| Papéis/permissões/governança | O comunicador é o usuário da interface; o participante é fonte de dados e não possui tela prevista no recorte atual; administração global está fora do escopo | Limitar a interface ao comunicador no protótipo atual, sem inventar CRUD, administração ou perfis não justificados |
| Volume de dados/histórico | Persistência de representações reduzidas e metadados, sem vídeo ou dado biométrico bruto; histórico organizado por sessão e timeline agregada | Permitir consulta pós-sessão sem replay de vídeo nem classificação individual; busca, filtros e comparação continuam como hipóteses a investigar |

## 4. Jornada do usuário — equipe

**Persona:** P02 — Camila Duarte  
**Objetivo da jornada:** conduzir uma aula de inglês por videoconferência, perceber a tempo mudanças no estado geral da turma e revisar posteriormente os momentos que podem exigir melhoria.  
**Início e fim da jornada:** começa antes da aula, quando Camila prepara a videoconferência e verifica o MindFlow AI, e termina depois da sessão, quando consulta o Dashboard para planejar uma aula futura.

| Etapa | Situação/ação | Objetivo | Pensamento/emoção | Dor | Oportunidade de design | Evidência |
|---|---|---|---|---|---|---|
| 1. Preparação | Abre a videoconferência, organiza os materiais e verifica se o MindFlow AI está ativo | Começar a aula sem atrasos ou falhas | Espera que a preparação seja rápida | Possui pouco tempo entre as aulas e pode não saber se o processamento está funcionando | Oferecer ativação simples e feedback claro do estado do sistema | H — proto-persona; possibilidade registrada no item 8 da Entrega 1 |
| 2. Condução | Explica um tópico enquanto compartilha slides ou exercícios | Ensinar com clareza e manter o ritmo | Focada, mas com atenção dividida | Não consegue observar continuamente todos os vídeos e o chat | Manter o indicador discreto e legível de relance | H01; Entrega 1, item 2.4 |
| 3. Percepção | Observa uma mudança estimada no estado agregado da turma | Decidir se precisa verificar a compreensão | Fica alerta, mas tem dúvida sobre a precisão do resultado | Pode interromper a aula sem necessidade se confiar em uma classificação incorreta | Representar a confiança ou incerteza do modelo de modo compreensível | H02 |
| 4. Adaptação | Faz uma pergunta, apresenta outro exemplo ou altera o ritmo | Verificar e apoiar a compreensão antes de continuar | Sente que ainda pode agir a tempo | O indicador não explica sozinho a causa do estado observado | Apresentar a estimativa como apoio à decisão, e não como diagnóstico ou comando automático | A02; Entrega 1, itens 3.1 e 4.4 |
| 5. Encerramento | Finaliza a aula e o registro da sessão | Concluir a atividade preservando somente os dados previstos | Quer segurança sobre o uso das informações | Participantes podem se sentir avaliados ou monitorados | Comunicar finalidade, processamento local, agregação e limites de uso | H03; Entrega 1, itens 5.4 e 9.3 |
| 6. Revisão | Consulta a timeline agregada no Dashboard antes de preparar outra aula | Identificar trechos que precisam ser retomados ou melhorados | Tem interesse, mas pouco tempo disponível | Um relatório extenso ou técnico pode não ser consultado | Exibir uma síntese objetiva e os momentos críticos da sessão | A03; R03; F02 e F03 da matriz de rastreabilidade |

> A jornada inclui momentos antes, durante e depois do uso. Ela descreve objetivos, decisões e dificuldades da persona, e não apenas uma sequência de telas.

## Síntese

As próximas entregas devem contemplar:

- a percepção rápida do estado agregado do grupo durante a sessão, relacionada a A01 e H01;
- a decisão do comunicador de verificar ou adaptar a condução, relacionada a A02;
- a comunicação da confiança e dos limites da classificação, relacionada a H02;
- a transparência sobre processamento local, agregação e ausência de avaliação individual, relacionada a H03;
- a revisão da timeline e dos momentos críticos após a sessão, relacionada a A03 e R03;
- a validação da utilidade do Semáforo Cognitivo em turmas pequenas;
- a confirmação, por pesquisa com usuários, das características atribuídas às proto-personas.

## Pendências para concluir a entrega

- Criar as personas P04 e P05, correspondentes aos integrantes Gustavo e Matheus.
- Atualizar a coluna **Persona** das linhas R01, R02 e R03 em `RASTREABILIDADE.md` depois que a equipe confirmar os vínculos.
- Substituir no repositório os arquivos SVG que ainda são placeholders, caso eles sejam utilizados no documento final.

## Checklist

- [ ] Existe pelo menos uma persona por integrante — atualmente existem 3 personas para 5 integrantes.
- [x] As personas existentes não são apenas diferenças demográficas superficiais.
- [x] Está claro que as três personas são proto-personas e que seus dados precisam ser validados.
- [x] As personas não transformam as hipóteses da Entrega 1 em fatos comprovados.
- [x] Objetivos e dores têm consequência para o design.
- [x] O contexto de uso está coerente com a Entrega 1.
- [x] O TCC já possui interface prevista; portanto, o item destinado a TCCs sem interface original não se aplica.
- [x] Os papéis existentes foram diferenciados por contexto, objetivos e tarefas.
- [x] A jornada possui etapas, dores e oportunidades e não é apenas um wireflow.
- [ ] Os IDs das personas ainda não foram adicionados à matriz de rastreabilidade.
