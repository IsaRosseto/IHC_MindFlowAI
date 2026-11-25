# Entrega 13 — Avaliação de IHC por inspeção heurística

**Data:** {{dd/mm/aaaa}}  
**Status:** ⬜ Iniciada 
**Responsabilidade:** 1 avaliação completa por integrante, sobre todas as telas/estados relevantes do projeto.

## Objetivo da atividade

Encontrar problemas de usabilidade por inspeção sistemática da interface com as **10 heurísticas de Nielsen**. Cada avaliador trabalha individualmente primeiro; depois a equipe consolida problemas duplicados e prioridades.

> **Parte de violações:** registre somente problemas reais. Não invente uma violação para “preencher” cada heurística. Para provar que todas foram exercitadas, use a **matriz de cobertura H1–H10**. Para heurísticas sem violação, a disciplina solicita um exemplo didático de boa prática.

## 1. Heurísticas adotadas

1. Visibilidade do status do sistema
2. Compatibilidade entre o sistema e o mundo real
3. Controle e liberdade do usuário
4. Consistência e padrões
5. Prevenção de erros
6. Reconhecimento em vez de memorização
7. Flexibilidade e eficiência de uso
8. Estética e design minimalista
9. Ajudar usuários a reconhecer, diagnosticar e recuperar-se de erros
10. Ajuda e documentação

## Cobertura especial para interfaces administrativas e analíticas

Quando existirem, não limite a avaliação às “telas principais”. Inspecione também:

- dashboard em estados normal, vazio e erro;
- filtros sem resultado e filtros combinados;
- relatórios e exportação;
- histórico/listas longas;
- formulários CRUD (criação, edição, exclusão, validação);
- alteração de perfil/permissão;
- confirmações de ações destrutivas;
- processamento/loading/progresso;
- falha e recuperação;
- comparação de resultados;
- mensagens de termos técnicos, métricas e recomendações;
- ajuda/documentação contextual.

Em TCCs técnicos, observe especialmente se a interface comunica o estado do processamento e traduz informações técnicas para o vocabulário do usuário escolhido.

## 2. Escopo da inspeção

| Item | Definição |
|---|---|
| Versão avaliada | MindFlow AI 2.0, conforme identificação da equipe, disponível em [mindflowiaa.netlify.app](https://mindflowiaa.netlify.app/). Inspeção em 18/11/2026; commit não informado. |
| Telas/estados | Página inicial; Minhas reuniões; resumo com dados de demonstração e resumo sem leituras; edição do resumo e do dashboard geral; erro de nome vazio; visualização salva selecionada; confirmação de exclusão cancelada; dashboard geral; comparação normal e sem seleção; configuração/prévia da extensão; suporte. |
| Fluxos | M01: consulta e personalização do resumo pós-aula, incluindo validação e retorno. Também foram percorridos dashboard geral/comparação, configuração da extensão e suporte, descritos pelo nome para não criar códigos MoLIC não documentados. |
| Dispositivo/viewport | Navegador Chrome em computador, ambiente remoto, janela de 1363 × 936 pixels. A inspeção não cobre todas as resoluções nem comprova conformidade de acessibilidade. |
| Avaliadores | A01 — Kayky Pires: registro elaborado com apoio de inspeção assistida e sujeito à revisão do avaliador. A02 — Rafael Dias. A03 — Isabella Rosseto: inspeção a partir da tarefa T03 (pop-up durante a aula e resumo pós-aula), com base nos prints da versão 2.0 e na página pública. Os demais integrantes acrescentarão seus próprios registros após a inspeção individual. |

## 3. Procedimento individual

Cada avaliador deve:

1. percorrer os fluxos/telas ao menos uma vez para familiarização;
2. inspecionar novamente aplicando sistematicamente H1–H10;
3. registrar cada problema com evidência e contexto;
4. atribuir severidade **depois de compreender bem o problema**, justificando a decisão;
5. não discutir achados com os demais antes de terminar a inspeção individual, quando o objetivo for preservar independência.

### Escala de severidade (0–4)

| Grau | Interpretação |
|---:|---|
| 0 | não é considerado problema de usabilidade |
| 1 | problema cosmético; corrigir se houver tempo |
| 2 | problema menor; baixa prioridade |
| 3 | problema maior; alta prioridade |
| 4 | catástrofe de usabilidade; correção imperativa antes de disponibilizar |

Ao justificar, considere **frequência, impacto e persistência** do problema no contexto real de uso.

---

## Avaliador A02 — Rafael Dias

### 4. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 | Página inicial, exemplo de resumo e apresentação de indicadores. | Possível violação. | V05 | — |
| H2 | Dashboard geral, resumo da reunião e explicações dos indicadores. | Sim. | V06 | — |
| H3 | Personalização, cancelamento de edição e confirmação de exclusão. | Não observada no conteúdo examinado. | — | BP07: as operações apresentam opções para cancelar ou voltar antes de confirmar alterações. |
| H4 | Comandos de personalização no dashboard geral e no resumo. | Sim. | V07 | — |
| H5 | Exclusão de reuniões e formulários de cadastro. | Não observada no conteúdo examinado. | — | BP08: a exclusão apresenta confirmação e o cadastro solicita confirmação da senha. |
| H6 | Indicadores percentuais do resumo, dashboard geral e central de ajuda. | Sim. | V08 | — |
| H7 | Comparação de reuniões e personalização de dashboards. | Não observada no conteúdo examinado. | — | BP09: o atalho "Usar as 2 mais recentes" reduz etapas para comparar reuniões. |
| H8 | Página inicial, cards de indicadores e organização dos dashboards. | Não observada no conteúdo examinado. | — | BP10: informações agrupadas em cartões e seções facilitam a localização dos resultados. |
| H9 | Comparação sem reuniões suficientes e validações de formulário. | Não observada no conteúdo examinado. | — | BP11: a comparação informa a necessidade de selecionar pelo menos duas reuniões. |
| H10 | Central de ajuda, explicações dos indicadores e personalização. | Não observada no conteúdo examinado. | — | BP12: a central de ajuda explica as métricas, os gráficos e a interpretação das estimativas. |

### 5. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V05 | H1 | Página inicial, exemplo de resumo da reunião. | A página inicial apresenta indicadores numéricos, como 67% de engajamento, 24 participantes e 2 alertas. No conteúdo examinado, esses números não possuem uma identificação explícita de que representam uma demonstração, podendo gerar dúvidas sobre a origem dos resultados. | Página inicial, seção "Resumo da reunião". Inserir print em `assets/13_heuristica/rafael_v05.png`. | 2 | Pode causar interpretação equivocada no primeiro contato com o sistema, principalmente para usuários novos. Não impede a navegação, mas dificulta distinguir informações ilustrativas de resultados reais. | Identificar claramente os exemplos com uma indicação como "Dados de demonstração" ou "Exemplo de resultado", próxima aos indicadores apresentados. |
| V06 | H2 | Dashboard geral e resumo da reunião. | O sistema apresenta termos como "janelas", "fontes" e "leituras", que podem não ser imediatamente compreendidos pelo instrutor corporativo. Embora sejam explicados na central de ajuda, exigem conhecimento adicional para interpretar os resultados. | Dashboard geral, seção "Volume de dados analisados", e resumo, seção "Leituras do intervalo". Inserir print em `assets/13_heuristica/rafael_v06.png`. | 2 | Os termos aparecem em diferentes partes da análise e podem aumentar o esforço de interpretação. Não impedem a execução das tarefas, mas dificultam a compreensão inicial das informações. | Apresentar explicações próximas aos termos, como "Janela (intervalo analisado)" e "Fontes (vídeos considerados na análise)", mantendo a precisão técnica sem exigir conhecimento prévio. |
| V07 | H4 | Personalização do dashboard geral e do resumo da reunião. | A interface utiliza diferentes expressões para ações semelhantes, como "Personalizar", "Personalizar agora", "Organizar dashboard" e "Montar visualização". Essa diferença pode dificultar o reconhecimento da mesma funcionalidade em contextos distintos. | Dashboard geral e resumo da reunião, nos comandos de personalização. Inserir print em `assets/13_heuristica/rafael_v07.png`. | 2 | A variação de nomes pode gerar hesitação durante a navegação, especialmente para usuários pouco familiarizados com o sistema. Entretanto, os comandos permanecem relacionados à atividade de edição. | Padronizar os comandos principais com uma nomenclatura consistente, como "Personalizar dashboard", mantendo "Salvar visualização" para confirmar as alterações. |
| V08 | H6 | Dashboard geral, resumo da reunião e indicadores percentuais. | O sistema apresenta porcentagens com significados diferentes, como intensidade estimada, parcela de fontes e confiança do modelo. Como essas diferenças são explicadas principalmente na documentação, o usuário pode precisar memorizar o significado de cada medida para interpretar os gráficos e cartões. | Resumo da reunião, gráficos de indicadores e central de ajuda, seção "Por que existem porcentagens diferentes?". Inserir print em `assets/13_heuristica/rafael_v08.png`. | 3 | A interpretação incorreta de uma porcentagem pode comprometer a análise dos resultados e influenciar decisões sobre a condução de treinamentos. O problema pode ocorrer repetidamente durante a consulta aos indicadores. | Identificar diretamente o significado de cada percentual com rótulos como "Intensidade estimada", "Parcela de fontes" e "Confiança da estimativa", disponibilizando explicações próximas aos valores. |

**Qualidade do relato:** os problemas devem ser confirmados com capturas das telas e inspeção visual. Em especial, V05 depende da verificação da sinalização dos dados demonstrativos, e V07 da comparação visual dos comandos nas duas interfaces.

### 6. Boas práticas — heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| H3 | BP07 — As interfaces de edição apresentam comandos para cancelar as alterações, e a exclusão utiliza uma etapa de confirmação. | Personalização e confirmação de exclusão. Inserir print em `assets/13_heuristica/rafael_bp07.png`. | Os controles permitem que o usuário desista de uma operação antes de confirmá-la, mantendo sua liberdade de escolha. O comportamento efetivo do cancelamento ainda deve ser verificado. |
| H5 | BP08 — O cadastro solicita confirmação da senha, e a exclusão de uma reunião apresenta suas consequências antes da confirmação. | Cadastro e confirmação de exclusão. Inserir print em `assets/13_heuristica/rafael_bp08.png`. | Esses mecanismos ajudam a evitar erros de digitação e exclusões acidentais. |
| H7 | BP09 — A comparação entre reuniões oferece o botão "Usar as 2 mais recentes". | Dashboard geral, seção "O que mudou entre as reuniões?". Inserir print em `assets/13_heuristica/rafael_bp09.png`. | O atalho diminui a quantidade de seleções necessárias para realizar uma comparação frequente. |
| H8 | BP10 — Os resultados são organizados em seções e cartões, separando indicadores, gráficos e ferramentas de personalização. | Dashboard geral e resumo da reunião. Inserir print em `assets/13_heuristica/rafael_bp10.png`. | A organização visual ajuda o usuário a localizar informações e distinguir os diferentes grupos de funcionalidades. |
| H9 | BP11 — Na comparação, o sistema informa que é necessário selecionar de duas a quatro reuniões e orienta quando não existem reuniões suficientes. | Dashboard geral, área de comparação. Inserir print em `assets/13_heuristica/rafael_bp11.png`. | A mensagem informa a condição necessária para realizar a tarefa, ajudando o usuário a compreender por que a comparação ainda não está disponível. |
| H10 | BP12 — A central de ajuda apresenta explicações sobre os indicadores, porcentagens, gráficos, alertas e personalização. | Central de ajuda, seção "Entenda seus resultados". Inserir print em `assets/13_heuristica/rafael_bp12.png`. | Oferece documentação relacionada às tarefas do usuário, auxiliando na interpretação dos resultados e no entendimento das funcionalidades. |

### Síntese individual — Rafael Dias

A avaliação A02 registrou **quatro possíveis violações**, relacionadas às heurísticas H1, H2, H4 e H6. Foram atribuídos três problemas de severidade 2 e um problema de severidade 3.

O problema de maior prioridade é **V08**, relacionado à dificuldade de diferenciar os significados das porcentagens apresentadas. Como o MindFlow AI utiliza diferentes tipos de medidas, a interpretação incorreta pode prejudicar a análise dos estados do grupo.

Os demais problemas estão associados à identificação dos dados demonstrativos, ao uso de termos técnicos e à inconsistência de nomenclatura dos comandos de personalização.

Como pontos positivos, destacam-se a presença de opções de cancelamento, a confirmação de operações importantes, os atalhos para comparação de reuniões e a central de ajuda.

O plano de melhoria proposto é:

1. **Alta prioridade — V08:** apresentar o significado de cada percentual diretamente nos indicadores e gráficos.
2. **Baixa prioridade — V06:** adicionar explicações contextuais aos termos técnicos.
3. **Baixa prioridade — V07:** padronizar a nomenclatura dos comandos de personalização.
4. **Baixa prioridade — V05:** identificar explicitamente os resultados utilizados como demonstração.
5. **Antes da consolidação:** verificar visualmente os achados, anexar as evidências e revisar as severidades, quando necessário.

As recomendações apresentadas não indicam correções já implementadas. Os achados devem ser confirmados durante a inspeção individual antes de serem considerados resultados definitivos da equipe.

---

## Avaliador A03 — Isabella Rosseto

**Autor(a):** Isabella Vieira Silva Rosseto — 22.222.036-0  
**Foco da inspeção:** percorri o sistema pela tarefa da Camila (P02, T03, M05): acompanhar a turma pelo pop-up da extensão durante a aula e, depois, consultar e organizar o resumo da reunião.  
**Base da inspeção:** versão 2.0 do MindFlow AI. Usei os prints das telas internas capturados pela equipe entre 18/11 e 22/11/2026 (pastas `assets/11_figma` e `assets/13_heuristica`), a página pública acessada em 25/11/2026 e os textos de mensagens e ajuda do próprio site. Não fiz login no sistema; por isso, os achados que dependem de interação (por exemplo, se o aviso de erro some sozinho) estão marcados para conferência antes da consolidação.

### 4. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 | Minhas reuniões; resumo de reunião sem leituras; cards de indicadores | Sim | V13 | — |
| H2 | Pop-up expandido da extensão; Minhas reuniões; tabela "Leituras do intervalo" | Sim | V09 | — |
| H3 | Pop-up compacto e expandido durante a aula; configuração da extensão | Sim | V16 | — |
| H4 | Exclusão de reunião e exclusão de visualização salva | Sim | V14 | — |
| H5 | Pop-up com estimativa baseada em uma única fonte | Sim | V11 | — |
| H6 | Pop-up compacto e expandido (rótulo do estado) | Sim | V12 | — |
| H7 | Pop-up compacto/expandido; seleção de intervalo no gráfico | Não | — | BP13 |
| H8 | Pop-up compacto durante a aula | Sim | V10 | — |
| H9 | Salvar visualização sem nome | Sim | V15 | — |
| H10 | Gráfico "Evolução da reunião"; central de ajuda | Não | — | BP14 |

### 5. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V09 | H2 | Pop-up expandido da extensão; Minhas reuniões; tabela "Leituras do intervalo" | A interface mostra termos da implementação, que não fazem parte do vocabulário de uma professora: "Python conectado · modelo carregado · alvo 30 fps", "Histórico Supabase: desativado no Python", "IA ATIVA · 13.9 fps reais", "Dados carregados do Supabase" e "dados de v_timeline_sessao". O código da reunião também aparece repetido no cabeçalho do pop-up ("mxc-cswp-ocwmxc-cswp-ocw"). | [Pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png), rodapé e cabeçalho; [Minhas reuniões](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/Captura%20de%20tela%202026-11-22%20204016.png), abaixo de "Reuniões recentes"; [Leituras do intervalo](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/timeline.png) | 2 | Aparece em várias telas, inclusive no pop-up usado durante a aula, mas não impede nenhuma tarefa. O impacto é de compreensão e de confiança: a professora não sabe se precisa fazer algo quando lê "Supabase desativado". | Mostrar essas informações só em uma área de diagnóstico para quem configura o sistema. Para a professora, trocar por mensagens de estado no vocabulário dela, por exemplo "Acompanhamento funcionando" ou "O histórico desta aula não está sendo salvo". |
| V10 | H8 | Pop-up compacto durante a aula | No modo compacto, a área "Conta conectada" com o e-mail e o botão "Sincronizar" ocupa mais espaço do que o estado da turma, que aparece só na parte de baixo, parcialmente visível. A informação que a professora precisa ver de relance fica em segundo plano. | [Pop-up compacto](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f01_popup_compacto.png) | 3 | O modo compacto é o que fica na tela enquanto a professora explica com a tela compartilhada (T03), então o problema aparece em toda aula. Esconder o estado da turma enfraquece justamente o uso principal do Semáforo (H01). | No modo compacto, mostrar primeiro o estado da turma, a confiança e os participantes contribuindo. Mover a conta e a sincronização para o modo expandido ou para um ícone pequeno. |
| V11 | H5 | Pop-up compacto e expandido com uma única fonte | O pop-up mostra "Confusão alto" para o grupo mesmo com "1 fonte(s)" e confiança de 30% a 33%. Não há nenhum aviso de que a base é insuficiente. Com uma única fonte, o "estado do grupo" é, na prática, o estado de uma pessoa. | [Pop-up compacto](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f01_popup_compacto.png) e [pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png) | 3 | Leva a um erro de interpretação com consequência real: a professora pode mudar a aula por causa de uma estimativa fraca, e o resultado deixa de ser agregado, o que entra em conflito com a privacidade dos alunos (H03, H05). Acontece sempre que poucas câmeras estão ligadas, situação comum em turmas pequenas. | Definir um mínimo de participantes (por exemplo, 3) e, abaixo dele, mostrar "Sem estimativa — poucas câmeras ligadas" em vez do estado. Quando a confiança estiver baixa, mostrar isso em texto junto do estado, e não só como número. |
| V12 | H6 | Pop-up compacto e expandido, rótulo do estado | O estado aparece como "Confusão alto →". A seta não tem explicação na tela: a professora precisa lembrar ou descobrir se ela indica tendência, mudança recente ou um link. A cor amarela também não diz, sozinha, se é um alerta. | [Pop-up compacto](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f01_popup_compacto.png) | 1 | Problema pequeno e cosmético: não impede a leitura do estado, mas gera dúvida na primeira vez que aparece. | Trocar a seta por um texto curto ("estável", "subindo", "caindo") ou explicar o símbolo ao passar o mouse. |
| V13 | H1 | Minhas reuniões; resumo de uma reunião sem leituras | Reuniões sem dados mostram "—", "0 participantes", "0 verdes · 0 amarelas · 0 vermelhas" e "Alertas: 0", sem dizer por que não há leituras. Isso pode ser lido como "não houve problema" quando, na verdade, não houve análise. Na mesma lista, uma reunião de 19/10 continua "Em andamento", "sem duração", sem forma de encerrá-la pela lista. | [Minhas reuniões](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/Captura%20de%20tela%202026-11-22%20204016.png), reunião "Sua reunião está pronta" e "Meet: eth-yedb-rxw"; [resumo sem leituras](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/erro%20salvar%20sem%20nome.png), cards de indicadores | 3 | Confundir ausência de dados com valor zero leva a uma conclusão errada sobre a aula, exatamente o que a meta da Entrega 8 pede para evitar. Aparece em todas as reuniões curtas ou sem câmeras. A reunião "em andamento" antiga deixa dúvida sobre o estado real do sistema. | Separar visualmente "sem dados" de "zero": por exemplo, "Nenhuma leitura registrada nesta reunião — as câmeras estavam desligadas ou a análise não foi iniciada". Encerrar ou marcar como "interrompida" a reunião que ficou aberta, com uma ação para resolver. |
| V14 | H4 | Exclusão de reunião e exclusão de visualização salva | Excluir uma reunião abre uma janela do próprio sistema, com título, consequência e botão vermelho. Excluir uma visualização salva usa o diálogo padrão do navegador ("mindflowiaa.netlify.app diz", OK/Cancelar), com outra aparência e sem explicar a consequência. | [Excluir reunião](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/excluir.png) e [excluir visualização](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/info%20excluir%20visualiza%C3%A7%C3%A3o.png) | 1 | As duas ações funcionam e pedem confirmação; a diferença é de padrão visual e de clareza, com baixo impacto. | Usar o mesmo modelo de janela de confirmação nas duas exclusões, dizendo o que será removido ("A visualização 'dsa' será excluída; os dados da reunião continuam salvos"). |
| V15 | H9 | Organizar dashboard, salvar visualização sem nome | Ao salvar sem nome, a mensagem "Dê um nome para a visualização." aparece na parte de baixo da tela, longe do campo "Nome da visualização", que fica no topo e não é destacado. | [Erro ao salvar sem nome](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/erro%20salvar%20sem%20nome.png) | 2 | A mensagem diz o que fazer, mas a professora precisa procurar o campo. Atrapalha pouco e só nessa situação. A confirmar na interação: se o aviso desaparece sozinho, o impacto aumenta. | Mostrar a mensagem logo abaixo do campo, destacar a borda do campo e colocar o cursor nele. |
| V16 | H3 | Pop-up compacto e expandido durante a aula | Nos prints do pop-up não aparece nenhum controle para pausar ou parar o acompanhamento. Pelo que vi, iniciar e encerrar ficam na página "Extensão" do site, fora da videochamada. Durante a aula, a professora não tem uma saída rápida se o acompanhamento atrapalhar. | [Pop-up compacto](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f01_popup_compacto.png) e [pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png); botões "Iniciar análise" e "Encerrar reunião" no texto da página do site | 2 | A professora não fica presa (ela pode fechar o pop-up ou ir ao site), mas a saída é lenta justamente no momento em que ela está apresentando. A confirmar no pop-up real se existe um controle fora da área capturada. | Colocar no pop-up um botão "Pausar acompanhamento", com aviso aos participantes, como previsto em RC07 e no MoLIC M05. |

**Qualidade do relato:** V15 e V16 dependem de interação que não consegui repetir sem login. Antes da consolidação, é preciso conferir no sistema se o aviso de V15 desaparece sozinho e se o pop-up tem algum controle de pausa fora da área capturada (V16).

### 6. Boas práticas — heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| H7 | BP13 — O pop-up tem dois modos: compacto, para acompanhar de relance, e expandido, com os quatro indicadores e o gráfico dos últimos cinco minutos. No resumo, o botão "Reunião inteira" volta ao intervalo completo depois de selecionar um trecho. | [Pop-up compacto](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f01_popup_compacto.png), [pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png) | A mesma informação atende quem quer só uma olhada durante a aula e quem quer detalhes, sem obrigar todo mundo ao caminho mais longo. |
| H10 | BP14 — O gráfico "Evolução da reunião" explica na própria tela como ler os dados: "As linhas mostram a intensidade estimada de cada indicador, não a porcentagem de pessoas". A central de ajuda complementa com "Como ler o gráfico" e "Qual é exatamente a regra do alerta?". | [Gráfico](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/graf.png), [central de ajuda](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/suporte.png) | A ajuda aparece no lugar onde a dúvida surge, e não só em uma página separada, e é escrita para a tarefa de interpretar o resultado. |

### Síntese individual — Isabella Rosseto

Registrei **oito violações** (V09 a V16), uma em cada heurística H1, H2, H3, H4, H5, H6, H8 e H9. H7 e H10 não tiveram violação e receberam exemplos de boa prática (BP13 e BP14).

| Severidade | Achados |
|---:|---|
| 3 | V10, V11, V13 |
| 2 | V09, V15, V16 |
| 1 | V12, V14 |

O padrão que mais se repete é o **uso durante a aula**. O pop-up, que deveria ser lido de relance enquanto a professora explica, mostra informações de conta e de implementação na frente do estado da turma (V09, V10). Ele também apresenta como "estado do grupo" uma estimativa feita com uma única fonte (V11) e não oferece um jeito rápido de pausar (V16). Depois da aula, o problema mais sério é confundir ausência de dados com valor zero (V13).

Plano de melhoria proposto:

1. **Antes do teste com usuários (alta prioridade):** V11 (mínimo de participantes e aviso de base insuficiente), V10 (estado da turma em primeiro plano no modo compacto) e V13 (diferenciar "sem dados" de "zero"). Os três afetam diretamente as tarefas UT01 e UT02 da Entrega 12.
2. **Prioridade média:** V16 (pausar pelo pop-up), V09 (tirar termos técnicos da visão da professora) e V15 (mensagem junto do campo).
3. **Baixa prioridade:** V12 (significado da seta) e V14 (padronizar a confirmação de exclusão).

Na consolidação, V09 se aproxima de V06 (Rafael), porque ambos tratam de termos técnicos, mas em telas diferentes. As recomendações acima são propostas e ainda não foram implementadas.

---
> Repita a seção para A02, A03... um avaliador por integrante.
---
## 7. Consolidação da equipe

Problemas iguais ou muito semelhantes encontrados por avaliadores diferentes devem ser consolidados, preservando quem os encontrou.

| ID consolidado | Achados individuais | Heurística | Problema | Severidade final | Prioridade | Responsável pela correção |
|---|---|---|---|---:|---|---|
| HC01 | V01(A01), V04(A02) | H1 | {{...}} | {{...}} | alta | {{...}} |

## 8. Síntese e plano de melhoria

- Quantidade de problemas por heurística e severidade.
- Problemas críticos/graves que bloqueiam teste ou release.
- Padrões recorrentes entre telas.
- Correções que serão feitas antes/para a avaliação com usuários.

## Checklist

- [ ] Cada integrante fez uma inspeção completa e identificada.
- [ ] Todas as telas/estados relevantes foram examinados.
- [ ] Estados administrativos, filtros, relatórios, históricos, processamento e erros foram incluídos quando existentes.
- [ ] A inspeção avaliou a interface/protótipo, não o mérito técnico do algoritmo/modelo.
- [ ] H1–H10 aparecem na matriz de cobertura de cada avaliador.
- [ ] Parte de violações contém apenas violações, sem “forçar” exemplos.
- [ ] Todo problema tem print/localização e contexto.
- [ ] Severidade possui justificativa, não apenas número.
- [ ] Recomendação resolve a causa ou reduz o impacto.
- [ ] Achados duplicados foram consolidados ao final.
