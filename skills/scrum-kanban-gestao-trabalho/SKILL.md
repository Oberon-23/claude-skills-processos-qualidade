---
name: "scrum-kanban-gestao-trabalho"
description: "Use para organizar e entregar trabalho com Scrum e Kanban: sprint, backlog, WIP, fluxo, métricas de fluxo, SLE, quadro, retrospectiva e escolher entre Scrum, Kanban ou os dois juntos."
---

# Scrum e Kanban para organizar e entregar trabalho

Ajude a pessoa a escolher entre Scrum, Kanban ou os dois juntos, montar a estrutura e usar os dados do próprio trabalho para melhorar. Responda em português do Brasil, em linguagem simples e com exemplos do contexto dela (equipe de TI, atendimento, projeto, estudo). Este guia é um resumo próprio, baseado nos guias oficiais: Scrum Guide (2020), Kanban Guide (maio de 2025) e Kanban Guide for Scrum Teams (2021). Recomende a leitura deles e, em dúvida sobre uma regra, confirme na versão vigente, sem reproduzir trechos.

## Princípios
- Scrum é um framework com responsabilidades, eventos e artefatos definidos, para entregar valor em ciclos curtos. Kanban é uma estratégia para otimizar o fluxo de valor; não define papéis nem ciclos.
- Os dois vivem de transparência, inspeção e adaptação. Decida com o que o trabalho mostra, não com opinião.
- Comece pelo que a equipe faz hoje e mude aos poucos.
- Ferramenta (Jira, Trello, Azure DevOps, planilha) não é método. Quadro sem regras explícitas e sem limite de WIP não é Kanban.
- Uma regra em nome do método só pode ser chamada de "obrigatória" se o guia a exige. O resto é prática sugerida: diga qual é qual.

## 1. Entender a situação
Pergunte só o essencial: tipo de trabalho (previsível ou imprevisível), tamanho e perfil da equipe, o que dói hoje (atraso, fila, retrabalho, prioridade mudando, falta de visibilidade) e que dados existem (datas de início e fim dos itens).

## 2. Escolher o caminho
| Situação | Caminho |
|---|---|
| Produto ou projeto com objetivo claro, entregas em partes e equipe estável | Scrum |
| Trabalho contínuo, pedidos que chegam o tempo todo, prioridade muda no dia (suporte, manutenção, operação) | Kanban |
| Já faz Scrum, mas a Sprint vira bagunça, itens ficam parados ou estouram | Scrum com práticas de Kanban |
| Sem método e sem vontade de cerimônia | Kanban, começando pelo quadro e pelo limite de WIP |

Não trate os dois como rivais. O Kanban Guide for Scrum Teams foi feito para somar ao Scrum, sem substituir nenhuma parte do Scrum Guide.

## 3. Scrum (Scrum Guide 2020)
**Um único time**, sem subtimes nem hierarquia: multifuncional, autogerenciado, em geral com até 10 pessoas. Se crescer demais, divida em times coesos que compartilham o mesmo objetivo e backlog do produto.
- **Developers**: fazem o trabalho do Incremento, criam o plano da Sprint, seguem a Definição de Pronto e ajustam o plano todo dia rumo à Meta da Sprint.
- **Product Owner** (uma pessoa, não um comitê): maximiza o valor do produto e cuida do Backlog do Produto: comunica a Meta do Produto, cria e ordena os itens, garante transparência. Pode delegar, mas segue responsável.
- **Scrum Master**: responsável por estabelecer o Scrum e a eficácia do time; ensina, remove impedimentos, garante que os eventos aconteçam dentro do tempo e ajuda o Product Owner e a organização.

**Eventos** (limites de tempo para uma Sprint de um mês; para Sprints menores, costumam ser menores):
| Evento | Propósito | Limite |
|---|---|---|
| Sprint | Contêiner de todos os eventos; duração fixa, nova Sprint começa logo após a anterior | Até 1 mês |
| Planejamento | Por que a Sprint é valiosa (Meta da Sprint), o que cabe e como será feito. A Meta deve estar definida até o fim do planejamento | 8 horas |
| Reunião diária | Inspecionar o avanço rumo à Meta e ajustar o plano; para os Developers, mesmo horário e local, formato livre | 15 minutos |
| Revisão | Inspecionar o resultado com quem tem interesse e ajustar o backlog; é sessão de trabalho, não só apresentação | 4 horas |
| Retrospectiva | Planejar melhorias em pessoas, interações, processos, ferramentas e Definição de Pronto | 3 horas |

Durante a Sprint: não faça mudanças que ponham a Meta em risco, não baixe a qualidade, refine o backlog conforme preciso e renegocie o escopo com o Product Owner. Só o Product Owner pode cancelar a Sprint, e só se a Meta ficar obsoleta.

**Artefatos e compromissos:**
- *Backlog do Produto* (compromisso: Meta do Produto): lista ordenada e emergente do que melhora o produto; refinamento contínuo, e os Developers estimam. Um item está pronto para o planejamento quando cabe em uma Sprint.
- *Backlog da Sprint* (compromisso: Meta da Sprint): Meta (por quê), itens escolhidos (o quê) e plano (como); é dos Developers e muda durante a Sprint.
- *Incremento* (compromisso: Definição de Pronto): passo concreto, verificado e utilizável rumo à Meta do Produto. Item que não cumpre a Definição de Pronto não entra no Incremento nem na Revisão e volta ao backlog. Se a organização tem uma definição padrão, ela é o mínimo.

## 4. Kanban (Kanban Guide 2025)
**Definição:** estratégia para otimizar o fluxo de valor por um processo, usada sobretudo em trabalho intelectual. O equilíbrio buscado é entre efetividade (entregar o que importa, quando importa), eficiência e previsibilidade.

**Três práticas que funcionam juntas:**
1. **Definir e visualizar o fluxo** (Definition of Workflow, DoW), em geral num quadro.
2. **Gerir ativamente os itens no fluxo**: controlar o WIP de forma explícita (puxar item novo só quando houver capacidade), evitar que itens envelheçam sem necessidade e desbloquear o que está travado.
3. **Melhorar o fluxo**: revisar o DoW de tempos em tempos e mudar quando os dados pedirem, sem esperar reunião formal.

**O DoW precisa ter, no mínimo:** (1) as unidades de valor (itens de trabalho); (2) critérios de início e fim; (3) um ou mais estados entre os dois (os itens nesses estados são o WIP); (4) como o WIP será controlado; (5) políticas explícitas de como o item passa por cada estado; (6) um SLE. Exceções ao controle de WIP também devem constar no DoW.

**SLE (Service Level Expectation):** previsão de quanto um item deve levar do início ao fim, com duas partes: um prazo e uma probabilidade (ex.: "85% dos itens em até N dias", com N medido no histórico). Sem histórico, comece com uma estimativa e revise quando houver dados. Deixe o SLE visível.

**Quatro métricas de fluxo (obrigatórias no guia):**
- **WIP**: itens iniciados e não terminados.
- **Vazão (throughput)**: itens terminados por unidade de tempo, contados.
- **Idade do item**: tempo desde o início até agora; só vale para itens em andamento e é a que avisa antes de o item atrasar.
- **Tempo de ciclo**: do início ao fim de um item.

O nome pode mudar (ex.: "tempo de fluxo"), o uso não. Métricas extras são bem-vindas. Use percentis em vez de média, porque o tempo costuma ter cauda longa.

Lei de Little: com a mesma vazão, mais itens ao mesmo tempo significam, em média, mais tempo para terminar cada um. Se o tempo de ciclo está alto, a primeira medida é reduzir o WIP.

Gráficos úteis: dispersão de tempo de ciclo (com linhas de percentil), diagrama de fluxo acumulado (faixas que se alargam mostram onde a fila cresce) e idade dos itens em andamento. Para checar estabilidade, use também a carta de controle da skill ferramentas-qualidade-melhoria-continua.

**Previsão:** com histórico de vazão ou de tempo de ciclo, dê faixas com probabilidade (ex.: "com X% de confiança, entre A e B") e não uma data única. Com poucos dados, avise que a previsão é frágil e diga o que coletar.

## 5. Scrum com Kanban (Kanban Guide for Scrum Teams)
O Scrum Guide continua valendo por inteiro. As quatro práticas, com os nomes do guia:
1. **Visualização do fluxo**: o quadro mostra onde o item é considerado iniciado e concluído, a definição dos itens, os estados do fluxo (ao menos um ativo), as políticas de cada estado e o limite de WIP.
2. **Limitar o WIP**: o time limita de forma explícita os itens em andamento e mantém o limite depois de definido; é o que cria o sistema puxado.
3. **Gestão ativa dos itens em andamento**: manter a entrada próxima à saída, evitar que itens envelheçam sem necessidade e agir rápido sobre os bloqueados, parados em fila ou que passam do SLE.
4. **Inspecionar e adaptar o DoW**, usando os eventos que o Scrum já tem. O DoW é do time: quem decide é o Scrum Team, não alguém de fora.

Não há evento novo. Como cada evento usa o Kanban:
- *Planejamento*: use vazão e tempo de ciclo históricos para entender a capacidade.
- *Reunião diária*: pelo quadro, olhando onde o fluxo falha (o que está bloqueado, lento ou além do SLE, e se o limite foi quebrado). O propósito dela não muda.
- *Revisão*: olhe as métricas, sobretudo a vazão, para falar de datas e do avanço da Meta do Produto.
- *Retrospectiva*: analise as métricas e o fluxo (ex.: diagrama de fluxo acumulado) e ajuste o DoW. Mudanças podem acontecer a qualquer hora, mas a retrospectiva dá a cadência.
- O Scrum exige ao menos um Incremento útil por Sprint, e o Kanban ajuda a achar gargalos e impedimentos.

## 6. Quando algo não funciona
| Sintoma | Causa provável | Ação |
|---|---|---|
| Sprint termina com muita coisa pela metade | Itens grandes, WIP alto | Quebrar itens, limitar WIP, terminar antes de começar |
| Prioridade muda todo dia | Meta da Sprint fraca ou backlog sem dono claro | Fortalecer a Meta e o Product Owner; definir regra para urgências no DoW |
| Quadro cheio, nada anda | Sem limite de WIP ou bloqueios ignorados | Definir WIP, rever itens velhos e bloqueados todo dia |
| Cerimônias viram reunião de status | Foco na pessoa e não no trabalho | Voltar à Meta e ao fluxo; cortar o que não gera decisão |
| Retrospectiva sem resultado | Ação sem dono ou prazo | Escolher 1 a 2 melhorias, cada uma com dono e prazo, e rever na próxima |
| Nunca fica "pronto" | Definição de Pronto vaga | Escrever critérios verificáveis |
| SLE sempre estourado | SLE chutado, WIP alto ou itens grandes | Recalcular com o histórico, reduzir WIP, quebrar itens |

## 7. Conexão com as outras skills
- Para mapear o fluxo antes de montar o quadro, use mapeamento-automacao-processos: SIPOC e fluxograma ajudam a definir os estados, e VA/BVA/NVA mostra onde há espera.
- Para achar a causa de itens que ficam presos ou voltam, use ferramentas-qualidade-melhoria-continua: Pareto dos motivos de bloqueio, Ishikawa, 5 Porquês e 5W2H.
- A retrospectiva é um PDCA curto: planejar a melhoria, executar na Sprint, checar com a métrica e agir.

## Formato da resposta
- Comece pelo caminho recomendado e o porquê, depois os detalhes. Tabela só para comparar.
- Para montar um quadro: estados com regra de entrada e de saída, definição de item, limite de WIP, SLE, tratamento de bloqueios e exceções. Entregue em tabela ou texto para colar na ferramenta.
- Para montar um Scrum: responsabilidades, duração da Sprint, calendário dos eventos dentro dos limites do guia, Definição de Pronto e modelo de Meta da Sprint.
- Suposições: liste tudo o que veio do contexto e não foi confirmado (tamanho do time, ferramenta, duração da Sprint, tipo de trabalho). Não invente números nem cite benchmarks de mercado sem fonte. Limite de WIP, SLE e percentis só com dados da equipe ou marcados como ponto de partida ilustrativo; o guia deixa o time escolher o limite, desde que explícito e mantido.
- Quando faltar dado, diga qual coletar: data de início e de fim de cada item, motivo de bloqueio e tipo de item.

## Cuidados
- Não venda Scrum ou Kanban como solução para tudo: se o problema é de processo, mapeie antes; se é de prioridade ou de pessoas, o quadro não resolve.
- Reunião diária não é relatório para o gestor.
- Vazão e velocidade não servem para comparar times nem para avaliar pessoas.
- Pontos de história são ferramenta de planejamento, não medida de produtividade; o tempo de ciclo medido costuma bastar.
- Mudar o método sem a equipe entender o porquê gera resistência: explique, combine e teste por um ciclo antes de decidir.
