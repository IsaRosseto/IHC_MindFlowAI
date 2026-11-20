# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** 25/10/2026  
**Status:** 🟩 Concluída
**Responsabilidade:** 1 solução por equipe


## Objetivo da atividade

Transformar o conhecimento sobre usuários, tarefas, plataforma e contexto em princípios e metas de usabilidade verificáveis, organizando a evolução do MindFlow AI pelo Ciclo de Vida de Engenharia de Usabilidade.

## Delimitação do sistema interativo

| Camada | O que pertence ao projeto | O que será avaliado em IHC |
|---|---|---|
| Contribuição técnica do TCC | Modelo temporal de IA que estima engajamento, tédio, confusão e frustração a partir de sinais visuais, com processamento local. | A avaliação de interação não comprova a precisão ou a validade científica das inferências. |
| Camada de interação da disciplina | Semáforo durante a sessão, consulta de reuniões e resultados, personalização, configuração da extensão e suporte. | Compreensão dos indicadores, leitura durante a apresentação, eficácia, eficiência, erros, satisfação e acessibilidade. |
| Integrações e dados de avaliação | Site, extensão, serviço Python e histórico. Na avaliação pós-sessão, poderão ser utilizados registros previamente preparados ou reuniões de demonstração. Para o tempo real, são propostos estímulos controlados, sem necessidade de processar imagens dos participantes do teste. | Identificar no plano a versão, a origem dos dados e quais estados são simulados ou integrados. Uma mensagem exibida em um estímulo controlado permite avaliar sua interpretação, mas não demonstra o desempenho do modelo em uma aula real. |



## 1. Características da plataforma

| Característica | Descrição | Consequência para IHC |
|---|---|---|
| Software | Site acessado por navegador, integrado à extensão e ao serviço Python local. | Utilizar linguagem consistente e informar a disponibilidade de cada componente. |
| Hardware/dispositivos | Notebook ou desktop e internet. A webcam participa da captura durante a videoconferência; a consulta de um histórico preparado não depende de nova captura. | Manter indicadores legíveis durante a apresentação e permitir revisão posterior sem exigir nova videoconferência. |
| Capacidades | Consultar reuniões e gráficos, escolher e organizar blocos de informação, salvar visualizações, configurar a extensão e acessar suporte. | Manter evidentes as ações Ver resumo, Organizar dashboard e Salvar visualização, explicar os indicadores e permitir conferir a configuração aplicada. |
| Restrições | Inferências sujeitas a erro e limitações de captura, iluminação e desempenho. A cobertura de compatibilidade da extensão por navegador, versão e sistema operacional ainda não está consolidada. | Distinguir dados indisponíveis de estimativas baixas. Tratar a compatibilidade não verificada como lacuna, registrando a configuração efetivamente utilizada em cada avaliação. |
| Conectividade/latência | O processamento visual é local; autenticação e sincronização do histórico dependem de serviços remotos. | Diferenciar espera, indisponibilidade e falha. Especificar recuperação sem perda de ajustes quando pertinente e verificar o que está implementado. |
| Segurança/privacidade | O projeto propõe processamento local e histórico de resultados, com acesso por conta. Essas escolhas não demonstram, isoladamente, conformidade legal ou ausência de risco de identificação. | Explicar finalidade, processamento, acesso e retenção; verificar as condições de uso dos dados em cada contexto. |
| Volume de dados/histórico | Novas sessões ampliam a lista de reuniões e os registros temporais disponíveis. | Identificar sessões por título e data e apresentar detalhes sob demanda. |
| Tempo de processamento | Carregamento e sincronização podem variar; não há um limite máximo de resposta comprovado nesta entrega. | Comunicar espera e resultado das ações. Registrar esperas na avaliação e evitar apresentar informações antigas como atuais. |
| Papéis/permissões | O comunicador consulta os resultados; os participantes precisam compreender o tratamento de seus dados. | Distinguir análise do comunicador e transparência para participantes. Definir e verificar as restrições de acesso às reuniões. |

## 2. Princípios gerais do projeto

### Princípios direcionados ao negócio

| Princípio/norma | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte |
|---|---|---|---|
| Proteção de dados pessoais — LGPD, conforme o tratamento realizado | O tratamento de imagens, contas e registros exige examinar finalidade, necessidade, transparência, segurança e fundamento legal no contexto de implantação. | Definir os dados necessários, as responsabilidades, os acessos e a retenção; informar o tratamento. Processamento local não comprova conformidade. A definição da base legal e das responsabilidades permanece sujeita à verificação no contexto real. | [LGPD — texto atualizado, especialmente arts. 6º, 7º, 11 e 46](https://www2.camara.leg.br/legin/fed/lei/2018/lei-13709-14-agosto-2018-787077-normaatualizada-pl.html) |


### Princípios direcionados à interface

| Princípio/norma | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte |
|---|---|---|---|
| Acessibilidade | Indicadores, gráficos e controles precisam atender diferentes condições visuais e formas de interação. | Associar cores a textos, verificar contraste, navegação por teclado e foco visível; disponibilizar explicações acessíveis e alternativas às ações de arraste. Esses requisitos ainda precisam ser inspecionados no produto. | [WCAG 2.2 — critérios 1.4.1, 1.4.3, 1.4.13, 2.1.1, 2.4.7 e 2.5.7](https://www.w3.org/TR/WCAG22/) |
| Visibilidade do estado e recuperação de erros | O usuário precisa compreender disponibilidade da análise, validação de entrada e resultado do salvamento. | Diferenciar carregamento, ausência de dados, validação e sucesso. Na personalização, explicar o nome não preenchido e permitir corrigi-lo; confirmar a exclusão de uma visualização salva. | [Heurísticas de Nielsen](https://www.nngroup.com/articles/ten-usability-heuristics/) |
| Controle, reconhecimento e consistência | O docente precisa reconhecer opções e consequências sem memorizar procedimentos extensos. | Manter nomes e comportamentos consistentes, seleções visíveis, retorno ao resumo e cancelamento da edição. O cancelamento direto e a confirmação de exclusão são ações distintas. | [Heurísticas de Nielsen](https://www.nngroup.com/articles/ten-usability-heuristics/) |
| Redução da carga visual e leitura contextual | P01/P02 representam o contexto de atenção dividida entre explicação, apresentação e acompanhamento do público. Essa condição é uma entrada da análise que justifica o princípio. | Priorizar informação resumida durante a sessão e explicações sob demanda. Apresentar as classificações como estimativas e comunicar indisponibilidade, sem prescrever a decisão pedagógica. A adequação da solução depende de avaliação com docentes. | [Entregas 3](03_personas_contexto_jornada.md), [4](04_cenarios_problema.md) e [5](05_analise_tarefas.md); [design minimalista e reconhecimento — Nielsen](https://www.nngroup.com/articles/ten-usability-heuristics/) |

## 3. Metas de usabilidade

### 3.1 Metas qualitativas

| Meta | Para quem/tarefa | Evidência desejada | Justificativa |
|---|---|---|---|
| MQ01 — Compreender indicadores e limites | Docentes de aulas on-line: T02/P01/C02 durante a sessão e T01/P01/C02 na consulta posterior; R01/R02/R03, H02 e ?04. | Explicar o significado do indicador, reconhecer seu caráter estimado e distinguir ausência de dados de um resultado baixo. | Reduzir interpretações indevidas sobre alunos e sobre a certeza das classificações. |
| MQ02 — Personalizar com autonomia | Docentes de aulas on-line: T01/P01/C02, R05 e H06. | Localizar a edição, escolher e organizar blocos, nomear, salvar e conferir a configuração sem ajuda do moderador. | Avaliar a qualidade da personalização enquanto sua necessidade continua em investigação. |
| MQ03 — Reconhecer estados do sistema | Docentes: T02 no acompanhamento e T01 na revisão; R01/R03/R05. | Identificar espera, indisponibilidade, erro de entrada e sucesso, explicando como prosseguir em cada caso. | Evitar confundir falta de informação, resultado estimado e falha de uma ação. |
| MQ04 — Encontrar explicações | Docentes: T01 e T02, com dúvidas sobre os indicadores; H02 e ?04. | Localizar uma explicação, interpretar o termo e retornar à atividade sem depender da equipe. | Responder às dúvidas observadas no walkthrough da Entrega 6. |
| MQ05 — Consultar o Semáforo com atenção dividida | Docentes: T02/P01/C02 e contexto de T03/P02/C05; R01/R02 e H01. | Perceber uma mudança, interpretar a informação e retomar a explicação; registrar interrupções, erros e relatos de distração. | Avaliar o recorte principal nas condições de uso que motivaram o projeto. T03 descreve a prática docente atual; o apoio do MindFlow será avaliado como proposta de interação. |

### 3.2 Metas quantitativas


| ID | Dimensão | Métrica | Tarefa/escopo | Meta | Como medir | Justificativa |
|---|---|---|---|---|---|---|
| MU01 | Eficácia | Taxa de conclusão correta sem ajuda | Docentes; T01/P01/C02, R05 e H06: localizar a reunião, personalizar, nomear, salvar e conferir. | ≥ 80% | Conclusões corretas sem ajuda ÷ participantes que iniciaram × 100. Sucesso exige reunião correta, nome, seleção e organização solicitadas e reconhecimento da configuração salva. | Limiar inicial para sinalizar autonomia da maioria dos participantes, mantendo falhas individuais visíveis. Não confirma a necessidade da funcionalidade. |
| MU02 | Eficiência | Tempo mediano das conclusões corretas sem ajuda | Mesma população e mesmo fluxo completo de MU01. | ≤ 3 minutos | Iniciar após a leitura do enunciado e encerrar quando o participante reconhecer o salvamento e conferir a configuração aplicada, incluindo esperas. | Limite inicial para um fluxo delimitado de revisão com poucas operações. Sua adequação será verificada no piloto, sem alegar benchmark externo. |
| MU03 | Satisfação | Média da satisfação pós-tarefa, de 1 a 5 | Docentes; T01/P01/C02; incluir também tentativas não concluídas. | ≥ 4/5 | Perguntar “Quão satisfeito você ficou ao realizar esta tarefa?”, de 1 — muito insatisfeito a 5 — muito satisfeito, com justificativa breve. Informar respostas válidas e ausentes. | Quatro representa uma avaliação positiva na escala adotada. É uma meta inicial de projeto, não uma escala padronizada nem evidência de utilidade da personalização. |
| MU04 | Compreensão e prevenção de erros | Percentual de participantes que interpretam corretamente todas as situações controladas do Semáforo | Docentes; T02/P01/C02, contexto de T03/P02/C05; R01/R02, H01/H02 e ?04. | ≥ 80% | Apresentar quatro situações padronizadas: estado estável, mudança de estado, incerteza e dados indisponíveis. Considerar sucesso quando todas forem explicadas corretamente sem ajuda, conforme rubrica definida antes da aplicação. | Limiar inicial que prioriza compreensão e evita compensar um erro importante de interpretação com acertos em outras situações. Não mede a precisão da IA. |
| MU05 | Eficiência de leitura | Tempo mediano de interpretação correta de uma mudança do Semáforo | Docentes; T02 e contexto de T03, em breve atividade de explicação com o mesmo roteiro e estímulos para todos. | ≤ 5 segundos | Medir da apresentação da mudança até a interpretação verbal correta. Calcular a mediana apenas das interpretações corretas sem ajuda e registrar separadamente erros, não respostas e interrupções da explicação. | Proposta inicial de leitura breve diante da atenção dividida. O piloto verificará sua viabilidade; atingir cinco segundos não demonstra, isoladamente, ausência de distração. |

Para MU01–MU05:

- registrar versão da interface, população efetiva, tamanho da amostra, instruções, resultados por participante, pedidos de ajuda, erros e abandonos;
- separar participantes e dados do piloto daqueles da aplicação principal;
- não classificar conclusão com orientação do moderador como conclusão sem ajuda;
- apresentar MU01/MU02 e MU04/MU05 em conjunto: rapidez não compensa uma interpretação ou conclusão incorreta;
- quando não houver conclusões/interpretações corretas sem ajuda, informar que a mediana correspondente não é calculável;
- registrar intervenções, pausas e comentários sobre atenção: tempo e acerto não comprovam, sozinhos, ausência de distração ou benefício pedagógico;
- identificar estímulos simulados e estados ainda não implementados. A Entrega 12 deverá preparar esses materiais e fixar a rubrica antes da aplicação;
- tratar os resultados como evidências contextuais de usabilidade. Eles não confirmam automaticamente H01, H02 ou H06 e não substituem a investigação de necessidades da Entrega 7.

### 3.3 Priorização das metas (se exigida na disciplina)

| Meta | Peso de prioridade | Justificativa |
|---|---:|---|
| Baixa taxa de erros | 30% | Interpretar ausência de dados como baixo engajamento, confundir estimativa com certeza ou selecionar a reunião errada pode orientar uma análise inadequada. Prioriza-se prevenir e recuperar erros de interação e interpretação; a taxa de erro do modelo é uma medida técnica separada. |
| Eficiência | 25% | Durante a aula, o docente divide atenção entre conteúdo e participantes. A leitura do Semáforo deve ser breve, e a revisão posterior deve evitar operações desnecessárias. |
| Facilidade de aprendizado | 20% | Indicadores afetivo-cognitivos, agregação e incerteza exigem explicações compreensíveis. P01 representa familiaridade tecnológica baixa a média, ainda a investigar com pessoas reais. |
| Facilidade de memorização | 15% | O uso ocorre entre aulas, e configurações podem ser menos frequentes. Nomes consistentes, reconhecimento de opções e ajuda contextual devem permitir retomar o uso após um intervalo. |
| Satisfação positiva do usuário | 10% | A experiência deve ser confortável e compreensível, inclusive quanto à percepção de monitoramento. A satisfação complementa a observação de erros e atenção e não substitui a voz dos participantes investigada em H03. |
| **Total** | **100%** | |


## 4. Como o ciclo será iterado


| Etapa do ciclo | Aplicação ao MindFlow e artefatos relacionados | Como a avaliação realimenta o projeto |
|---|---|---|
| Análise de requisitos | Entregas 1 e 2: problema, hipóteses e referências; Entregas 3 a 5: perfis, contexto, cenários e tarefas; Entrega 7: investigação com pessoas; seções 1, 2 e 3 desta entrega: plataforma, princípios e metas. | Evidências sobre necessidades podem alterar o perfil prioritário, os cenários e as tarefas. Personas e modelos anteriores continuam sendo artefatos de análise, sem confirmar hipóteses por sua existência. |
| Nível 1 — Projeto essencial | Examinar como o apoio proposto altera o trabalho docente, formular o modelo conceitual da Entrega 9 e explorar protótipos iniciais, como os da Entrega 6. | Dúvidas sobre utilidade, vocabulário ou organização podem exigir reformular a proposta de interação e retornar aos requisitos. O protótipo digital da Entrega 6 não comprova que tenha existido uma etapa anterior em papel. |
| Nível 2 — Padrões de telas e diálogos | Relacionar conversas, falas e signos das Entregas 9 e 10 aos padrões de navegação e componentes documentados na Entrega 11. | Problemas de consistência e localização de ações levam à revisão de diálogos, nomes, hierarquia visual e componentes, seguida de nova avaliação. |
| Nível 3 — Projeto detalhado | Refinar estados e caminhos: resumo sem dados, validação de nome, salvamento, cancelamento, exclusão e retorno à tarefa; preparar os estados do acompanhamento em tempo real. | O planejamento da Entrega 12 e as avaliações das Entregas 13–14 devem verificar critérios definidos e indicar ajustes específicos em controles, mensagens, acessibilidade e recuperação. |
| Instalação/uso | Disponibilização e acompanhamento do uso da versão avaliada, quando houver adoção real. A publicação do site, por si só, não comprova adoção pelo público prioritário. | Registrar feedback de uso autorizado, limitações e novas necessidades; iniciar nova iteração quando surgirem problemas ou mudanças de contexto. |


A próxima iteração seguirá estas decisões:

1. **Investigar necessidades:** aplicar os instrumentos permitidos da Entrega 7 após sua revisão e piloto. O teste de usabilidade será planejado como avaliação posterior, sem substituir a coleta de necessidades.
2. **Preparar a avaliação:** na Entrega 12, selecionar tarefas, identificar versões, preparar dados/estímulos, definir rubricas, responsáveis e procedimentos para verificar as metas desta revisão. Registrar o que será integrado ou simulado.
3. **Avaliar e comparar:** usar inspeção e observação de usuários nas entregas posteriores, relacionando cada problema à tarefa, à meta, ao estado da interface e à evidência obtida.
4. **Retornar à etapa pertinente:** dificuldades de interpretação podem modificar signos e explicações; dificuldades de edição podem modificar controles e mensagens; evidências de ausência de necessidade podem simplificar ou retirar a personalização, mantendo a consulta de resultados útil sem ela.
5. **Reavaliar:** submeter as tarefas afetadas à nova avaliação, comparando versões sob condições equivalentes. Metas não serão relaxadas depois da aplicação principal apenas para declarar sucesso.


## Checklist

- [x] Capacidades e restrições têm impacto de IHC explicitado.
- [x] Está claro o limite entre contribuição técnica do TCC e camada interativa da disciplina.
- [x] Resultados/processamento simulados no protótipo foram explicitados.
- [x] Metas de usabilidade avaliam a interação, não substituem métricas técnicas do TCC.
- [x] Normas/princípios estão contextualizados, não apenas copiados.
- [x] Metas quantitativas são mensuráveis e associadas a tarefas/público.
- [x] Eficácia, eficiência e satisfação são consideradas quando pertinentes.
- [x] Metas poderão ser verificadas nas Entregas 12–14.
