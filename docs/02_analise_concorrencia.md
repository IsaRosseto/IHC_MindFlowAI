# Entrega 2 — Público-alvo e análise de concorrência

**Data:** 26/08/2026  
**Status:** 🟨 em andamento  
**Responsabilidade mínima:** cada integrante analisa pelo menos 1 concorrente/interface representativa; a equipe produz síntese comparativa.

## Objetivo da atividade

Compreender soluções do mesmo domínio **e também interfaces familiares ao público-alvo**. O objetivo não é copiar telas, mas identificar convenções, padrões, affordances percebidas, problemas recorrentes, expectativas e oportunidades de design.

> **Concorrente não precisa ser idêntico ao produto.** Pode atuar na mesma área, resolver objetivo semelhante ou disputar a mesma necessidade. Quando não houver concorrente direto, use produtos análogos e softwares que o público já utiliza.

### Para TCCs que não previam interface

Não procure apenas um “concorrente do algoritmo”. Investigue **interfaces profissionais que materializam atividades semelhantes** às que o usuário escolhido precisaria realizar.

Exemplos:

- TCC de banco de dados → consoles de administração, ferramentas para DBA, monitoramento e análise de consultas;
- TCC de LLM/ML → painéis de experimentos, gestão de modelos/datasets, comparação de métricas, revisão de resultados;
- TCC de análise de dados → dashboards, ferramentas de BI, filtros, relatórios e exploração;
- TCC de infraestrutura/API → portais administrativos, observabilidade, logs, gestão de credenciais e uso;
- TCC de cibersegurança → consoles de alertas, triagem, histórico e auditoria.

A pergunta é: **“que convenções esse perfil já conhece para executar tarefas equivalentes?”**

## Entrada obrigatória da Entrega 1

Retome o mapa inicial de alternativas e produtos citado na Entrega 1. Aqui a equipe deixa de trabalhar apenas com impressão inicial e passa a **investigar sistematicamente** cada solução.

| Item citado na Entrega 1 | Tipo | Por que foi citado | Status inicial | Decisão nesta entrega |
|---|---|---|---|---|
| Noldus FaceReader | Análogo | É um software onde consegue identificar diversas impressões faciais, como alegria, tristeza, etc... onde nosso software busca tambem fazer a identificação dessas impressões. | F | Analisar |

Se uma hipótese da Entrega 1 for confirmada ou refutada durante esta análise, atualize `H01`, `H02`... em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

## 1. Público-alvo desta análise

Professores, palestrantes, docentes que fazem reuniões online por videoconferência.

## 2. Concorrentes diretos/indiretos

### Análise C01 — Noldus FaceReader

**Autor(a):** Rafael Dias - 22.222.039-4 <br>
**Tipo:** Análogo <br>
**Link oficial:** [{{Noldus FaceReader}}](https://noldus.com/facereader) <br>
**Data de acesso:** 26/08/2026

#### Contexto e proposta

Noldus FaceReader - É um produto que realiza a identificação das reações faciais dos usuarios capturando em tempo real ou por videos, demonstrando como as pessoas reagem ao seu produto

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Análise automática de expressões faciais | Detecta expressões como felicidade, tristeza, raiva, surpresa, medo, nojo, desprezo e estado neutro, indicando também a intensidade de cada expressão | [Identificação](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/02_concorrencia/evidencia_noldus.png) | ele Gera um indicador com o nivel de confiança para cada reação facilitando a demonstração a quem utiliza |

#### Experiência do usuário e opiniões

Use avaliações públicas, relatos, estudos, testes próprios ou outra fonte identificável. Não trate opinião isolada como verdade universal.

#### Preço/modelo de negócio

O Noldus FaceReader é um software comercial B2B, vendido a partir de licenças, principalmente para laboratorios, univesidades, empresas e instituições de pesquisa. O Noldus oferece 3 tipos de licenças: Essential - € 2000, Advanced - € 9000 e Premium - € 12500. Além dessas versões existe uma versão gratuita de 14 dias.

#### Padrões e tendências percebidos

Demonstra uma tendência para usos de estudo, para entender como os usuarios reagem a produtos ou areas de ensino. Tendo alto nivel de resultados para cada expressão.

#### Pontos positivos, limitações e lições

| ID | Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|---|
| C01 | Identificação da reação das pessoas | Graficos demonstrando o nivel de confiança da emoção (Execução do software) | Possui a funcionalidade parecida com a do nosso projeto de identificar a emoção dos usuarios, demonstrando um farol cognitivo captura em tempo real. |

> Repita a subseção para C02, C03... até atender à quantidade da equipe.

## 3. Softwares que o público-alvo usa no cotidiano

Analise interfaces que moldam a expectativa do público, mesmo que não sejam concorrentes.

| Software | Por que o público usa | Padrões relevantes | Prints | O que aprender |
|---|---|---|---|---|
| Microsoft Teams | Para realizar aulas, reuniões e compartilhar materiais. | Menus laterais, abas, ícones conhecidos e organização dos participantes. | [Teams](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/02_concorrencia/Accordion%201.png) | Manter navegação simples e informações importantes de fácil acesso. |
| Google Meet | Para realizar videoconferências e aulas on-line. | Interface limpa, poucos controles e ações principais bem destacadas. | [Meet](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/02_concorrencia/meet.jpg) | Evitar excesso de informações e priorizar as funções principais. |
| Google Classroom | Para organizar atividades, materiais e comunicação com alunos. | Organização por turmas, cards e divisão do conteúdo em seções. | {{link local}} | Utilizar blocos bem organizados para facilitar a localização das informações. |

## 3.1 Padrões de interface relevantes ao escopo de IHC

Registre somente padrões encontrados nas soluções analisadas e que possam ter relação com objetivos reais da equipe.

| Padrão observado | Produto(s) | Para qual tarefa serve | Vantagem percebida | Risco/limitação | Aplicável ao nosso escopo? |
|---|---|---|---|---|---|
| dashboard | Noldus FaceReader | Demonstração dos niveis cognitivos | Identifica qual a confiança para cada reação | Excesso de informações e dificil entendimento | Sim |
| relatório | Noldus FaceReader | Para avaliar os resultados das reações dos participantes | Os relatorios geração não são estruturados de forma gerencial | Os dados são gerados em forma de excel, tendo que estruturar o tudo | Talvez |
| histórico + filtros | Noldus FaceReader| Consegue filtrar participantes por nome, nome da análise, combinação participante/análise, gênero e idade. Também pode selecionar somente determinados estímulos ou marcadores de evento e escolher quais parâmetros deseja visualizar | Flexibilidade para filtrar itens expecificos a serem vistos | Expõe usuarios expecificos | Sim/Não |
| administração/CRUD | Noldus FaceReader | Gerenciamento de projetos, adicionar novos participantes, excluir novos participantes e editar os dados deles | Manutenção e controle de quem esta em cada projeto | {{...}} | Não |
| comparação de resultados | Noldus FaceReader | Facilita a comparação entre diferentes resultados das analises feitas | Consegue comparar diferentes conjuntos de dados/testes | {{...}} | Talvez |

> O objetivo não é concluir “todo concorrente tem dashboard, então teremos um”. O padrão só será adotado se apoiar uma tarefa rastreável.

## 4. Síntese comparativa da equipe

| Critério | C01 - Noldus FaceReader | C02 | C03 | Oportunidade para o projeto |
|---|---|---|---|---|
| Navegação | Possui diversas telas, gráficos, tabelas e opções de análise. Apesar de oferecer muitos recursos, a grande quantidade de informações pode tornar a interface complexa e poluída para usuários menos experientes |  |  | Criar uma navegação mais simples, limpa e direta, priorizando as informações mais importantes para o profissional |
| Feedback/estado | Apresenta feedback visual durante a análise, mostrando expressões identificadas, intensidade, valência, arousal e qualidade da detecção facial |  |  | Apresentar os estados identificados de maneira clara e de fácil interpretação, destacando alterações importantes ao longo da aula |
| Prevenção/recuperação de erro | Informa problemas durante a análise, como quando não consegue encontrar ou classificar um rosto, além de apresentar um indicador de qualidade da detecção. Porém, alguns problemas exigem que o próprio usuário ajuste câmera, iluminação ou configurações |  |  | Fornecer mensagens de erro simples, indicando o problema e sugerindo diretamente como corrigi-lo |
| Terminologia | Utiliza diversos termos técnicos, como Action Units, FACS, Valence, Arousal, Stimuli e Event Markers, que podem dificultar o entendimento de usuários sem conhecimento técnico |  |  | Utilizar uma linguagem mais próxima do contexto educacional e explicar termos técnicos por meio de descrições, dicas ou tooltips |
| Acessibilidade | Alto volume de graficos e termos tecnicos, assim dificultando usuarios com baixo nivel tecnico nas informações demonstradas |  |  | Desenvolver e criar visualizações com padrões de acessibilidade e linguagem simples para entendimento de todo o publico |
| Eficiência | Permite automatizar análises faciais, analisar vários dados, comparar participantes e grupos, realizar análises em lote e exportar resultados, reduzindo o trabalho manual do profissional |  |  | Automatizar a análise das aulas e videoconferencias para apresentar ao profissional somente os principais resultados e insights, reduzindo o esforço necessário para interpretar os dados |

## 5. Recomendações derivadas

Liste recomendações com origem explícita.

- **RC01:** Desenvolver Dashboard e farol cognitivo em tempo real para identificar pontos de melhoria em apresentações/aulas, além da identificação pontual de perda de atenção do publico - deruvada de **C01 (Noldus FaceReader)**.
- **RC02:** {{...}}

## Referências

[Pagina inicial](https://noldus.com/facereader)
[Documentação](https://noldus.com/shared/resources/book/noldus-product-documentation/chapter/facereader)

## Checklist

- [ ] O mapa inicial de alternativas da Entrega 1 foi revisitado e aprofundado.
- [ ] Hipóteses relevantes sobre mercado/padrões foram atualizadas na rastreabilidade quando surgiram evidências.
- [ ] Há pelo menos uma análise completa por integrante.
- [ ] Cada análise contém prints legíveis da interface.
- [ ] Prints mostram telas/estados relevantes, não apenas logos/homepage.
- [ ] Foram analisados concorrentes e/ou interfaces representativas ao público.
- [ ] Em TCC sem interface original, foram investigadas ferramentas profissionais análogas às atividades do usuário escolhido.
- [ ] Padrões como dashboard, relatório, filtros e CRUD foram analisados como soluções para tarefas, não como requisitos automáticos.
- [ ] Opiniões de UX têm fonte.
- [ ] A síntese compara critérios comuns e produz recomendações.
- [ ] Não há “copiar porque o concorrente faz”; há justificativa de adequação ao público/contexto.
