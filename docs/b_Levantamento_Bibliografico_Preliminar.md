# Etapa (b) — Levantamento Bibliográfico

> **Como preencher:** este documento deve ser preenchido **em conjunto pelo grupo**, mas com registro individualizado da contribuição de cada integrante em cada passo. Substitua os campos entre `[ ]` pelas informações do seu grupo. Não apague as instruções em itálico — elas ajudam na avaliação do orientador.

---

## 1. Identificação do Grupo

| Campo | Informação |
|---|---|
| Curso / Disciplina | Ciência da Computação / Computabilidade e Complexidade de Algoritmos |
| Projeto de Pesquisa / IC | Grafos e Roteamento Urbano |
| Orientador(a) | Profa. Dra. Andréa Ono Sakai |
| Data de entrega desta etapa | 12/09/2026 |
| Integrantes do grupo | Gabriel Souza de Carvalho, Pedro Henrique dos Santos, Carlos Eduardo Laera Prado, Brayan Allan Nagatani Campos de Almeida, João Marcelo El Hafi Batista |
| Tema (da etapa "a") | Complexidade e escalabilidade de Dijkstra e variantes dependentes do tempo em redes urbanas |

---

## FASE 1 — Planejamento da Busca

### Passo 1 — Pergunta de pesquisa e palavras-chave

**1.1 Problema/pergunta de pesquisa (versão de trabalho)**
*Ainda não precisa ser a versão final (isso vem na etapa "c"), mas deve orientar a busca desta fase.*

> Como a literatura caracteriza complexidade, memória e escalabilidade de Dijkstra e suas variantes (dependente do tempo e bidirecional) na busca pelo caminho mínimo em redes urbanas dinâmicas?

**1.2 Conceitos-chave e sinônimos**
*Liste os conceitos centrais da pergunta e seus sinônimos, em português e inglês.*

| Conceito-chave | Sinônimos / termos relacionados (PT) | Sinônimos / termos relacionados (EN) |
|---|---|---|
| `Algoritmo de Dijkstra` | `Variantes de Dijkstra, Dijkstra dependente do tempo, Dijkstra bidirecional` | `Dijkstra's algorithm, time-dependent Dijkstra, bidirectional Dijkstra` |
| `Redes Urbanas Dinâmicas` | `Tráfego variável, roteamento urbano, tráfego dependente do tempo` | `Dynamic urban networks, variable traffic, time-dependent traffic, urban routing` |
| `Caminho Mínimo` | `Menor caminho, rota mais curta, otimização de rotas` | `Shortest path, routing, route optimization` |
| `Complexidade e Desempenho` | `Escalabilidade, uso de memória, custo computacional, tempo de resposta` | `Algorithmic complexity, scalability, memory usage, computational cost, response time` |

*Responsável por este passo: Gabriel Souza de Carvalho*

---

### Passo 2 — Strings de busca

*Combine os termos do passo 1 com operadores booleanos (`AND`, `OR`, `NOT`). Use aspas para termos compostos e truncamento (`*`) quando a base permitir.*

| Nº | String de busca | Base(s) em que será usada | Elaborada por |
|---|---|---|---|
| 1 | `("Dijkstra's algorithm" OR "Dijkstra*") AND ("time-dependent" OR "dynamic traffic") AND ("shortest path")` | *`Google Acadêmico, ACM Digital Library`* | `Pedro Henrique dos Santos` |
| 2 | `("bidirectional Dijkstra" OR "time-dependent Dijkstra") AND ("complexity" OR "scalability" OR "memory") AND ("urban network*" OR "routing")` | *`ScienceDirect (Elsevier)`* | `Carlos Eduardo Laera Prado e João Marcelo El Hafi Batista` |
| 3 | `("Dijkstra") AND ("dependente do tempo" OR "bidirecional" OR "tráfego dinâmico") AND ("caminho mínimo" OR "escalabilidade")` | *`IEEE Xplore`* | `Brayan Allan Nagatani Campos de Almeida` |

---

### Passo 3 — Bases de dados escolhidas

*Selecione de 2 a 4 bases relevantes ao tema. Registre a justificativa — isso vai para a seção de metodologia do artigo/relatório de IC.*

| Base de dados | Por que foi escolhida | Responsável pela busca nesta base |
|---|---|---|
| *`IEEE Xplore`* | `Principal acervo de Ciência da Computação e Engenharia, essencial para encontrar literatura técnica sobre teoria dos grafos, algoritmos de roteamento e sistemas de transporte inteligente (ITS).` | `Pedro Henrique dos Santos` |
| *`ACM Digital Library`* | `Referência central em teoria da computação. Escolhida especificamente pela alta concentração de artigos que analisam formalmente a complexidade matemática, uso de memória e escalabilidade de algoritmos gulosos.` | `Gabriel Souza de Carvalho` |
| *`ScienceDirect (Elsevier)`* | `Possui forte foco em pesquisa operacional, modelagem de transportes e logística. É vital para entender como o problema do caminho mínimo com tráfego dependente do tempo é equacionado na literatura teórica.` | `Carlos Eduardo Laera Prado` |
| *`Google Acadêmico`* | `Permite uma varredura algorítmica ampla para capturar publicações recentes (estado da arte), teses e dissertações sobre as variantes de Dijkstra, cruzando termos em português e inglês.` | `Brayan Allan Nagatani Campos de Almeida e João Marcelo El Hafi Batista` | 

---

### Passo 4 — Critérios de inclusão e exclusão

**Critérios de inclusão:**
- `Artigos publicados entre 2016 e 2026, inclusive, para garantir relevância e atualidade do estado da arte.`
- `Artigos científicos revisados por pares (revistas acadêmicas e anais de conferências consolidadas).`
- `Trabalhos redigidos em português ou inglês.`
- `Documentos com texto completo disponível na íntegra nas bases institucionais ou de acesso aberto.`
- `Artigos que abordem centralmente a análise teórica, matemática ou de complexidade estrutural/memória do algoritmo de Dijkstra e suas variantes (Dependente do Tempo e Bidirecional) aplicados a caminhos mínimos.`

**Critérios de exclusão:**
- `Resumos expandidos, editoriais, apresentações de slides ou artigos sem o texto completo disponível.`
- `Artigos em duplicidade (encontrados em mais de uma base de dados).`
- `Trabalhos cuja contribuição central seja a implementação de software, engenharia de hardware ou avaliação predominantemente empírica, sem fundamentação teórica ou análise formal de complexidade, memória ou escalabilidade.`
- `Artigos focados no planejamento de múltiplas entregas (como o Problema do Caixeiro Viajante - TSP ou VRP) ou em outras heurísticas como o A*, garantindo que não haja sobreposição com os Grupos 1 e 10.`
- `Materiais não revisados por pares (pre-prints não validados, trabalhos de conclusão de curso de graduação ou artigos de opinião).`

*Definidos em conjunto por: `Gabriel Souza de Carvalho, Pedro Henrique dos Santos, Carlos Eduardo Laera Prado, João Marcelo El Hafi Batista e Brayan Allan Nagatani Campos de Almeida`*

---

## FASE 2 — Execução da Busca e Triagem

### Passo 5 — Execução das buscas e registro dos resultados

*Anote quantos resultados cada string trouxe em cada base (útil para o fluxograma tipo PRISMA, se o projeto exigir). Exporte as referências (BibTeX, RIS, CSV) para um gerenciador de referências.*

| Base | String usada (nº) | Data da busca | Nº de resultados | Executada por |
|---|---|---|---|---|
| `Google Scholar` | `1` | `10/09/2026` | `≈ 2.400` | `Brayan Allan Nagatani Campos de Almeida` |
| `ScienceDirect` | `2` | `10/09/2026` | `≈ 60` | `Carlos Eduardo Laera Prado` |
| `ACM Digital Library` | `1` | `10/09/2026` | `≈ 70` | `Gabriel Souza de Carvalho` |
| `IEEE Xplore` | `3` | `10/09/2026` | `≈ 3` | `Pedro Henrique dos Santos` |

**Total de resultados brutos (soma de todas as buscas):** `≈ 2.533`

**Gerenciador de referências utilizado:** `Zotero`
**Formato de exportação:** `BibTeX`

---

### Passo 6 — Triagem por título e resumo (1ª filtragem)

*Leia apenas título e resumo de cada resultado. Classifique: incluir / excluir / dúvida. Remova duplicatas entre bases.*

| Item de controle | Quantidade |
|---|---|
| Total de resultados antes da triagem | `2.533` |
| Duplicatas removidas | `130` |
| Classificados como "Incluir" | `13` |
| Classificados como "Excluir" | `2.325` |
| Classificados como "Dúvida" | `65` |

*A triagem detalhada, artigo por artigo, deve ser registrada na planilha de controle do projeto (aba "Triagem de Artigos"). Aqui, registre apenas o resumo quantitativo.*

**Como as dúvidas foram resolvidas?** *(ex.: discussão em grupo, consulta ao orientador)*
`As principais dúvidas ocorreram em trabalhos que mencionavam Dijkstra e shortest path no título ou resumo, mas não deixavam claro se o algoritmo era efetivamente o objeto principal da análise ou apenas utilizado como baseline de comparação. Também houve incerteza em relação a estudos que mencionavam abordagens "híbridas" ou "aceleradas". Nesses casos, o texto completo e a metodologia foram consultados para determinar se havia uso de heurísticas (como A*, para evitar sobreposição com o Grupo 1), TSP/VRP ou outras estratégias incompatíveis com os critérios de inclusão. Os trabalhos que apresentavam evidências suficientes de aderência temática, mas cuja elegibilidade não podia ser confirmada apenas pelo resumo, foram mantidos como potenciais para a leitura integral.`

*Responsável(is) por esta triagem: `Gabriel Souza de Carvalho, Pedro Henrique dos Santos, Carlos Eduardo Laera Prado e Brayan Allan Nagatani Campos de Almeida e João Marcelo El Hafi Batista`*

---

### Passo 7 — Triagem por leitura completa (2ª filtragem)

*Para os artigos que passaram na primeira filtragem, leia introdução e conclusão. Aplique os critérios de inclusão/exclusão (passo 4) de forma mais rigorosa.*

| Item de controle | Quantidade |
|---|---|
| Total de artigos que entraram nesta filtragem | `13` |
| Aprovados (conjunto definitivo para fichamento) | `4` |
| Excluídos nesta etapa | `9` |

**Principais motivos de exclusão nesta filtragem:**
- `Uso de heurísticas ou algoritmos híbridos: Artigos que no resumo citavam Dijkstra, mas que na metodologia revelaram dependência central do algoritmo A* ou de estratégias de aceleração heurística, violando os critérios de inclusão e a diferenciação com o Grupo 1.`
- `Sobreposição com escopo de múltiplas entregas: Trabalhos que aplicavam o caminho mínimo como subrotina para solucionar o Problema do Caixeiro Viajante (TSP) ou Roteamento de Veículos (VRP), fugindo do foco estrito no caminho mínimo ponto a ponto.`
- `Falta de análise teórica formal: Artigos focados exclusivamente em testes empíricos de implementação de software sem dedução matemática de complexidade assintótica, consumo de memória ou escalabilidade.`
- `Inadequação da dinâmica temporal ou do domínio: Trabalhos aplicados a redes viárias estáticas ou a domínios fora do roteamento urbano dinâmico (como redes de sensores, robótica e redes de comunicação).`

*Responsável(is) por esta triagem: `Gabriel Souza de Carvalho, Pedro Henrique dos Santos, Carlos Eduardo Laera Prado e Brayan Allan Nagatani Campos de Almeida e João Marcelo El Hafi Batista`*

---

## 3. Lista Final de Artigos Selecionados (Conjunto Definitivo)

*Liste aqui os artigos que passaram por todas as filtragens e seguirão para o fichamento (etapa "j"). Referência completa no formato ABNT/APA definido pelo projeto.*

Padrão ABNT
1. `CONSTANTINOU, Costas K.; ELLINAS, Georgios; PANAYIOTOU, Christos G.; POLYCARPOU, Marios M. Shortest Path Routing in Transportation Networks with Time-Dependent Road Speeds. In: PROCEEDINGS OF THE INTERNATIONAL CONFERENCE ON VEHICLE TECHNOLOGY AND INTELLIGENT TRANSPORT SYSTEMS – VEHITS. [S. l.]: SciTePress, 2016. p. 91–98. DOI: 10.5220/0005807000910098.`
2. `BAUM, Moritz; DIBBELT, Julian; PAJOR, Thomas; WAGNER, Dorothea. Dynamic Time-Dependent Route Planning in Road Networks with User Preferences. In: EXPERIMENTAL ALGORITHMS: 15TH INTERNATIONAL SYMPOSIUM, SEA 2016, PROCEEDINGS. Cham: Springer, 2016. v. 9685, p. 33–49. DOI: 10.1007/978-3-319-38851-9_3.`
3. `HENI, Hamza; COELHO, Leandro C.; RENAUD, Jacques. Determining time-dependent minimum cost paths under several objectives. Computers & Operations Research, v. 105, p. 102–117, 2019. DOI: 10.1016/j.cor.2019.01.007.`
4. `SUN, Yanming; LI, Jie; LIU, Shixian. Study on the Shortest Reliable Path of Stochastic Time-Dependent Transportation Networks considering Waiting Time at Signalized Intersections. Journal of Advanced Transportation, v. 2023, art. 8298068, p. 1–14, 2023. DOI: 10.1155/2023/8298068.`

Padrão APA
1. `Constantinou, C. K., Ellinas, G., Panayiotou, C. G., & Polycarpou, M. M. (2016). Shortest path routing in transportation networks with time-dependent road speeds. In Proceedings of the International Conference on Vehicle Technology and Intelligent Transport Systems – VEHITS (pp. 91–98). SciTePress. https://doi.org/10.5220/0005807000910098`

2. `Baum, M., Dibbelt, J., Pajor, T., & Wagner, D. (2016). Dynamic time-dependent route planning in road networks with user preferences. In Experimental Algorithms: 15th International Symposium, SEA 2016, Proceedings (Vol. 9685, pp. 33–49). Springer. https://doi.org/10.1007/978-3-319-38851-9_3`

3. `Heni, H., Coelho, L. C., & Renaud, J. (2019). Determining time-dependent minimum cost paths under several objectives. Computers & Operations Research, 105, 102–117. https://doi.org/10.1016/j.cor.2019.01.007`

4. `Sun, Y., Li, J., & Liu, S. (2023). Study on the shortest reliable path of stochastic time-dependent transportation networks considering waiting time at signalized intersections. Journal of Advanced Transportation, 2023, Article 8298068, 1–14. https://doi.org/10.1155/2023/8298068`

---

## 4. Contribuição Individual dos Integrantes

> **Importante:** cada integrante deve descrever, com suas próprias palavras, o que efetivamente fez em cada passo desta etapa. Contribuições genéricas como "ajudei em tudo" não serão aceitas. Use verbos de ação e seja específico (ex.: "executei a busca no IEEE Xplore com a string 2 e obtive 84 resultados; fiz a triagem por título/resumo de 40 desses").

### Integrante 1 — `Gabriel Souza de Carvalho`
- **Passo(s) em que atuou:** `1, 3, 4, 5, 6 e 7`
- **O que fez em cada passo:** `Formulei a pergunta de pesquisa preliminar e construí a tabela de conceitos-chave e sinônimos no Passo 1. Elaborei a justificativa técnica da ACM Digital Library no Passo 3 e executei a busca da String 1 nessa base no Passo 5 (obtendo ≈ 70 resultados). Redigi os critérios de inclusão e exclusão no Passo 4 para blindar o escopo e participei ativamente da triagem por resumo (Passo 6) e por texto completo (Passo 7).`
- **Tempo dedicado (aprox.):** `3h`
- **Evidência da contribuição** *(print de busca, planilha de triagem, exportação BibTeX, etc.)*: `Registro de commit no repositório do GitHub, arquivo BibTeX exportado da ACM Digital Library e preenchimento das definições de conceitos e pergunta de pesquisa na planilha do projeto. `

### Integrante 2 — `Pedro Henrique dos Santos`
- **Passo(s) em que atuou:** `2, 3, 4, 5, 6 e 7`
- **O que fez em cada passo:** `Estruturei a String 1 de busca booleana com operadores AND/OR e aspas para termos compostos no Passo 2. Redigi a justificativa da base IEEE Xplore no Passo 3 e executei a busca da String 3 no IEEE Xplore no Passo 5 (obtendo ≈ 3 resultados). Colaborei no refinamento dos critérios no Passo 4 e na filtragem de duplicatas e seleção final nos Passos 6 e 7.`
- **Tempo dedicado (aprox.):** `3h`
- **Evidência da contribuição:** `Arquivo .bib exportado diretamente do IEEE Xplore, salvamento dos metadados no Zotero`

### Integrante 3 — `Carlos Eduardo Laera Prado`
- **Passo(s) em que atuou:** `2, 3, 4, 5, 6 e 7`
- **O que fez em cada passo:** `Elaborei a String 2 com foco em complexidade, memória e escalabilidade em redes urbanas no Passo 2 (em parceria com o João). Redigi a justificativa da ScienceDirect no Passo 3 e conduzi a busca com a String 2 nessa base no Passo 5 (obtendo ≈ 60 resultados). Atuei na definição dos critérios de exclusão no Passo 4 e no descarte de falsos positivos (trabalhos focados em A* e heurísticas) nos Passos 6 e 7.`
- **Tempo dedicado (aprox.):** `3h`
- **Evidência da contribuição:** `Registros das referências exportadas da ScienceDirect importados na biblioteca do Zotero e preenchimento das justificativas de exclusão de artigos.`

### Integrante 4 — `Brayan Allan Nagatani Campos de Almeida`
- **Passo(s) em que atuou:** `2, 3, 4, 5, 6 e 7`
- **O que fez em cada passo:** `Elaborei a String 3 em português e inglês no Passo 2. Redigi a justificativa do Google Acadêmico no Passo 3 e conduzi a varredura da String 1 nessa base no Passo 5 (obtendo ≈ 2.400 resultados) em dupla com o João Marcelo. Auxiliei no cruzamento de critérios no Passo 4 e na filtragem massiva dos resumos no Passo 6 e leitura integral no Passo 7.`
- **Tempo dedicado (aprox.):** `3h`
- **Evidência da contribuição:** `Registro da varredura bruta do Google Acadêmico exportado em lote para o Zotero e preenchimento dos registros iniciais.`

### Integrante 5 — `João Marcelo El Hafi Batista`
- **Passo(s) em que atuou:** `2, 3, 4, 5, 6 e 7`
- **O que fez em cada passo:** `Fiz parte da elaboração da String 2 com o Carlos no Passo 2. Participei da justificativa e da execução da busca de alto volume no Google Acadêmico (String 1, ≈ 2.400 resultados) junto com o Brayan no Passo 3 e 5. Contribuí para a consolidação dos critérios no Passo 4, na remoção de duplicatas no Passo 6 e na triagem fina da leitura completa no Passo 7 para selecionar os 4 artigos definitivos.`
- **Tempo dedicado (aprox.):** `3h`
- **Evidência da contribuição:** `Relatório de deduplicação (remoção de 130 duplicatas) gerado no Zotero e anotações das justificativas de descarte por leitura de metodologia.`


### 4.1 Quadro-resumo de participação por passo

| Passo | Responsável(is) | % estimado de participação de cada um |
|---|---|---|
| 1. Pergunta e palavras-chave | `Gabriel Souza de Carvalho` | `100%` |
| 2. Strings de busca | `Pedro Henrique, Carlos Eduardo, Brayan Allan, João Marcelo` | `Pedro (25%), Carlos (25%), Brayan (25%), João (25%)` |
| 3. Bases de dados | `Gabriel, Pedro, Carlos, Brayan, João Marcelo` | `Gabriel (20%), Pedro (20%), Carlos (20%), Brayan (20%), João (20%)` |
| 4. Critérios de inclusão/exclusão | `Gabriel, Pedro, Carlos, Brayan, João Marcelo` | `Gabriel (20%), Pedro (20%), Carlos (20%), Brayan (20%), João (20%)` |
| 5. Execução das buscas | `Gabriel, Pedro, Carlos, Brayan, João Marcelo` | `Gabriel (20%), Pedro (20%), Carlos (20%), Brayan (20%), João (20%)` |
| 6. Triagem título/resumo | `Gabriel, Pedro, Carlos, Brayan, João Marcelo` | `Gabriel (20%), Pedro (20%), Carlos (20%), Brayan (20%), João (20%)` |
| 7. Triagem texto completo | `Gabriel, Pedro, Carlos, Brayan, João Marcelo` | `Gabriel, Pedro, Carlos, Brayan, João Marcelo	Gabriel (20%), Pedro (20%), Carlos (20%), Brayan (20%), João (20%)` |

### 4.2 Quadro-resumo geral de participação na etapa

| Integrante | % estimado de participação total nesta etapa |
|---|---|
| `Gabriel Souza de Carvalho` | `20%` |
| `Pedro Henrique dos Santos` | `20%` |
| `Carlos Eduardo Laera Prado` | `20%` |
| `Brayan Allan Nagatani Campos de Almeida` | `20%` |
| `João Marcelo El Hafi Batista` | `20%` |

*A soma das porcentagens deve ser igual a 100%. Divergências de percepção sobre a participação devem ser discutidas em grupo antes do envio — o orientador pode solicitar esclarecimentos individuais em caso de disparidade relevante.*

---

## 5. Checklist Final da Etapa

**Fase 1 — Planejamento**
- [x] Pergunta de pesquisa de trabalho definida
- [x] Conceitos-chave e sinônimos (PT/EN) listados
- [x] Strings de busca elaboradas com operadores booleanos
- [x] Bases de dados escolhidas e justificadas
- [x] Critérios de inclusão e exclusão definidos

**Fase 2 — Execução e triagem**
- [x] Buscas executadas e resultados registrados por base/string
- [x] Referências exportadas para o gerenciador de referências
- [x] Triagem por título/resumo concluída (com duplicatas removidas)
- [x] Triagem por texto completo (introdução/conclusão) concluída
- [x] Conjunto definitivo de artigos para fichamento compilado

**Documentação**
- [x] Contribuição individual de cada integrante registrada por passo
- [x] Quadro-resumo de participação preenchido (soma = 100%)

---


