# Etapa 5 Busca e triagem dos artigos

## Solicitação

Registre as buscas realizadas e justifique a inclusão ou exclusão de cada artigo.

## Registro das buscas

| Base | String usada | Data | Filtros | Resultados encontrados | Responsável |
|---|---|---|---|---:|---|
| `Google Scholar` | `1 — ("Dijkstra's algorithm" OR "Dijkstra*") AND ("time-dependent" OR "dynamic traffic") AND ("shortest path")` | `10/09/2026` | `2016–2026; demais critérios aplicados na triagem` | `≈ 2.400` | `Brayan Allan Nagatani Campos de Almeida` |
| `ScienceDirect (Elsevier)` | `2 — ("bidirectional Dijkstra" OR "time-dependent Dijkstra") AND ("complexity" OR "scalability" OR "memory") AND ("urban network*" OR "routing")` | `10/09/2026` | `2016–2026; demais critérios aplicados na triagem` | `≈ 60` | `Carlos Eduardo Laera Prado` |
| `ACM Digital Library` | `1 — ("Dijkstra's algorithm" OR "Dijkstra*") AND ("time-dependent" OR "dynamic traffic") AND ("shortest path")` | `10/09/2026` | `2016–2026; demais critérios aplicados na triagem` | `≈ 70` | `Gabriel Souza de Carvalho` |
| `IEEE Xplore` | `3 — ("Dijkstra") AND ("dependente do tempo" OR "bidirecional" OR "tráfego dinâmico") AND ("caminho mínimo" OR "escalabilidade")` | `10/09/2026` | `2016–2026; demais critérios aplicados na triagem` | `≈ 3` | `Pedro Henrique dos Santos` |

**Total de resultados encontrados:** `≈ 2.533`

## Resumo da triagem

- Total de resultados encontrados: `2.533`
- Duplicatas removidas: `130`
- Artigos avaliados por título e resumo: `2.403`
- Artigos selecionados para leitura completa: `13`
- Artigos incluídos no conjunto final: `4`

## Decisões

| Artigo | Título e resumo | Texto completo | Motivo da exclusão ou inclusão |
|---|---|---|---|
| `Constantinou et al. (2016)` | `Incluir` | `Aprovar` | `Aborda diretamente o problema de caminho mínimo em redes de transporte com velocidades dependentes do tempo e apresenta análise formal da complexidade do Dijkstra Dependente do Tempo.` |
| `Baum et al. (2016)` | `Incluir` | `Aprovar` | `Analisa roteamento em redes rodoviárias dependentes do tempo, incluindo abordagem bidirecional, com foco no comportamento algorítmico e na escalabilidade.` |
| `Heni, Coelho e Renaud (2019)` | `Incluir` | `Aprovar` | `Analisa caminhos mínimos dependentes do tempo por meio de uma adaptação do Dijkstra label-setting, considerando propriedades teóricas e desempenho computacional do problema.` |
| `Sun, Li e Liu (2023)` | `Incluir` | `Aprovar` | `Formula o problema de caminho mínimo em redes de transporte estocásticas e dependentes do tempo, considerando atrasos em interseções semaforizadas e utilizando Dijkstra na resolução.` |
| `9 artigos excluídos na leitura completa` | `Dúvida/Incluir` | `Excluir` | `Excluídos após leitura detalhada por incompatibilidade com os critérios definidos, principalmente por uso de A* ou heurísticas, aplicação a TSP/VRP ou problemas de múltiplas entregas, ausência de análise teórica suficiente ou inadequação do domínio/dinâmica temporal.` |

## Produto da etapa

Conjunto definitivo de artigos e registro das decisões.

## Checklist

- [x] Todas as buscas possuem data e string.
- [x] As duplicatas foram removidas.
- [x] Os critérios foram aplicados igualmente.
- [x] Toda exclusão possui justificativa.
- [x] Os artigos finais estão diretamente ligados ao problema.