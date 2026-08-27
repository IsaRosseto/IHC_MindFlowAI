# Entrega 2 — Público-alvo e análise de concorrência

**Data:** 26/08/2026  
**Status:** 🟨 em andamento  
**Responsabilidade mínima:** cada integrante analisa pelo menos 1 concorrente/interface representativa; a equipe produz síntese comparativa.

## Objetivo da atividade

Compreender soluções do mesmo domínio **e também interfaces familiares ao público-alvo**. O objetivo não é copiar telas, mas identificar convenções, padrões, affordances percebidas, problemas recorrentes, expectativas e oportunidades de design.

> **Concorrente não precisa ser idêntico ao produto.** Pode atuar na mesma área, resolver objetivo semelhante ou disputar a mesma necessidade. Quando não houver concorrente direto, use produtos análogos e softwares que o público já utiliza.

### Para TCCs que não previam interface

Não procure apenas um "concorrente do algoritmo". Investigue **interfaces profissionais que materializam atividades semelhantes** às que o usuário escolhido precisaria realizar.

Exemplos:

- TCC de banco de dados → consoles de administração, ferramentas para DBA, monitoramento e análise de consultas;
- TCC de LLM/ML → painéis de experimentos, gestão de modelos/datasets, comparação de métricas, revisão de resultados;
- TCC de análise de dados → dashboards, ferramentas de BI, filtros, relatórios e exploração;
- TCC de infraestrutura/API → portais administrativos, observabilidade, logs, gestão de credenciais e uso;
- TCC de cibersegurança → consoles de alertas, triagem, histórico e auditoria.

A pergunta é: **"que convenções esse perfil já conhece para executar tarefas equivalentes?"**

## Entrada obrigatória da Entrega 1

Retome o mapa inicial de alternativas e produtos citado na Entrega 1. Aqui a equipe deixa de trabalhar apenas com impressão inicial e passa a **investigar sistematicamente** cada solução.

| Item citado na Entrega 1 | Tipo | Por que foi citado | Status inicial | Decisão nesta entrega |
|---|---|---|---|---|
| Reações por emoji manuais (Zoom, Google Meet, Teams) | ferramenta cotidiana | Citada na Entrega 1 como alternativa que o comunicador já usa hoje pra sentir o clima da reunião | F | analisar |

Se uma hipótese da Entrega 1 for confirmada ou refutada durante esta análise, atualize `H01`, `H02`... em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

## 1. Público-alvo desta análise

Professores, palestrantes e facilitadores que conduzem sessões de videoconferência e precisam perceber o estado do grupo em tempo real, sem tirar a atenção da própria condução da sessão, o mesmo comunicador definido como usuário prioritário na Entrega 1.

## 2. Concorrentes diretos/indiretos

### Análise C01 — Reações por emoji manuais (Zoom / Google Meet / Teams)

**Autor(a):** Isabella Rosseto - 22.222.036-0
**Tipo:** análogo  
**Link oficial:** [Zoom Support](https://support.zoom.com/) e [Google Meet Help](https://support.google.com/meet/)  
**Data de acesso:** 27/08/2026

#### Contexto e proposta

> As reações por emoji são um recurso nativo das principais plataformas de videoconferência (Zoom, Google Meet, Microsoft Teams). A proposta é simples, o participante clica num ícone (aplausos, joinha, mão levantada etc.) e esse ícone aparece brevemente pra todo mundo ver, sem precisar interromper quem está falando. É a forma mais comum hoje de dar um sinal não verbal numa reunião online, e foi o que a equipe já tinha citado como alternativa atual na Entrega 1.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Reação temporária | No Zoom, o participante clica no botão Reactions e escolhe entre 11 emojis padrão. O ícone aparece do lado do nome do participante na lista e some sozinho depois de 10 segundos | <img width="760" height="403" alt="image" src="https://github.com/user-attachments/assets/4d31f18c-af59-4ecc-b870-219208295ba9" />| O tempo curto (10s) evita poluir a tela, mas também significa que se o comunicador não estiver olhando naquele instante, perde o sinal |
| Reação persistente | Ícones como "Levantar a mão" e "Sim/Não" ficam fixos até o próprio participante ou o host removerem manualmente | <img width="520" height="196" alt="image" src="https://github.com/user-attachments/assets/cb7e820a-3761-4ff0-b021-20d973e899f6" /> | Só esse tipo de reação dá um sinal confiável de estado sustentado, o resto é só um pulso rápido |
| Contagem agregada por ícone | O Zoom mostra, acima de cada ícone, o número total de pessoas que reagiram daquele jeito |<img width="306" height="470" alt="image" src="https://github.com/user-attachments/assets/ebfb6ffa-74d2-45fd-bc0a-79b7413002ea" /> | É o único lugar onde existe uma leitura agregada do grupo, mas só conta quem decidiu clicar, não reflete quem está de fato engajado ou confuso |
| Badge no vídeo + explosão de emoji na tela | No Google Meet, a reação aparece como um selo no canto do vídeo da pessoa e sobe flutuando pela tela, com várias reações ao mesmo tempo aparecendo como uma explosão de emojis | <img width="239" height="226" alt="image" src="https://github.com/user-attachments/assets/63039f19-0b4d-4582-9575-54e328c94cc6" /> | Reforça a reação como algo visual e rápido, mas ainda depende inteiramente de ação manual do participante |

#### Experiência do usuário e opiniões

Use avaliações públicas, relatos, estudos, testes próprios ou outra fonte identificável. Não trate opinião isolada como verdade universal.

> Segundo a própria documentação do Google Workspace, o objetivo declarado das reações é oferecer uma forma leve e não disruptiva de participar da reunião sem interromper quem está falando. Não achamos, nessa busca inicial, pesquisa de usuário publicada medindo se essa forma de sinal realmente ajuda o apresentador a perceber o clima do grupo, fica como uma lacuna a investigar melhor.


#### Padrões e tendências percebidos

> Ícone pequeno, temporário e não bloqueante é o padrão dominante. A diferença entre reação temporária (10 segundos, some sozinha) e persistente (fica até alguém remover) parece ser a única forma que essas plataformas já usam pra distinguir reação pontual de estado sustentado, o que é justamente o problema que o Semáforo Cognitivo do MindFlow tenta resolver de um jeito automático, sem depender do participante escolher manter o ícone ativo.

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| Reação some sozinha em poucos segundos, não polui a tela | Zoom, expiração de 10s | O Semáforo Cognitivo também deveria evitar acumular informação antiga na tela, sempre mostrar o estado mais recente |
| Contagem agregada acima de cada ícone já é um padrão aceito pra ler o grupo de relance | Zoom, contador por ícone | Reforça que um resumo agregado simples, tipo porcentagem do grupo em cada estado, é uma leitura que esse público já sabe interpretar |
| Depende inteiramente de ação manual do participante | Descrição de uso em ambas plataformas | É exatamente a limitação que o MindFlow resolve ao captar sinal passivo pela webcam, sem exigir clique de ninguém |
| Host pode ligar/desligar o recurso pra reunião inteira | Toggle de reações do Google Meet | O MindFlow provavelmente também vai precisar de um controle parecido, dar ao comunicador a opção de ativar ou não o Semáforo Cognitivo numa sessão específica |

> Repita a subseção para C02, C03... até atender à quantidade da equipe.

## 3. Softwares que o público-alvo usa no cotidiano

Analise interfaces que moldam a expectativa do público, mesmo que não sejam concorrentes.

| Software | Por que o público usa | Padrões relevantes | Prints | O que aprender |
|---|---|---|---|---|
| Microsoft Teams | Pra realizar aulas, reuniões e compartilhar materiais | Menus laterais, abas, ícones conhecidos e organização dos participantes | <img width="1920" height="1241" alt="image" src="https://github.com/user-attachments/assets/eb4e12aa-3326-4898-b206-cf8fd79209ab" /> | Manter navegação simples e informações importantes de fácil acesso |
| Google Meet | Pra realizar videoconferências e aulas online | Interface limpa, poucos controles e ações principais bem destacadas | <img width="1600" height="1100" alt="image" src="https://github.com/user-attachments/assets/0e0b0ba6-688e-4438-86b0-089ffaa6fa94" /> | Evitar excesso de informações e priorizar as funções principais |
| Mentimeter / Slido | Pra medir compreensão do público em um momento específico da aula ou apresentação | Tela cheia com resultado em tempo real (barra, nuvem de palavras), geralmente compartilhada com o público |<img width="1280" height="713" alt="image" src="https://github.com/user-attachments/assets/f598c146-9a0c-4ba3-81e6-67cc66910b14" /> | Mostra que esse público já está acostumado a interromper a sessão pra checar entendimento, o MindFlow se diferencia por não precisar dessa pausa |

## 3.1 Padrões de interface relevantes ao escopo de IHC

Registre somente padrões encontrados nas soluções analisadas e que possam ter relação com objetivos reais da equipe.

| Padrão observado | Produto(s) | Para qual tarefa serve | Vantagem percebida | Risco/limitação | Aplicável ao nosso escopo? |
|---|---|---|---|---|---|
| dashboard | não identificado nesta análise | | | | não |
| relatório | não identificado nesta análise | | | | não |
| histórico + filtros | não identificado nesta análise | | | | não |
| administração/CRUD | não identificado nesta análise | | | | não |
| comparação de resultados | não identificado nesta análise | | | | não |
| indicador temporário/persistente por ícone | Zoom, Google Meet, Teams | Sinalizar um estado pontual ou sustentado sem interromper a fala | Leve, rápido de reconhecer, já é familiar pro público | Depende de ação manual, capta só quem se manifesta | talvez, como referência de linguagem visual, não como mecanismo de captação |
| contagem agregada por tipo de reação | Zoom | Dar uma leitura rápida de quantas pessoas reagiram de cada jeito | Fácil de ler de relance, sem precisar abrir outra tela | Só reflete quem clicou, não o grupo todo | sim, como inspiração pra exibir o "clima" agregado do grupo |

> O objetivo não é concluir "todo concorrente tem dashboard, então teremos um". O padrão só será adotado se apoiar uma tarefa rastreável.

## 4. Síntese comparativa da equipe

| Critério | C04 - Reações por emoji | C02 | C03 | Oportunidade para o projeto |
|---|---|---|---|---|
| Navegação | Barra de reações fixa nos controles da chamada, acesso direto sem menu extra | | | Manter o Semáforo Cognitivo dentro do próprio fluxo da chamada, sem exigir troca de tela |
| Feedback/estado | Ícone temporário (some em 10s) ou persistente (fica até remover), com contagem agregada por tipo | | | Usar um indicador automático e contínuo, em vez de depender do participante escolher reagir |
| Prevenção/recuperação de erro | Participante pode remover a própria reação; host pode limpar todas de uma vez | | | Pensar em como o comunicador poderia "corrigir" ou ignorar um alerta que pareça equivocado |
| Terminologia | Nomes de emoji comuns, linguagem do dia a dia | | | Usar linguagem simples nos rótulos dos estados, evitando termo técnico de IA |
| Acessibilidade | Depende de clique manual, pode ser barreira pra quem tem limitação motora | | | O MindFlow evita essa barreira por não depender de ação alguma do participante |
| Eficiência | Leitura rápida do ícone, mas exige ação ativa do participante a cada sinal | | | Buscar a mesma leitura rápida, sem exigir nenhuma ação do participante |

## 5. Recomendações derivadas

Liste recomendações com origem explícita.

- **RC01:** Não depender de ação manual do participante pra gerar o sinal, diferente das reações por emoji, que exigem clique a cada sinal. O MindFlow deve manter o sinal passivo captado pela webcam, derivada de **C01 (Reações por emoji)**.
- **RC02:** Evitar acumular informação antiga na tela do Semáforo Cognitivo, sempre mostrar o estado mais recente, do mesmo jeito que a reação temporária do Zoom some sozinha depois de alguns segundos, derivada de **C01 (Reações por emoji)**.
- **RC03:** Oferecer ao comunicador um controle simples pra ligar ou desligar o Semáforo Cognitivo na sessão, do mesmo jeito que o host pode ligar ou desligar as reações no Google Meet, derivada de **C01 (Reações por emoji)**.

## Referências

- Zoom Support. Reactions in a Zoom Meeting. https://support.zoom.com/ (acesso em 27/08/2026)
- Google Meet Help. Use reactions in a video call. https://support.google.com/meet/ (acesso em 27/08/2026)

## Checklist

- [x] O mapa inicial de alternativas da Entrega 1 foi revisitado e aprofundado.
- [ ] Hipóteses relevantes sobre mercado/padrões foram atualizadas na rastreabilidade quando surgiram evidências.
- [ ] Há pelo menos uma análise completa por integrante. *(só essa análise foi feita até agora, faltam as dos outros integrantes)*
- [ ] Cada análise contém prints legíveis da interface. *(prints marcados como PENDENTE, equipe vai anexar)*
- [ ] Prints mostram telas/estados relevantes, não apenas logos/homepage. *(depende dos prints que a equipe ainda vai anexar)*
- [x] Foram analisados concorrentes e/ou interfaces representativas ao público.
- [x] Em TCC sem interface original, foram investigadas ferramentas profissionais análogas às atividades do usuário escolhido. *(não se aplica integralmente, já que o TCC previa interface, mas mesmo assim analisamos um análogo)*
- [x] Padrões como dashboard, relatório, filtros e CRUD foram analisados como soluções para tarefas, não como requisitos automáticos.
- [x] Opiniões de UX têm fonte. *(quando não havia fonte confiável, marcamos explicitamente como lacuna, em vez de inventar opinião)*
- [ ] A síntese compara critérios comuns e produz recomendações. *(só a coluna C01 está preenchida, falta completar C02 e C03 com outros concorrentes)*
- [x] Não há "copiar porque o concorrente faz"; há justificativa de adequação ao público/contexto.
