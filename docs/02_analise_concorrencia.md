# Entrega 2 — Público-alvo e análise de concorrência

**Data:** {{26/08/2026}}  
**Status:** 🟨 iniciada  
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
| Read IA | concorrente | Concorrente direto, com quase os mesmos objetivos | F | analisar |

Se uma hipótese da Entrega 1 for confirmada ou refutada durante esta análise, atualize `H01`, `H02`... em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

## 1. Público-alvo desta análise

Professores, palestrantes, docentes que fazem reuniões online por videoconferência.

## 2. Concorrentes diretos/indiretos

### Análise C01 — {{produto}}

**Autor(a):** {{Kayky Pires - 22.222.040-2}}  
**Tipo:** direto 
**Link oficial:** [{{Read IA}} ](https://www.read.ai/pt) 
**Data de acesso:** 26/08/2026

#### Contexto e proposta

Read é o seu copiloto de IA — transformando reuniões, e-mails e mensagens em resumos, insights e respostas instantâneas em todos os dispositivos, onde quer que você trabalhe.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Transcrição da Reunião | O Read AI registra e transcreve automaticamente as falas da reunião, separando o conteúdo por participante. | [Trasncrição](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/02_concorrencia/Transcri%C3%A7%C3%A3o%20READIA.png) | A organização por participante facilita a compreensão de quem falou e permite consultar rapidamente partes específicas da reunião. |
|Resumo automático|Após a reunião, a IA gera um resumo com os principais assuntos discutidos, decisões, perguntas e pontos relevantes.|[Resumo](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/02_concorrencia/Resumo%20READIA.png)|Reduz a quantidade de informação que o usuário precisa analisar e apresenta uma visão geral da reunião de forma mais objetiva|
|Métricas da reunião|O sistema reúne diferentes indicadores de desempenho, como engajamento, sentimento e outras métricas relacionadas à participação e comunicação.|[Metrica](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/02_concorrencia/Dash%20READIA.png)|A centralização das métricas em um painel facilita a comparação das informações, mas exige boa hierarquia visual para não sobrecarregar o usuário|
|---|---|---|---|

#### Experiência do usuário e opiniões

Use avaliações públicas, relatos, estudos, testes próprios ou outra fonte identificável. Não trate opinião isolada como verdade universal.

#### Preço/modelo de negócio

Utiliza o modelo freemium, oferecendo um plano gratuito limitado a 5 reuniões por mês e planos pagos por usuário. Atualmente, o plano Pro custa a partir de US$ 15/mês por usuário no pagamento anual, enquanto os planos Enterprise e Enterprise+ oferecem recursos adicionais para equipes e organizações

#### Padrões e tendências percebidos

Apresenta tendência de centralizar, em um único painel, transcrição, resumo, métricas de engajamento, sentimento e destaques da reunião. Também se percebe forte uso de inteligência artificial para reduzir o esforço de análise do usuário e transformar reuniões longas em informações visuais e objetivas.

#### Pontos positivos, limitações e lições

| ID | Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|---|
|C01| Visualização de engajamento e sentimento da reunião. | Dashboard do Read AI. | Possui função semelhante ao MindFlow, sendo necessário diferenciar o projeto pelo foco educacional e pelos estados afetivo-cognitivos analisados. |

> Repita a subseção para C02, C03... até atender à quantidade da equipe.

## 3. Softwares que o público-alvo usa no cotidiano

Analise interfaces que moldam a expectativa do público, mesmo que não sejam concorrentes.

| Software | Por que o público usa | Padrões relevantes | Prints | O que aprender |
|---|---|---|---|---|
| Microsoft Teams | Para realizar aulas, reuniões e compartilhar materiais. | Menus laterais, abas, ícones conhecidos e organização dos participantes. | [Teams](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/02_concorrencia/Accordion%201.png) | Manter navegação simples e informações importantes de fácil acesso. |
| Google Meet | Para realizar videoconferências e aulas on-line. | Interface limpa, poucos controles e ações principais bem destacadas. | [Meet](https://github.com/IsaRosseto/IHC_MindFlowAI/blob/main/assets/02_concorrencia/meet.jpg) | Evitar excesso de informações e priorizar as funções principais. |
| Google Classroom | Para organizar atividades, materiais e comunicação com alunos. | Organização por turmas, cards e divisão do conteúdo em seções. | {{link local}} | Utilizar blocos bem organizados para facilitar a localização das informações. |


## 3.1 Padrões de interface relevantes ao escopo de IHC

| Padrão observado | Produto(s) | Para qual tarefa serve | Vantagem percebida | Risco/limitação | Aplicável ao nosso escopo? |
|---|---|---|---|---|---|
| Dashboard | Read AI | Visualizar métricas e informações gerais da reunião. | Centraliza os principais dados em uma única tela. | O excesso de indicadores pode dificultar a interpretação. | Sim |
| Relatório | Read AI | Consultar resumo, transcrição, engajamento, sentimento e destaques da reunião. | Facilita a análise após o término da reunião. | Pode apresentar muitas informações ao mesmo tempo. | Sim |
| Histórico + filtros | Read AI | Localizar e consultar reuniões anteriores. | Facilita o acesso a resultados passados. | Muitos filtros podem aumentar a complexidade da interface. | Sim |
| Administração/CRUD | Read AI | Gerenciar reuniões, usuários e configurações da conta. | Permite organizar e controlar os dados da plataforma. | Não é uma funcionalidade central para o objetivo do MindFlow AI. | Talvez |
| Comparação de resultados | Read AI | Analisar diferenças entre métricas e momentos de uma reunião. | Ajuda a identificar variações de engajamento e sentimento. | As métricas podem ser interpretadas de forma equivocada sem contexto. | Sim |
> O objetivo não é concluir “todo concorrente tem dashboard, então teremos um”. O padrão só será adotado se apoiar uma tarefa rastreável.

## 4. Síntese comparativa da equipe

| Critério | C01 - Read AI | C02 | C03 | Oportunidade para o projeto |
|---|---|---|---|---|
| Navegação | Dashboard organizado por reuniões, relatórios e métricas. |  |  | Criar uma navegação simples e com acesso rápido às análises das videoconferências. |
| Feedback/estado | Apresenta indicadores de engajamento, sentimento e destaques da reunião. |  |  | Mostrar de forma clara os estados identificados e suas mudanças ao longo da sessão. |
| Prevenção/recuperação de erro | Utiliza padrões conhecidos de interface e organização das informações. |  |  | Usar mensagens claras e elementos visuais que reduzam erros de interpretação. |
| Terminologia | Utiliza termos relacionados a reuniões, engajamento, sentimento e comunicação. |  |  | Utilizar linguagem simples e próxima da realidade dos docentes. |
| Acessibilidade | Utiliza gráficos, textos e indicadores visuais para apresentar os dados. |  |  | Evitar depender apenas de cores e combinar gráficos com textos e valores. |
| Eficiência | Automatiza transcrição, resumo e análise da reunião em um único ambiente. |  |  | Automatizar a análise e apresentar ao docente apenas as informações mais relevantes. |

## 5. Recomendações derivadas

Liste recomendações com origem explícita.

- **RC01:** Criar um dashboard simples e objetivo para visualizar os principais resultados da videoconferência — derivada de **C01 (Read AI)**.

- **RC02:** {{...}}

## Referências

https://www.read.ai/pt

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
