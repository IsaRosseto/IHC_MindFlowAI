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
