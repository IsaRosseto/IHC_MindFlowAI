# Entrega 4 — Cenários de análise/problema

**Data:** {{dd/mm/aaaa}}  
**Status:** ⬜ não iniciada  
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

## Cenário C05 — Aluno que não sabe como está sendo percebido numa aula online

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

> Repita para C02, C03... com autoria individual.

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
