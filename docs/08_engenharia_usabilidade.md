# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** 25/10/2026  
**Status:** 🟨 iniciada
**Responsabilidade:** 1 solução por equipe

## Objetivo da atividade

Transformar o conhecimento acumulado sobre usuários, tarefas, plataforma e contexto em princípios e **metas de usabilidade verificáveis**, mantendo o caráter iterativo do projeto.

## Delimitação do sistema interativo

Antes das características da plataforma, separe:

| Camada | O que pertence ao projeto | O que será avaliado em IHC |
|---|---|---|
| contribuição técnica do TCC | Modelo temporal de IA que estima engajamento, tédio, confusão e frustração a partir de sinais visuais, processados localmente em Python. | desempenho técnico não é substituído pelo teste de IHC |
| camada de interação da disciplina | Semáforo em tempo real, consulta de reuniões, interpretação de indicadores, personalização de dashboards, configuração da extensão e suporte. Esta avaliação detalha a personalização dos resultados de uma aula concluída. | compreensão, eficácia, eficiência, satisfação, erros, acessibilidade etc. |
| integrações/dados simulados | Avaliação planejada no sistema integrado: extensão, Python, histórico e site, utilizando uma aula previamente registrada. Não se prevê simulação do processamento nessa tarefa. | Avaliar telas, carregamento, confirmação e falha. Qualquer simulação necessária será declarada no roteiro e ao participante. O teste de interação não comprova a precisão do modelo. |

Em um protótipo de disciplina, é aceitável simular processamento ou resultados quando a implementação técnica não estiver integrada, desde que isso seja declarado e a simulação seja suficiente para avaliar a interação.

## 1. Características da plataforma

| Característica | Descrição | Consequência para IHC |
|---|---|---|
| Software | Site acessado por navegador, integrado à extensão e ao serviço Python local. | Manter linguagem consistente e informar a disponibilidade dos componentes. |
| Hardware/dispositivos | Notebook ou desktop, webcam e internet; recursos compartilhados com a videoconferência. | Manter indicadores legíveis sem encobrir o conteúdo da aula. |
| Capacidades | Consultar reuniões e gráficos, personalizar dashboards e extensão e acessar suporte. | Destacar **Ver Resumo** e **Nova Visualização**, explicar indicadores e permitir conferir as alterações. |
| Restrições | Inferências sujeitas a erro e limitações de captura e desempenho. A compatibilidade da extensão será conferida antes do teste. | Distinguir ausência de dados de valores baixos e comunicar os limites das inferências. |
| Conectividade/latência | Análise local; autenticação e sincronização do histórico dependem de serviços remotos. | Diferenciar falhas locais de falhas de sincronização e permitir nova tentativa sem perder ajustes. |
| Segurança/privacidade | Processamento visual local e histórico numérico, sem depender da persistência de vídeo bruto. | Explicar finalidade e processamento, restringir acesso e priorizar resultados agregados. |
| Volume de dados/histórico | Novas aulas ampliam o histórico e a quantidade de registros temporais. | Identificar sessões por título e data e oferecer resumo com detalhes sob demanda. |
| Tempo de processamento | Preparação, consulta e confirmação têm tempos variáveis, ainda sem máximo comprovado nesta entrega. | Mostrar carregamento, confirmação e erro; distinguir informações antigas de atualizações recentes. |
| Papéis/permissões | O comunicador utiliza os painéis; participantes precisam de informações sobre o processamento. | Separar as interfaces de análise e transparência e impedir acesso a reuniões não autorizadas. |

## 2. Princípios gerais do projeto

Inclua apenas normas, leis, padrões e princípios realmente relevantes, explicando **como** afetam o projeto. Não transforme esta seção em lista de links.

| Princípio/norma | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte |
|---|---|---|---|
| Contexto de uso | Karol divide a atenção entre aula e ferramentas e possui familiaridade tecnológica baixa a média. | Priorizar leitura rápida durante a aula e personalização posterior, com linguagem compreensível. | [Entrega 1](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/docs/01_conhecendo_o_problema.md) / [Entrega 3](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/docs/03_personas_contexto_jornada.md) |
| LGPD, se aplicável | Sinais visuais e informações de contas e sessões exigem avaliar finalidade e base legal. | Definir a base legal aplicável, informar o tratamento e limitar coleta, retenção e acesso. Processamento local não comprova conformidade. | [LGPD — arts. 6º, 7º, 11 e 46](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm) |
| Acessibilidade | Gráficos e controles precisam atender diferentes condições visuais e formas de interação. | Associar cores a textos, assegurar contraste, teclado e foco visível e oferecer explicações acessíveis pelo foco. | [WCAG 2.2 — critérios 1.4.1, 1.4.3, 1.4.13, 2.1.1 e 2.4.7](https://www.w3.org/TR/WCAG22/) |
| Visibilidade, controle e recuperação de erros | O usuário precisa reconhecer estados e efeitos da edição. | Informar análise ativa, ausência de dados e falhas; confirmar alterações e permitir retornar à edição. | [Heurísticas de Nielsen — visibilidade, controle e recuperação de erros](https://www.nngroup.com/articles/ten-usability-heuristics/) |

## 3. Metas de usabilidade

Usabilidade deve ser discutida **no contexto de uso**. Metas quantitativas devem dizer o que será medido, em qual tarefa, com qual população e qual limite será considerado aceitável.

O foco é o docente representado pela proto-persona **P01 — Karol**, ainda a validar com usuários, e a tarefa de **personalizar os resultados de uma aula concluída**, conforme o [HTA, GOMS e CTT do recorte individual](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/Kayky-Response/docs/05_analise_tarefas.md) e as [telas da Entrega 6](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/docs/06_prototipacao_papel.md).

Na [matriz de rastreabilidade](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/RASTREABILIDADE.md), o Semáforo em tempo real permanece como foco principal do projeto. Esta avaliação detalha os fluxos **PF02/PF03** e as telas **P01 — Minhas Reuniões, P02 — Resumo e P03 — Editar Resumo** da Entrega 6. A ligação específica dessa personalização à persona P01 e ao cenário C02 ainda precisa ser registrada; R03 atualmente associa a revisão pós-sessão a outras personas. A compreensão das estimativas se relaciona a **H02**; **H01** (utilidade e distração durante a aula) e **H03** (aceitação pelos participantes) exigem investigação própria e permanecem abertas.

### 3.1 Metas qualitativas

| Meta | Para quem/tarefa | Evidência desejada | Justificativa |
|---|---|---|---|
| Compreender indicadores e limites | Docente consultando o resumo. | Explicar as estimativas e distinguir ausência de dados de valores baixos. | Evitar conclusões definitivas sobre os alunos. |
| Personalizar com autonomia | Docente escolhendo e organizando elementos. | Localizar a edição, selecionar, confirmar e avaliar sem ajuda. | Permitir priorizar engajamento ou sinais de tédio, confusão e frustração. |
| Reconhecer estados do sistema | Comunicador utilizando a integração. | Identificar carregamento, confirmação e falha e explicar como prosseguir. | Reduzir dúvidas sobre funcionamento e alterações. |
| Encontrar explicações | Docente com dúvidas sobre os cards. | Consultar ajuda, explicar um indicador e retornar à tarefa. | Atender às dificuldades registradas na simulação da Entrega 6. |

### 3.2 Metas quantitativas

Os valores são **metas iniciais propostas, ainda não verificadas**, para professores experientes em videoconferências, sem conhecimento prévio do fluxo de personalização. Outros perfis eventualmente incluídos terão resultados identificados separadamente.

Em computador, com conta autenticada, componentes preparados e histórico disponível, o participante deverá localizar uma aula em **Minhas Reuniões**, abrir **Ver Resumo**, acessar **Nova Visualização**, selecionar e organizar dois indicadores e um gráfico e confirmar. O roteiro definirá a mesma aula e configuração para todos, sem demonstrar o caminho.

| ID | Dimensão | Métrica | Tarefa/escopo | Meta | Como medir | Justificativa |
|---|---|---|---|---|---|---|
| MU01 | eficácia | taxa de conclusão correta sem ajuda | Personalização da aula, do histórico à confirmação. | ≥ 80% | Teste observado: conclusões corretas sem ajuda ÷ participantes que iniciam × 100. Conferir aula, elementos e organização. | Verificar autonomia no fluxo completo. |
| MU02 | eficiência | tempo mediano das conclusões corretas sem ajuda | Mesmo fluxo de MU01. | ≤ 3 minutos | Cronometrar após a leitura do enunciado até a confirmação correta, incluindo esperas. Registrar falhas e pedidos de ajuda. | Evitar esforço excessivo na revisão da aula. |
| MU03 | satisfação | média da satisfação pós-tarefa, de 1 a 5 | Personalização, incluindo tentativas sem conclusão. | ≥ 4/5 | Perguntar: “Quão satisfeito você ficou ao realizar esta tarefa?”, de 1 — muito insatisfeito a 5 — muito satisfeito, com justificativa breve. | Considerar a percepção do usuário. |

Serão registrados tamanho da amostra, conclusões e falhas. MU01 e MU02 serão analisadas juntas: rapidez não compensará conclusão insuficiente. Sem conclusões corretas sem ajuda, MU02 não será calculável. O teste-piloto verificará o roteiro e as metas; revisões serão justificadas antes da avaliação principal.

### 3.3 Priorização das metas (se exigida na disciplina)

Se o professor solicitar porcentagens que somem 100%, trate-as como **peso de prioridade**, não como métrica de usabilidade.

| Meta | Peso de prioridade | Justificativa |
|---|---:|---|
| MU01 | 45% | Concluir corretamente e com autonomia é a prioridade do fluxo. |
| MU02 | 30% | O tempo precisa ser compatível com a rotina do docente. |
| MU03 | 25% | A satisfação complementa os dados de conclusão e tempo. |
| **Total** | **100%** | |

## 4. Como o ciclo será iterado

Explique que artefatos serão revisitados após protótipos e avaliações.

Após protótipos e avaliações, a equipe comparará resultados e metas, registrando problemas de navegação, compreensão, acessibilidade e execução.

Conforme as evidências, serão revisitados:

- **Personas, contexto e cenários:** atualizar hipóteses conforme a coleta da Entrega 7 e os testes.
- **HTA, GOMS e CTT:** revisar etapas, alternativas e relações temporais e alinhar os títulos à tarefa descrita, pois o recorte individual ainda contém títulos de configuração do acompanhamento para modelos de personalização pós-aula.
- **Modelo conceitual e protótipos:** ajustar termos, botões, explicações, estados e confirmação das alterações.
- **Metas e plano de avaliação:** revisar procedimentos e justificar alterações, preservando os valores anteriores.

Cada problema será associado à tarefa, à tela, à evidência e à mudança proposta. A matriz deverá relacionar o fluxo de personalização às personas, aos cenários, aos modelos e às metas MU01–MU03, preservando o histórico das decisões. As tarefas afetadas serão avaliadas novamente, e os resultados das Entregas 12–14 alimentarão a rastreabilidade para verificar se houve melhoria.

## Checklist

- [x] Capacidades e restrições têm impacto de IHC explicitado.
- [x] Está claro o limite entre contribuição técnica do TCC e camada interativa da disciplina.
- [x] Resultados/processamento simulados no protótipo foram explicitados.
- [x] Metas de usabilidade avaliam a interação, não substituem métricas técnicas do TCC.
- [x] Normas/princípios estão contextualizados, não apenas copiados.
- [x] Metas quantitativas são mensuráveis e associadas a tarefas/público.
- [x] Eficácia, eficiência e satisfação são consideradas quando pertinentes.
- [x] Metas poderão ser verificadas nas Entregas 12–14.
