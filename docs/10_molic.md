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

## M01 — {{nome do cenário/objetivo}}

**Autor(a):** {{nome — matrícula}}  
**Cenário de interação de origem:** {{CI01}}  
**Objetivo(s):** {{O01}}  
**Tarefa(s) relacionada(s):** {{T01}}  
**Signos relevantes:** {{...}}

### Diagrama

``` mermaid
flowchart TD
    INICIO((" "))

    CONSULTAR("`**Consultar resumo da reunião**
    Ver identificação da reunião {
    d: título, data }
    Examinar estados cognitivos {
    d: engajamento, tédio, confusão, frustração }
    Consultar visualização atual {
    d: indicadores exibidos }`")

    PERSONALIZAR("`**Personalizar visualização**
    Consultar opções de personalização {
    d: indicadores disponíveis }
    Definir informações do resumo {
    d+u: indicadores selecionados para exibição }`")

    SALVAR[" "]

    CONFERIR("`**Conferir resumo personalizado**
    Examinar resultado da personalização {
    d: indicadores exibidos, dados dos indicadores }
    Consultar configuração aplicada {
    d: seleção de indicadores salva }`")

    FIM(((" ")))

    INICIO -->|"u: abrir resumo da reunião; gco: Personalizar visualização do resumo"| CONSULTAR

    CONSULTAR -->|"u: personalizar visualização"| PERSONALIZAR

    PERSONALIZAR -->|"u: salvar alterações"| SALVAR

    SALVAR -->|"d: configuração salva e aplicada"| CONFERIR

    SALVAR -.->|"[SR] d: não foi possível salvar; seleções preservadas"| PERSONALIZAR

    PERSONALIZAR -.->|"u: cancelar alterações"| CONSULTAR

    CONFERIR -->|"u: editar novamente"| PERSONALIZAR

    CONFERIR -->|"gcc: Personalizar visualização do resumo"| FIM

    classDef processo fill:#000000,stroke:#000000;
    classDef abertura fill:#000000,stroke:#000000;
    class SALVAR processo;
    class INICIO abertura;
```


### Leitura do diagrama

#### Caminho principal

1. O docente abre o resumo da reunião. O marcador `gco: Personalizar visualização do resumo` identifica a abertura da conversa relacionada a esse objetivo.
2. Na cena **Consultar resumo da reunião**, o sistema apresenta o título, a data, os estados cognitivos e os indicadores atualmente exibidos.
3. Ao solicitar `u: personalizar visualização`, o docente acessa a cena **Personalizar visualização**, consulta os indicadores disponíveis e define quais deseja exibir. Essa seleção é representada por `d+u: indicadores selecionados para exibição`.
4. O docente solicita `u: salvar alterações`, iniciando o processo de salvamento pelo sistema.
5. Quando o salvamento é concluído, o sistema comunica `d: configuração salva e aplicada` e apresenta a cena **Conferir resumo personalizado**. O docente examina os indicadores exibidos, seus dados e a configuração salva.
6. Após a conferência, o marcador `gcc: Personalizar visualização do resumo` indica o encerramento da conversa sobre esse objetivo.

#### Alternativas e rupturas

| Situação | Onde ocorre | Como o usuário percebe | Caminho de recuperação/saída |
|---|---|---|---|
| Cancelamento da personalização | Na cena **Personalizar visualização**. | Após solicitar `u: cancelar alterações`, o docente retorna ao resumo com a configuração anterior. | As alterações não salvas são descartadas, sem confirmação, e o docente pode continuar consultando o resumo. |
| Falha no salvamento | No processo do sistema, após `u: salvar alterações`. | O sistema comunica `[SR] d: não foi possível salvar; seleções preservadas`. | O docente retorna à personalização com suas seleções preservadas e pode tentar salvar novamente, modificar a seleção ou cancelar. |
| Necessidade de novos ajustes | Na cena **Conferir resumo personalizado**. | Ao examinar o resultado, o docente identifica a necessidade de modificar a configuração e solicita `u: editar novamente`. | Retorna à personalização, ajusta os indicadores e realiza um novo salvamento antes de concluir a conferência. |

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
