# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** {{27/08/2026}}  
**Status:** 🟨 iniciada  
**Responsabilidade:** 1 persona por integrante; 1 mapa de empatia, 1 contexto de uso consolidado e 1 jornada por equipe (salvo orientação diferente do docente).

## Objetivo da atividade

Representar grupos de usuários de forma útil para decisões de design. Persona não é personagem decorativo: suas características devem alterar requisitos, prioridades, linguagem, fluxos ou critérios de avaliação.

## Atenção a projetos técnicos

Em TCCs sem interface original, a persona pode representar um **profissional que se apropria da contribuição técnica**: DBA, analista, cientista de dados, administrador, pesquisador, técnico, operador, gestor ou especialista de domínio.

Não escolha um perfil apenas porque “parece combinar” com a tecnologia. Explique **qual objetivo esse perfil teria e qual parte da contribuição do TCC produziria valor para ele**. Se ainda for hipótese, mantenha como hipótese/proto-persona a validar.

Também considere papéis diferentes quando houver tarefas distintas, por exemplo:

- operador que executa análises;
- administrador que configura e gerencia permissões;
- especialista que interpreta resultados;
- gestor que consulta relatórios e decide;
- auditor que revisa histórico.

## Entradas da Entrega 1

Antes de criar personas, retome os tipos de usuários, características relevantes, objetivos e hipóteses registradas na Entrega 1. A persona **não deve transformar uma hipótese inicial em fato por meio de uma história fictícia**.

| Item da Entrega 1 | Status inicial | Evidência disponível agora | Como será tratado nesta entrega |
|---|---|---|---|
| Comunicador, como professor, instrutor ou palestrante, é o usuário prioritário da interface | F | Perfil definido pela equipe na seção 7.2 da Entrega 1 | Incorporar |
| Objetivo de perceber, durante a sessão, se o grupo está engajado, entediado, confuso ou frustrado | H | Registrado como hipótese na atividade A01 da seção 3.2 | Manter como hipótese |
| Revisar após a sessão os momentos de maior confusão ou desengajamento | H | Registrado como hipótese na atividade A03 da seção 3.2 | Manter como hipótese |
| Dificuldade de acompanhar visualmente vários participantes enquanto apresenta conteúdo | H | Registrada como hipótese nas seções 2.4 e 4.2 | Manter como hipótese |

## 1. Personas

### Persona P01 — Karol

**Autor(a):** Kayky Pires — 22.222.040-2  
**Tipo:** primária  
**Base de evidências:** proto-persona baseada na Entrega 1  
**Hipóteses da Entrega 1 relacionadas:** H01

<img src="https://raw.githubusercontent.com/IsaRosseto/IHC_MindFlowAI/main/assets/03_personas/Karol.png" width="300">

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | 30–45 anos; professora que ministra aulas por videoconferência |
| Ocupação/papel | Professora de Filosofia no ensino a distância e responsável pela condução das aulas |
| Conhecimento do domínio | Alto domínio do conteúdo que ensina e 7 anos de experiência como professora |
| Experiência tecnológica | Familiaridade baixa a média com plataformas de videoconferência, ambientes virtuais de aprendizagem e compartilhamento de conteúdo |
| Objetivos | Conduzir aulas claras e perceber quando os alunos apresentam dificuldades de compreensão, desmotivação ou frustração |
| Necessidades | Compreender como a turma está reagindo durante a aula e saber quando precisa mudar a forma de explicar o conteúdo |
| Dores/frustrações | Sente falta de observar as expressões e reações dos alunos como fazia presencialmente e se preocupa quando recebe pouco retorno da turma |
| Motivadores | Paixão por ensinar, ajudar os alunos a compreender conteúdos complexos e melhorar continuamente suas aulas |
| Restrições/acessibilidade | Possui mobilidade reduzida após um acidente, dificultando o deslocamento até a instituição; durante as aulas também precisa dividir a atenção entre conteúdo, chat, alunos e apresentação |
| Ambiente típico de uso | Pequena sala organizada e bem iluminada em sua residência, utilizando notebook, webcam e internet para ministrar aulas online |
| Comportamentos relevantes | Observa câmeras e chat, pergunta se os alunos entenderam e, diante de pouca participação, utiliza resumos, tópicos nos slides e novos exemplos para tentar facilitar a compreensão |

**Decisões de design influenciadas por P01:**

- Priorizar informações simples e rápidas de interpretar durante a aula.
- Evitar excesso de elementos e interações que disputem a atenção da professora.
- Apresentar informações de forma clara, considerando sua familiaridade tecnológica baixa a média.
- Permitir que estimativas do sistema sejam apresentadas como apoio, sem transmitir certeza absoluta sobre o estado dos alunos.
> Repita para P02, P03... Cada integrante deve produzir ao menos uma persona.

### Síntese das personas

Explique diferenças entre os perfis e qual persona é prioritária. Evite personas duplicadas que só mudam nome/foto.

## 2. Mapa de empatia — equipe

**Persona escolhida:** {{P01}}  
**Justificativa:** {{por que esse perfil é relevante}}

![Mapa de empatia](../assets/03_personas/mapa_empatia.svg)

Documente também em texto: o que vê; ouve; diz/faz; pensa/sente; dores; ganhos. Diferencie **evidência** de **hipótese**.

## 3. Contexto de uso — consolidação

| Dimensão | Descrição | Implicação de design |
|---|---|---|
| Usuários | Comunicador responsável pela sessão, com foco na persona Karol, professora de Filosofia em aulas EAD síncronas | A interface deve priorizar leitura rápida, linguagem simples e baixo esforço de interação |
| Tarefas | Conduzir a aula, apresentar conteúdo, acompanhar dúvidas e tentar perceber se a turma está compreendendo ou perdendo o interesse | As informações principais devem ser compreendidas de relance, sem interromper a condução da aula |
| Equipamentos | Notebook ou desktop com webcam, microfone e acesso à plataforma de videoconferência | A interface deve funcionar de forma leve e integrada ao contexto de videoconferência, sem exigir equipamentos adicionais |
| Ambiente físico | Karol ministra as aulas em uma sala organizada e bem iluminada em sua residência, podendo sofrer com instabilidade de internet | O sistema deve tolerar variações de conexão e não depender de condições ideais para apresentar informações básicas ao usuário |
| Ambiente social/organizacional | Aula remota com aproximadamente 35 alunos, em que parte da turma pode permanecer com câmera e microfone desligados | A interface deve trabalhar com informações agregadas do grupo e evitar exposição ou identificação individual dos participantes |
| Papéis/permissões/governança | O professor é o principal usuário da interface; os alunos são participantes da sessão e fonte dos dados analisados | Os resultados devem ser direcionados ao comunicador, respeitando privacidade, consentimento e os princípios de LGPD previstos no projeto |
| Volume de dados/histórico | O sistema gera informações continuamente durante a sessão e prevê armazenamento de dados agregados e histórico por aula, sem armazenar vídeo bruto | O dashboard deve organizar os dados por sessão e por período, permitindo revisão posterior sem comprometer a privacidade dos participantes |

## 4. Jornada do usuário — equipe

**Persona:** {{P01}}  
**Objetivo da jornada:** {{...}}  
**Início e fim da jornada:** {{...}}

| Etapa | Situação/ação | Objetivo | Pensamento/emoção | Dor | Oportunidade de design | Evidência |
|---|---|---|---|---|---|---|
| 1 | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |

> A jornada pode incluir etapas **antes, durante e depois** do uso do produto. Não transforme a jornada em lista de telas.

## Síntese

Quais necessidades e objetivos devem obrigatoriamente aparecer nos cenários e nas tarefas seguintes?

## Checklist

- [ ] Existe pelo menos uma persona por integrante.
- [ ] As personas não são apenas diferenças demográficas superficiais.
- [ ] Está claro o que é dado real e o que é hipótese/proto-persona.
- [ ] A persona não “validou por ficção” uma hipótese da Entrega 1; afirmações continuam marcadas como hipótese quando não há evidência.
- [ ] Objetivos e dores têm consequência para o design.
- [ ] Contexto de uso está coerente com a Entrega 1.
- [ ] Em TCC sem interface original, a persona possui relação explícita com a contribuição técnica.
- [ ] Papéis administrativos, técnicos e decisórios só foram criados quando possuem objetivos/tarefas diferentes.
- [ ] Jornada possui etapas, dores e oportunidades e não é apenas wireflow.
- [ ] IDs das personas foram adicionados à rastreabilidade.
