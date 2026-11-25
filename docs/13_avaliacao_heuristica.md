# Entrega 13 — Avaliação de IHC por inspeção heurística

**Data:** 25/11/2026  
**Status:** 🟩 concluída  
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
| Avaliadores | A01 — Kayky Pires: registro elaborado com apoio de inspeção assistida e sujeito à revisão do avaliador. A02 — Rafael Dias. A03 — Isabella Rosseto: inspeção a partir da tarefa T03 (pop-up durante a aula e resumo pós-aula), com base nos prints da versão 2.0 e na página pública. A04 — Gustavo Bertoluzzi: inspeção pela ótica da privacidade e da transparência (P05, C03, T04), com base nos prints da versão 2.0. A04 — Gustavo Bertoluzzi. A05 — Matheus Ferreira de Freitas: inspeção pela ótica da persona P04 (reunião comercial B2B, CI01/M01), ao vivo nas páginas públicas e na estrutura e nos textos de todas as telas em 20/11/2026, e pelos prints da versão 2.0 do repositório. |

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

## Avaliador A04 — Gustavo Bertoluzzi

**Autor(a):** Gustavo Bertoluzzi Cardoso — 22.123.016-2  
**Versão:** MindFlow AI 2.0 (site e extensão)  
**Data:** 25/11/2026  
**Foco da inspeção:** percorri o sistema pela ótica da privacidade e da transparência, que vem da persona P05 (Bruno), do cenário C03 e da tarefa T04. Como o Bruno não tem tela própria na versão 2.0, avaliei como o sistema comunica ao docente, e por meio dele aos participantes, o que é processado, quem entra na estimativa e o que é guardado. Também conferi se o resultado continua agregado em todas as telas (R04).  
**Estados especiais examinados:** pop-up compacto e expandido com uma fonte analisada e uma ignorada; página "Extensão" (preferências do painel, prévia "Como ficará no Meet" e quadro de privacidade); Minhas reuniões com reunião em andamento e reunião sem leituras; tabela "Leituras do intervalo"; cards do dashboard geral com a explicação do alerta; central de ajuda.  
**Limitação:** a inspeção foi feita sobre os prints da versão 2.0 guardados no repositório (pastas `assets/06_prototipos`, `assets/11_figma` e `assets/13_heuristica`), sem interação ao vivo com o sistema. O fluxo de início do acompanhamento na extensão não aparece nos prints, então os achados sobre o aviso aos participantes (V18) precisam ser confirmados nesse fluxo antes da consolidação.

### 4. Matriz de cobertura das 10 heurísticas

| H | Heurística | Fluxos/telas examinados | Violação? | IDs das violações | Boas práticas observadas |
|---:|---|---|---|---|---|
| 1 | Visibilidade do status do sistema | Pop-up compacto e expandido; prévia "Como ficará no Meet"; Minhas reuniões | sim | V18, V21 | BP23 |
| 2 | Compatibilidade sistema–mundo real | Minhas reuniões; card "Participantes analisados"; descrições das preferências da extensão | sim | V22 | BP24 |
| 3 | Controle e liberdade do usuário | Preferências da extensão | não | — | BP25 |
| 4 | Consistência e padrões | Mensagens de privacidade do pop-up, da página "Extensão" e do quadro de privacidade; nomes das quatro reações em todas as telas | sim | V19 | BP26 |
| 5 | Prevenção de erros | Pop-up expandido (fonte do apresentador) | não | — | BP27 |
| 6 | Reconhecimento em vez de memorização | Página "Extensão" com prévia em tempo real | não | — | BP28 |
| 7 | Flexibilidade e eficiência de uso | Exibição fixa ou ao passar o mouse para cada informação da extensão | não | — | BP29 |
| 8 | Estética e design minimalista | Pop-up expandido, lista "Fontes anônimas detectadas" | sim | V20 | BP30 |
| 9 | Reconhecer, diagnosticar e recuperar erros | Erro ao salvar visualização sem nome | não | — | BP31 |
| 10 | Ajuda e documentação | Ícones (i) do dashboard geral; central de ajuda | não | — | BP32 |

### 5. Análise por heurística

**H1 — Visibilidade do status do sistema.** *Atende:* o pop-up mostra junto do estado a base da estimativa ("Confiança: 33% · 1 fonte(s)") e separa fontes analisadas e ignoradas (BP23). *Viola:* nas telas examinadas, só o docente sabe que a análise está ativa; nada indica isso a quem tem a imagem analisada (V18). A prévia permite esconder a confiança do estado, que aparece sozinho como "Engajamento alto" (V21).

**H2 — Compatibilidade entre o sistema e o mundo real.** *Atende:* as preferências da extensão são descritas pelo efeito, e não pela implementação ("Mostra se o engajamento subiu, caiu ou ficou estável") (BP24). *Viola:* "45 participantes" e "Participantes analisados: 45" somam participações de várias reuniões como se fossem pessoas, e "analisados" é justamente o termo que reforça a sensação de vigilância (V22).

**H3 — Controle e liberdade do usuário.** *Atende:* a página "Extensão" tem "Restaurar padrão", que desfaz as mudanças de preferência (BP25). *Viola:* não encontrei violação no recorte. A falta de pausa no pop-up, que também seria H3, já foi registrada por Isabella (V16).

**H4 — Consistência e padrões.** *Atende:* as quatro reações aparecem com os mesmos nomes e na mesma ordem no pop-up, na prévia, na tabela de leituras e no gráfico (BP26). *Viola:* as mensagens de privacidade mudam de tela para tela e prometem coisas diferentes (V19).

**H5 — Prevenção de erros.** *Atende:* o pop-up reconhece a imagem do próprio apresentador ("APRESENTADOR DETECTADO") e a deixa fora da estimativa ("1 ignorada(s)"), o que evita que o rosto do docente distorça o estado do grupo (BP27). *Viola:* não encontrei violação nova. A estimativa com uma única fonte, que também é um problema de privacidade, já está registrada em V11 (Isabella).

**H6 — Reconhecimento em vez de memorização.** *Atende:* a prévia "Como ficará no Meet" mostra na hora o efeito de cada escolha, sem que o docente precise lembrar o que cada opção faz (BP28). *Viola:* não encontrei violação.

**H7 — Flexibilidade e eficiência de uso.** *Atende:* cada informação da extensão pode ficar fixa ou aparecer só ao passar o mouse, o que deixa o docente regular quanta informação vê durante a aula (BP29). *Viola:* não encontrei violação.

**H8 — Estética e design minimalista.** *Atende:* a prévia compacta mostra só o estado, o número de fontes e as quatro reações (BP30). *Viola:* o pop-up expandido lista cada fonte separadamente, com estados técnicos, informação que o docente não precisa e que vai contra a ideia de mostrar só o grupo (V20).

**H9 — Reconhecer, diagnosticar e recuperar-se de erros.** *Atende:* ao tentar salvar uma visualização sem nome, a mensagem diz o que falta ("Dê um nome para a visualização.") (BP31). *Viola:* não encontrei violação nova; a posição dessa mensagem já está em V15 (Isabella).

**H10 — Ajuda e documentação.** *Atende:* os ícones (i) do dashboard geral explicam a regra do alerta no próprio card e dizem que "o alerta apenas marca uma mudança que vale revisar" (BP32). *Viola:* não encontrei violação na ajuda do docente. Falta ajuda para o participante, mas registrei isso como parte de V18, porque o problema é a ausência de qualquer comunicação com ele.

### 6. Declaração de violações

Registrei apenas problemas reais. Escala de severidade de 0 a 4 (seção 3).

| ID | H | Tela/estado | Ação/condição | Problema | Consequência | Evidência | Severidade | Justificativa | Recomendação |
|---|---|---|---|---|---|---|---:|---|---|
| V18 | H1 | Pop-up da extensão; prévia "Como ficará no Meet"; Minhas reuniões | A reunião é analisada com participantes de câmera ligada | Toda a indicação de que a análise está ativa fica no painel do docente. A prévia "Como ficará no Meet" mostra só o que o docente vê, e "Minhas reuniões" diz que as reuniões são iniciadas pela extensão e aparecem automaticamente. Nas telas examinadas, não há aviso aos participantes nem lembrete para o docente avisá-los | O participante não sabe que a imagem dele está sendo analisada nem o que acontece com ela, que é exatamente a situação do C03; o docente pode iniciar a análise sem ter avisado ninguém | [Pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png); [página Extensão](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/06_prototipos/extensao.png); [Minhas reuniões](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/Captura%20de%20tela%202026-11-22%20204016.png) | 3 | Acontece em toda reunião analisada e atinge todos os participantes, não só o usuário da tela; contraria RC04, RC09 e R04 e é o centro da H03. Não dei 4 porque não bloqueia a tarefa do docente e porque o fluxo de início ainda precisa ser conferido (ver limitação) | Antes da primeira estimativa, exigir o envio de um aviso aos participantes (no chat ou num indicador da chamada) com o que é captado, o que o docente recebe e o que não é feito com os dados, como previsto na CI01, na CI02 e no MoLIC M02; na prévia, mostrar também o que o participante vê |
| V19 | H4 | Pop-up expandido; página "Extensão"; quadro de privacidade da página "Extensão" | Docente lê as mensagens de privacidade para entender, ou explicar aos participantes, o que é guardado | Cada tela diz uma coisa: "Nenhum nome de participante é coletado" (pop-up), "Nenhum nome de participante é salvo" (Extensão) e "As preferências salvas aqui não incluem vídeo, nome ou reação individual" (quadro de privacidade). "Coletado" e "salvo" não são a mesma promessa, e nenhuma delas diz onde a imagem é processada nem se o vídeo é guardado durante a análise | O docente não consegue dar ao participante uma resposta segura sobre o que acontece com a imagem dele | [Pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png), rodapé; [página Extensão](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/06_prototipos/extensao.png), subtítulo e quadro "Privacidade" | 2 | Aparece sempre que o assunto é privacidade, mas não impede nenhuma tarefa do docente; o impacto é na confiança e na explicação aos participantes | Escrever uma única mensagem de privacidade e repeti-la igual em todas as telas, dizendo o que é captado, onde é processado, o que é guardado e o que não é |
| V20 | H8 | Pop-up expandido, "Fontes anônimas detectadas" | Docente abre o pop-up expandido durante a aula | O pop-up lista cada vídeo separadamente com estados técnicos ("Fonte 02 · APRESENTADOR DETECTADO", "Fonte 03 · IA ATIVA · 13.9 fps reais"). O docente não precisa dessa lista para a tarefa, e com poucas pessoas na chamada cada "fonte" corresponde a alguém que ele pode reconhecer | Informação de baixa utilidade compete com o estado do grupo e mostra a análise pessoa por pessoa, o oposto da agregação prometida (R04) | [Pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png) | 2 | Fica no modo expandido, que não é o de uso contínuo, mas aparece em toda aula em que ele é aberto. Os termos técnicos já estão em V09; aqui o problema é a lista individual | Trocar a lista pela contagem "1 de 2 vídeos contribuindo · 1 ignorado (apresentador)", sem itens por fonte, e deixar os estados técnicos numa área de diagnóstico |
| V21 | H1 | Página "Extensão", opção "Confiança do resultado"; prévia "Como ficará no Meet" | Docente configura o painel e deixa a confiança como "Ao passar o mouse" | Na prévia, o estado aparece como "Engajamento alto · 3 fontes", sem nenhuma indicação de incerteza; a confiança só aparece se o docente passar o mouse | O docente lê de relance uma estimativa como se fosse certeza, que é o risco da H02 | [Página Extensão](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/06_prototipos/extensao.png), opção "Confiança do resultado" e prévia | 2 | Depende da configuração, mas, quando acontece, vale para todas as aulas seguintes; o print não mostra se essa é a configuração padrão, o que precisa ser conferido | Manter sempre visível uma indicação curta de confiança (por exemplo, "confiança baixa") junto do estado, permitindo esconder só o detalhe numérico |
| V22 | H2 | Minhas reuniões, cabeçalho; dashboard geral, card "Participantes analisados" | Docente lê os totais gerais | "45 participantes" aparece ao lado de "43% engajamento médio", e o card "Participantes analisados: 45" explica, em letra menor, que é a "Soma das reuniões". A mesma pessoa que esteve em várias aulas conta várias vezes, e "analisados" é um termo de vigilância | O docente pode achar que analisou 45 pessoas diferentes; se repetir o termo para os alunos, aumenta o desconforto que a H03 prevê | [Minhas reuniões](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/Captura%20de%20tela%202026-11-22%20204016.png); [dashboard geral](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/06_prototipos/explica%C3%A7%C3%B5es.png) | 1 | O card do dashboard já explica a soma, e o número não muda nenhuma decisão de condução da aula | Usar "participações somadas" ou "vídeos que contribuíram", e evitar "analisados" nos textos vistos pelo docente e pelos participantes |

**Qualidade do relato:** V18 e V21 dependem de telas que não estão nos prints (início do acompanhamento e configuração padrão da extensão). Antes da consolidação, é preciso conferir no sistema se existe algum aviso aos participantes ao iniciar a análise (V18) e qual é o valor padrão da opção "Confiança do resultado" (V21).

### 6.1 Boas práticas observadas

| ID | H | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|---|
| BP23 | H1 | O pop-up mostra a base da estimativa junto do estado ("Confiança: 33% · 1 fonte(s)") e quantas fontes foram analisadas e ignoradas | [Pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png) | O docente vê em que se apoia o estado exibido, e não só o resultado |
| BP24 | H2 | As preferências da extensão são descritas pelo efeito: "Mostra se o engajamento subiu, caiu ou ficou estável", "Exibe engajamento, tédio, confusão e frustração" | [Página Extensão](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/06_prototipos/extensao.png) | O docente escolhe pelo que vai ver na aula, sem precisar saber como o sistema funciona |
| BP25 | H3 | "Restaurar padrão" na página Extensão | [Página Extensão](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/06_prototipos/extensao.png) | O docente pode experimentar configurações e voltar ao início sem refazer tudo |
| BP26 | H4 | Engajamento, tédio, confusão e frustração aparecem com os mesmos nomes e na mesma ordem no pop-up, na prévia, na tabela de leituras e no gráfico | [Pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png); [Leituras do intervalo](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/timeline.png); [gráfico](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/13_heuristica/graf.png) | O que o docente aprende ao vivo vale para o resumo depois da aula (as cores, por outro lado, mudam; ver V17) |
| BP27 | H5 | A imagem do apresentador é reconhecida e deixada fora da estimativa ("APRESENTADOR DETECTADO", "1 ignorada(s)") | [Pop-up expandido](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/f02_popup_expandido.png) | Evita que o rosto do próprio docente seja somado ao estado do grupo |
| BP28 | H6 | A prévia "Como ficará no Meet" muda na hora conforme as escolhas | [Página Extensão](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/06_prototipos/extensao.png) | O docente vê o resultado da configuração em vez de ter que imaginar ou lembrar |
| BP29 | H7 | Cada informação pode ficar fixa ou aparecer só ao passar o mouse | [Página Extensão](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/06_prototipos/extensao.png) | Quem quer só uma olhada e quem quer detalhes usam o mesmo painel |
| BP30 | H8 | A prévia compacta mostra só o estado, o número de fontes e as quatro reações | [Página Extensão](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/06_prototipos/extensao.png), prévia | Pouca informação competindo com a aula, no modo usado durante a explicação |
| BP31 | H9 | "Dê um nome para a visualização." ao tentar salvar sem nome | [Erro ao salvar sem nome](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/11_figma/erro%20salvar%20sem%20nome.png) | A mensagem diz o que falta, em linguagem simples |
| BP32 | H10 | Os ícones (i) do dashboard geral explicam a regra do alerta no próprio card e dizem que "o alerta apenas marca uma mudança que vale revisar" | [Dashboard geral](https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/06_prototipos/explica%C3%A7%C3%B5es.png) | A ajuda aparece onde a dúvida surge e deixa claro que o alerta não manda o docente fazer nada |

### Síntese individual — Gustavo Bertoluzzi

Analisei as **10 heurísticas**. Encontrei **cinco violações** (V18 a V22) em quatro delas: H1, H2, H4 e H8. Registrei também **dez boas práticas** (BP23 a BP32), uma por heurística.

| Severidade | Achados | Heurísticas |
|---:|---|---|
| 3 | V18 | H1 |
| 2 | V19, V20, V21 | H4, H8, H1 |
| 1 | V22 | H2 |

O padrão que se repete é que **a privacidade é tratada como texto solto, e não como parte da interação**:

- o participante não recebe nenhuma informação sobre a análise (V18);
- as mensagens de privacidade não são as mesmas de uma tela para outra (V19);
- o pop-up mostra a análise vídeo por vídeo, mesmo prometendo um resultado do grupo (V20);
- o vocabulário de "participantes analisados" reforça a ideia de vigilância (V22).

Também há um ponto ligado à H02: a confiança pode sumir da leitura de relance (V21).

Pontos fortes a manter: a fonte do apresentador fica fora da estimativa (BP27), a prévia em tempo real (BP28), a base da estimativa junto do estado (BP23) e a explicação do alerta no próprio card (BP32).

Plano de melhoria proposto:

1. **Antes do teste com usuários (alta prioridade):** V18. O teste da Entrega 12 processa a imagem de pessoas na chamada, então o aviso aos participantes precisa existir ou ser feito pelo moderador, com o mesmo conteúdo, até a interface tê-lo.
2. **Prioridade média:** V19 (uma única mensagem de privacidade), V20 (trocar a lista por fonte pela contagem) e V21 (confiança sempre visível de forma resumida).
3. **Baixa prioridade:** V22 (trocar "participantes analisados").

Na consolidação, V20 se aproxima de V09 (Isabella), porque as duas tratam do conteúdo técnico do pop-up expandido, e V18 e V20 se ligam a V11 (Isabella), porque todas tratam da privacidade quando há poucas fontes. As recomendações são propostas e ainda não foram implementadas.

---

## Avaliador A05 — Matheus Ferreira de Freitas

**Autor(a):** Matheus Ferreira de Freitas — 22.125.085-5  
**Versão:** MindFlow AI 2.0, site publicado em [mindflowiaa.netlify.app](https://mindflowiaa.netlify.app/) e extensão (pop-up no Meet)  
**Data:** inspeção ao vivo em 20/11/2026 (páginas públicas e estrutura de todas as telas) e em 25/11/2026 (conta logada: Minhas reuniões, resumo de demonstração, aparência da extensão)  
**Foco da inspeção:** percorri o sistema pela ótica da persona P04 (Manoel, vendedor B2B), do cenário C01 e do MoLIC M01: ativar o acompanhamento numa reunião com clientes de outra empresa, perceber o estado do grupo enquanto apresenta com a tela compartilhada, voltar dias depois ao resumo para registrar o retorno do cliente. Todas as telas foram examinadas: página inicial, entrar/criar conta/recuperar senha, Minhas reuniões, nova reunião e sala de espera, análise em andamento, indicador flutuante, pop-up compacto e expandido da extensão, resumo da reunião (cards, evolução, trecho, anotação, exclusão), dashboard geral e comparação, aparência da extensão, central de ajuda, perfil e dados de cadastro.  
**Dispositivo/viewport:** navegador no computador, janela de 1000 × 760 px (prints) e 1366 × 900 px (leitura das telas).  
**Limitação:** a inspeção ao vivo cobriu as páginas públicas, a estrutura e os textos de todas as telas (árvore de acessibilidade do site) e, com a conta logada, Minhas reuniões, o resumo de uma reunião de demonstração e a aparência da extensão; o pop-up durante uma reunião real e o dashboard geral com dados foram conferidos pelos prints da versão 2.0 guardados em `assets/11_figma` e `assets/13_heuristica`. Nenhuma reunião foi criada, encerrada ou excluída. Achados que dependem de interação não repetida estão marcados como "a confirmar".

### 4. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 | Minhas reuniões (situação de cada reunião), análise em andamento, indicador flutuante, pop-up da extensão, resumo. | Não observada no recorte. | — | BP33: a reunião em andamento aparece com "Em andamento" e "AO VIVO", o indicador mostra "atualizado há" e "n de N analisados", e o resumo informa "Sem leituras" em vez de deixar o espaço vazio. |
| H2 | Minhas reuniões, cards do resumo, tabela "Leituras do intervalo", pop-up expandido, recuperar senha. | Sim. | V23. | — |
| H3 | Navegação entre página inicial, entrar, Minhas reuniões, resumo e dashboard com o botão Voltar do navegador; botões "Voltar para a tela anterior"; cancelar no editor. | Sim. | V28. | — |
| H4 | Textos sobre a plataforma de reunião (entrar, Minhas reuniões, aparência da extensão) e formulário "Nova reunião"; confirmações de exclusão de reunião e de visualização salva. | Sim. | V26, V32. | — |
| H5 | Pop-up da extensão com uma única fonte analisada; formulário de criar conta; exclusão de reunião. | Sim. | V25, V30. | — |
| H6 | Lista de reuniões (títulos, códigos, botão "×"), seletor de visualização, blocos do editor. | Sim. | V27, V29. | — |
| H7 | Marcação de momentos durante a reunião (análise em andamento e pop-up) e anotação por intervalo no resumo. | Sim. | V31. | — |
| H8 | Indicador flutuante e pop-up compacto/expandido durante a reunião; cards e gráficos do resumo. | Sim. | V24. | — |
| H9 | Validação de nome vazio no editor; comparação com menos de duas reuniões; falha de acesso sem login. | Não observada no recorte. | — | BP34: "Dê um nome para a visualização.", "Selecione de 2 a 4 reuniões." e "Entre na sua conta para carregar as reuniões." dizem o que falta e o que fazer, sem código de erro. |
| H10 | Central de ajuda, ajuda rápida, textos de apoio dos cards e da prévia da extensão. | Não observada no recorte. | — | BP35: a central explica janelas, parcela do grupo, intensidade e confiança ("não é a taxa de acerto"), e a prévia avisa que 72% de engajamento "não representa 72% de certeza". |

### 5. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V23 | H2 | Minhas reuniões (cabeçalho e cada linha), cards do resumo ("Fontes em engajamento alto", "Participantes: Sem inferências", "Janelas analisadas"), tabela "Leituras do intervalo" ("dados de v_timeline_sessao"), pop-up expandido ("Python conectado · modelo carregado · alvo 30 fps", "Histórico Supabase"), recuperar senha ("o Supabase enviará um link"). | O sistema fala a língua do modelo e da infraestrutura, não a do vendedor: "fontes", "inferências", "janelas", "no banco", nomes de banco e de tabela e status do processo Python aparecem nas telas de uso diário. Manoel pensa em "clientes" e "momentos da reunião"; "fontes em engajamento alto" é o número principal da lista e ele precisa da central de ajuda para saber o que significa. | [Minhas reuniões, conta do avaliador](../assets/13_heuristica/a05_minhas_reunioes.jpg); [resumo: leituras de v_timeline_sessao](../assets/13_heuristica/a05_resumo_evolucao_anotacao.jpg); [pop-up expandido](../assets/11_figma/f02_popup_expandido.png); [recuperar senha](../assets/13_heuristica/a05_entrar_recuperar_senha.jpg) | 2 | Aparece em todas as telas de consulta e se repete a cada uso; não impede a tarefa, mas obriga a traduzir os termos e passa a impressão de um painel técnico, o que pesa contra a adoção por quem não é da área (lacuna ?04 da Entrega 7: usar o vocabulário dos participantes). | Trocar "fontes" por "participantes" nas telas do usuário (mantendo a contagem de câmeras ignoradas na ajuda), "janelas" por "trechos", retirar nomes de banco/tabela e status do Python das telas de uso e deixá-los só em "Status técnico", que já é opcional na aparência da extensão. |
| V24 | H8 | Pop-up expandido da extensão durante a reunião; indicador flutuante ("Engajado · 67%"). | Enquanto Manoel apresenta com a tela compartilhada, o pop-up mostra quatro percentuais (40% engajamento, 55% tédio, 56% confusão, 49% frustração), "Confiança: 33%", gráfico dos últimos 5 minutos, lista de fontes e status técnico. É informação demais para ler no momento em que ele precisa só saber "está tudo bem ou mudou?". Os percentuais de "intensidade" parecem certeza: a própria prévia precisa avisar que 72% "não representa 72% de certeza". | [pop-up expandido](../assets/11_figma/f02_popup_expandido.png); [pop-up compacto](../assets/11_figma/f01_popup_compacto.png); [prévia "Como ficará no Meet", com "Status técnico" marcado por padrão](../assets/13_heuristica/a05_extensao_previa.jpg) | 3 | Acontece na tarefa mais crítica e frequente (toda reunião), compete com a atenção que deveria estar nos clientes e induz leitura errada dos números; o pop-up compacto reduz o problema, mas ainda traz percentual de confiança e contagem de fontes como primeira informação. | Durante a reunião, mostrar por padrão só o estado predominante com cor e rótulo, a tendência e a confiança em faixas (alta/média/baixa), como decidido na Entrega 9; percentuais e gráfico só sob demanda (expandir) e com a explicação do que o número significa ao lado. |
| V25 | H5 | Pop-up compacto e expandido com "1 fonte" analisada. | O acompanhamento exibe estado e percentuais calculados sobre uma única pessoa ("Confusão alto · Confiança 33% · 1 fonte"). Numa reunião comercial com dois clientes, isso expõe a reação de um indivíduo identificável e contradiz a promessa de leitura coletiva. Não há mínimo de participantes nem aviso antes de exibir a estimativa (a confirmar se existe bloqueio em algum tamanho de grupo). | [pop-up expandido](../assets/11_figma/f02_popup_expandido.png); [pop-up compacto](../assets/11_figma/f01_popup_compacto.png) | 3 | Erro de privacidade que o sistema deveria impedir, não o usuário; em reunião B2B pequena é o caso comum, e Manoel só percebe se raciocinar sobre o "1 fonte". Impacto alto para a confiança dos clientes e para a aceitação (H05 e RC da Entrega 9). | Não calcular nem exibir estado com menos de N participantes (por exemplo 3): mostrar "sem estimativa" com o motivo e as saídas (tentar novamente, continuar sem acompanhamento), como previsto na ruptura do M01. |
| V26 | H4 | Entrar ("consulte aqui os dados coletados no Google Meet", "Abra a reunião no Meet"), Minhas reuniões ("iniciadas pela extensão no Google Meet", "Acompanhe pelo Google Meet"), aparência da extensão ("Como ficará no Meet") × formulário "Nova reunião" (plataforma: Microsoft Teams como padrão, Google Meet, Zoom). | O produto diz, nas instruções, que funciona no Google Meet, mas o formulário de nova reunião oferece Teams e Zoom. Para Manoel, que apresenta no Teams (C01), não fica claro se o acompanhamento funciona na plataforma dele ou se ele precisa mudar de ferramenta com os clientes. | [recuperar senha / painel esquerdo](../assets/13_heuristica/a05_entrar_recuperar_senha.jpg); [Minhas reuniões: "Abra o Google Meet"](../assets/13_heuristica/a05_minhas_reunioes.jpg); [aparência da extensão: "Como ficará no Meet"](../assets/13_heuristica/a05_extensao_previa.jpg) | 2 | Inconsistência entre telas da mesma versão; aparece logo na entrada e na lista, e pode fazer o vendedor desistir antes de testar ou criar uma reunião numa plataforma não suportada. | Usar um único nome ("plataforma de reunião") e listar as plataformas realmente suportadas em um só lugar; no formulário, oferecer apenas as que a extensão atende. |
| V27 | H6 | Minhas reuniões: título e identificação das reuniões. | As reuniões recebem como título o código da chamada ("Meet: eth-yedb-rxw", "srt-gavn-aaxsrt-gavn-aax", com o código duplicado) ou um texto genérico ("Sua reunião está pronta"), e a linha mostra data, duração e código interno, mas não cliente nem proposta. Dias depois, quando chega o retorno do cliente (objetivo O07), Manoel precisa reconhecer a reunião certa numa lista sem busca, lembrando qual código era de qual cliente. | [Minhas reuniões](../assets/13_heuristica/Captura%20de%20tela%202026-11-22%20204016.png) | 2 | Repete-se a cada reunião e piora com o histórico; o título pode ser editado (lápis), mas a tarefa depende de o usuário lembrar de renomear. A duplicação do código no título sugere falha de geração do nome. | Pedir título (cliente/assunto) ao iniciar ou encerrar a reunião, com o código apenas como detalhe; corrigir a duplicação do código; mostrar na lista o que o usuário usa para reconhecer (título dado por ele, participantes, momentos marcados). |
| V28 | H3 | Toda a navegação do site: página inicial → Entrar → Minhas reuniões → resumo/dashboard. | As telas trocam sem criar entrada no histórico do navegador e sem mudar o endereço (tudo fica em "/"). O botão Voltar do navegador não devolve à tela anterior (ao sair da página inicial para "Entrar", a aba fica sem histórico) e não é possível guardar ou compartilhar o endereço do resumo de uma reunião; só os botões internos "Voltar para a tela anterior" funcionam. | Verificado em 20/11/2026 com o botão Voltar do navegador e pelo endereço da aba; [página inicial](../assets/13_heuristica/a05_pagina_inicial.jpg) | 2 | Quebra uma expectativa básica da web que o usuário usa sem pensar; não bloqueia, porque existem botões internos, mas obriga a redescobrir o caminho e impede atalhos como favoritar o resumo para o follow-up. | Usar rotas próprias por tela (histórico do navegador e endereço de cada reunião), mantendo os botões internos. |
| V29 | H6 | Minhas reuniões: botão "×" ao lado de "Ver resumo" em cada linha. | A ação que exclui a reunião inteira (histórico, leituras e anotações) é um "×" pequeno, sem rótulo, colado ao botão principal da linha. Nada na lista diz o que o "×" faz antes do clique; o usuário descobre pelo diálogo de confirmação. | [Minhas reuniões](../assets/13_heuristica/Captura%20de%20tela%202026-11-22%20204016.png); [diálogo de exclusão](../assets/13_heuristica/excluir.png) | 2 | O diálogo evita a perda de dados (há confirmação clara), por isso não é grave; mas o controle fica na área de toque/clique da ação mais usada e sem reconhecimento prévio, o que gera cliques indevidos e sustos repetidos. | Rotular a ação ("Excluir") ou movê-la para um menu da reunião, afastada de "Ver resumo"; manter o diálogo atual. |
| V30 | H5 | Criar conta (formulário). | O formulário tem sete campos e um aceite, mas não marca quais são obrigatórios: nome, instituição, e-mail, senha, confirmação e termos são exigidos; gênero e atuação são opcionais. O usuário só descobre ao tentar enviar. "Instituição" também é obrigatório para um vendedor de empresa, com rótulo pensado para escola. | [criar conta](../assets/13_heuristica/a05_criar_conta.jpg) | 1 | Acontece uma vez, no cadastro, e a validação do navegador aponta o campo; mesmo assim é um erro evitável com um asterisco ou "(opcional)". | Marcar os campos obrigatórios (ou os opcionais) e rotular "Instituição ou empresa", como já está em "Dados de cadastro". |
| V31 | H7 | Análise em andamento, indicador flutuante e pop-up durante a reunião; "Anotação por intervalo" no resumo. | Não existe um atalho para marcar um momento enquanto a reunião acontece. A anotação só pode ser feita depois, no resumo, clicando duas vezes no gráfico para delimitar um trecho e escrevendo o que aconteceu. Para Manoel, o momento que importa é a "pílula de dúvida" (objetivo O03): sem marcar na hora, ele precisa reconstruir pela memória, no gráfico, quando foi cada trecho da proposta. | [Evolução da reunião, trecho e anotação por intervalo](../assets/13_heuristica/a05_resumo_evolucao_anotacao.jpg); [Evolução da reunião](../assets/13_heuristica/timeline.png) | 2 | É a tarefa frequente do usuário experiente, repetida a cada bloco da proposta; o caminho existente funciona, mas custa mais esforço justamente no uso que o produto propõe (ligar reação a trecho). | Um botão "Marcar este momento" no indicador flutuante/pop-up, com rótulo curto opcional; os momentos marcados aparecem no gráfico do resumo, onde a anotação por intervalo já existe. |
| V32 | H4 | Confirmação de exclusão: reunião (Minhas reuniões) × visualização salva (editor do resumo e do dashboard geral). | Excluir uma reunião abre um diálogo próprio ("Ação permanente", botões "Cancelar"/"Excluir reunião"); excluir uma visualização salva usa a janela padrão do navegador, com "OK"/"Cancelar". Duas aparências e dois vocabulários para a mesma classe de ação, e "OK" não diz o que será feito. | [diálogo de exclusão da reunião](../assets/13_heuristica/excluir.png); [confirmação da visualização](../assets/11_figma/info%20excluir%20visualiza%C3%A7%C3%A3o.png) | 1 | Ambas confirmam antes de apagar; a diferença é de consistência e de clareza do botão, não de perda de dados. | Usar o mesmo diálogo nas duas exclusões, com o nome do item e um botão que diga a ação ("Excluir visualização"). |

**Qualidade do relato:** V25 e V28 dependem de conferir no sistema, respectivamente, se existe algum bloqueio por tamanho de grupo antes de exibir a estimativa e se a mesma falta de histórico ocorre entre Minhas reuniões, resumo e dashboard após o login.

### 6. Boas práticas — heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| H1 | BP33 — "Em andamento"/"Concluída" em cada reunião, "AO VIVO" e "Última leitura" na análise, "4 de 5 analisados" e "atualizado há" no indicador, "Sem leituras para esta reunião" no gráfico. | [Minhas reuniões sem dados: "—" em vez de 0%](../assets/13_heuristica/a05_minhas_reunioes.jpg); [resumo sem leituras](../assets/13_heuristica/graf.png) | O usuário sabe se o acompanhamento está ativo, em que base a estimativa foi feita e há quanto tempo, e distingue "sem dados" de resultado. |
| H9 | BP34 — "Dê um nome para a visualização." ao salvar sem nome; "Selecione de 2 a 4 reuniões." e "Conclua pelo menos duas reuniões para comparar." na comparação; "Entre na sua conta para carregar as reuniões." sem login. | [nome vazio](../assets/13_heuristica/sem%20nome.png) | As mensagens dizem em linguagem simples o que falta e o que fazer, sem código técnico, e mantêm o que o usuário já preencheu. |
| H10 | BP35 — Central de ajuda com perguntas do tipo "O que significam verde, amarelo e vermelho?" e "Qual é exatamente a regra do alerta?"; ajuda rápida pelo botão "Ajuda"; a prévia da extensão explica que confiança "não é a precisão comprovada". | [central de ajuda](../assets/13_heuristica/suporte.png); [explicação do card "Alertas" no resumo](../assets/13_heuristica/a05_resumo_cards.jpg) | A ajuda é organizada pela dúvida do usuário, não pelo menu, e explica os limites do indicador, o que é essencial para a hipótese H02 (interpretar a incerteza). |

### Síntese individual — Matheus Ferreira de Freitas

Analisei as **10 heurísticas** pela ótica do Manoel (P04, C01, M01). Encontrei **dez violações** (V23 a V32) em sete heurísticas — H2, H3, H4, H5, H6, H7 e H8 — e registrei **três boas práticas** (BP33 a BP35) nas heurísticas sem violação no recorte (H1, H9 e H10).

Os problemas de severidade 3 estão na reunião ao vivo, que é onde o Manoel usa o produto com clientes: V24 (pop-up com quatro percentuais, gráfico e status técnico enquanto ele apresenta) e V25 (estimativa exibida com uma única pessoa analisada). Os dois batem de frente com decisões da Entrega 9 para a CI01: estado em cor e rótulo, confiança em faixas e nenhuma estimativa abaixo de um mínimo de participantes. Os de severidade 2 tratam do vocabulário técnico (V23), da plataforma suportada (V26), do reconhecimento da reunião certa dias depois (V27), do histórico do navegador (V28), do "×" de exclusão (V29) e da falta de um jeito de marcar o momento da pílula de dúvida durante a reunião (V31).

Na consolidação, V23 se junta a V02 (Kayky), V06 (Rafael) e V09 (Isabella), porque todos tratam de termos técnicos; V24 e V25 se ligam a V09 e V11 (Isabella) e a V18 e V20 (Gustavo), que também tratam do pop-up e da privacidade com poucas fontes; V26 repete V03 (Kayky) a partir de outra persona; V27 se aproxima de V04 (Kayky), sobre a lista sem busca. As recomendações são propostas de correção, não mudanças já feitas, e V25 e V28 devem ser confirmadas no sistema antes de virarem resultado da equipe.

---

## 7. Consolidação da equipe

Foram consolidados os **32 achados** dos avaliadores A01 (Kayky, V01–V04), A02 (Rafael, V05–V08), A03 (Isabella, V09–V17), A04 (Gustavo, V18–V22) e A05 (Matheus, V23–V32). Achados iguais ou muito parecidos viraram um só, preservando quem os encontrou. A severidade final é a maior atribuída entre os avaliadores, conferida pela equipe; a prioridade segue a severidade (3 = alta, 2 = média, 1 = baixa).

| ID consolidado | Achados individuais | Heurística | Problema | Severidade final | Prioridade | Responsável pela correção |
|---|---|---|---|---:|---|---|
| HC01 | V01 (A01), V13 (A03) | H1 | Reuniões sem leituras aparecem com "—", "0%", "0 alertas" ou "0 verdes · 0 amarelas · 0 vermelhas", sem dizer que não houve análise; ausência de dados é lida como valor zero. Uma reunião antiga continua "Em andamento" | 3 | alta | Equipe — site (resumo, lista e dashboard geral) |
| HC02 | V11 (A03), V21 (A04), V25 (A05) | H5 | O pop-up mostra o estado do grupo mesmo com uma única fonte e com confiança baixa, e a confiança pode ficar escondida até passar o mouse; a estimativa fraca parece certa e, com poucas pessoas, deixa de ser agregada | 3 | alta | Equipe — extensão (pop-up e configuração) |
| HC03 | V10 (A03), V20 (A04), V24 (A05) | H8 | O pop-up prioriza informações secundárias: no modo compacto, a conta e "Sincronizar" ocupam mais espaço que o estado da turma; no expandido, a lista de fontes com estados técnicos ocupa a área de leitura | 3 | alta | Equipe — extensão (pop-up) |
| HC04 | V18 (A04) | H1 | O participante não vê, nas telas examinadas, nenhuma indicação de que a análise está ativa; tudo fica no painel do comunicador | 3 | alta | Equipe — extensão (interface do participante, F13–F17 da E11) |
| HC05 | V08 (A02) | H6 | Porcentagens com significados diferentes (intensidade estimada, parcela de fontes, confiança) aparecem lado a lado, e a diferença está explicada só na central de ajuda | 3 | alta | Equipe — site (resumo e dashboard) |
| HC06 | V02 (A01), V06 (A02), V09 (A03), V22 (A04), V23 (A05) | H2 | Termos internos ou técnicos aparecem para o comunicador: "Supabase", "Python conectado", "fps", "v_timeline_sessao", "janelas", "fontes", "leituras" e "participantes analisados" (que soma a mesma pessoa várias vezes) | 2 | média | Equipe — site e extensão |
| HC07 | V03 (A01), V07 (A02), V19 (A04), V26 (A05) | H4 | Textos e rótulos diferentes para a mesma coisa: orientações que citam só o Google Meet, vários nomes para "personalizar" e "coletado" × "salvo" nas mensagens de privacidade | 2 | média | Equipe — site e extensão |
| HC08 | V17 (A03) | H4 | As cores dos indicadores mudam entre o pop-up e o gráfico do resumo (tédio vermelho × azul; frustração roxa × vermelha) | 2 | média | Equipe — extensão e site |
| HC09 | V04 (A01) | H7 | O histórico de reuniões não tem busca nem filtro por data ou situação | 2 | média | Equipe — site (Minhas reuniões) |
| HC10 | V05 (A02) | H1 | A página inicial mostra números de exemplo sem indicar que são dados de demonstração | 2 | média | Equipe — site (página inicial) |
| HC11 | V16 (A03) | H3 | O pop-up não oferece forma rápida de pausar o acompanhamento durante a aula | 2 | média | Equipe — extensão (pop-up, F07 da E11) |
| HC12 | V15 (A03) | H9 | O aviso "Dê um nome para a visualização" aparece longe do campo de nome, que não é destacado | 2 | média | Equipe — site (personalização) |
| HC13 | V14 (A03), V32 (A05) | H4 | As duas exclusões usam confirmações diferentes (janela do sistema × diálogo do navegador) | 1 | baixa | Equipe — site (personalização) |
| HC14 | V12 (A03) | H6 | A seta em "Confusão alto →" não é explicada | 1 | baixa | Equipe — extensão (pop-up) |
| HC15 | V27 (A05) | H6 | As reuniões recebem como título o código da chamada (por exemplo, "Meet: eth-yedb-rxw"), e o comunicador precisa lembrar qual é qual pela data | 2 | média | Equipe — site (Minhas reuniões) |
| HC16 | V28 (A05) | H3 | As telas do site trocam sem criar entrada no histórico do navegador; o botão Voltar não volta para a tela anterior | 2 | média | Equipe — site (navegação) |
| HC17 | V29 (A05) | H6 | O "×" ao lado de "Ver resumo" exclui a reunião inteira, mas não diz isso; o símbolo costuma significar "fechar" | 2 | média | Equipe — site (Minhas reuniões) |
| HC18 | V30 (A05) | H5 | O formulário de cadastro não indica quais campos são obrigatórios | 1 | baixa | Equipe — site (cadastro) |
| HC19 | V31 (A05) | H7 | Não há atalho para marcar um momento enquanto a sessão acontece; a marcação só é feita depois, no resumo | 2 | média | Equipe — extensão (pop-up, F05 e F12 da E11) |

## 8. Síntese e plano de melhoria

**Quantidade de problemas por heurística e severidade (após a consolidação):**

| Heurística | Sev. 3 | Sev. 2 | Sev. 1 | Total |
|---|---:|---:|---:|---:|
| H1 — Visibilidade do status | 2 (HC01, HC04) | 1 (HC10) | — | 3 |
| H2 — Mundo real | — | 1 (HC06) | — | 1 |
| H3 — Controle e liberdade | — | 2 (HC11, HC16) | — | 2 |
| H4 — Consistência | — | 2 (HC07, HC08) | 1 (HC13) | 3 |
| H5 — Prevenção de erros | 1 (HC02) | — | 1 (HC18) | 2 |
| H6 — Reconhecimento | 1 (HC05) | 2 (HC15, HC17) | 1 (HC14) | 4 |
| H7 — Flexibilidade | — | 2 (HC09, HC19) | — | 2 |
| H8 — Minimalismo | 1 (HC03) | — | — | 1 |
| H9 — Recuperação de erros | — | 1 (HC12) | — | 1 |
| H10 — Ajuda | — | — | — | 0 |
| **Total** | **5** | **11** | **3** | **19** |

Nenhum problema recebeu severidade 4. H10 não teve violação em nenhuma avaliação; a central de ajuda e as explicações junto ao gráfico foram citadas como boas práticas por todos os avaliadores.

**Problemas graves que precisam ser resolvidos antes do teste com usuários (Entrega 14):** HC01, HC02, HC03, HC04 e HC05. Eles afetam diretamente a leitura do estado do grupo (tarefas UT01 e UT02 da Entrega 12) e a transparência para os participantes (H03).

**Padrões recorrentes entre telas:**

- **Linguagem do sistema no lugar da linguagem do comunicador** (HC06, HC07): aparece no site e na extensão e foi apontada pelos quatro avaliadores.
- **Estimativa apresentada com mais certeza do que tem** (HC01, HC02, HC05): ausência de dados lida como zero, base pequena tratada como grupo e porcentagens confundidas.
- **Pop-up pensado para configuração, e não para a leitura de relance durante a sessão** (HC03, HC11, HC14, HC19).
- **Participante sem informação dentro da chamada** (HC04), ligado às telas F13 a F17 propostas na Entrega 11.

**Correções planejadas antes ou para a avaliação com usuários:**

1. Diferenciar "sem dados" de "zero" em todo o site e encerrar reuniões que ficaram abertas (HC01).
2. Definir um mínimo de participantes, mostrar a confiança sempre em texto e trocar o estado por "sem estimativa" abaixo do mínimo (HC02).
3. Reorganizar o pop-up: estado, confiança e participantes contribuindo em primeiro plano; conta, sincronização e fontes no modo expandido ou em diagnóstico (HC03), com o botão de pausa (HC11).
4. Criar o aviso e o indicador para o participante (HC04, telas F13 e F14).
5. Rotular cada porcentagem com o que ela mede (HC05).
6. Depois do teste: padronizar termos, cores e confirmações (HC06–HC08, HC13), melhorar o histórico com busca e títulos reconhecíveis (HC09, HC15), deixar claro o "×" de exclusão (HC17), fazer o botão Voltar funcionar (HC16), marcar os dados de demonstração (HC10), aproximar o aviso do campo (HC12), indicar campos obrigatórios (HC18), permitir marcar momentos durante a sessão (HC19) e explicar a seta (HC14).

**Limitações:** as inspeções usaram a versão 2.0 publicada e prints das telas internas; parte dos achados de interação (V15, V16) precisa ser confirmada no sistema.

## Checklist

- [x] Cada integrante fez uma inspeção completa e identificada (A01 a A05).
- [x] Todas as telas/estados relevantes foram examinados (lista, resumo, personalização, dashboard geral, extensão, pop-up, ajuda, página inicial).
- [x] Estados administrativos, filtros, relatórios, históricos, processamento e erros foram incluídos quando existentes.
- [x] A inspeção avaliou a interface/protótipo, não o mérito técnico do algoritmo/modelo.
- [x] H1–H10 aparecem na matriz de cobertura de cada avaliador.
- [x] Parte de violações contém apenas violações, sem “forçar” exemplos.
- [x] Todo problema tem print/localização e contexto.
- [x] Severidade possui justificativa, não apenas número.
- [x] Recomendação resolve a causa ou reduz o impacto.
- [x] Achados duplicados foram consolidados ao final (seção 7, HC01 a HC19).
