---
name: "mapeamento-automacao-processos"
description: "Use para mapear, analisar, redesenhar e automatizar processos (BPM/CBOK): SIPOC, BPMN, fluxograma, VSM, valor agregado, tempo de ciclo, mudas, métricas, RPA/BPMS e priorização. Inclui achar gargalos e onde automatizar um fluxo de trabalho, como o atendimento de chamados, e gerar o diagrama em arquivo .bpmn."
---

# Mapeamento, análise e automação de processos

Responda em português do Brasil, em linguagem simples e com exemplos do contexto da pessoa. Este guia é um resumo próprio de práticas consolidadas de gestão de processos. Para aprofundar, recomende como leitura o BPM CBOK (ABPMP), *Fundamentals of Business Process Management* (Dumas et al.), Falconi e Imai, sem reproduzir trechos dessas obras.

## Antes de mapear
- Olhe o processo pelo lado de quem recebe o resultado, de ponta a ponta, e envolva quem executa: mudar processo é tanto sobre pessoas quanto sobre fluxo.
- Classifique o processo: entrega valor direto ao cliente (primário), apoia outros processos (suporte) ou governa e mede (gestão). A classificação depende de quem é o dono; se não estiver claro, coloque nas suposições.
- Se o pedido já diz onde o processo começa e termina, faça o primeiro mapa com as suposições marcadas e pergunte o que faltar no fim. Se não diz, pergunte no máximo 4 coisas: gatilho e entrega, quem participa (pessoas, áreas, sistemas), qual é a dor e qual é o volume. Processo grande: divida em subprocessos.
- Com vários processos candidatos, priorize por impacto no cliente, no resultado financeiro e em outras áreas (matriz 2x2 ou pontuação).

## Notação
Escolha e diga em uma linha por quê.
- **SIPOC**: visão de uma página (fornecedores, entradas, 5 a 7 etapas, saídas, clientes); serve para alinhar o escopo.
- **Fluxograma**: rápido, para o caminho principal.
- **Raias**: mostram quem faz cada etapa e onde há repasse; combinam com qualquer notação.
- **BPMN 2.0**: para detalhar decisões, eventos de tempo e de mensagem, exceções, subprocessos e laços.
- **VSM**: quando o foco é tempo e espera por etapa.

Níveis de detalhe: visão geral, processo ponta a ponta, fluxo de trabalho e passos da tarefa. Nomeie tarefas com verbo + objeto, rotule as saídas das decisões e use um só nome para cada coisa. Mapeie o que acontece de fato, não o que o manual diz, e valide com quem executa.

## Coletar dados
Entrevistas e observação com quem executa, documentos, relatórios e registros do sistema. Se a ferramenta guarda o histórico de estados com data e hora, use-o para medir os tempos reais e achar desvios (mineração de processos).

## Analisar o AS-IS
**Qualitativa**
- Classifique cada etapa: gera valor para o cliente (VA), é necessária para o negócio, como controle ou registro (BVA), ou é desperdício, como espera, retrabalho e repasse desnecessário (NVA). Elimine o desperdício e enxugue o necessário com cuidado.
- Cite os tipos de desperdício que aparecerem (espera, retrabalho, processamento em excesso, movimentação, transporte, estoque, superprodução), sem listar os que não se aplicam.
- Para causa raiz e priorização, use a skill ferramentas-qualidade-melhoria-continua.
- Para cada ponto de controle, pergunte o que acontece se ele falhar.

**Quantitativa** (só com dados; se faltarem, diga o que medir)
- Dimensões: tempo, custo, qualidade e capacidade ou flexibilidade.
- Tempo de ciclo e eficiência = tempo de trabalho efetivo ÷ tempo total (mostra quanto é espera).
- Lei de Little: itens em andamento = taxa de chegada × tempo de ciclo.
- Recurso muito ocupado gera fila longa.
- Simulação ou "e se o volume dobrar?" quando a decisão depender disso.

Cuidados: não desenhe a solução durante a análise (anote as ideias à parte); detalhe só o que muda a decisão; fale das atividades, não do valor do trabalho das pessoas. Destaque os 3 problemas de maior impacto.

## Desenhar o TO-BE
Ideias de redesenho, use as que couberem: menos repasses entre áreas; um só ponto de contato para o cliente; coletar cada informação uma vez, na origem; pedir antes o que vai faltar depois; trilhas separadas para casos simples e complexos; etapas em paralelo; juntar ou eliminar tarefas; qualidade logo no início; padronizar. Defina primeiro o que precisa acontecer, depois quem faz e com qual ferramenta.

Toda melhoria cobra algo: ganhar em tempo, custo, qualidade ou flexibilidade costuma piorar outra dimensão. Diga qual é o trade-off. Compare com o AS-IS, proponha um piloto e cuide da mudança com as pessoas.

## Automatizar
Simplifique e padronize antes de automatizar: automatizar um processo ruim só deixa o erro mais rápido. Às vezes treinamento ou redesenho bastam.

Escada, da mais simples: configuração e regras da própria ferramenta, planilhas e macros, Power Query, Power Automate, scripts Python ou SQL, RPA, BPMS ou sistema dedicado. Pare no degrau que resolve.

**RPA** combina com tarefa manual e repetitiva, regras claras, dados digitais e estruturados, poucas exceções, volume constante e processo estável. Não combina com julgamento, entrada não estruturada, papel ou processo que muda muito. Decida por custo total e retorno, comece com robôs simples e envolva TI e segurança desde o início.

**BPMS** serve quando o próprio modelo deve conduzir o trabalho: distribuir tarefas, fazer cumprir regras e monitorar. Pesam a integração com sistemas antigos e a resistência à mudança.

## Medir e sustentar
Defina o indicador e a linha de base antes de mudar. Use poucos indicadores, com dono, meta, fórmula clara e revisão periódica; na rotina, cubra qualidade, custo, prazo, pessoas e segurança. Sustente com dono do processo, padrão treinado, modelos atualizados e ciclo de melhoria (skill ferramentas-qualidade-melhoria-continua).

## Formato da resposta
- Comece pelo resultado, depois os detalhes. Tabelas só para comparar.
- **Pedido de mapeamento** ("mapeia o processo", "onde dá para automatizar"): siga a ordem, mesmo resumida: escopo e tipo de processo, SIPOC, diagrama, AS-IS (VA/BVA/NVA e desperdícios), gargalos, TO-BE com trade-off, automação com critério, suposições e dados a medir.
- **Pedido de um item só** (ex.: só o diagrama): entregue esse item com um resumo curto (escopo, etapas, suposições), sem SIPOC nem análise completa.
- **Pedido que também quer causa e plano** (ex.: reabertura alta): leia a skill ferramentas-qualidade-melhoria-continua, faça uma única rodada de perguntas, defina o indicador (fórmula e linha de base) e siga: mapa, causas, PDCA e controle.
- **Suposições**: liste tudo o que veio do contexto e não foi confirmado, como ferramenta, níveis de atendimento, canais, prazos e tipo de processo. Não invente números e não cite faixas "típicas" de mercado (prazos, custos, percentuais) sem fonte. Se usar uma estimativa, marque-a como ilustrativa no próprio trecho e repita nas suposições.
- **Diagramas**: Mermaid na conversa. Arquivo .bpmn quando pedido ou útil: BPMN 2.0 com raias e desenho (BPMNDI), com o gargalo e a automação de cada tarefa no campo Documentation e os gateways exclusivos com o marcador visível (isMarkerVisible="true"). Valide o XML por script e tente sempre renderizar (ex.: bpmn-js em navegador headless) e olhar a imagem antes de entregar; corrija sobreposições e setas cruzadas. Diga o que foi conferido e o que não foi. Indique abrir em demo.bpmn.io ou no Camunda Modeler.