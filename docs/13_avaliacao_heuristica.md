# Entrega 13 — Avaliação de IHC por inspeção heurística

**Data:** {{18/11/2026}}  
**Status:** ⬜ iniciada  
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
| Avaliadores | A01 — Kayky Pires: registro elaborado com apoio de inspeção assistida e sujeito à revisão do avaliador. Os demais integrantes acrescentarão seus próprios registros após a inspeção individual. |

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

> Repita a seção para A02, A03... um avaliador por integrante.

## 7. Consolidação da equipe

Problemas iguais ou muito semelhantes encontrados por avaliadores diferentes devem ser consolidados, preservando quem os encontrou.

| ID consolidado | Achados individuais | Heurística | Problema | Severidade final | Prioridade | Responsável pela correção |
|---|---|---|---|---:|---|---|
| A definir na consolidação. | Aguardando registros A02–A05. | — | Agrupar problemas repetidos após as análises individuais. | — | A definir. | A definir pela equipe. |


## 8. Síntese e plano de melhoria

A análise A01 registrou **quatro violações**: uma em H1, uma em H2, uma em H4 e uma em H7. A distribuição proposta é de **um problema de severidade 3** e **três de severidade 2**. Não foram atribuídos graus 0, 1 ou 4 aos achados registrados. H3, H5, H6, H8, H9 e H10 possuem exemplos de boa prática no recorte examinado.

O problema prioritário é **V01**, porque representar ausência de leituras como 0% pode induzir interpretação incorreta. Recomenda-se corrigi-lo antes de apresentar os resultados aos docentes. Não foi identificado um bloqueio de navegação de severidade 4 nas condições examinadas.

Os padrões recorrentes são comunicação inconsistente da disponibilidade de dados, exposição de termos internos e orientações ainda restritas ao Meet. O histórico extenso também evidencia uma oportunidade de melhorar a localização de reuniões.

O plano proposto é:

1. **Alta prioridade — V01:** distinguir “Sem dados” de 0% no gráfico, seleção e demais representações.
2. **Baixa prioridade — V02 e V03:** revisar o vocabulário e atualizar os textos sobre plataformas.
3. **Baixa prioridade — V04:** acrescentar busca e filtros para o histórico.
4. **Antes de fechar a avaliação:** anexar prints, revisar o registro A01 e complementar os estados ainda não verificados.
5. **Após as análises individuais:** consolidar achados, definir responsáveis e prazos de correção e atualizar esta síntese com os números da equipe.

As melhorias são recomendações; este documento não afirma que já foram implementadas. As contagens acima são de A01, não da avaliação completa da equipe.

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
