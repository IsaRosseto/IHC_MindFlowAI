<!-- P02 preenchida (Matheus), com base no material da disciplina CC8122-Personas.pdf (lema, objetivos pessoais × práticos, tarefas, relacionamentos, expectativas). Demais personas e seções de equipe: template intacto — cada integrante faz a sua. -->

# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** 31/08/2026  
**Status:** 🟨 em andamento — P02 preenchida; demais personas e seções de equipe pendentes  
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
| {{usuário/objetivo/característica/H01...}} | F / H / ? | {{...}} | incorporar / manter como hipótese / descartar / investigar |

## 1. Personas

### Persona P01 — {{nome fictício}}

**Autor(a):** {{nome — matrícula}}  
**Tipo:** primária / secundária  
**Base de evidências:** entrevista / questionário / literatura / observação / proto-persona a validar / combinação  
**Hipóteses da Entrega 1 relacionadas:** {{H01, H02 ou —}}

![Persona P01](../assets/03_personas/persona_p01.svg)

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | {{somente o que impacta o uso}} |
| Ocupação/papel | {{...}} |
| Conhecimento do domínio | {{...}} |
| Experiência tecnológica | {{...}} |
| Objetivos | {{...}} |
| Necessidades | {{...}} |
| Dores/frustrações | {{...}} |
| Motivadores | {{...}} |
| Restrições/acessibilidade | {{...}} |
| Ambiente típico de uso | {{...}} |
| Comportamentos relevantes | {{...}} |

**Decisões de design influenciadas por P01:**

- {{...}}

> Repita para P02, P03... Cada integrante deve produzir ao menos uma persona.

---

### Persona P02 — Carlos, o instrutor corporativo cobrado por resultado

**Autor(a):** Matheus Ferreira de Freitas — 22.125.085-5  
**Tipo:** primária  
**Base de evidências:** proto-persona a validar (contextos de uso do TCC1; experiência da equipe com treinamentos corporativos)  
**Hipóteses da Entrega 1 relacionadas:** H01, H02

![Persona P02](../assets/03_personas/persona_p02.svg)

| Campo | Descrição |
|---|---|
| Lema | “Número sem explicação, pra mim, é chute.” |
| Faixa etária / contexto relevante | 35 anos; analista sênior de TI que ministra onboardings e treinamentos obrigatórios (segurança, compliance, ferramentas internas) |
| Ocupação/papel | Instrutor interno; 2–4 sessões por mês, de 20 a 200 participantes, quase todos de câmera desligada |
| Conhecimento do domínio | Alto no conteúdo técnico; médio em didática — dar aula não é a função principal dele |
| Experiência tecnológica | Alta: Teams, dashboards (Power BI), ferramentas de TI; confortável com métricas, desconfiado de números sem explicação |
| Objetivos pessoais | Ser levado a sério como instrutor, mesmo sem ser "professor de carreira" |
| Objetivos práticos | Garantir que o time realmente absorveu o treinamento (A01/A03); provar valor do treinamento para a gestão |
| Necessidades | Saber quais partes do treinamento funcionaram e quais geraram confusão, com evidência que ele possa citar |
| Dores/frustrações | Plateia 100% muda e de câmera fechada; pesquisa de reação no fim ("nota 9") que não diz nada; refazer treinamento inteiro quando bastava refazer um módulo |
| Motivadores | Eficiência; dado que sustente decisão; menos sessões repetidas |
| Restrições/acessibilidade | Ambiente corporativo com restrições de segurança/LGPD — nada de gravar vídeo dos colegas; ferramentas precisam passar pela TI |
| Ambiente típico de uso | Escritório/home office, dois monitores, Teams + slides |
| Comportamentos relevantes | Já usa relatórios do Teams (presença); confere quem concluiu; questiona como a métrica foi calculada antes de confiar nela |
| Tarefas típicas (frequência/duração) | Ministrar 2–4 treinamentos de 60–120 min por mês (crítica); reportar resultados à gestão (mensal); atualizar material (contínua) |
| Relacionamentos | Participantes (colegas de empresa); gestão que cobra resultado; TI/segurança; DPO |
| Expectativas sobre o produto | Espera o padrão dos dashboards que já usa: visão geral → drill-down → "como isso foi calculado" (Power BI) [H] |

**Decisões de design influenciadas por P02:**

- Indicador de confiança/qualidade do sinal visível — esse perfil rejeita caixa-preta (RC02, H02).
- Comparativo entre sessões no pós-sessão (o "ao longo do tempo" do TCC) para justificar mudanças de formato.
- Materiais de privacidade prontos (o-que-processamos) para ele defender a adoção junto à TI/DPO (RC05).


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
| Usuários | {{...}} | {{...}} |
| Tarefas | {{...}} | {{...}} |
| Equipamentos | {{...}} | {{...}} |
| Ambiente físico | {{...}} | {{...}} |
| Ambiente social/organizacional | {{...}} | {{...}} |
| Papéis/permissões/governança | {{...}} | {{...}} |
| Volume de dados/histórico | {{...}} | {{...}} |

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
