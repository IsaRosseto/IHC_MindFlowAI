# Entrega 10 — MoLIC

**Data:** {{dd/mm/aaaa}}  
**Status:** ⬜ não iniciada  
**Responsabilidade:** 1 solução completa por integrante

## Objetivo da atividade

Modelar a interação como uma **conversa entre usuário e preposto do designer**, oferecendo visão global dos caminhos que permitem ao usuário atingir seus objetivos — incluindo alternativas e rupturas relevantes. MoLIC não deve ser reduzida a um fluxograma de telas.

> Use a **notação MoLIC ensinada na disciplina**. Este template foca critérios de qualidade e não substitui a legenda/notação apresentada em aula.

## Atenção a TCCs sem interface original

O MoLIC não modela o algoritmo por dentro. Ele modela a **conversa de interação necessária para que uma pessoa use a contribuição**.

Exemplos de conversas:

- usuário escolhe dados/parâmetros → sistema valida → usuário inicia análise → sistema comunica processamento → usuário interpreta resultado;
- usuário consulta histórico → refina filtros → abre execução → compara com outra;
- administrador seleciona perfil → altera permissão → sistema comunica consequências → administrador confirma/cancela;
- analista recebe alerta → examina evidências → classifica ocorrência → registra decisão.

Modele também rupturas plausíveis: entrada inválida, falha de processamento, ausência de resultado, permissão insuficiente, filtro sem resultados, conflito de alteração, cancelamento ou necessidade de recuperação.

## M01 — Consultar e personalizar o resumo de uma aula concluída

**Autor(a):** Kayky Pires — 22.222.040-2  
**Cenário de interação de origem:** CI01 — Acompanhar os estados da turma e revisar os resultados da aula, derivado do cenário de problema C02, relacionado à persona P01 — Karol.  
**Objetivo(s):** O01 — Personalizar a visualização do resumo da reunião; O05 — Avaliar a adequação da visualização personalizada; cobertura parcial de O03 — Analisar os resultados de uma aula concluída.  
**Tarefa(s) relacionada(s):** T01 — Personalizar a visualização dos resultados de uma aula concluída no MindFlow AI.  
**Signos relevantes:** título da reunião, data da reunião, indicador cognitivo, significado do indicador, valor do indicador, escala, disponibilidade de dados, seleção de indicadores e resultado do salvamento.


### Diagrama

flowchart TB

    INICIO((" "))

    REUNIOES("`**Selecionar um resumo**
    Consultar reuniões disponíveis {
    d: títulos, datas e situações }

    Identificar a reunião desejada {
    d: acesso ao resumo }`")

    CONSULTAR("`**Consultar e avaliar o resumo**
    Identificar a reunião {
    d: título, data }

    Examinar a visualização atual {
    d: indicadores, gráficos,
    disponibilidade de dados }

    Compreender as informações {
    d: significado dos indicadores }`")

    PERSONALIZAR("`**Personalizar visualização**
    Escolher e organizar os elementos {
    d+u: seleção, ordem e tamanho dos blocos }

    Identificar a visualização {
    d+u: nome da visualização }`")

    SALVAR[" "]

    CONFERIR("`**Conferir resumo personalizado**
    Reconhecer o salvamento {
    d: nome da visualização,
    confirmação de salvamento }

    Avaliar o resultado {
    d: configuração aplicada,
    indicadores e disponibilidade de dados }`")

    CONFIRMAR("`**Confirmar exclusão da visualização**
    Identificar a visualização salva {
    d: nome da visualização }

    Confirmar a intenção {
    d: Excluir a visualização selecionada? }`")

    EXCLUIR[" "]

    FIM(((" ")))

    INICIO -->|"u: acessar Minhas Reuniões"| REUNIOES

    REUNIOES -->|"`u: selecionar Ver resumo
    gco: Analisar os resultados de uma aula concluída`"| CONSULTAR

    CONSULTAR -->|"`u: voltar a Minhas Reuniões
    gcc: Analisar os resultados de uma aula concluída`"| REUNIOES

    CONSULTAR -->|"`visualização atende à necessidade
    gcc: Analisar os resultados de uma aula concluída`"| FIM

    CONSULTAR -->|"`u: Organizar dashboard
    gco: Personalizar a visualização do resumo da reunião`"| PERSONALIZAR

    PERSONALIZAR -->|"u: Salvar visualização"| SALVAR

    SALVAR -.->|"`nome não informado
    [SR] d: Dê um nome para a visualização`"| PERSONALIZAR

    SALVAR -->|"`d: visualização salva na sua conta
    gcc: Personalizar a visualização do resumo da reunião
    gco: Avaliar a adequação da visualização personalizada`"| CONFERIR

    PERSONALIZAR -.->|"`u: Cancelar
    gcc: Personalizar a visualização do resumo da reunião — abandonado`"| CONSULTAR

    CONFERIR -->|"`visualização atende à necessidade
    gcc: Avaliar a adequação da visualização personalizada
    gcc: Analisar os resultados de uma aula concluída`"| FIM

    CONFERIR -->|"`u: voltar a Minhas Reuniões
    gcc: Avaliar a adequação da visualização personalizada
    gcc: Analisar os resultados de uma aula concluída`"| REUNIOES

    CONFERIR -->|"`u: Organizar dashboard
    gcc: Avaliar a adequação da visualização personalizada
    gco: Personalizar a visualização do resumo da reunião`"| PERSONALIZAR

    PERSONALIZAR -->|"`precond: visualização já salva
    u: Excluir`"| CONFIRMAR

    CONFIRMAR -.->|"u: Cancelar"| PERSONALIZAR

    CONFIRMAR -->|"u: OK"| EXCLUIR

    EXCLUIR -->|"`d: visualização excluída
    gcc: Personalizar a visualização do resumo da reunião — abandonado`"| CONSULTAR

    classDef cena fill:#ffffff,stroke:#333333,stroke-width:1.5px,color:#111111;
    classDef processo fill:#000000,stroke:#000000,color:#000000;
    classDef abertura fill:#000000,stroke:#000000;
    classDef encerramento fill:#ffffff,stroke:#000000,stroke-width:2px;

    class REUNIOES,CONSULTAR,PERSONALIZAR,CONFERIR,CONFIRMAR cena;
    class SALVAR,EXCLUIR processo;
    class INICIO abertura;
    class FIM encerramento;



### Leitura do diagrama

#### Caminho principal

1. O usuário acessa **Minhas Reuniões**, consulta os títulos, as datas e as situações das reuniões e identifica aquela que deseja analisar.
2. Ao selecionar **Ver resumo**, inicia a conversa sobre **Analisar os resultados de uma aula concluída**.
3. Na cena **Consultar e avaliar o resumo**, examina a identificação da reunião, os indicadores, os gráficos, suas explicações e a disponibilidade de dados.
4. Ao identificar a necessidade de modificar a apresentação, solicita **Organizar dashboard**, iniciando a conversa sobre **Personalizar a visualização do resumo da reunião**.
5. Na cena **Personalizar visualização**, escolhe os blocos, ajusta sua ordem e seu tamanho e informa o nome da visualização.
6. O usuário solicita **Salvar visualização**. O processo do sistema verifica o preenchimento do nome e realiza a tentativa de salvamento.
7. Quando o salvamento é concluído, o sistema comunica **“Visualização salva na sua conta”** e apresenta o resumo com a configuração aplicada. Encerra-se a conversa sobre a personalização e inicia-se a avaliação da visualização personalizada.
8. Na cena **Conferir resumo personalizado**, o usuário verifica o resultado. Quando considera a visualização adequada, conclui a tarefa. Esse encerramento não exige um botão adicional nem representa sair da aplicação.

#### Alternativas e rupturas

| Situação | Onde ocorre | Como o usuário percebe | Caminho de recuperação/saída |
|---|---|---|---|
| A visualização inicial já atende à necessidade | Na cena **Consultar e avaliar o resumo**. | O usuário reconhece que as informações já estão apresentadas de forma adequada. | Conclui a tarefa sem iniciar a personalização. |
| Retorno a Minhas Reuniões | Nas cenas **Consultar e avaliar o resumo** e **Conferir resumo personalizado**. | O usuário decide voltar à lista de reuniões. | Solicita o retorno a **Minhas Reuniões** e pode selecionar outro resumo. As conversas abertas sobre a análise e, quando aplicável, a avaliação da visualização são encerradas. |
| Cancelamento da personalização | Na cena **Personalizar visualização**. | O usuário decide interromper a edição e seleciona **Cancelar**. | Retorna diretamente à consulta do resumo, sem concluir um novo salvamento. Não há confirmação de descarte nesse caminho. |
| Tentativa de salvar sem nome | No processo do sistema iniciado por **Salvar visualização**. | O sistema comunica **“Dê um nome para a visualização.”** | O editor permanece aberto com os blocos selecionados. O usuário informa o nome e solicita novamente o salvamento. A conferência do resumo personalizado somente é alcançada após o sucesso. |
| Necessidade de novos ajustes | Na cena **Conferir resumo personalizado**. | O usuário identifica que a configuração aplicada ainda precisa de modificações. | Seleciona **Organizar dashboard**, retorna à personalização e pode ajustar os elementos e salvar novamente. |
| Exclusão de uma visualização salva | Após abrir novamente o editor de uma visualização já salva e selecionar **Excluir**. | O sistema apresenta o nome da visualização e solicita a confirmação da exclusão. | Ao selecionar **Cancelar**, retorna ao editor sem excluir. Ao selecionar **OK**, o sistema realiza a exclusão e retorna à consulta do resumo. Essa confirmação corresponde à exclusão de uma visualização salva. |
| Ausência de dados | Nas cenas de consulta e conferência do resumo. | A interface apresenta mensagens como **“Sem leituras para esta reunião”** e **“Sem reações neste intervalo”**. | O usuário pode reconhecer a indisponibilidade, personalizar a apresentação ou retornar às reuniões. Esse estado não representa um erro de salvamento. |

### Checklist específico de modelagem

- [ ] Existe **ponto de abertura** coerente com o início do objetivo.
- [ ] As **cenas de conversa** representam tópicos/assuntos, não nomes de páginas apenas.
- [ ] As transições/falas deixam claro o que o usuário ou o sistema comunica.
- [ ] Há **ponto(s) de encerramento** para objetivos concluídos/abandonados quando aplicável.
- [ ] Processamentos do sistema estão representados conforme a notação adotada em aula, sem “inventar” fala do usuário.
- [ ] Rupturas (breakdowns) relevantes têm feedback e caminho de recuperação, não becos sem saída.
- [ ] Acessos ubíquos/atalhos só aparecem quando semanticamente justificáveis.
- [ ] O diagrama cobre caminhos alternativos importantes, e não apenas o “happy path”.
- [ ] Nomes de objetivos, tópicos e signos são coerentes com a Entrega 9.
- [ ] O diagrama é legível em tamanho normal no GitHub.
- [ ] O MoLIC representa a conversa usuário–sistema, não o fluxo interno do algoritmo.
- [ ] Processamento, filtros, administração, relatórios e históricos incluem retornos/rupturas quando relevantes.

> Repita M02, M03... para todos os integrantes.

## Consolidação da equipe

### Cobertura dos objetivos

| Objetivo | MoLIC que cobre | Lacunas/duplicidades | Decisão |
|---|---|---|---|
| O01 | M01 | O diagrama contempla consulta, seleção de indicadores, salvamento, conferência e recuperação de falha. Não há duplicidades identificadas neste recorte. Falta um encerramento explícito para quem decide sair sem salvar. | Manter o M01 para a personalização do resumo, com cancelamento direto e preservação das seleções em caso de falha. Registrar a saída sem salvar como lacuna desta versão. |

### Preparação para o Figma

Liste os estados/telas que serão necessários **a partir das conversas modeladas**, incluindo feedback, confirmação, erro e recuperação.

## Erros frequentes a evitar

- desenhar apenas caixas com nomes de telas e setas de navegação;
- não modelar falhas, cancelamento, volta ou recuperação;
- usar rótulos genéricos (“Tela 1”, “Processo 2”) sem tópico de conversa;
- criar no Figma fluxos que não existem no MoLIC;
- diagrama sem legenda/fonte editável e com texto ilegível.
