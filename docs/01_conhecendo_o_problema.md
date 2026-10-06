
# Entrega 1 - Conhecendo o projeto, o usuário e o problema

**Data:** 13/08/2026

**Status:** ✅ CONCLUÍDO

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
- **usuário direto** × **stakeholder ou pessoa afetada**.

---

## Como classificar as respostas

Sempre que a resposta fizer uma afirmação sobre usuários, problemas, atividades, necessidades, contexto ou mercado, use:

- **[F] Fato conhecido** - existe evidência/fonte;
- **[H] Hipótese** - afirmação plausível que ainda precisa ser investigada;
- **[?] Não sabemos ainda** - lacuna relevante.

Quando usar `[F]`, informe a origem. Hipóteses prioritárias devem receber IDs (`H01`, `H02`...) e também ser registradas em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

> **Exemplo:** `[H] H01 - DBAs considerariam útil comparar automaticamente o plano atual de execução com uma recomendação produzida pelo algoritmo.`

Uma hipótese explicitada é melhor do que uma suposição escondida.

---

# 0. Identificação do TCC e da equipe

## 0.1 Membros

| Nome completo | Matrícula | GitHub |
|---|---:|---|
| Gustavo Bertoluzzi Cardoso | 22.123.016-2 | Gugzica3 |
| Isabella Vieira Silva Rosseto | 22.222.036-0 | IsaRosseto |
| Kayky Pires | 22.222.040-2 | kaykyypiress |
| Matheus Ferreira de Freitas | 22.125.085-5 | freitasfmatheus |
| Rafael Dias | 22.222.039-4 | rafadias008 |

## 0.2 Título atual do TCC

*MindFlow AI - Classificação Temporal de Estados Cognitivos em Videoconferências utilizando Redes LSTM e Fusão Multimodal*

## 0.3 Orientador(a)

Prof.ª Dra. Leila Cristina Carneiro Bergamasco

## 0.4 Qual é o resultado principal atualmente previsto no TCC?

Marque e descreva:

- [x] sistema/aplicação interativa;
- [ ] algoritmo;
- [x] modelo de IA/ML/LLM;
- [ ] biblioteca/API/framework;
- [ ] análise de dataset;
- [ ] estudo/benchmark/avaliação experimental;
- [ ] infraestrutura/backend;
- [ ] componente embarcado/IoT;
- [ ] outro:

**Descrição:**

> **[F - fonte: documentação do TCC1 sobre o modelo] IA:** o projeto prevê um modelo temporal treinado a partir do dataset DAiSEE para produzir classificações relacionadas a quatro dimensões afetivo-cognitivas: engajamento, tédio, confusão e frustração.

> **[F - fonte: documentação do TCC1 sobre a arquitetura da aplicação] SISTEMA:** também está prevista uma camada de aplicação que utiliza as classificações produzidas pelo modelo durante videoconferências, com processamento dos sinais visuais no dispositivo e apresentação de informações ao comunicador durante e após a sessão.

## 0.5 O TCC já previa desenvolvimento de interface com usuário?

- [x] Sim, a interface já faz parte do TCC.
- [ ] Parcialmente; existe alguma interação, mas ainda não está bem definida.
- [ ] Não. O TCC é predominantemente técnico e não previa interface.

**Explique o que está formalmente previsto no TCC:**

> **[F - fonte: documentação do TCC1 sobre a camada de aplicação]** Está prevista uma camada de aplicação com dois momentos de interação: um durante a sessão, representado inicialmente pela proposta do Semáforo Cognitivo, e outro após a sessão, representado por um Dashboard e possibilidade de consulta das informações registradas.

> Essas interfaces ainda não foram implementadas e suas características de interação ainda precisam ser investigadas e refinadas.

---

# 1. Entendendo a contribuição do projeto

## 1.1 Explique o TCC em uma frase, sem citar linguagem de programação, framework ou banco de dados.

> O MindFlow AI analisa sinais visuais captados pela webcam durante uma videoconferência e produz estimativas relacionadas a estados afetivo-cognitivos dos participantes, buscando oferecer informações que possam apoiar quem conduz a sessão.

## 1.2 Qual situação, atividade ou problema do mundo real motivou o TCC?

> **[F]** O uso de videoconferências cresceu de forma expressiva. Segundo o Microsoft Work Trend Index, houve aumento de 252% no tempo semanal dedicado a reuniões virtuais entre 2020 e 2022.

> **[H]** Nesse contexto, a equipe considera plausível que professores, instrutores e apresentadores encontrem dificuldade para acompanhar sinais do público enquanto também precisam explicar conteúdos, compartilhar a tela, controlar o tempo e utilizar outros recursos da videoconferência.

> Essa dificuldade específica ainda precisa ser investigada diretamente com os possíveis usuários.

## 1.3 Qual é a capacidade/contribuição central produzida pelo TCC?

> **[F - fonte: documentação técnica do TCC1]** O TCC busca classificar continuamente, a partir de sinais visuais, padrões relacionados a quatro dimensões afetivo-cognitivas: engajamento, tédio, confusão e frustração.

> Essas quatro dimensões representam **capacidades técnicas do modelo** e não devem ser assumidas automaticamente como a linguagem ou as informações mais adequadas para a interface.

## 1.4 O que se espera que esteja diferente para pessoas, organizações ou processos se essa contribuição for bem-sucedida?

> **[H]** A expectativa é que quem conduz uma aula, treinamento ou apresentação consiga perceber possíveis sinais de que o grupo está deixando de acompanhar o conteúdo e tenha informações adicionais para decidir se deve continuar, verificar a compreensão ou adaptar sua condução.

> Ainda precisa ser investigado quais informações realmente são úteis para essas decisões e se o recebimento de informações durante a própria sessão ajuda o comunicador ou aumenta sua carga de atenção.

## 1.5 O que é mérito técnico/científico do TCC e o que seria uma possível aplicação prática?

| Mérito/contribuição técnica | Possível aplicação/valor em uso |
|---|---|
| **[F - fonte: documentação técnica do TCC1]** Fusão multimodal com pré-processamento e arquitetura temporal para classificação de quatro dimensões afetivo-cognitivas | **[H]** Utilizar as estimativas produzidas pelo modelo como uma fonte adicional de informação para quem conduz aulas, treinamentos ou apresentações |
| **[F - fonte: arquitetura proposta no TCC1]** Processamento local dos sinais visuais e redução da necessidade de transmitir ou persistir vídeo bruto | **[H]** Reduzir a exposição dos dados visuais durante o processamento. A suficiência dessas decisões para atender expectativas de privacidade ou requisitos legais ainda precisa ser investigada |

---

# 2. Entendendo as pessoas envolvidas

## 2.1 Quem interage diretamente com o produto, se já existe interface prevista?

> **[H]** O usuário direto inicialmente considerado é o **comunicador**, entendido como a pessoa que conduz uma sessão e consulta as informações produzidas pelo MindFlow.

> Professor, instrutor, palestrante ou apresentador são exemplos possíveis desse papel. Entretanto, ainda precisa ser investigado se esses profissionais apresentam necessidades suficientemente semelhantes para serem tratados como um único perfil.

> Os participantes da videoconferência não são considerados, neste recorte inicial, usuários diretos da interface. Eles são **pessoas afetadas pelo sistema e fontes dos sinais utilizados no processamento**, já que seus sinais visuais podem participar da análise mesmo sem acesso ao Semáforo ou ao Dashboard.

## 2.2 Quem poderia usar, configurar, administrar, operar, interpretar ou tomar decisões a partir da contribuição técnica?

| Perfil | Relação com a contribuição | O que faria | Status/evidência |
|---|---|---|---|
| Professor em aula on-line | Possível usuário direto | Interpretaria informações durante ou após a aula para apoiar decisões sobre sua condução | H |
| Instrutor em treinamento corporativo | Possível usuário direto | Poderia utilizar informações para acompanhar o treinamento e decidir se precisa verificar compreensão ou adaptar sua condução | H |
| Palestrante/apresentador | Possível usuário direto | Poderia utilizar informações durante ou após uma apresentação | H |
| Participante da videoconferência | Pessoa afetada e fonte de dados | Teria sinais visuais processados durante a sessão, sem operar diretamente a interface destinada ao comunicador | H |
| Pesquisador/orientador acadêmico | Usuário indireto da contribuição técnica | Poderia utilizar o modelo e o pipeline como base para estudos relacionados | H |

## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

| Stakeholder/pessoa afetada | Como é afetado | Usa interface? | Status/evidência |
|---|---|---|---|
| Participante da videoconferência | Seus sinais visuais podem participar do processamento que gera inferências utilizadas pelo comunicador, podendo também ser afetado por decisões tomadas a partir dessas informações | Não, no recorte inicial | H |
| Instituição/empresa responsável pela sessão | Pode estabelecer regras, políticas ou condições para adoção da ferramenta | Provavelmente não diretamente | ? |
| Profissional responsável por privacidade ou governança de dados | Pode precisar avaliar riscos, políticas e condições de uso da ferramenta em uma instituição | Não necessariamente | H |

## 2.4 Que características desses perfis podem influenciar a interação?

> **[H]** Quem conduz uma videoconferência pode precisar dividir a atenção entre fala, conteúdo apresentado, tempo, chat e participantes. Isso pode tornar inadequadas informações que exijam leitura demorada ou interpretação complexa durante a própria sessão.

> **[?]** Ainda precisamos investigar se professores, instrutores e palestrantes apresentam necessidades semelhantes quanto à atenção, possibilidade de interromper a sessão, responsabilidade pelo público e critérios de sucesso.

---

# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

> **[H]** O comunicador quer conduzir uma aula, treinamento ou apresentação de forma que o público consiga acompanhar o conteúdo e identificar, enquanto ainda existe possibilidade de intervenção, quando pode ser necessário verificar a compreensão ou adaptar a condução.

> O objetivo não é simplesmente visualizar uma classificação, um semáforo ou um dashboard. A interface seria uma possível forma de apoiar uma atividade humana maior: **acompanhar a sessão e decidir como conduzi-la diante de sinais incompletos**.

## 3.2 Quais são as atividades mais importantes?

| ID | Atividade/objetivo | Quem realiza | Frequência/criticidade inicial | Status/evidência |
|---|---|---|---|---|
| A01 | Acompanhar os sinais disponíveis durante a sessão para perceber possíveis dificuldades de acompanhamento ou compreensão do grupo | Comunicador | Alta frequência, alta criticidade | H |
| A02 | Decidir se deve manter ou adaptar a condução da sessão a partir das informações disponíveis | Comunicador | Frequência variável, alta criticidade | H |
| A03 | Revisar posteriormente momentos da sessão para refletir sobre pontos que podem ser melhorados | Comunicador | Pós-sessão, criticidade média/alta | H |

> As quatro categorias produzidas pelo modelo não são utilizadas aqui como definição automática das necessidades humanas. Ainda precisa ser investigado qual informação o comunicador realmente busca ao acompanhar seu público.

## 3.3 Qual atividade parece mais frequente? Por quê?

> **[H]** A01 parece ser a atividade mais frequente porque acompanhar os sinais do público pode acontecer durante praticamente toda a sessão. A02 ocorre em momentos específicos, quando o comunicador percebe alguma informação que considera relevante e precisa decidir se deve agir.

## 3.4 Qual parece mais crítica? Que consequência existe se for mal executada?

> **[H]** A interpretação dos sinais disponíveis é crítica porque influencia as decisões posteriores. Se o comunicador interpretar incorretamente uma situação, pode interromper ou modificar a sessão sem necessidade ou, no sentido contrário, deixar de perceber uma dificuldade relevante.

> **[F - fonte: resultados preliminares do TCC1]** O modelo possui desempenho desigual entre as dimensões classificadas, o que reforça a necessidade de não apresentar suas saídas como descrição certa do estado interno dos participantes.

---

# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje, antes da interface imaginada na disciplina?

> **[H]** A hipótese inicial da equipe é que comunicadores utilizem principalmente sinais disponíveis na própria videoconferência, como câmeras, perguntas, chat, respostas verbais, reações manuais e atividades realizadas durante a sessão.

> Também podem recorrer a perguntas diretas para verificar se o grupo está acompanhando.

> **[?]** Ainda é necessário investigar quais recursos as plataformas atuais oferecem para apoiar essa percepção e quais estratégias são realmente mais utilizadas pelos diferentes perfis de comunicador.

## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

> **[H]** Pode ser difícil acompanhar simultaneamente uma apresentação, o chat, o tempo disponível e vários participantes. Câmeras desligadas, iluminação ruim, enquadramento inadequado, baixa participação e sinais contraditórios podem tornar ainda mais difícil interpretar o que está acontecendo com o grupo.

> Existe também o risco de o comunicador formar uma percepção geral a partir de apenas alguns participantes mais visíveis ou participativos.

## 4.3 Que informações o profissional precisa interpretar para tomar decisão?

> **[H]** O comunicador pode precisar perceber se existem sinais suficientes para justificar uma verificação de compreensão ou uma mudança na condução, se esses sinais representam uma parcela relevante do grupo e se a situação está mudando ao longo da sessão.

> **[?]** Ainda não sabemos quais informações, categorias ou representações são realmente consideradas úteis por professores, instrutores ou palestrantes para tomar essas decisões.

## 4.4 O que acontece quando a atividade falha ou quando o resultado é interpretado incorretamente?

> **[H]** Se o comunicador não percebe uma dificuldade relevante durante a sessão, pode continuar o conteúdo sem verificar se o grupo ainda está acompanhando.

> No sentido contrário, interpretar um sinal ambíguo como problema pode levar a interrupções desnecessárias ou mudanças de ritmo que não eram necessárias.

> Caso uma futura inferência automática seja utilizada como apoio, falsos positivos e falsos negativos também podem afetar essas decisões. Por isso, a saída do modelo deverá ser tratada como **estimativa**, e não como verdade sobre o estado dos participantes.

## 4.5 Conte uma situação concreta

> **[H]** Uma professora ministra uma aula para trinta alunos por videoconferência. Enquanto compartilha slides, tenta observar ocasionalmente a grade de participantes, mas apenas parte da turma mantém a câmera ligada e os vídeos aparecem em miniaturas pequenas.

> Ao entrar em um tópico mais complexo, percebe pouca participação e quase nenhuma pergunta. Ela não consegue saber se o silêncio significa compreensão, atenção, dúvida ou simplesmente falta de participação.

> Como ainda existe conteúdo previsto para aquela aula, decide continuar.

> Posteriormente, uma atividade ou avaliação pode revelar que vários alunos tiveram dificuldade justamente naquele tópico. Nesse caso, a professora descobre apenas depois que teria sido útil verificar melhor a compreensão durante a explicação.

> Essa narrativa representa uma hipótese de problema e ainda precisa ser investigada com usuários reais.

## 4.6 Que evidência existe hoje?

| Evidência/fonte | O que sustenta | Limitação |
|---|---|---|
| Microsoft Work Trend Index (2022) | Aumento de 252% no tempo semanal em reuniões virtuais entre 2020 e 2022 | Não demonstra especificamente dificuldade do comunicador em perceber o público |
| Bailenson, J. N. (2021), *Nonverbal Overload* | Discute mecanismos de sobrecarga associados à videoconferência | É um argumento teórico, não uma investigação específica com comunicadores utilizando o MindFlow |
| Fauville et al. (2021), estudo com 10.591 participantes | Apresenta evidências relacionadas à fadiga em videoconferências | O foco está nos participantes e na fadiga, não na percepção do comunicador |
| Resultados preliminares do TCC1, POC utilizando aproximadamente 22% do DAiSEE | Indicam viabilidade técnica inicial para extração e classificação dos sinais estudados | Amostra parcial, dados desbalanceados e ausência de validação com usuários reais |

---

# 5. Entendendo o contexto de uso

## 5.1 Onde e em quais situações a interação poderia ocorrer?

> **[H]** Foram inicialmente mapeados diferentes contextos plausíveis: aulas remotas ou híbridas, treinamentos corporativos, apresentações técnicas e outras videoconferências em que exista uma pessoa responsável por conduzir o conteúdo para um grupo.

> Esses contextos não são considerados equivalentes neste momento.

> **[?]** Ainda precisamos investigar **qual situação representa melhor o contexto prioritário que deverá orientar posteriormente a modelagem, prototipação e avaliação do projeto de IHC**.

## 5.2 Em quais dispositivos/equipamentos?

> **[F - fonte: arquitetura proposta no TCC1]** O processamento foi inicialmente pensado para ocorrer no dispositivo utilizado durante a videoconferência, principalmente notebook ou desktop com webcam.

> **[?]** O uso em dispositivos móveis ainda não está definido.

## 5.3 Existem condições físicas relevantes?

> **[H]** Iluminação inadequada, ângulo da câmera, enquadramento parcial, conexão instável, compartilhamento de tela, interrupções externas e ambiente doméstico ou profissional podem interferir tanto na captura dos sinais quanto na atenção de quem conduz a sessão.

## 5.4 Existem fatores sociais ou organizacionais?

> **[H]** Existe assimetria entre os participantes, cujos sinais visuais podem ser processados, e o comunicador, que recebe as informações resultantes.

> Em ambientes educacionais ou corporativos também podem existir diferenças de autoridade e expectativas sobre uso de câmera, participação e privacidade.

> Essas situações podem gerar necessidades relacionadas a informação, transparência, consentimento, controle ou contestação.

> **[?]** Ainda precisa ser investigado quais mecanismos seriam necessários e quais requisitos institucionais ou legais se aplicariam a cada contexto.

## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

> **[F - fonte: arquitetura/camada de aplicação prevista no TCC1]** O projeto prevê persistência de representações reduzidas e metadados associados à sessão, sem depender da persistência de vídeo bruto, além de uma visualização posterior dos dados registrados.

> **[H]** Ainda precisa ser investigado quais informações históricas realmente seriam úteis ao usuário e por quanto tempo deveriam permanecer disponíveis.

## 5.6 Um erro pode produzir consequência relevante? Qual?

> **[H]** Sim.

> Um falso negativo pode fazer com que uma possível dificuldade deixe de ser sinalizada, criando uma falsa sensação de segurança.

> Um falso positivo pode indicar uma dificuldade que não corresponde ao que está ocorrendo e influenciar o comunicador a interromper ou modificar a sessão sem necessidade.

> Erros perceptíveis também podem reduzir a confiança do usuário na ferramenta.

---

# 6. Entendendo mercado e alternativas existentes

> Nesta entrega faça apenas um **levantamento inicial**. A análise aprofundada ocorre na Entrega 2.

## 6.1 Como pessoas resolvem problemas semelhantes hoje?

| Alternativa atual | Quem usa | Para quê | Status/evidência |
|---|---|---|---|
| Observação das câmeras e das reações dos participantes | Professores, instrutores e apresentadores | Tentar perceber como o público está acompanhando | H |
| Perguntas diretas ao grupo | Professores, instrutores e apresentadores | Verificar compreensão ou solicitar participação | H |
| Chat, reações e enquetes da plataforma | Participantes e comunicadores | Produzir retorno explícito durante a sessão | H |
| Revisão posterior de resultados, atividades ou feedbacks | Professores e instrutores | Identificar problemas que não foram percebidos durante a sessão | H |

## 6.2 Existem produtos que atuam na mesma área, mesmo sem serem equivalentes ao TCC?

> **[H - levantamento preliminar a verificar na Entrega 2] Read AI:** parece oferecer recursos relacionados à transcrição, resumo e análise de reuniões virtuais.

> **[H - levantamento preliminar a verificar na Entrega 2] Noldus FaceReader:** parece realizar análise automática de expressões faciais e possui relação conceitual com o MindFlow por trabalhar com sinais faciais.

> **[H - levantamento preliminar a verificar na Entrega 2] Microsoft Teams Education Insights:** parece oferecer informações relacionadas à participação e à atividade de estudantes dentro do ecossistema Microsoft Teams.

> Essas descrições ainda precisam ser verificadas em fontes oficiais antes de serem tratadas como fatos sobre os produtos.

## 6.3 Quais interfaces profissionais esse público já conhece?

> **[H]** Plataformas de videoconferência, dashboards de métricas, ferramentas de apresentação e ambientes de aprendizagem são interfaces potencialmente familiares aos perfis considerados.

## 6.4 O que essas soluções parecem fazer bem?

> **[H]** Algumas alternativas parecem oferecer recursos úteis de comunicação, participação, registro, transcrição e revisão posterior de sessões.

## 6.5 O que parecem fazer mal, dificultar ou não atender?

> **[?]** Ainda não existe evidência suficiente nesta entrega para concluir quais lacunas permanecem nas alternativas existentes. Essa análise deverá ser aprofundada na Entrega 2.

## 6.6 Que padrões de interface ou vocabulário parecem familiares a esse público?

> **[H]** Indicadores visuais simples, dashboards, gráficos, resumos e linhas do tempo podem ser padrões familiares, mas sua adequação ao contexto do MindFlow ainda precisa ser avaliada.

---

# 7. Derivando o escopo de IHC da disciplina

## 7.1 Escolha o caminho do projeto

### Caminho A - TCC já possui interface

> **[H]** Para a disciplina, a equipe pretende investigar prioritariamente a proposta de feedback durante a própria sessão, representada inicialmente pelo Semáforo Cognitivo, mantendo a revisão pós-sessão como recorte secundário.

> A escolha pelo tempo real é, neste momento, uma **hipótese de recorte e posicionamento**, baseada na possibilidade de apoiar decisões enquanto a sessão ainda está acontecendo.

> **[?]** Ainda precisa ser investigado se outras ferramentas existentes oferecem recursos semelhantes e se o tempo real realmente representa um diferencial relevante.

### Caminho B - TCC não possui interface prevista

*Não se aplica. O TCC já prevê interface.*

## 7.2 Qual perfil será priorizado no projeto de IHC?

> **[H]** Como categoria inicial, será considerado o **comunicador**, isto é, a pessoa responsável por conduzir uma sessão de videoconferência e interpretar as informações apresentadas.

> Professor, instrutor e palestrante são exemplos de perfis que podem ocupar esse papel.

> **[?]** Ainda será necessário investigar se esses perfis possuem objetivos, responsabilidades e contextos suficientemente semelhantes para serem tratados como um único usuário prioritário ou se um deles deverá ser escolhido como recorte principal.

## 7.3 Qual objetivo desse usuário será priorizado?

> **[H]** Perceber, sem perder excessivamente a atenção da própria condução, possíveis sinais relevantes sobre como o grupo está acompanhando a sessão e utilizar essas informações para decidir se deve verificar a compreensão ou adaptar sua condução.

> As categorias de engajamento, tédio, confusão e frustração são capacidades técnicas disponíveis no modelo, mas ainda precisa ser investigado se correspondem à linguagem e às informações realmente úteis para o comunicador.

## 7.4 Que interface será explorada na disciplina?

> **Para fins da disciplina de IHC, será investigada uma interface que permita ao comunicador utilizar as estimativas produzidas pelo MindFlow AI como apoio para interpretar possíveis mudanças durante uma sessão de videoconferência, sem tratar essas estimativas como descrição certa do estado dos participantes.**

> O Semáforo Cognitivo em tempo real será tratado como uma **solução candidata priorizada**, com o Dashboard pós-sessão como recorte secundário. Sua utilidade e sua forma de apresentação ainda deverão ser avaliadas.

## 7.5 Qual é a relação dessa interface com o TCC?

- [x] Já fazia parte do TCC.
- [ ] É um aprofundamento de algo parcialmente previsto.
- [ ] É uma extensão conceitual criada para a disciplina.
- [ ] É um protótipo demonstrativo de aplicação potencial.
- [ ] Outra.

> **Declaração:** a interface desenvolvida nesta disciplina é um artefato de aprendizagem de IHC baseado no tema do TCC. Sua inclusão ou implementação definitiva no TCC somente ocorrerá se isso for posteriormente decidido pela equipe e pelo orientador.

---

# 8. Levantando possibilidades de interação - sem desenhar ainda

A equipe pode registrar possibilidades para investigação. **Não significa que todas serão implementadas.**

Marque apenas as que parecem plausíveis e explique o objetivo correspondente.

| Possibilidade | Pode fazer sentido? | Objetivo/tarefa que justificaria | Evidência atual |
|---|---|---|---|
| Dashboard/visão geral | Sim | Revisar posteriormente como as estimativas variaram ao longo da sessão | Já previsto conceitualmente no TCC |
| Configuração/parametrização | Talvez | Ajustar características da forma de apresentação ou processamento quando necessário | H |
| Entrada/upload/seleção de dados | Não | O recorte inicial trabalha com sinais captados durante a videoconferência | F |
| Acompanhamento de processamento | Talvez | Permitir compreender se o processamento está ativo e em condições adequadas | H |
| Relatório/resultados | Talvez | Apoiar revisão posterior dos momentos registrados durante a sessão | H |
| Histórico com busca/filtros | Talvez | Localizar sessões ou momentos anteriores caso essa necessidade seja confirmada | H |
| Comparação de resultados | Talvez | Comparar sessões diferentes caso isso corresponda a uma tarefa real do usuário | H |
| Explicabilidade/detalhamento | Talvez | Ajudar o usuário a compreender as limitações e a natureza das estimativas apresentadas | H |
| Administração/configurações globais | Não no recorte inicial | Relaciona-se mais à administração técnica do sistema que à condução da sessão | H |
| Usuários/perfis/permissões | Talvez | Pode se tornar relevante caso existam papéis diferentes na adoção da ferramenta | ? |
| CRUD de entidade do domínio | Não | Não foi identificada uma tarefa humana que justifique esse padrão neste momento | H |
| Auditoria/logs | Talvez | Pode ser relevante para governança e rastreabilidade, mas ainda não para o usuário prioritário | H |
| Alertas/ocorrências | Talvez | Poderia chamar atenção para mudanças relevantes, caso H01 seja confirmada | H |
| Ajuda/documentação | Talvez | Explicar o significado e principalmente os limites das informações produzidas pelo sistema | H |

> **Atenção:** "login + dashboard + CRUD" não é uma solução universal. Cada padrão deve surgir de uma tarefa real.

---

# 9. Benefícios e ações iniciais

## 9.1 Qual benefício concreto o projeto de IHC pretende oferecer?

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |
|---|---|---|---|
| Oferecer uma fonte adicional de informação que possa ajudar o comunicador a perceber possíveis dificuldades durante a sessão | Dificuldade de acompanhar simultaneamente conteúdo, participantes e outros sinais da videoconferência | Comunicador | H |
| Permitir revisar posteriormente momentos relevantes da sessão para refletir sobre sua condução | Falta de feedback estruturado sobre momentos anteriores da sessão | Comunicador | H |

## 9.2 Que ações o usuário deverá conseguir realizar?

| ID | O usuário precisa conseguir... | Para alcançar... | Prioridade inicial |
|---|---|---|---|
| T01 | Consultar rapidamente uma estimativa agregada durante a sessão | Obter informação adicional sem interromper excessivamente a condução | Alta |
| T02 | Compreender que a informação apresentada é uma estimativa e possui limitações | Evitar confiança excessiva ou interpretação como verdade absoluta | Alta |
| T03 | Revisar posteriormente momentos relevantes registrados durante uma sessão | Refletir sobre possíveis pontos de melhoria | Média |
| T04 | Consultar informações adicionais sobre determinados momentos da sessão, caso essa necessidade seja confirmada | Obter maior contexto durante a revisão | Baixa/média |

## 9.3 Tecnologias/restrições já definidas no TCC

| Tecnologia/restrição | Por que existe | Possível impacto na interação |
|---|---|---|
| Processamento local, evitando o envio de vídeo bruto para processamento remoto | Decisão técnica voltada à redução da exposição dos dados visuais | A interface deverá trabalhar prioritariamente com informações derivadas, sem depender da exibição de vídeo bruto |
| Modelo com desempenho ainda parcial e desigual entre dimensões | Limitação técnica identificada no TCC | A interface não deve apresentar a classificação como certeza sobre o estado dos participantes |
| Agregação dos resultados | Decisão técnica e de projeto que reduz a exposição individual | A interface pode priorizar informações sobre o grupo em vez de avaliações individuais |
| Necessidade de resposta compatível com uso durante videoconferência | O sistema pretende explorar situações durante a própria sessão | A interação não deve aumentar excessivamente a carga de atenção do comunicador |

> O processamento local, a redução da persistência de vídeo bruto e a agregação são decisões técnicas relevantes para reduzir riscos de privacidade, mas **não constituem, por si só, comprovação de conformidade jurídica com a LGPD**.

---

# 10. Hipóteses e dúvidas prioritárias

| ID | Hipótese/dúvida | Por que importa | Como poderá ser investigada |
|---|---|---|---|
| H01 | Um comunicador considera útil receber algum tipo de informação durante a própria sessão sem que isso se transforme em mais uma fonte de distração | Se for falsa, o recorte de tempo real pode precisar ser reduzido, alterado ou abandonado | Investigação com usuários nas próximas entregas |
| H02 | O comunicador precisa compreender adequadamente a natureza, as limitações e a incerteza das inferências produzidas pelo modelo para utilizá-las como apoio à decisão | Afeta a maneira como as informações poderão ser apresentadas e interpretadas | Investigar compreensão, confiança e interpretação de diferentes formas de comunicação da incerteza |
| H03 | Participantes podem sentir desconforto ou preocupação ao saber que sinais de seu comportamento visual estão sendo processados | Pode gerar necessidades de transparência, informação ou controle e ampliar o escopo de interação | Investigação com participantes e análise do contexto de uso |
| H04 | O uso de informações durante a própria sessão pode representar uma oportunidade relevante de diferenciação para o MindFlow em relação às soluções existentes | Se ferramentas existentes atenderem à mesma necessidade de forma suficiente, o posicionamento e o recorte da solução precisarão ser revistos | Levantamento aprofundado de alternativas na Entrega 2 |
| ?01 | Quais ferramentas existentes oferecem análise durante a sessão e quais informações disponibilizam ao usuário? | É necessário responder antes de sustentar uma diferenciação competitiva | Análise de concorrentes e produtos relacionados |
| ?02 | Professor, instrutor e palestrante podem realmente ser tratados como um mesmo perfil prioritário? | Diferenças entre esses profissionais podem alterar tarefas, contexto, linguagem e decisões de interface | Entregas de perfil, contexto e investigação com usuários |
| ?03 | Qual contexto de videoconferência deve orientar prioritariamente a modelagem e avaliação do projeto? | Evita projetar uma solução genérica demais para situações muito diferentes | Análise de contexto e investigação com usuários |
| ?04 | As categorias engajamento, tédio, confusão e frustração são realmente compreensíveis e úteis para o comunicador? | As saídas técnicas do modelo podem não corresponder diretamente às informações que o usuário precisa para decidir | Entrevistas, avaliação de vocabulário e investigação de tarefas |

Registre em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

---

# 11. Síntese da equipe

| Pergunta | Síntese atual |
|---|---|
| Qual é a contribuição central do TCC? | Produzir classificações temporais relacionadas a estados afetivo-cognitivos a partir de sinais visuais de participantes de videoconferências |
| O TCC já previa interface? | Sim. Semáforo Cognitivo, Dashboard e outras formas de aplicação já são consideradas no projeto |
| Quem é o usuário prioritário de IHC? | Inicialmente, o comunicador que conduz a sessão. Ainda precisa ser investigado se professor, instrutor e palestrante podem ser tratados como um único perfil |
| O que ele precisa alcançar? | Perceber possíveis sinais relevantes durante a sessão e decidir se precisa verificar compreensão ou adaptar sua condução |
| Qual problema/atividade será estudado? | A dificuldade de acompanhar o público e interpretar sinais enquanto conduz uma videoconferência |
| Como isso acontece hoje? | [H] Principalmente por observação dos participantes, chat, perguntas e outras formas de interação disponíveis na videoconferência |
| Qual é o contexto de uso? | Diferentes contextos de videoconferência foram identificados, mas o contexto prioritário ainda precisa ser investigado |
| Que interface/recorte será explorado? | Feedback durante a sessão como recorte principal de investigação e revisão pós-sessão como recorte secundário |
| Como a interface se relaciona ao TCC? | A aplicação interativa já é considerada no TCC, embora suas características de interação ainda precisem ser investigadas |
| Quais pontos ainda são hipóteses ou lacunas? | H01 a H04 e ?01 a ?04 |

### Delimitação

**Dentro do escopo inicial de IHC:** investigar como o comunicador poderia receber e interpretar informações produzidas pelo MindFlow durante e após uma videoconferência.

**Questões ainda abertas:** perfil prioritário dentro da categoria de comunicador, contexto de uso prioritário, linguagem mais adequada para apresentar as inferências, utilidade do feedback em tempo real e possíveis necessidades de informação ou controle das pessoas afetadas.

**Fora do escopo inicial de IHC:** administração técnica do modelo, manutenção do pipeline de IA e atividades de pesquisa acadêmica sobre o modelo que não estejam relacionadas à interação do usuário.

**Dentro do escopo formal do TCC:** modelo temporal, pipeline de processamento, arquitetura da aplicação e formas previstas de apresentação das informações.

**Interface da disciplina será implementada no TCC?** Ainda não definido. A equipe deverá decidir posteriormente com a orientadora.

---

# 12. Como esta entrega alimenta as próximas

- **Entrega 2:** aprofundará o levantamento de mercado, concorrentes e interfaces profissionais representativas e deverá ajudar a responder `?01`.
- **Entrega 3:** deverá aprofundar perfis e contextos, contribuindo para `?02` e `?03`.
- **Entrega 4:** deverá aprofundar situações problemáticas concretas.
- **Entrega 5:** deverá modelar tarefas humanas centrais, evitando partir diretamente das funcionalidades imaginadas para o sistema.
- **Entrega 6:** deverá experimentar alternativas em baixa fidelidade.
- **Entrega 7:** deverá investigar hipóteses com dados.
- **Entrega 8:** deverá definir restrições e metas de usabilidade.
- **Entregas 9 a 11:** deverão transformar o recorte em modelo de interação e protótipo.
- **Entregas 12 a 14:** deverão avaliar a interface construída na disciplina.

A Entrega 1 é uma **fotografia inicial do conhecimento**. Ela pode e deve ser revisada quando surgirem novas evidências.

---

# 13. Relação com INOVA e comunicação do projeto

Prepare uma explicação de até três frases:

1. **Problema/atividade humana:** Durante videoconferências, quem conduz uma aula, treinamento ou apresentação pode ter dificuldade para acompanhar os sinais disponíveis do público enquanto também precisa explicar o conteúdo, controlar o tempo e utilizar outras ferramentas.

2. **Contribuição técnica do TCC:** O MindFlow AI processa sinais visuais captados pela webcam e produz classificações temporais relacionadas a quatro dimensões afetivo-cognitivas, buscando realizar esse processamento localmente.

3. **Como uma pessoa poderia utilizar essa contribuição:** Essas estimativas poderiam servir como uma fonte adicional de informação para quem conduz a sessão, tanto durante a videoconferência quanto em uma revisão posterior. A utilidade e a melhor forma de apresentar essas informações ainda precisam ser investigadas.

Essa síntese ajuda a apresentar o projeto para público não especializado sem reduzir seu mérito técnico e sem transformar as capacidades do modelo em necessidades de usuário já confirmadas.

---

# Checklist de qualidade

- [x] Está clara a diferença entre tema do TCC, escopo formal do TCC e escopo de IHC.
- [x] A equipe declarou se o TCC já previa interface.
- [x] Se não previa, foi derivado um usuário plausível e um objetivo de uso. *(Não se aplica, pois o TCC já previa interface.)*
- [x] A interface de IHC não foi apresentada como obrigação automática do TCC.
- [x] A contribuição do TCC foi descrita sem começar por tecnologias de implementação.
- [x] Usuários diretos, stakeholders e pessoas afetadas foram diferenciados.
- [x] Foram considerados profissionais que interpretam, decidem ou podem participar da governança do uso, quando pertinente.
- [x] Objetivo do usuário não foi confundido com objetivo do projeto.
- [x] Processo/problema atual foi descrito antes da solução.
- [x] Existe situação concreta de uso/problema.
- [x] Contexto físico, social/organizacional, dispositivos e consequências de erro foram considerados.
- [x] Mercado/alternativas existentes foram levantados inicialmente sem transformar o levantamento preliminar em conclusão competitiva.
- [x] Possibilidades como dashboard, relatório, histórico, filtros e configurações foram tratadas como hipóteses ou soluções candidatas, não como requisitos automáticos.
- [x] Cada possibilidade de interface possui relação com um objetivo ou atividade que poderia justificá-la.
- [x] Afirmações relevantes sobre usuários, problemas e contexto estão diferenciadas entre `[F]`, `[H]` e `[?]`.
- [x] Hipóteses prioritárias receberam IDs e foram registradas para rastreabilidade.
- [x] O recorte de IHC é viável para ser refinado, modelado, prototipado e avaliado durante o semestre.
- [x] A equipe consegue explicar problema humano → contribuição computacional → possível forma de uso sem apresentar a solução como já validada.
