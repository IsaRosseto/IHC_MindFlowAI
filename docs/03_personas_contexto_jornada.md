# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** {{dd/mm/aaaa}  
**Status:** ⬜ não iniciada  
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

### Persona P05 — Bruno D. Roger

**Autor(a):** Gustavo Bertoluzzi Cardoso - 22.123.016-2  
**Tipo:** secundária  
**Base de evidências:** proto-persona a validar. A gente já tinha percebido lá na Entrega 1 que o aluno que participa da chamada é afetado pelo sistema mas não chega a usar a interface, então essa persona vem daí  
**Hipóteses da Entrega 1 relacionadas:** H03

<img width="450" alt="Gemini_Generated_Image_nocb3hnocb3hnocb" src="https://github.com/user-attachments/assets/1ea7d2ce-5920-4bab-874f-091bec03ca7a" />

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | 20 anos, aluno de graduação que assiste aula por videoconferência como parte de uma disciplina EAD |
| Ocupação/papel | Participante da chamada, ele que fornece os dados captados pela webcam, mas quem usa a tela do MindFlow é o professor, não ele |
| Conhecimento do domínio | Conhecimento baixo ou médio do conteúdo da matéria, afinal ele tá ali pra aprender |
| Experiência tecnológica | Usa Zoom, Meet e vídeo chamada o tempo todo no celular, mas nunca ouviu falar de um sistema que analisa expressão facial durante aula |
| Objetivos | Acompanhar a aula, entender o conteúdo e conseguir tirar dúvida quando precisa |
| Necessidades | Saber o que é feito com a imagem dele captada pela câmera e sentir que assistir aula não é a mesma coisa que estar sendo vigiado |
| Dores/frustrações | Fica incomodado de pensar que o rosto dele pode estar sendo analisado por um sistema sem saber direito o que tá sendo medido. Tem medo de que parecer confuso ou parecer desatento vire algum tipo de avaliação sobre ele, mesmo sabendo que o resultado é só um número agregado da turma inteira |
| Motivadores | Aprender direito o conteúdo e ter a privacidade dele respeitada durante a aula |
| Restrições/acessibilidade | Pode escolher deixar a câmera desligada, mas às vezes isso depende da regra do professor ou da instituição |
| Ambiente típico de uso | Assiste aula de casa, no quarto ou num espaço dividido com a família, usando notebook ou até celular |
| Comportamentos relevantes | Liga e desliga a câmera dependendo de como tá se sentindo naquele dia, fica mais retraído quando sabe que tem algo analisando ele e provavelmente nunca ouviu falar do Semáforo Cognitivo, porque essa tela é só do professor |

**Decisões de design influenciadas por P05:**

- Reforça que precisa existir algum aviso pro aluno de que a aula está sendo classificada, mesmo que ele nunca veja o resultado
- Confirma que o resultado do sistema tem que ficar agregado, sem apontar aluno específico, pra não virar avaliação individual
- Ajuda a justificar o processamento local no próprio dispositivo, não só pela LGPD, mas também pra diminuir a sensação de estar sendo vigiado
- Levanta uma dúvida pra investigar depois, se desligar a câmera pode prejudicar o aluno de alguma forma


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
