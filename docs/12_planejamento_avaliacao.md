# Entrega 12 — Planejamento da avaliação de usabilidade (DECIDE)

**Data:** {{18/11/2026}}  
**Status:** 🟨 iniciada  
**Responsabilidade:** 1 solução por equipe

## Objetivo da atividade

Planejar a avaliação antes de executá-la, ligando perguntas de avaliação a métodos, participantes, tarefas, métricas, aspectos práticos, ética e forma de análise.

## O que está sendo avaliado

Em projetos cuja interface foi criada ou ampliada para a disciplina, o plano deve declarar explicitamente que a avaliação investiga **a qualidade da interação/protótipo**, não a validade científica ou o desempenho técnico do algoritmo/modelo do TCC.

Exemplos de perguntas:

- o DBA consegue localizar e comparar duas execuções?
- o analista entende o significado de um indicador?
- o administrador consegue alterar uma permissão sem risco de erro não percebido?
- o usuário compreende que o processamento está em andamento e consegue recuperar-se de uma falha?
- os filtros ajudam a localizar o histórico relevante?
- um relatório permite identificar a informação necessária para a decisão?

Se o protótipo utiliza dados ou resultados simulados, documente isso no plano.

## A. Método DECIDE

| Etapa | Aplicação no projeto |
|---|---|
| **D — Determine the goals** | Verificar autonomia, eficiência, satisfação e compreensão do Semáforo, conforme MU01–MU05 e MQ01–MQ05 da Entrega 8. |
| **E — Explore the questions** | Investigar localização das ações, salvamento, recuperação de erros e interpretação dos indicadores e seus limites. |
| **C — Choose the evaluation paradigm and techniques** | Inspeção individual pelos cinco integrantes, seguida de consolidação; observação remota de três docentes nesta etapa inicial, com cronômetro, anotações e pergunta de satisfação. |
| **I — Identify the practical issues** | Testes previstos para 24/11/2026, com 10 minutos por docente, além da preparação técnica. Piloto com a orientadora, em data a definir; preparar materiais e distribuir as funções antes da aplicação. |
| **D — Decide how to deal with ethical issues** | Obter consentimento e autorização de todos cujas imagens forem processadas. Não gravar; usar códigos, permitir desistência e seguir acesso restrito e retenção da Entrega 7. |
| **E — Evaluate, interpret and present the data** | Comparar taxas, medianas e satisfação às metas; agrupar dúvidas e erros; apresentar achados anonimizados e priorizados, separando piloto e aplicação final. |

## B. Perguntas de avaliação

| ID | Pergunta | Método | Métrica/evidência | Critério esperado |
|---|---|---|---|---|
| QA01 | O docente localiza a aula, personaliza, nomeia, salva e confere sem ajuda? | Observação de UT01. | Conclusão correta e intervenções. | MU01: ≥ 80%; 3/3 com a amostra inicial completa. |
| QA02 | Quanto tempo leva para concluir esse fluxo? | Cronometragem de UT01. | Tempo das conclusões corretas sem ajuda, incluindo esperas. | MU02: mediana ≤ 3 minutos. |
| QA03 | Qual a satisfação após a tentativa? | Pergunta pós-UT01. | Nota de 1 a 5 e motivo breve, inclusive após falha. | MU03: média ≥ 4/5. |
| QA04 | O docente distingue estado estável, mudança, incerteza e indisponibilidade? | UT02 com quatro casos padronizados. | Acerto por caso, conforme rubrica. | MU04: ≥ 80% acertam todos os casos sem ajuda. |
| QA05 | O docente interpreta uma mudança enquanto apresenta? | UT02 e cronometragem. | Tempo até interpretação correta, erros e interrupções. | MU05: mediana ≤ 5 segundos entre acertos sem ajuda. |
| QA06 | O docente reconhece resultados das ações e se recupera de erros? | Inspeção e observação de UT01/UT03. | Salvamento, validação, cancelamento e exclusão. | MQ03: reconhecer o estado e como prosseguir. |
| QA07 | O docente encontra e compreende uma explicação de indicador? | Observação e pergunta ao final. | Localização, interpretação e retorno. | MQ01/MQ04: compreender sem orientação do moderador. |

## C. Escopo e participantes

| Item | Planejamento |
|---|---|
| Perfis | Docentes com experiência em videoconferência, relacionados a P01/C02 e ao contexto de atenção dividida de T03/P02/C05. |
| Critérios de inclusão/exclusão | Adultos que aceitem participar e tenham computador compatível. Excluir integrantes, elaboradores da interface e participante do piloto da amostra final. Quem recusar processamento da imagem poderá realizar apenas o bloco pós-aula. |
| Nº de participantes | Três docentes nesta etapa inicial, U01–U03; piloto separado, P00. Pessoas de apoio não contam como docentes avaliados. A cobertura da amostra exigida na Entrega 14 será conferida separadamente. |
| Ambiente | Remoto, com compartilhamento da interface e sem gravação. |
| Dispositivo | Computador, câmera, microfone, internet, navegador, extensão e serviços necessários funcionando. Preparação técnica anterior às tarefas. |
| Protótipo/versão | MindFlow AI **2.0**, com funcionamento ampliado para outros sites de reunião. Registrar plataforma utilizada, navegador e versões ou commits do site, extensão e serviço local. |
| Teste piloto | Será realizado com a orientadora da equipe, em data a definir, antes da aplicação com os docentes. Verificará a clareza das informações, indicadores e comandos do dashboard e da extensão. O piloto de usabilidade ainda não foi realizado; o piloto anterior foi do software. |
| Recrutamento e cronograma | Professores conhecidos da faculdade. Aplicação inicial com três docentes prevista para **24/11/2026**, com horários a combinar. Piloto de usabilidade com a orientadora antes dessa aplicação, em data a definir. |
| Responsáveis | Nas sessões com docentes, um integrante será moderador e os demais serão observadores; a distribuição poderá variar entre sessões. Nomes a definir. A inspeção heurística continua individual para os cinco integrantes. |
| Duração e registro | 10 minutos por docente; anotações e cronômetro, sem gravações. Registrar tempo adicional de preparação, se houver. |
| Condição para iniciar | Combinar disponibilidade e funções, preparar os casos e verificar o funcionamento da versão 2.0. Realizar o piloto de usabilidade e incorporar os ajustes de clareza necessários antes da aplicação. |

## D. Lista de tarefas de avaliação

UT identifica tarefas deste protocolo; a terceira coluna apresenta os vínculos com a Entrega 5.

| ID | Cenário neutro entregue ao usuário | Objetivo oculto da avaliação | Critério de sucesso | Tempo-limite (se houver) |
|---|---|---|---|---|
| UT01 | Encontre a “Aula de teste A”. Prepare uma visualização com a evolução temporal antes do indicador de engajamento, sem a tabela de leituras detalhadas. Dê um nome e confira se a configuração ficou disponível. | T01/P01/C02; MU01–MU03 e MQ02/MQ03; fluxo pós-aula M01. | Aula correta, blocos e ordem solicitados, tabela ocultada, nome preenchido e configuração salva e reconhecida sem ajuda. | Até 4 minutos; a meta de eficiência continua sendo 3 minutos. |
| UT02 | Explique brevemente o tema combinado. Ao perceber uma mudança no acompanhamento, diga o que ela comunica e continue a explicação. Depois, interprete as outras situações apresentadas e seus limites. | T02/P01/C02 e contexto T03/P02/C05; MU04/MU05 e MQ01/MQ05. | Interpretar sem ajuda os casos estável, mudança, incerteza e indisponibilidade, conforme rubrica. | Até 3 minutos; observar a mudança por até 15 segundos, mantendo a meta de 5 segundos. |
| UT03 — complementar | Tente guardar esta configuração de teste ainda sem nome e prossiga conforme a resposta recebida. Depois, remova a visualização de teste indicada. | Recuperação e exclusão; MQ03. Não integra MU01–MU05. | Corrigir o nome, salvar e compreender a confirmação de exclusão. Cancelar a edição retorna diretamente ao resumo. | Até 1 minuto, se houver tempo; caso contrário, registrar não aplicada. |

> Uma boa instrução descreve o objetivo do participante sem dizer **onde clicar** ou usar o rótulo exato do controle que está sendo testado.

## E. Instrumentos

Instrumentos redigidos no [protocolo de avaliação](../instrumentos/protocolo_avaliacao_mindflow.md):

- [Termo e registro de consentimento](../instrumentos/protocolo_avaliacao_mindflow.md#1-consentimento).
- [Preparação e roteiro padronizado](../instrumentos/protocolo_avaliacao_mindflow.md#2-preparação-e-roteiro).
- [Perguntas de perfil e pós-tarefa](../instrumentos/protocolo_avaliacao_mindflow.md#3-perguntas-breves).
- [Rubricas e registro de observação](../instrumentos/protocolo_avaliacao_mindflow.md#4-rubricas-e-registro).
- [Roteiro e ficha de inspeção heurística](../instrumentos/protocolo_avaliacao_mindflow.md#5-inspeção-heurística).

## F. Plano de análise

- **Resultado:** total quando todos os critérios forem atingidos sem ajuda; parcial quando houver conclusão incompleta ou ajuda; falha quando não concluir no limite ou abandonar. Separar problemas técnicos, desistência da pesquisa e tarefas não apresentadas.
- **Eventos:** erro é ação ou interpretação incompatível com o objetivo; dúvida é hesitação ou pergunta; ajuda é orientação necessária à solução. Repetir o enunciado sem pistas e consultar a ajuda da interface não descaracterizam autonomia.
- **Tempo:** em UT01, medir após o enunciado até reconhecer o salvamento e conferir a configuração, incluindo esperas. Em UT02, medir da mudança visível à interpretação correta. Registrar erros, não respostas e interrupções. A medição remota manual é aproximada.
- **Satisfação:** perguntar “Quão satisfeito você ficou ao realizar esta tarefa?”, de 1 — muito insatisfeito a 5 — muito satisfeito, com motivo breve. Incluir tentativas malsucedidas e informar respostas ausentes.
- **Metas:** MU01 = sucessos totais entre quem iniciou; MU02 = mediana dos tempos de sucesso sem ajuda; MU03 = média das notas; MU04 = percentual correto nos quatro casos entre quem recebeu todos; MU05 = mediana das interpretações corretas sem ajuda. Informar denominadores. MU01/MU04 exigem 3/3 com a amostra inicial completa. Cobertura incompleta impede concluir atendimento integral; sem acertos, a mediana não é calculável.
- **Achados:** agrupar dúvidas e erros por tema, relacionando tarefa, tela/estado e evidência. Distinguir falas literais de paráfrases. Na inspeção, priorizar por severidade 0–4, considerando frequência, impacto e persistência, conforme Entrega 13.
- **Apresentação:** separar piloto e aplicação final, identificar simulações e limitações da amostra de conveniência. Não inferir precisão da IA, benefício pedagógico ou memorização após intervalo. Registros individuais ficam restritos até o término da disciplina; publicar apenas síntese anonimizada, conforme Entrega 7.

## G. Participantes cujas imagens são processadas e interface do participante

**Contribuição de:** Gustavo Bertoluzzi Cardoso — 22.123.016-2 (persona P05, cenário C03, tarefa T04, CI02 e MoLIC M02)

### G.1 O que fica fora desta etapa e por quê

A tarefa T04 (participar da aula controlando a própria participação) **não entra** nas tarefas UT01 a UT03. A versão 2.0 não tem interface para o participante: nas telas inspecionadas, a indicação de que a análise está ativa fica só no painel do docente (Entrega 13, V18). Não há o que testar com alunos agora sem inventar uma tela que não existe. Por isso, as perguntas abaixo ficam **planejadas, mas não aplicadas** nesta etapa. Elas serão usadas quando os estados do M02 estiverem no protótipo (Entrega 11).

| ID | Pergunta | Método | Métrica/evidência | Critério esperado |
|---|---|---|---|---|
| QA08 | O participante entende, só pelo aviso, o que é captado, o que o comunicador recebe e o que não é feito com os dados? | Teste com protótipo dos estados do M02, com alunos do perfil P05 (critérios da A03, Entrega 7), e pergunta de compreensão logo depois do aviso | Respostas corretas às três perguntas: "o que a câmera capta?", "o que a professora vê?", "o vídeo é guardado?" | Todos acertam as três sem ajuda; um erro sobre "o que a professora vê" conta como falha, porque é o medo central do C03 |
| QA09 | O participante consegue escolher, e depois mudar, a forma de participar e reconhecer o próprio estado no indicador? | Mesmo teste, com uma tarefa neutra ("participe desta aula do jeito que preferir; depois de alguns minutos, a situação muda e você quer continuar aparecendo, mas sem ser analisado") | Conclusão, ajudas e leitura correta do indicador depois de cada mudança | Todos concluem sem ajuda e leem corretamente o estado depois de cada mudança; se a opção "câmera ligada sem análise" não existir no protótipo (H03), a segunda parte é registrada como não aplicada |

### G.2 Cuidados com quem aparece na câmera em UT02

UT02 processa a imagem de quem está na chamada, mesmo que essas pessoas não sejam avaliadas. Para que o teste não reproduza o problema que o C03 descreve, proponho os pontos abaixo, a confirmar pela equipe antes do piloto. Eles complementam a etapa **D — Decide how to deal with ethical issues**:

- só têm a câmera analisada as pessoas de apoio que assinaram o consentimento antes da sessão; quem entrar sem consentimento fica com a câmera desligada ou a análise é pausada;
- antes de iniciar o acompanhamento, o moderador lê para todos um aviso padronizado, com o mesmo conteúdo previsto no M02: o que a câmera capta, que o docente vê só o estado do grupo, que o vídeo não é guardado e que nenhum resultado individual é registrado. Enquanto a interface não tiver esse aviso (V18), ele é feito pelo moderador;
- o docente avaliado pode deixar a própria câmera desligada sem perder a tarefa, como já previsto em C;
- não se anota nenhuma reação atribuída a uma pessoa de apoio; o registro de UT02 trata só da interpretação feita pelo docente;
- com menos de três pessoas de câmera ligada, o caso é tratado como "indisponibilidade", e não como estimativa do grupo, para não expor uma pessoa (mínimo provisório da Entrega 9; H05).

## Checklist

- [ ] As seis etapas DECIDE foram contextualizadas, não apenas expandidas por sigla.
- [ ] Perguntas de avaliação têm método e evidência correspondentes.
- [ ] O plano distingue avaliação de IHC de avaliação técnica/científica do TCC.
- [ ] Dados ou processamentos simulados no protótipo estão declarados.
- [ ] Tarefas vêm de objetivos/cenários relevantes.
- [ ] Critérios de sucesso foram definidos antes da coleta.
- [ ] Questões práticas e éticas estão resolvidas.
- [ ] Instrumentos estão prontos antes da Entrega 13/14.
- [ ] Plano diz como dados serão analisados e apresentados.
