
# Entrega 1 — Conhecendo o projeto, o usuário e o problema

**Data:** 13/08/2026

**Status:** ✅ CONCLUIDO

**Responsabilidade:** 1 solução consolidada por equipe

## Objetivo da atividade

Reinterpretar o tema do TCC sob a perspectiva de Interação Humano-Computador e construir um **entendimento comum entre os integrantes da equipe**.

A disciplina utiliza preferencialmente o tema do TCC para os exercícios de IHC. Isso vale tanto para TCCs que já preveem uma interface quanto para trabalhos cujo resultado principal é algoritmo, modelo, API, biblioteca, análise de dados, infraestrutura, estudo experimental ou outro artefato técnico.

> **Importante:** a interface projetada na disciplina é um artefato de aprendizagem de IHC. Ela **não se torna automaticamente uma obrigação do TCC**. Sua incorporação ao trabalho de conclusão depende de decisão da equipe e do orientador.

Antes de preencher, leia [`../GUIA_ESCOPO_IHC.md`](../GUIA_ESCOPO_IHC.md).

Nesta primeira semana a equipe **não deve começar desenhando telas**. Primeiro deverá compreender:

- o que o TCC realmente produz;
- quem poderia obter valor dessa contribuição;
- quais pessoas interagem, administram, configuram, interpretam ou são afetadas;
- o que essas pessoas precisam alcançar;
- como atividades relacionadas acontecem hoje;
- problemas, limitações e contexto;
- alternativas existentes;
- qual recorte de interação fará sentido para a disciplina.

Ao final desta entrega, a equipe deve diferenciar:

- **tema do TCC** × **escopo formal do TCC** × **escopo de IHC da disciplina**;
- **objetivo do projeto** × **objetivo do usuário**;
- **problema do usuário** × **solução tecnológica**;
- **fato conhecido** × **hipótese** × **lacuna de conhecimento**;
- **capacidade técnica** × **forma de uso dessa capacidade**;
- **funcionalidade** × **atividade/resultado que o usuário precisa alcançar**;
- **usuário direto** × **stakeholders**.

---

## Como classificar as respostas

Sempre que a resposta fizer uma afirmação sobre usuários, problemas, atividades, necessidades, contexto ou mercado, use:

- **[F] Fato conhecido** — existe evidência/fonte.
- **[H] Hipótese** — afirmação plausível que ainda precisa ser investigada.
- **[?] Não sabemos ainda** — lacuna relevante.

Quando usar `[F]`, informe a origem. Hipóteses prioritárias devem receber IDs (`H01`, `H02`...) e também ser registradas em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

> **Exemplo:** `[H] H01 — DBAs considerariam útil comparar automaticamente o plano atual de execução com uma recomendação produzida pelo algoritmo.`

Uma hipótese explicitada é melhor do que uma suposição escondida.

---

# 0. Identificação do TCC e da equipe

## 0.1 Membros

| Nome completo | Matrícula | GitHub |
|---|---:|---|
| Gustavo Bertoluzzi Cardoso| 22.123.016-2 | Gugzica3 |
| Isabella Vieira Silva Rosseto | 22.222.036-0 | IsaRosseto |
| Kayky Pires | 22.222.040-2	| kaykyypiress |
| Matheus Ferreira de Freitas | 22.125.085-5 | freitasfmatheus |
| Rafael Dias | 22.222.039-4 | rafadias008 |

## 0.2 Título atual do TCC

*MindFlow AI* - Classificação Temporal de Estados Cognitivos em Videoconferências utilizando Redes LSTM e Fusão Multimodal

## 0.3 Orientador(a)
Prof.ª Dra. Leila Cristina Carneiro Bergamasco


## 0.4 Qual é o resultado principal atualmente previsto no TCC?

Marque e descreva:

- [X] sistema/aplicação interativa;
- [ ] algoritmo;
- [X] modelo de IA/ML/LLM;
- [ ] biblioteca/API/framework;
- [ ] análise de dataset;
- [ ] estudo/benchmark/avaliação experimental;
- [ ] infraestrutura/backend;
- [ ] componente embarcado/IoT;
- [ ] outro: 

**Descrição:** 
> IA - Tem um modelo LSTM treinado no DAiSEE que classifica quatro estados cognitivos (engajamento, tédio, confusão, frustração). 

> SISTEMA - O sistema que roda esse modelo durante a videochamada: captura a webcam localmente, processa, agrega por janela de tempo e mostra pro comunicador via Semáforo Cognitivo ao vivo e dashboard depois. O modelo é o motor, mas a aplicação/interface já é parte formal do que o TCC promete entregar.

## 0.5 O TCC já previa desenvolvimento de interface com usuário?

- [X] Sim, a interface já faz parte do TCC.
- [ ] Parcialmente; existe alguma interação, mas ainda não está bem definida.
- [ ] Não. O TCC é predominantemente técnico e não previa interface.

**Explique o que está formalmente previsto no TCC:** 
> Teremos  uma "camada de aplicação" desenhada, com dois trilhos: um de tempo real (Semáforo Cognitivo, alerta discreto sobre o estado do grupo durante a sessão) e um de pós-sessão (Dashboard com timeline de engajamento e um chatbot RAG pra consultar a sessão). Nada disso está implementado ainda

---

# 1. Entendendo a contribuição do projeto

## 1.1 Explique o TCC em uma frase, sem citar linguagem de programação, framework ou banco de dados.
> O MindFlow AI observa, pela webcam, como as pessoas em uma videochamada estão reagindo (engajadas, entediadas, confusas ou frustradas) e devolve esse retrato ao facilitador da reunião em tempo real, sem gravar ou transmitir nenhum vídeo.

## 1.2 Qual situação, atividade ou problema do mundo real motivou o TCC?

> [F] O tempo em reuniões virtuais explodiu, segundo o Microsoft Work Trend Index, subiu 252% entre 2020 e 2022 , e com isso professores, palestrantes e facilitadores perderam boa parte dos sinais não-verbais que usariam presencialmente pra perceber se o público está ligado, perdido ou de saco cheio. 

## 1.3 Qual é a **capacidade/contribuição central** produzida pelo TCC?

> Nosso TCC produz, melhora, analisa ou permite classificar, de forma contínua e temporal, o estado afetivo-cognitivo de participantes de uma videochamada a partir de sinais visuais captados pela própria webcam.


## 1.4 O que se espera que esteja diferente **para pessoas, organizações ou processos** se essa contribuição for bem-sucedida?

> [H] A expectativa é que o professor ou palestrante consiga perceber, na hora, que o grupo está perdendo engajamento ou se confundindo, e mude o rumo ali mesmo em vez de só descobrir depois, na nota da prova ou no silêncio do chat. Em treinamento corporativo é parecido: dar um retorno objetivo pra quem apresenta. 

## 1.5 O que é mérito técnico/científico do TCC e o que seria uma possível aplicação prática?

| Mérito/contribuição técnica | Possível aplicação/valor em uso |
|---|---|
| Fusão multimodal precoce (early fusion)com pré-processamento (Z-score, BorderlineSMOTE, PCA com 95% de variância retida) e uma arquitetura LSTM multi-saída para quatro dimensões cognitivas simultâneas| Um assistente de apoio ao facilitador em aulas, treinamentos corporativos e apresentações técnicas, que sinaliza em tempo real o estado predominante do grupo sem exigir que ninguém acione câmera ou responda enquetes |
| Arquitetura Privacy by Design/Edge AI alinhada à LGPD | Um produto viável de ser adotado em instituições de ensino ou empresas com restrições reais de privacidade, sem depender de processamento em nuvem de vídeo/áudio dos participantes |

---

# 2. Entendendo as pessoas envolvidas

## 2.1 Quem interage diretamente com o produto, se já existe interface prevista?

> [H] Dois perfis, mas de formas bem diferentes. O comunicador (professor, palestrante, facilitador) é quem olha a tela: Semáforo em tempo real, Dashboard depois e decide algo a partir disso. 
> Os participantes da chamada também "interagem" no sentido de que são a fonte dos dados (webcam capturada e processada), mas não veem nenhuma tela.

## 2.2 Quem poderia **usar, configurar, administrar, operar, interpretar ou tomar decisões** a partir da contribuição técnica?

Considere perfis profissionais e stakeholders, não apenas consumidores finais.

| Perfil | Relação com a contribuição | O que faria | Status/evidência |
|---|---|---|---|
| Professor/instrutor em aula ou treinamento | Usuário direto principal do trilho de tempo real | Acompanharia o Semáforo Cognitivo durante a aula e ajustaria ritmo/conteúdo em resposta a quedas de engajamento ou aumento de confusão | H |
| Palestrante/apresentador corporativo | Usuário direto do trilho de tempo real e do dashboard pós-sessão | Monitoraria o estado da audiência ao vivo e revisaria a timeline depois, para entender quais trechos da apresentação geraram mais confusão ou frustração|H| 
| Participante da videochamada | Fonte de dados, não usuário da interface | Teria sua webcam processada localmente durante a sessão | F (cliente local em sessão) |
| Pesquisador/orientador acadêmico | Usuário indireto do modelo em si, fora do escopo do sistema pronto | Poderia usar o pipeline de extração e o modelo como base para outros estudos sobre estados afetivos em ambientes de aprendizagem | H|

## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

| Stakeholder | Como é afetado | Usa interface? | Status/evidência |
|---|---|---|---|
| Participante da videochamada | Tem seu comportamento visual inferido e classificado, mesmo sem ver o resultado; pode ser afetado por decisões que o comunicador toma com base nessa inferência |não |H |
| Instituição/empresa que promove a sessão | Pode adotar a ferramenta como política de qualidade de ensino/apresentação, ou usar dados agregados para avaliar formadores | provavelmente não diretamente| ? |
| Encarregado de dados/DPO da instituição| Responsável por garantir que o uso da ferramenta está de acordo com a LGPD| não, mas pode precisar auditar/aprovar o uso | H | 

## 2.4 Que características desses perfis podem influenciar a interação?

Considere conhecimento do domínio, experiência tecnológica, frequência de uso, necessidades de acessibilidade, responsabilidade profissional, familiaridade com métricas, linguagem técnica, urgência etc.

> [H] O comunicador está com a atenção dividida, falando, compartilhando tela, controlando o tempo,  então a tela de tempo real precisa ser lida de relance, sem número ou gráfico complicado. Daí o semáforo fazer mais sentido que um dashboard completo nesse momento. No pós-sessão já sobra mais tempo pra olhar uma timeline ou conversar com o chatbot. 
---

# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

Não responda "usar o algoritmo", "clicar no sistema" ou "ver o dashboard".

> [H] Ele quer conduzir a aula ou apresentação de um jeito que as pessoas realmente entendam e não saiam perdidas ou frustradas, manter a sessão funcionando enquanto ela acontece, não descobrir depois que deu errado. O objetivo não é "ver o semáforo", é decidir na hora se vale parar pra pergunta, trocar de exemplo, dar uma pausa ou acelerar. Hoje ele não tem como saber isso olhando pra a galeria e apresentando o contéudo ao mesmo tempo.

## 3.2 Quais são as atividades mais importantes?

| ID | Atividade/objetivo | Quem realiza | Frequência/criticidade inicial | Status/evidência |
|---|---|---|---|---|
| A01 |Perceber, durante a sessão, se o grupo está engajado, entediado, confuso ou frustrado| Comunicador (professor/palestrante/facilitador)| Alta frequência (toda sessão), alta criticidade| H| 
| A02 | Ajustar a condução da sessão em resposta a esse estado (mudar ritmo, abrir pergunta, dar exemplo)| Comunicador| Frequência variável dentro da sessão, alta criticidade| H|
| A03| Revisar, após a sessão, em quais momentos o grupo mais se confundiu ou desengajou, para melhorar a próxima vez| Comunicador| Baixa frequência (pós-sessão), criticidade média/alta para formação continuada| H |

## 3.3 Qual atividade parece mais frequente? Por quê?

> [H] A01 (perceber o estado do grupo) é a mais frequente porque roda o tempo todo, é o pano de fundo da sessão inteira. A A02 (ajustar a condução) é mais pontual, só entra quando o sinal justifica mudar algo.

## 3.4 Qual parece mais crítica? Que consequência existe se for mal executada?

> [H] A01 é a mais crítica das três porque as outras dependem dela. Se o comunicador não percebe direito o estado do grupo, seja porque o sistema deu falso negativo (achou que tava tudo bem) ou falso positivo (alertou à toa), ele toma decisão errada ou não toma decisão nenhuma. E isso não é só um risco teórico: os próprios resultados do TCC1 mostram desempenho fraco em algumas dimensões (como reconhecer o estado de Tédio) 

---

# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje, antes da interface imaginada na disciplina?

Pode existir software concorrente, linha de comando, planilha, notebook, script, painel técnico, processo manual, consulta a logs, análise visual, troca de mensagens, decisão por especialista etc.

> [H] Hoje o comunicador confia na própria leitura visual e intuitiva do grupo. Zoom, Teams e Meet não têm nenhum indicador estruturado de estado cognitivo do grupo; o máximo que existe são reações manuais tipo emoji, enquete pontual ou métrica superficial (quem tá com câmera ligada, quem falou). No meio acadêmico, o mais comum é só perguntar "todo mundo entendeu?" e confiar na resposta (ou no silêncio).

## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

> [H] É difícil pegar sinal sutil (tédio, por exemplo) quando o rosto tá mal enquadrado, mal iluminado ou a câmera simplesmente desligada. É cansativo ficar escaneando uma grade de vinte rostos enquanto também fala e compartilha tela. E é pouco transparente porque, mesmo quando o comunicador nota algo, não sabe se é o grupo todo ou só a impressão de uma ou duas pessoas.

## 4.3 Que informações o profissional precisa interpretar para tomar decisão?

> [H] No mínimo: qual proporção do grupo está em cada estado num dado momento, se isso tá subindo, caindo ou estável ao longo da sessão, e se dá pra associar uma queda de engajamento ou pico de confusão a um ponto específico da apresentação (um slide, um tópico). É basicamente o que o Dashboard e o Chatbot pretendem entregar depois da sessão.
> 
## 4.4 O que acontece quando a atividade falha ou quando o resultado é interpretado incorretamente?

> [H] Se o comunicador não percebe a tempo, a aula segue por um caminho que já não tá funcionando: o grupo se distancia mais, ou a frustração não resolvida compromete a persistência (. E no sentido contrário: se o MindFlow errar, o comunicador pode interromper a aula à toa, ou pior, parar de confiar na ferramenta depois de um erro perceptível. Esse risco de adoção já aparece meio implícito quando o artigo insiste que é "apoio analítico, não diagnóstico".

## 4.5 Conte uma situação concreta.

Escreva uma pequena narrativa com pessoa, objetivo, atividade, contexto, dificuldade e consequência. **Não descreva ainda a futura solução.**

> [H] Uma professora dá aula pra trinta alunos por videoconferência. Compartilha slide, tenta de vez em quando olhar a grade, só oito têm câmera ligada, em miniaturas pequenas num canto da tela. Ela entra num tópico mais difícil da matéria. Metade da turma começa a se perder, mas isso não aparece em lugar nenhum: ninguém liga o microfone, ninguém reage no chat. Ela segue o plano até o fim sem perceber que perdeu parte da turma ali. Só na próxima prova, quando a maioria erra as questões daquele tópico, ela entende tarde demais pra ajustar aquela aula  que devia ter parado, dado outro exemplo ou aberto espaço pra pergunta naquele momento.

## 4.6 Que evidência existe hoje?

| Evidência/fonte | O que sustenta | Limitação |
|---|---|---|
| Microsoft Work Trend Index (2022)| Aumento de 252% no tempo semanal em reuniões virtuais entre 2020-2022 | Não fala especificamente sobre engajamento/percepção do facilitador, só sobre volume de reuniões | 
| Bailenson, J. N. (2021), "Nonverbal Overload"| Fundamenta teoricamente os mecanismos de sobrecarga em videoconferência (contato visual excessivo, autoexposição, redução de mobilidade, sobrecarga cognitiva)| É um argumento teórico, não um estudo com facilitadores medindo diretamente a "cegueira situacional" |
| Fauville et al. (2021), amostra de 10.591 participantes| Confirma empiricamente associação entre esses mecanismos e maior fadiga, com efeitos diferentes por gênero | Foco em fadiga dos participantes, não especificamente na percepção do facilitador sobre o grupo | 
| Resultados preliminares do próprio TCC1 (POC sobre 22% do DAiSEE) | Mostra que é tecnicamente viável extrair esses sinais e classificá-los, ainda que com acurácia parcial| Amostra pequena, desbalanceada, sem validação com usuários reais ainda |

---

# 5. Entendendo o contexto de uso

## 5.1 Onde e em quais situações a interação poderia ocorrer?

> [H] Sala de aula remota ou híbrida, treinamento corporativo online, apresentação técnica pra equipe distribuída, reunião colaborativa de porte médio com um facilitador claro. Não parece fazer muito sentido em conversa 1:1 ou reunião pequena e informal, onde a leitura humana já dá conta.

## 5.2 Em quais dispositivos/equipamentos?

> [F] É pra rodar no dispositivo do participante. Na prática, notebook ou desktop com webcam, que é o cenário padrão de videoconferência corporativa/acadêmica. Celular não é mencionado ainda.

## 5.3 Existem condições físicas relevantes?

Considere iluminação, ruído, mobilidade, conexão, privacidade, uso compartilhado, interrupções, pressão de tempo etc.

> [H] Várias: iluminação ruim ou ângulo de câmera ruim degradam a extração dos landmarks; ver só busto e rosto limita o que dá pra tirar da postura; conexão instável afeta a taxa de captura. 

## 5.4 Existem fatores sociais ou organizacionais?

Considere papéis, chefias, equipes, permissões, aprovação, responsabilidade profissional, auditoria, turnos e colaboração.

> [H] Bastante coisa. Tem uma assimetria clara entre quem tá sendo "lido" (os participantes) e quem recebe o resultado (o comunicador) isso já levanta questão de consentimento. Em empresa, pode rolar receio de a ferramenta virar avaliação de desempenho individual, mesmo não sendo essa a intenção do sistema. Na universidade, provavelmente precisa de aprovação institucional antes de usar com aluno de verdade, por causa da LGPD.

## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

> [F] Sim, persistir só representações reduzidas e metadados, sem dado biométrico bruto, e mostrar timeline com momentos críticos no pós-sessão. Ou seja, tem histórico por sessão, mas de propósito sem o dado bruto.

## 5.6 Um erro pode produzir consequência relevante? Qual?

> [H] Sim, pros dois lados. 
> Falso negativo (não avisa uma queda real de engajamento) faz o comunicador perder a chance de ajustar a aula, a mesma falha de sempre, só que agora com falsa sensação de segurança. 
> Falso positivo (aponta frustração que não existe) pode gerar interrupção desnecessária ou fazer o comunicador parar de confiar na ferramenta,.

---

  

# 6. Entendendo mercado e alternativas existentes

  

> Nesta entrega faça apenas um **levantamento inicial**. A análise aprofundada ocorre na Entrega 2.

  

## 6.1 Como pessoas resolvem problemas semelhantes hoje?

  

| Alternativa atual | Quem usa | Para quê | Status/evidência |
|---|---|---|---|
| Alteram mapa de apresentações/aulas sem evidências do que causa o desengajamento de quem esta assistindo | Palestrante/Professores | Com intuito de melhorar o entendimento do publico sobre o tema | H |

  

## 6.2 Existem produtos que atuam na mesma área, mesmo sem serem equivalentes ao TCC?

  

> [F] Read AI, é um assistente de inteligência artificial criado para gerenciar, transcrever e resumir reuniões virtuais em plataformas como Zoom, Google Meet e Microsoft Teams. Ele realiza transcrições ao vivo, resumos automaticos, análise de engajamento e feedback de comunicação.
> [F] Noldus FaceReader: é um software de análise automática de expressões faciais capaz de identificar estados como felicidade, tristeza, raiva, surpresa, medo, nojo e neutralidade, apresentando também a intensidade dessas expressões ao longo do tempo. Embora seja voltado principalmente para pesquisas comportamentais, possui relação com o MindFlow AI por utilizar informações faciais para analisar estados e reações dos indivíduos.
> [F] Microsoft Teams Education Insights: é uma ferramenta integrada ao Microsoft Teams para Educação que fornece aos docentes informações sobre a participação e o engajamento digital dos estudantes. O sistema apresenta dados como participação em reuniões, tempo de presença, acesso a arquivos, realização de atividades, mensagens, respostas e reações. Diferentemente do MindFlow AI, seu foco está principalmente nas ações realizadas pelo estudante dentro da plataforma, e não na classificação automática de estados afetivo-cognitivos como engajamento, tédio, confusão e frustração.

  

## 6.3 Quais interfaces profissionais esse público já conhece?

  

Exemplos possíveis: ferramentas de banco, IDEs, consoles de nuvem, dashboards, plataformas de dados, ferramentas de monitoramento, painéis de IA, sistemas administrativos.

  

> [H] Dashboards de monitoramento de métricas.

  

## 6.4 O que essas soluções parecem fazer bem?

  

> [F] Geração de resumos e transcrições das reuniões.

  

## 6.5 O que parecem fazer mal, dificultar ou não atender?
> [H] Demonstração dos indicadores da reunião são muito macro, sem conseguir indicar os principais pontos de melhoria.


## 6.6 Que padrões de interface ou vocabulário parecem familiares a esse público?
> [H] Indicador por cor tipo semáforo, dashboard com gráfico e métrica, resumo automático no estilo Read AI. Timeline de reunião também já é um padrão que esse público reconhece de cara.


---

# 7. Derivando o escopo de IHC da disciplina

  

## 7.1 Escolha o caminho do projeto

  

### Caminho A — TCC já possui interface

  

> [H] O recorte vai ser o trilho de tempo real do comunicador: acompanhar o Semáforo Cognitivo ao vivo, e como secundário a revisão pós-sessão pelo Dashboard. Faz sentido priorizar esse fluxo porque é onde o problema realmente acontece, o comunicador dando aula ou apresentando sem saber o estado do grupo. Ferramentas como o Read AI já resolvem bem o pós-reunião (resumo, transcrição), mas ninguém ataca o tempo real do jeito que o MindFlow propõe, então esse é o recorte que mais diferencia o projeto.

  

### Caminho B — TCC não possui interface prevista

  

*Não se aplica, o TCC já prevê interface (ver 0.5 e Caminho A).*

  

## 7.2 Qual perfil será priorizado no projeto de IHC?

  

> O **comunicador**: professor, instrutor ou palestrante conduzindo a sessão.

  

>  **Por que esse perfil foi escolhido?** É quem efetivamente olha a interface e decide algo com base nela. É quem sente o problema na pele, tentando dar aula e monitorar a turma ao mesmo tempo. E é em torno dele que o TCC já estrutura o semáforo e o dashboard.

  

## 7.3 Qual objetivo desse usuário será priorizado?

  

> Perceber em tempo real, sem tirar a atenção da própria condução da sessão, se o grupo está engajado, entediado, confuso ou frustrado, pra poder agir enquanto ainda dá tempo.

  

## 7.4 Que interface será explorada na disciplina?

  

Complete:

  

>  **Para fins da disciplina de IHC, será projetada uma interface que permita ao comunicador utilizar as estimativas cognitivas geradas pelo MindFlow AI para perceber e reagir ao estado de engajamento do grupo, no contexto de uma sessão de videoconferência ao vivo, sem tirar a atenção dele da própria condução da sessão.**

  

> O foco é o Semáforo Cognitivo em tempo real, com o Dashboard pós-sessão como recorte secundário.

  

## 7.5 Qual é a relação dessa interface com o TCC?

  

- [X] Já fazia parte do TCC.

- [ ] É um aprofundamento de algo parcialmente previsto.

- [ ] É uma extensão conceitual criada para a disciplina.

- [ ] É um protótipo demonstrativo de aplicação potencial.

- [ ] Outra: {{...}}.

  

>  **Declaração:** a interface desenvolvida nesta disciplina é um artefato de aprendizagem de IHC baseado no tema do TCC. Sua inclusão ou implementação no TCC somente ocorrerá se isso for posteriormente decidido pela equipe e pelo orientador.

  

---

  

# 8. Levantando possibilidades de interação — sem desenhar ainda

 

A equipe pode registrar possibilidades para investigação. **Não significa que todas serão implementadas.**


Marque apenas as que parecem plausíveis e explique o objetivo correspondente.

  

| Possibilidade | Pode fazer sentido? | Objetivo/tarefa que justificaria | Evidência atual |
|---|---|---|---|
| Dashboard/visão geral | sim | Revisar depois da sessão como o engajamento variou ao longo do tempo | Já previsto no TCC |
| Configuração/parametrização | talvez | Ajustar granularidade da janela de agregação ou sensibilidade do alerta | Mencionado como parâmetro do pipeline, não como tela pro usuário final |
| Entrada/upload/seleção de dados | não | A entrada é a webcam ao vivo, não upload manual | F |
| Acompanhamento de processamento | talvez | Indicar que o sistema tá ativo e capturando, por transparência | H |
| Relatório/resultados | sim | Resumo do que aconteceu na sessão, tipo o que o Read AI já faz mas focado em estado cognitivo | Já previsto (Dashboard + persistência) |
| Histórico com busca/filtros | talvez | Comparar sessões diferentes ao longo do semestre | H |
| Comparação de resultados | talvez | Comparar engajamento entre aulas diferentes do mesmo comunicador | H |
| Explicabilidade/detalhamento | sim | Entender por que o sistema marcou um momento como "confuso", já que o modelo erra bastante em algumas dimensões | H |
| Administração/configurações globais | não | Fora do recorte, perfil é comunicador comum, não administrador | H |
| Usuários/perfis/permissões | não | Não é foco, assume-se um comunicador por sessão | H |
| CRUD de entidade do domínio | não | Não tem entidade que peça CRUD nesse recorte | H |
| Auditoria/logs | talvez | Pode importar pra LGPD/compliance, mas não pro comunicador comum | H |
| Alertas/ocorrências | sim | É o núcleo do Semáforo Cognitivo | Já previsto |
| Ajuda/documentação | talvez | Explicar na primeira vez o que os estados significam e os limites do sistema | H |

  

>  **Atenção:** "login + dashboard + CRUD" não é uma solução universal. Cada padrão deve surgir de uma tarefa real.

  

---

  

# 9. Benefícios e ações iniciais

  

## 9.1 Qual benefício concreto o projeto de IHC pretende oferecer?

  

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |
|---|---|---|---|
| Deixar o comunicador perceber, sem esforço extra, quedas de engajamento ou picos de confusão/frustração enquanto ainda pode agir | Cegueira situacional do facilitador em videoconferência | Comunicador | H |
| Deixar o comunicador revisar depois quais momentos deram mais dificuldade, pra melhorar a próxima sessão | Falta de feedback estruturado sobre a própria condução | Comunicador | H |

  

## 9.2 Que ações o usuário deverá conseguir realizar?

  

| ID | O usuário precisa conseguir... | Para alcançar... | Prioridade inicial |
|---|---|---|---|
| F01 | Ver de relance, sem parar de conduzir a sessão, o estado predominante do grupo | Perceber a tempo uma queda de engajamento ou pico de confusão/frustração | alta |
| F02 | Entender o que um alerta do semáforo significa sem precisar de treinamento | Confiar e agir sobre a informação sem ficar em dúvida | alta |
| F03 | Revisar depois da sessão a timeline do engajamento do grupo | Identificar trechos que precisam ser revistos ou melhorados | média |
| F04 | Perguntar sobre momentos específicos da sessão via chatbot | Ter mais contexto do que só um gráfico | baixa/média |

  

## 9.3 Tecnologias/restrições já definidas no TCC

  

A tecnologia aparece **agora**, depois do entendimento do uso.
  
| Tecnologia/restrição | Por que existe | Possível impacto na interação |
|---|---|---|
| Processamento local (Edge AI), sem enviar vídeo/áudio bruto pra servidor | Privacy by Design e LGPD | A interface não pode mostrar replay de vídeo do participante, só dado agregado |
| Modelo com acurácia ainda parcial e desigual entre dimensões (tédio é o pior caso) | Limitação técnica já identificada nos resultados do TCC1 | A interface precisa deixar claro que a estimativa tem incerteza, não é certeza absoluta |
| Agregação por janela de tempo em vez de classificação por pessoa | Decisão de design pra preservar privacidade | A tela mostra o "clima" do grupo, não o estado de uma pessoa específica |
| Latência compatível com uso ao vivo, em hardware de consumo | Requisito de tempo real do TCC | A interface do tempo real precisa ser leve, sem travar ou atrasar durante a fala |

  

---

  

# 10. Hipóteses e dúvidas prioritárias

  

| ID | Hipótese/dúvida | Por que importa | Como poderá ser investigada |
|---|---|---|---|
| H01 | Professor/palestrante acha útil um indicador discreto do estado do grupo durante a própria aula, sem virar mais uma distração | Se for falsa, o semáforo precisa virar outra coisa, tipo só resumo pós-sessão | Entrega 2/3 |
| H02 | O nível de confiança do modelo precisa aparecer na tela pra não deixar o comunicador confiar cegamente numa classificação errada | Muda como o dashboard e o semáforo mostram a informação | Entrega 7/8 |
| H03 | Participante da chamada sentiria desconforto sabendo que o comportamento dele tá sendo classificado, mesmo com processamento local | Pode exigir tela de consentimento, ampliando o escopo além do comunicador | Entrega 2/4 |
| H04 | O MindFlow se diferencia de ferramentas tipo Read AI justamente por atuar em tempo real e não só no pós-reunião | Se for falsa, o valor central do produto precisa ser repensado | Entrega 2 |
  

Registre em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

  

---

  

# 11. Síntese da equipe

  

| Pergunta | Síntese atual |
|---|---|
| Qual é a contribuição central do TCC? | Classificar em tempo real, localmente no dispositivo, o estado afetivo-cognitivo de participantes de uma videoconferência a partir de sinais visuais da webcam |
| O TCC já previa interface? | Sim, Semáforo Cognitivo em tempo real e Dashboard/Chatbot pós-sessão já fazem parte do TCC |
| Quem é o usuário prioritário de IHC? | O comunicador (professor, instrutor, palestrante ou facilitador) |
| O que ele precisa alcançar? | Perceber a tempo quando o grupo desengaja, confunde ou frustra, e ajustar a condução da sessão |
| Qual problema/atividade será estudado? | A cegueira situacional do facilitador em videoconferência |
| Como isso acontece hoje? | Observação visual direta e informal da grade, reações manuais e pergunta aberta, sem indicador estruturado |
| Qual é o contexto de uso? | Aulas remotas/híbridas, treinamento corporativo e apresentação técnica, em notebook/desktop com webcam |
| Que interface/recorte será explorado? | Semáforo Cognitivo em tempo real como foco principal, Dashboard pós-sessão como secundário |
| Como a interface se relaciona ao TCC? | Já fazia parte do TCC, ainda não implementada |
| Quais pontos ainda são hipóteses? | H01 a H04, na Seção 10 |

  

### Delimitação

  

**Dentro do escopo de IHC:** experiência do comunicador com o Semáforo Cognitivo em tempo real e o Dashboard pós-sessão.

**Fora do escopo de IHC:** configuração/administração do sistema, permissões multiusuário, interface do Chatbot RAG.

**Dentro do escopo formal do TCC:** modelo LSTM multi-saída, pipeline de extração multimodal, arquitetura Edge AI, Semáforo Cognitivo, Dashboard e Chatbot RAG.

**Interface da disciplina será implementada no TCC?** não definido, a equipe ainda vai decidir com a orientadora.

  

---

  

# 12. Como esta entrega alimenta as próximas

  

-  **Entrega 2:** verifica mercado, concorrentes e interfaces profissionais representativas.

-  **Entrega 3:** detalha perfis e contexto.

-  **Entrega 4:** aprofunda situações problemáticas.

-  **Entrega 5:** modela tarefas centrais.

-  **Entrega 6:** experimenta alternativas em baixa fidelidade.

-  **Entrega 7:** investiga hipóteses com dados.

-  **Entrega 8:** define restrições e metas de usabilidade.

-  **Entregas 9–11:** transformam o recorte em modelo de interação e protótipo.

-  **Entregas 12–14:** avaliam a interface construída na disciplina.

  

A Entrega 1 é uma **fotografia inicial do conhecimento**. Ela pode e deve ser revisada quando surgirem evidências.

  

---

  

# 13. Relação com INOVA e comunicação do projeto

  

Prepare uma explicação de até três frases:

  

1.  **Problema/atividade humana:** Em videoconferência, quem conduz a aula ou reunião perde a maior parte dos sinais não-verbais que usaria presencialmente pra perceber se o grupo tá engajado, entediado, confuso ou frustrado.

2.  **Contribuição técnica do TCC:** O MindFlow AI usa uma LSTM alimentada por landmarks de rosto, postura e olhar, extraídos localmente da webcam, pra classificar em tempo real o estado cognitivo do grupo, sem enviar vídeo pra nenhum servidor.

3.  **Como uma pessoa poderia utilizar essa contribuição:** Um professor acompanharia um semáforo discreto durante a própria aula, perceberia na hora se precisa mudar de exemplo ou abrir espaço pra dúvida, e depois revisaria um painel com a timeline do engajamento da turma.

  

Essa síntese ajuda a apresentar o projeto para público não especializado sem reduzir seu mérito técnico.

  

---

  

# Checklist de qualidade

  

- [ ] Está clara a diferença entre tema do TCC, escopo formal do TCC e escopo de IHC.

- [ ] A equipe declarou se o TCC já previa interface.

- [ ] Se não previa, foi derivado um usuário plausível e um objetivo de uso. *(não se aplica, TCC já previa interface)*

- [ ] A interface de IHC não foi apresentada como obrigação automática do TCC.

- [ ] A contribuição do TCC foi descrita sem começar por tecnologias de implementação.

- [ ] Usuários diretos e stakeholders foram diferenciados.

- [ ] Foram considerados profissionais que configuram, administram, interpretam ou decidem, quando pertinente.

- [ ] Objetivo do usuário não foi confundido com objetivo do projeto.

- [ ] Processo/problema atual foi descrito antes da solução.

- [ ] Existe situação concreta de uso/problema.

- [ ] Contexto físico, social/organizacional, dispositivos e consequências de erro foram considerados.

- [ ] Mercado/alternativas existentes foram levantados inicialmente.

- [ ] Possibilidades como dashboard, relatório, histórico, filtros e CRUD foram tratadas como hipóteses de solução, não como requisitos automáticos.

- [ ] Cada possibilidade de interface tem um objetivo/tarefa que poderia justificá-la.

- [ ] Afirmações relevantes estão marcadas `[F]`, `[H]` ou `[?]`.

- [ ] Hipóteses prioritárias receberam IDs e foram para a rastreabilidade.

- [ ] O recorte de IHC é viável para modelar, prototipar e avaliar no semestre.

- [ ] A equipe consegue explicar problema humano → contribuição computacional → forma de uso.
