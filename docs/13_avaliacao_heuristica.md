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
## Avaliador A01 — Kayky Pires

### 4. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 | Lista de reuniões, resumo sem leituras, gráfico geral, comparação e exportação. | Sim. | V01. | — |
| H2 | Lista, tabela de leituras, explicações dos indicadores e suporte. | Sim. | V02. | — |
| H3 | Edição do resumo, cancelamento e confirmação de exclusão de visualização salva. | Não observada no recorte. | — | BP01: cancelar a edição restaurou o estado anterior; cancelar a confirmação manteve a visualização. |
| H4 | Textos de Minhas reuniões e da configuração/prévia da extensão, comparados ao suporte ampliado da versão 2.0 informado pela equipe. | Sim. | V03. | — |
| H5 | Tentativas de salvar sem nome no resumo e no dashboard geral; confirmação de exclusão. | Não observada no recorte. | — | BP02: nome vazio gera validação e a exclusão de uma visualização salva exige confirmação. |
| H6 | Seletores de visualização, opções de blocos e preferências da extensão. | Não observada no recorte. | — | BP03: nomes e seleções ficam visíveis, incluindo a visualização ativa. |
| H7 | Lista extensa de reuniões e controles de organização dos dashboards. | Sim. | V04. | — |
| H8 | Organização visual do resumo, cards, gráficos, edição e prévia da extensão. | Não observada no recorte. | — | BP04: títulos, agrupamentos e rótulos textuais distinguem indicadores e ações. |
| H9 | Mensagens de nome vazio e comparação sem seleção suficiente. | Não observada no recorte. | — | BP05: mensagens descrevem o que falta para prosseguir. |
| H10 | Botão de ajuda, central de suporte, explicações de indicadores e preferências da extensão. | Não observada no recorte definido. | — | BP06: a central explica intensidade, parcela do grupo e confiança, além da personalização. |

### 5. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H1 | Resumo sem leituras e gráfico de engajamento por reunião no dashboard geral. | A mesma reunião apresenta “—” e zero janelas no resumo, mas aparece como 0% no gráfico geral e na seleção para comparação. O docente pode interpretar ausência de dados como baixo engajamento. | https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/13_heuristica/Captura%20de%20tela%202026-11-22%20204016.png | 3 | O problema reaparece para reuniões sem leituras e persiste enquanto forem representadas como zero. O impacto é alto: pode orientar uma interpretação incorreta dos resultados, embora não bloqueie a navegação. | Diferenciar valor zero de informação indisponível em todas as telas. Usar “Sem dados” ou “—”, com explicação, sem representar ausência como 0%. Conferir também a apresentação na comparação e exportação. |
| V02 | H2 | Minhas reuniões e tabela “Leituras do intervalo” no resumo. | São exibidos nomes internos como “Supabase”, sem necessidade para a análise docente. Esses termos exigem conhecimento técnico que não faz parte da tarefa. |https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/13_heuristica/supabase.png | 2 | Os termos aparecem em telas de consulta recorrente e permanecem durante a leitura. Não impedem a tarefa, mas acrescentam esforço de interpretação e podem gerar dúvidas sobre a origem dos dados. | Utilizar linguagem da atividade, como “Reuniões disponíveis” e “Leituras do período selecionado”. Manter detalhes internos em documentação técnica. |
| V03 | H4 | Orientações de Minhas reuniões e da configuração/prévia da extensão. | A versão 2.0 possui funcionamento ampliado para outros sites de reunião, conforme informado pela equipe, mas as orientações ainda citam somente Google Meet, como em “Como ficará no Meet”. Isso comunica um alcance mais restrito que o informado para a versão. | https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/13_heuristica/Captura%20de%20tela%202026-11-22%20204016.png | 2 | A orientação desatualizada aparece no acesso à configuração e pode levar o docente a supor incompatibilidade com outra plataforma. O funcionamento não foi bloqueado nesta inspeção, mas a dúvida permanece até o texto ser atualizado. | Atualizar as instruções para a plataforma selecionada ou usar “plataforma de reunião”. Informar os sites efetivamente suportados pela versão, sem listar compatibilidades ainda não verificadas. |
| V04 | H7 | Histórico de Minhas reuniões com muitos registros. | A lista extensa não apresenta busca por título ou filtros por data e situação. Para localizar uma reunião antiga, o docente precisa percorrer os registros visualmente. |https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/13_heuristica/Captura%20de%20tela%202026-11-22%20204016.png 2 | A dificuldade tende a aumentar conforme o histórico cresce e se repete a cada procura. A reunião pode ser encontrada pela rolagem, mas o caminho exige mais esforço, principalmente com títulos semelhantes. | Disponibilizar busca por título e filtros de período e situação, mantendo a seleção atual visível e oferecendo opção para limpar os filtros. |

**Qualidade do relato:** o problema deve ser observável e localizado. Evite “interface confusa” sem dizer **o que**, **onde**, **quando** e **para quem**.

### 6. Boas práticas — heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| H3 | BP01 — Cancelar a edição restaurou a visualização anterior. Cancelar a confirmação de exclusão manteve a visualização salva. | https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/13_heuristica/excluir%20person.png | Oferece saída da operação e mantém o controle com o usuário. Cancelar a edição e confirmar uma exclusão são comportamentos distintos. |
| H5 | BP02 — Salvar sem nome exibiu validação; excluir uma visualização salva apresentou confirmação com seu nome. | https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/13_heuristica/sem%20nome.png | A validação evita uma configuração sem identificação e a confirmação reduz exclusões acidentais. Foi verificado o cancelamento, sem executar a exclusão definitiva. |
| H6 | BP03 — A visualização ativa aparece no seletor; blocos e preferências apresentam opções e seleções visíveis. | https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/13_heuristica/blocos%20view.png | Permite reconhecer a configuração atual e as possibilidades disponíveis sem memorizar uma sequência de comandos. |
| H8 | BP04 — O resumo utiliza títulos, cards agrupados, legendas e rótulos para separar indicadores e ações. | https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/13_heuristica/graf.png | A hierarquia visual ajuda a localizar e distinguir informações. Esta observação não representa uma medição de contraste ou certificação de acessibilidade. |
| H9 | BP05 — A tentativa de salvar sem nome exibiu “Dê um nome para a visualização”; a comparação sem seleção pediu pelo menos duas reuniões. |https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/13_heuristica/sem%20nome.png | As mensagens apontam a condição que falta e indicam como prosseguir, sem depender de códigos técnicos. |
| H10 | BP06 — A central de ajuda explica os indicadores, seus limites e como personalizar a visualização. |https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/13_heuristica/suporte.png | Oferece explicações ligadas às dúvidas da tarefa, incluindo que confiança não equivale à precisão comprovada da IA. |


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
**Versão:** MindFlow AI 2.0 (site e extensão)  
**Data:** 25/11/2026  
**Foco da inspeção:** percorri o sistema pela tarefa da Camila (P02, T03, M05): acompanhar a turma pelo pop-up da extensão durante a aula e, depois, consultar e organizar o resumo da reunião.  
**Estados especiais examinados:** pop-up compacto e expandido (ao vivo); reunião em andamento; reunião sem leituras (estado vazio); erro ao salvar sem nome; confirmação de exclusão de reunião e de visualização; seleção de intervalo no gráfico; central de ajuda; mensagem de falha de carregamento na página inicial.  

### 4. Matriz de cobertura das 10 heurísticas

| H | Heurística | Fluxos/telas examinados | Violação? | IDs das violações | Boas práticas observadas |
|---:|---|---|---|---|---|
| 1 | Visibilidade do status do sistema | Pop-up ao vivo; Minhas reuniões; resumo sem leituras | sim | V13 | BP13 |
| 2 | Compatibilidade sistema–mundo real | Pop-up expandido; Minhas reuniões; tabela "Leituras do intervalo"; central de ajuda | sim | V09 | BP14 |
| 3 | Controle e liberdade do usuário | Pop-up durante a aula; Organizar dashboard; seleção de intervalo | sim | V16 | BP15 |
| 4 | Consistência e padrões | Pop-up × gráfico do resumo; exclusões; lista de reuniões | sim | V14, V17 | BP16 |
| 5 | Prevenção de erros | Pop-up com uma fonte; exclusão de reunião | sim | V11 | BP17 |
| 6 | Reconhecimento em vez de memorização | Rótulo do estado no pop-up; Organizar dashboard; legenda do gráfico | sim | V12 | BP18 |
| 7 | Flexibilidade e eficiência de uso | Pop-up compacto/expandido; seleção de intervalo | não | — | BP19 |
| 8 | Estética e design minimalista | Pop-up compacto; Minhas reuniões | sim | V10 | BP20 |
| 9 | Reconhecer, diagnosticar e recuperar erros | Salvar sem nome; falha de carregamento na página inicial | sim | V15 | BP21 |
| 10 | Ajuda e documentação | Gráfico "Evolução da reunião"; central de ajuda | não | — | BP22 |

### 5. Análise por heurística

Para cada heurística, registro o que o sistema **atende** e o que **viola**, sempre a partir da tarefa da professora durante e depois da aula.

**H1 — Visibilidade do status do sistema.** *Atende:* o pop-up indica "AO VIVO" e "últimos 5 minutos" no gráfico, e a lista de reuniões mostra o estado de cada uma com selos ("Concluída", "Em andamento") (BP13). *Viola:* uma reunião sem leituras aparece com "0 alertas" e "0 verdes · 0 amarelas · 0 vermelhas", como se nada tivesse acontecido, sem dizer que não houve análise; e uma reunião de 19/10 continua "Em andamento" (V13).

**H2 — Compatibilidade entre o sistema e o mundo real.** *Atende:* a central de ajuda e a página inicial falam com a professora no vocabulário dela ("perceber mudanças no envolvimento do grupo", "decidir se vale adaptar o ritmo"), e o pop-up avisa que "nenhum nome de participante é coletado" (BP14). *Viola:* o pop-up e o site mostram termos de implementação, como "Python conectado", "Supabase", "v_timeline_sessao" e "fps" (V09).

**H3 — Controle e liberdade do usuário.** *Atende:* a organização do dashboard tem "Cancelar" e o "×" para fechar sem salvar, e o botão "Reunião inteira" desfaz a seleção de um trecho do gráfico (BP15). *Viola:* durante a aula, o pop-up não mostra uma forma de pausar o acompanhamento; a saída fica no site, fora da videochamada (V16).

**H4 — Consistência e padrões.** *Atende:* cada reunião da lista segue o mesmo padrão (data, título, estado, resultado e "Ver resumo"), o que facilita percorrer o histórico (BP16). *Viola:* as cores dos indicadores mudam entre o pop-up e o resumo (V17), e as duas exclusões usam janelas de confirmação diferentes (V14).

**H5 — Prevenção de erros.** *Atende:* excluir uma reunião mostra "Ação permanente", diz o que será removido e usa um botão vermelho separado do "Cancelar" (BP17). *Viola:* o pop-up apresenta como estado do grupo uma estimativa feita com uma única fonte, o que favorece uma interpretação errada (V11).

**H6 — Reconhecimento em vez de memorização.** *Atende:* em "Organizar dashboard", todos os blocos disponíveis aparecem listados pelo nome, com caixa de seleção; e o gráfico tem legenda com as cores de cada indicador, de alerta e de anotação (BP18). *Viola:* a seta em "Confusão alto →" não é explicada na tela, e a professora precisa lembrar o que ela significa (V12).

**H7 — Flexibilidade e eficiência de uso.** *Atende:* o pop-up tem modo compacto e expandido, e no resumo dá para selecionar um trecho do gráfico e voltar à reunião inteira com um clique (BP19). *Viola:* não encontrei violação.

**H8 — Estética e design minimalista.** *Atende:* a lista "Minhas reuniões" é limpa, com uma ação principal por linha e as informações secundárias em texto menor (BP20). *Viola:* no pop-up compacto, a conta e o botão "Sincronizar" ocupam mais espaço do que o estado da turma, que é o que a professora precisa ver de relance (V10).

**H9 — Reconhecer, diagnosticar e recuperar-se de erros.** *Atende:* quando o carregamento falha, a página inicial explica a causa e o que fazer ("A biblioteca do Supabase não carregou. Confira sua internet."), e o erro ao salvar sem nome diz exatamente o que falta ("Dê um nome para a visualização.") (BP21). *Viola:* esse aviso aparece longe do campo de nome, que não é destacado (V15).

**H10 — Ajuda e documentação.** *Atende:* o gráfico explica na própria tela como ler as linhas ("intensidade estimada de cada indicador, não a porcentagem de pessoas"), e a central de ajuda tem respostas por tarefa, como "Como ler o gráfico?" e "Qual é exatamente a regra do alerta?" (BP22). *Viola:* não encontrei violação.

### 6. Declaração de violações

Registrei apenas problemas reais. Escala de severidade de 0 a 4 (seção 3).

| ID | H | Tela/estado | Ação/condição | Problema | Consequência | Evidência | Severidade | Justificativa | Recomendação |
|---|---|---|---|---|---|---|---:|---|---|
| V09 | H2 | Pop-up expandido; Minhas reuniões; "Leituras do intervalo" | Professora abre o pop-up durante a aula ou consulta a lista e o resumo depois | Aparecem termos de implementação: "Python conectado · modelo carregado · alvo 30 fps", "Histórico Supabase: desativado no Python", "IA ATIVA · 13.9 fps reais", "Dados carregados do Supabase", "dados de v_timeline_sessao"; o código da reunião aparece repetido no cabeçalho do pop-up | A professora não sabe se precisa fazer algo ao ler "Supabase desativado" e perde confiança no sistema | [Pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png); [Minhas reuniões](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/Captura%20de%20tela%202026-11-22%20204016.png); [Leituras do intervalo](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/timeline.png) | 2 | Aparece em várias telas, inclusive no pop-up da aula, mas não impede nenhuma tarefa | Deixar essas informações em uma área de diagnóstico e mostrar à professora mensagens como "Acompanhamento funcionando" ou "O histórico desta aula não está sendo salvo" |
| V10 | H8 | Pop-up compacto | Professora acompanha a turma de relance enquanto explica com a tela compartilhada | A área "Conta conectada", com e-mail e "Sincronizar", ocupa mais espaço do que o estado da turma, que fica parcialmente visível embaixo | A informação principal fica em segundo plano no momento em que ela mais precisa | [Pop-up compacto](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f01_popup_compacto.png) | 3 | Acontece em toda aula, no modo usado durante a explicação (T03), e enfraquece o uso principal do Semáforo (H01) | No modo compacto, mostrar primeiro estado, confiança e participantes contribuindo; mover conta e sincronização para o modo expandido |
| V11 | H5 | Pop-up compacto e expandido | Poucas câmeras ligadas (no print, 1 fonte) | O pop-up mostra "Confusão alto" como estado do grupo, com confiança de 30% a 33%, sem avisar que a base é insuficiente | A professora pode mudar a aula por causa de uma estimativa fraca; com uma fonte, o "grupo" é uma pessoa, o que fere a privacidade (H03, H05) | [Pop-up compacto](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f01_popup_compacto.png); [pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png) | 3 | Erro de interpretação com consequência real, frequente em turmas pequenas | Definir um mínimo de participantes (por exemplo, 3) e, abaixo dele, mostrar "Sem estimativa — poucas câmeras ligadas"; com confiança baixa, avisar em texto junto do estado |
| V12 | H6 | Pop-up, rótulo do estado | Professora lê o estado de relance | "Confusão alto →": a seta não tem explicação e a cor amarela não diz sozinha se é alerta | Dúvida na primeira vez que aparece | [Pop-up compacto](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f01_popup_compacto.png) | 1 | Cosmético; não impede a leitura do estado | Trocar a seta por "estável", "subindo" ou "caindo", ou explicar ao passar o mouse |
| V13 | H1 | Minhas reuniões; resumo sem leituras | Professora abre uma reunião curta ou sem câmeras ligadas | Aparecem "—", "0 participantes", "0 verdes · 0 amarelas · 0 vermelhas" e "Alertas: 0", sem explicar por que não há leituras; uma reunião de 19/10 continua "Em andamento", "sem duração" | "Sem dados" é lido como "não houve problema na aula"; o estado real do sistema fica em dúvida | [Minhas reuniões](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/Captura%20de%20tela%202026-11-22%20204016.png); [resumo sem leituras](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/erro%20salvar%20sem%20nome.png) | 3 | Leva a uma conclusão errada sobre a aula, justamente o que a Entrega 8 pede para evitar | Mostrar "Nenhuma leitura registrada nesta reunião — as câmeras estavam desligadas ou a análise não foi iniciada"; marcar como "interrompida" a reunião que ficou aberta |
| V14 | H4 | Exclusão de reunião × exclusão de visualização | Professora exclui uma visualização salva | A reunião usa janela do sistema, com título e consequência; a visualização usa o diálogo padrão do navegador ("mindflowiaa.netlify.app diz") | Padrões diferentes para a mesma ação, e a segunda não diz o que acontece com os dados | [Excluir reunião](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/excluir.png); [excluir visualização](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/info%20excluir%20visualiza%C3%A7%C3%A3o.png) | 1 | As duas pedem confirmação; o impacto é pequeno | Usar a mesma janela nas duas exclusões, dizendo o que será removido |
| V15 | H9 | Organizar dashboard | Professora tenta salvar sem dar nome à visualização | O aviso "Dê um nome para a visualização." aparece na parte de baixo da tela, longe do campo de nome, que não é destacado | Ela precisa procurar o campo para corrigir | [Erro ao salvar sem nome](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/erro%20salvar%20sem%20nome.png) | 2 | A mensagem diz o que fazer, mas a correção demora; a conferir na interação se o aviso some sozinho | Mostrar a mensagem embaixo do campo, destacar a borda e colocar o cursor nele |
| V16 | H3 | Pop-up durante a aula | O acompanhamento atrapalha a aula e a professora quer pausar | Nos prints não aparece controle para pausar ou parar; iniciar e encerrar ficam na página "Extensão" do site | A saída é lenta justamente enquanto ela apresenta | [Pop-up compacto](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f01_popup_compacto.png); [pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png) | 2 | Não prende a professora (ela pode ir ao site), mas atrasa; a conferir se há controle fora da área capturada | Colocar "Pausar acompanhamento" no pop-up, com aviso aos participantes (RC07, MoLIC M05) |
| V17 | H4 | Pop-up expandido × gráfico "Evolução da reunião" | Professora compara o que viu ao vivo com o resumo depois da aula | As cores dos indicadores mudam: no pop-up, tédio é vermelho e frustração é roxa; no resumo, tédio é azul e frustração é vermelha | Ela pode associar a cor ao indicador errado ao passar do pop-up para o resumo | [Pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png), legenda do gráfico; [gráfico do resumo](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/graf.png), legenda | 2 | Os rótulos estão escritos, então o erro é evitável, mas a cor é o atalho de leitura usado de relance | Usar a mesma cor para cada indicador na extensão e no site |

**Qualidade do relato:** V15 e V16 dependem de interação que não consegui repetir sem login. Antes da consolidação, é preciso conferir no sistema se o aviso de V15 desaparece sozinho e se o pop-up tem algum controle de pausa fora da área capturada (V16).

### 6.1 Boas práticas observadas

Registro uma boa prática para cada heurística, inclusive nas que também tiveram violação, para mostrar o que deve ser mantido.

| ID | H | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|---|
| BP13 | H1 | O pop-up mostra "AO VIVO" e "últimos 5 minutos"; a lista de reuniões mostra "Concluída" ou "Em andamento" | [Pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png); [Minhas reuniões](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/Captura%20de%20tela%202026-11-22%20204016.png) | A professora sabe se está vendo dados atuais e em que situação cada reunião está |
| BP14 | H2 | A ajuda e a página inicial usam a linguagem de quem apresenta ("perceber mudanças no envolvimento do grupo"); o pop-up avisa "Nenhum nome de participante é coletado" | [Central de ajuda](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/suporte.png); [pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png) | Fala do objetivo da professora, e não do funcionamento do modelo |
| BP15 | H3 | "Cancelar" e "×" em Organizar dashboard; "Reunião inteira" desfaz a seleção de um trecho | [Organizar dashboard](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/erro%20salvar%20sem%20nome.png) | Ela pode experimentar e desistir sem consequência |
| BP16 | H4 | Todas as linhas de "Minhas reuniões" seguem o mesmo padrão: data, título, estado, resultado e "Ver resumo" | [Minhas reuniões](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/Captura%20de%20tela%202026-11-22%20204016.png) | Depois de entender uma linha, a professora entende todas |
| BP17 | H5 | A exclusão de reunião avisa "Ação permanente", diz o que será removido e separa "Cancelar" de "Excluir reunião" | [Excluir reunião](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/excluir.png) | Evita apagar o histórico de uma aula por engano |
| BP18 | H6 | Em "Organizar dashboard", os blocos aparecem listados pelo nome, com caixa de seleção; o gráfico tem legenda de cores, alerta e anotação | [Organizar dashboard](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/erro%20salvar%20sem%20nome.png); [gráfico](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/graf.png) | A professora escolhe o que vê na tela, sem precisar lembrar o nome dos blocos |
| BP19 | H7 | Pop-up compacto e expandido; seleção de trecho no gráfico com volta rápida para "Reunião inteira" | [Pop-up compacto](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f01_popup_compacto.png); [pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png) | Atende quem quer só uma olhada e quem quer detalhes, sem obrigar todo mundo ao caminho mais longo |
| BP20 | H8 | "Minhas reuniões" tem uma ação principal por linha e informações secundárias em texto menor | [Minhas reuniões](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/Captura%20de%20tela%202026-11-22%20204016.png) | Pouca informação competindo pela atenção na hora de escolher a aula |
| BP21 | H9 | "A biblioteca do Supabase não carregou. Confira sua internet." na página inicial; "Dê um nome para a visualização." ao salvar sem nome | Página inicial (25/11/2026); [erro ao salvar sem nome](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/erro%20salvar%20sem%20nome.png) | As mensagens dizem o que aconteceu e o que fazer, em linguagem simples |
| BP22 | H10 | O gráfico explica na própria tela como ler as linhas; a central de ajuda tem "Como ler o gráfico?" e "Qual é exatamente a regra do alerta?" | [Gráfico](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/graf.png); [central de ajuda](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/suporte.png) | A ajuda aparece onde a dúvida surge e é escrita para a tarefa de interpretar o resultado |

### Síntese individual — Isabella Rosseto

Analisei as **10 heurísticas**. Encontrei **nove violações** (V09 a V17) em oito delas; H7 e H10 não tiveram violação. Registrei também **dez boas práticas** (BP13 a BP22), uma por heurística, para indicar o que deve ser mantido nas próximas versões.

| Severidade | Achados | Heurísticas |
|---:|---|---|
| 3 | V10, V11, V13 | H8, H5, H1 |
| 2 | V09, V15, V16, V17 | H2, H9, H3, H4 |
| 1 | V12, V14 | H6, H4 |

O padrão que mais se repete é o **uso durante a aula**. O pop-up, que deveria ser lido de relance enquanto a professora explica:

- mostra informações de conta e de implementação na frente do estado da turma (V09, V10);
- apresenta como "estado do grupo" uma estimativa feita com uma única fonte (V11);
- não oferece um jeito rápido de pausar (V16);
- usa cores diferentes das do resumo (V17).

Depois da aula, o problema mais sério é confundir ausência de dados com valor zero (V13).

Por outro lado, o sistema já tem pontos fortes que devem ser mantidos: a confirmação de exclusão de reunião (BP17), a explicação do gráfico na própria tela (BP22), os dois modos do pop-up (BP19) e o padrão da lista de reuniões (BP16).

Plano de melhoria proposto:

1. **Antes do teste com usuários (alta prioridade):** V11, V10 e V13. Os três afetam diretamente as tarefas UT01 e UT02 da Entrega 12.
2. **Prioridade média:** V17 (mesmas cores na extensão e no site), V16 (pausar pelo pop-up), V09 (tirar termos técnicos da visão da professora) e V15 (mensagem junto do campo).
3. **Baixa prioridade:** V12 (significado da seta) e V14 (padronizar a confirmação de exclusão).

Na consolidação, V09 se aproxima de V06 (Rafael), porque ambos tratam de termos técnicos, mas em telas diferentes. As recomendações são propostas e ainda não foram implementadas.

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
