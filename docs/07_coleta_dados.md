# Entrega 7 — Coleta de dados, necessidades e aspectos éticos

**Data:** {{dd/mm/aaaa}}  
**Status:** ⬜ não iniciada

## Objetivo da atividade

Planejar dados necessários para compreender usuários e requisitos de IHC, escolher técnicas adequadas e documentar instrumentos de modo que a aplicação possa ser reproduzida por pessoas diferentes.

## Para escopos de IHC derivados de TCC técnico

Quando o usuário e a interface foram propostos pela disciplina, uma prioridade da coleta é investigar se esse **cenário de uso realmente faz sentido**. Não trate o exercício de comercialização da Entrega 1 como validação de mercado.

Perguntas úteis incluem:

- esse perfil realmente realiza a atividade imaginada?
- quais ferramentas usa hoje?
- quais informações consulta?
- quais decisões toma?
- que vocabulário utiliza?
- quais parâmetros compreende e quais deveriam ser abstraídos?
- precisa de dashboard, histórico, filtros, relatórios ou comparação? Por quê?
- quais erros são frequentes e quais são críticos?
- existem papéis/permissões diferentes?
- que resultados do algoritmo/modelo seriam úteis ou difíceis de interpretar?

Quando o acesso ao perfil profissional for difícil, discuta com o docente alternativas metodológicas (especialistas próximos, dados secundários, literatura, participantes proxy) e registre as limitações. **Não esconda a limitação da amostra.**

## Hipóteses e lacunas prioritárias herdadas da Entrega 1

Antes de decidir “que dados coletar”, retome os itens `[H]` e `[?]` da Entrega 1 e o registro de hipóteses em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md). A coleta deve responder perguntas reais do projeto, e não apenas produzir um formulário porque a técnica foi solicitada.

| ID | Hipótese/lacuna | Evidência atual | Decisão que depende da resposta | Prioridade |
|---|---|---|---|---|
| H01 | Comunicadores consideram útil acompanhar, durante a própria sessão, um indicador discreto do estado do grupo sem que ele se torne uma nova fonte de distração. | Personas, cenários e análise de tarefas indicam a dificuldade de perceber o estado do público durante videoconferências. A análise de concorrência também identificou ferramentas com indicadores e feedback em tempo real, porém ainda não há evidência coletada diretamente com usuários do MindFlow sobre a utilidade e o nível de distração desse recurso. | Manter o Semáforo Cognitivo em tempo real como principal recorte de interação ou priorizar apenas análises e informações pós-sessão. | alta |
| H02 | O comunicador precisa visualizar alguma indicação de confiança ou incerteza da classificação para evitar confiança excessiva em uma previsão incorreta da IA. | A análise do Noldus FaceReader mostrou o uso de níveis de confiança associados às classificações e reforçou que resultados de reconhecimento devem ser tratados como estimativas. Ainda falta compreender quanto dessa informação os usuários desejam ou conseguem interpretar durante uma sessão. | Definir se a confiança do modelo será exibida e, caso seja, se aparecerá como percentual, faixa, indicação visual simplificada ou apenas em uma visualização detalhada. | média |
| H03 | Participantes podem sentir desconforto ao saber que suas expressões e comportamentos estão sendo processados para classificação de estados afetivo-cognitivos, mesmo quando o processamento ocorre localmente. | A análise de concorrência identificou preocupações com percepção de invasão em ferramentas de reunião e mecanismos explícitos de transparência sobre dados. Entretanto, ainda não há evidência direta de participantes sobre sua aceitação do funcionamento proposto pelo MindFlow. | Definir necessidade e forma de consentimento e transparência, quais informações devem ser apresentadas ao participante e se será necessário incluir interfaces específicas para esse público. | alta |
| H04 | O uso de informações em tempo real constitui um diferencial relevante do MindFlow em relação às soluções existentes. | A análise de concorrência refinou a hipótese: algumas ferramentas também possuem recursos em tempo real, enquanto outras trabalham principalmente com dados pós-sessão, atividade digital ou feedback explícito. Assim, tempo real isoladamente não parece ser um diferencial suficiente. | Refinar a proposta de valor do MindFlow, considerando como diferenciais a combinação entre análise em tempo real, estados afetivo-cognitivos, apoio imediato ao comunicador e contexto de videoconferência. | baixa |
| ?01 | Quais ferramentas existentes realizam análise de engajamento, comportamento ou estados dos participantes e quais informações disponibilizam em tempo real? | A lacuna foi parcialmente respondida na Entrega 2 com a análise de Read AI, Noldus FaceReader, Microsoft Teams Education Insights, reações manuais de plataformas de videoconferência, Adobe Connect Engagement Dashboard e outras ferramentas relacionadas. | Determinar quais funcionalidades já são padrões do domínio, quais não representam diferenciais do MindFlow e quais oportunidades ainda permanecem abertas para o projeto. | baixa |

## Parte A — necessidades e requisitos de IHC

> **Responsabilidade:** solução individual por integrante.

### A01 — {{autor}}

**Autor(a):** {{nome — matrícula}}

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Como o comunicador percebe atualmente se o público está engajado, confuso, entediado ou frustrado durante uma videoconferência | H01 | Permite compreender quais sinais e estratégias já são usados e se existe realmente dificuldade em acompanhar o estado do grupo durante a sessão | Definir se o Semáforo Cognitivo em tempo real é necessário e quais informações deve apresentar |
| Em quais momentos da sessão o comunicador sente maior necessidade de receber informações sobre o estado do público | H01 | Ajuda a entender quando o feedback seria útil e quando poderia gerar distração | Definir frequência de atualização, destaque visual e momento de exibição dos indicadores |
| Quais ações o comunicador tomaria ao perceber aumento de confusão, tédio, frustração ou queda de engajamento | H01 | Permite verificar se os dados gerados pelo sistema podem apoiar decisões reais durante a apresentação | Definir quais estados devem receber maior destaque e se o sistema deve apresentar sugestões de ação |
| Preferência entre informação em tempo real e análise após o término da sessão | H01 | Permite identificar qual dos dois momentos possui maior valor para o usuário | Priorizar o Semáforo em tempo real, o Dashboard histórico ou ambos |
| Nível de compreensão e interesse do comunicador sobre a confiança das classificações realizadas pela IA | H02 | É necessário verificar se apresentar a confiança melhora a interpretação ou apenas aumenta a carga cognitiva | Definir se a confiança será exibida e se aparecerá como percentual, faixa ou indicador simplificado |
| Forma considerada mais clara para indicar que uma classificação da IA possui incerteza | H02 | Diferentes formas de representação podem gerar interpretações distintas | Definir a representação visual da confiança ou incerteza do modelo |
| Grau de conforto dos participantes com o processamento de imagem da webcam para identificação de estados afetivo-cognitivos | H03 | O funcionamento do sistema pode ser percebido como invasivo ou gerar resistência ao uso | Definir requisitos de consentimento, transparência e controle do participante |
| Quais informações os participantes gostariam de receber antes de autorizar o uso da câmera para análise | H03 | Permite identificar quais explicações são necessárias para garantir uma decisão consciente | Definir o conteúdo da tela ou aviso de consentimento e transparência |
| Grau de aceitação do uso de dados agregados do grupo em comparação com resultados individuais | H03 | Informações individuais apresentam maior risco de exposição, vigilância e constrangimento | Definir se os resultados serão exclusivamente agregados ou se haverá algum nível de detalhamento individual |
| Quais informações do Dashboard são consideradas úteis após uma sessão | H01 / H02 | Permite evitar a inclusão de gráficos, filtros e métricas que não apoiem nenhuma tarefa real | Definir KPIs, gráficos, histórico, filtros e nível de detalhamento do Dashboard |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Professores e docentes que realizam aulas on-line | Ter experiência conduzindo aulas por videoconferência, preferencialmente de forma recorrente | Representam diretamente parte do público prioritário do MindFlow |
| Instrutores e facilitadores de treinamentos on-line | Conduzir apresentações, cursos ou treinamentos por videoconferência | Representam usuários com necessidades semelhantes às personas definidas no projeto |
| Palestrantes ou outros comunicadores que utilizam videoconferência | Ter experiência conduzindo sessões para grupos remotamente | Permitem verificar se as necessidades identificadas também aparecem fora do contexto estritamente educacional |
| Participantes de aulas, palestras ou treinamentos on-line | Ter participado de sessões por videoconferência com uso de câmera | São afetados pelo processamento das imagens e são relevantes principalmente para investigar privacidade, transparência e aceitação relacionadas à H03 |

#### Aspectos éticos

A participação deve ser **voluntária**, com consentimento claro sobre o objetivo da pesquisa e sobre quais dados serão coletados. Devem ser solicitadas apenas as informações necessárias, evitando dados pessoais sem relação com o estudo.

As respostas devem ser preferencialmente **anônimas ou pseudonimizadas**, e qualquer gravação deve ocorrer somente com autorização do participante.

Como o MindFlow envolve análise de imagens da webcam e inferência de estados afetivo-cognitivos, é necessário considerar riscos de **privacidade, sensação de vigilância e interpretações incorretas**. Os resultados não devem ser tratados como diagnósticos ou avaliações definitivas sobre os participantes.

Os dados coletados devem ter acesso restrito, ser utilizados apenas para o projeto e descartados quando não forem mais necessários.
> Repita A02, A03...

## Parte B — ferramentas de coleta

> Cada integrante deve preparar uma técnica/instrumento completo. As técnicas devem ser diferentes entre si e **questionário deve estar entre as técnicas escolhidas**, conforme o enunciado da disciplina.

### Instrumento I01 — Questionário

**Autor(a):** Kayky Pires — 22.222.040-2  
**Técnica:** Questionário on-line  
**Objetivo:** Investigar como comunicadores percebem o estado do público durante videoconferências, quais informações consideram úteis durante e após a sessão e suas percepções sobre confiança da IA e privacidade.  
**Público:** Professores, instrutores, palestrantes e outros comunicadores que conduzem atividades por videoconferência.

#### Procedimento padronizado de aplicação

1. Preparar o questionário em uma plataforma de formulários on-line.
2. Apresentar, no início do formulário, o objetivo da pesquisa e informar que a participação é voluntária.
3. Solicitar o consentimento do participante antes do início das perguntas.
4. Aplicar o questionário sem solicitar dados pessoais desnecessários.
5. Encerrar agradecendo a participação e informando que os dados serão utilizados apenas para fins acadêmicos.
6. Armazenar as respostas de forma restrita à equipe do projeto e analisar os resultados de forma agregada e anônima.

#### Instrumento

[**Link do formulário I01**](https://forms.cloud.microsoft/r/fHf6y8q6ZK)

#### Como os dados serão analisados

As questões fechadas serão analisadas por meio da **distribuição e frequência das respostas**, identificando padrões de percepção, necessidades e preferências dos participantes.

As respostas abertas serão analisadas por **codificação temática**, agrupando conteúdos semelhantes em categorias como utilidade do feedback em tempo real, confiança na IA, privacidade e informações desejadas no dashboard.

Ao final, os resultados serão relacionados às hipóteses **H01, H02 e H03**, permitindo verificar se elas foram sustentadas, refutadas ou precisam ser refinadas.

## Síntese

Explique quais lacunas de conhecimento sobre usuários o conjunto de técnicas pretende reduzir. Indique explicitamente quais hipóteses da Entrega 1 deverão ficar **sustentadas, refutadas ou refinadas** após a análise dos dados. Quando os dados forem coletados/analisados, atualize o histórico em `RASTREABILIDADE.md`.

## Checklist

- [ ] Hipóteses/lacunas prioritárias da Entrega 1 foram revisitadas.
- [ ] Se o escopo de IHC foi derivado de TCC técnico, a coleta investiga a plausibilidade do usuário, tarefa e contexto adotados.
- [ ] Perguntas não pressupõem que dashboard, CRUD, filtros ou relatórios sejam necessários; investigam a necessidade.
- [ ] Cada dado a coletar responde uma dúvida concreta do projeto ou justifica outra necessidade de informação.
- [ ] Parte A identifica dados e perfis de coleta de forma específica.
- [ ] Aspectos éticos são contextualizados para o projeto.
- [ ] Há uma técnica completa por integrante e técnicas distintas.
- [ ] Questionário está incluído entre as técnicas.
- [ ] Cada instrumento possui objetivo, público, procedimento e conteúdo integral.
- [ ] Perguntas evitam indução e coletam apenas dados necessários.
- [ ] Está claro como os dados serão analisados e usados no design.
