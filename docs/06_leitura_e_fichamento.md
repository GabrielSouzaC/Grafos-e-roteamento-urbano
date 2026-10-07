# Etapa 6 Leitura e fichamento

## Solicitação

Preencha uma cópia deste template para cada artigo selecionado.

## Artigo 1 — Constantinou et al. (2016)

### Identificação do artigo

- Referência completa: `CONSTANTINOU, Costas K.; ELLINAS, Georgios; PANAYIOTOU, Christos G.; POLYCARPOU, Marios M. Shortest Path Routing in Transportation Networks with Time-Dependent Road Speeds. In: Proceedings of the International Conference on Vehicle Technology and Intelligent Transport Systems – VEHITS. SciTePress, 2016, p. 91–98. DOI: 10.5220/0005807000910098.`
- DOI ou URL: `https://doi.org/10.5220/0005807000910098`
- Base de origem: `SciTePress`
- Leitor responsável: `Grupo 4`
- Data da leitura: `07/10/2026`

## Fichamento

### Problema investigado

`O artigo investiga o problema do caminho mínimo em redes de transporte dependentes do tempo, nas quais a velocidade das vias varia conforme o intervalo temporal. Como o tempo de travessia de uma aresta depende do instante de partida, é necessário determinar formalmente esse tempo durante a execução do algoritmo de caminho mínimo.`

### Objetivo do estudo

`Desenvolver um procedimento para determinar o tempo de travessia das vias quando a velocidade é modelada como uma função linear do tempo dentro de cada intervalo e integrá-lo ao algoritmo de Dijkstra, permitindo obter caminhos mínimos ótimos em redes de transporte dependentes do tempo. O artigo também demonstra a validade da propriedade FIFO para o modelo considerado.`

### Método utilizado

`O estudo formula um modelo de rede dependente do tempo baseado nas velocidades das vias e desenvolve os procedimentos ATT e ATT_L para calcular o tempo de travessia das arestas a partir do instante de partida. Esses procedimentos são incorporados ao Dijkstra Dependente do Tempo (TD-Dijkstra). O artigo também apresenta uma análise formal da complexidade e uma demonstração matemática da propriedade FIFO.`

### Contexto, amostra ou dados

`O modelo considera redes de transporte nas quais velocidades foram medidas em diversos instantes durante um período extenso, podendo representar, por exemplo, padrões observados ao longo de um ano. As velocidades são organizadas em intervalos temporais, cujo número é representado por K. O instante de partida pode assumir qualquer valor real. O estudo possui foco teórico e não apresenta exemplos numéricos como parte central da avaliação.`

### Principais resultados

`O procedimento ATT apresenta complexidade O(K). A partir dessa característica, o artigo deduz que o TD-Dijkstra possui complexidade O(n² + mK) na implementação simples. Utilizando uma Fibonacci heap, a complexidade pode ser reduzida para O(n log n + mK), em que n representa o número de vértices, m o número de arestas e K a quantidade de intervalos temporais considerados. O artigo também demonstra que o modelo de velocidade utilizado satisfaz a propriedade FIFO, permitindo a obtenção de caminhos mínimos ótimos nas redes analisadas.`

### Limitações apresentadas

`A formulação principal considera a velocidade da via como uma função linear do tempo dentro de cada intervalo. Além disso, o comportamento futuro da rede é estimado a partir dos padrões de velocidade observados anteriormente. O artigo não apresenta uma análise assintótica independente de uso de memória nem uma avaliação empírica de escalabilidade em redes reais.`

### Contribuição para o nosso artigo

`É a principal referência do corpus para a análise formal da complexidade do Dijkstra Dependente do Tempo. O estudo fornece diretamente as expressões O(n² + mK) e O(n log n + mK), permitindo analisar matematicamente o impacto da dimensão temporal K sobre o custo do algoritmo e compará-lo posteriormente com outras variantes.`

### Comentário crítico

`O principal ponto forte é o formalismo matemático e a explicitação da influência de K na complexidade. Para a revisão do Grupo 4, o artigo fornece uma base teórica muito clara para demonstrar que a dinâmica temporal acrescenta um custo ao problema em relação ao Dijkstra clássico. Como limitação para a nossa matriz, o trabalho não trata o uso de memória como uma dimensão assintótica independente e também não apresenta uma análise experimental de escalabilidade.`

### Citação literal opcional

> `Não utilizada nesta etapa.`

Página: `—`

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.

---

# Artigo 2 — Baum et al. (2016)

### Identificação do artigo

- Referência completa: `BAUM, Moritz; DIBBELT, Julian; PAJOR, Thomas; WAGNER, Dorothea. Dynamic Time-Dependent Route Planning in Road Networks with User Preferences. In: Experimental Algorithms: 15th International Symposium, SEA 2016, Proceedings. Cham: Springer, 2016. v. 9685, p. 33–49. DOI: 10.1007/978-3-319-38851-9_3.`
- DOI ou URL: `https://doi.org/10.1007/978-3-319-38851-9_3`
- Base de origem: `Springer / KITopen`
- Leitor responsável: `Grupo 4`
- Data da leitura: `07/10/2026`

## Fichamento

### Problema investigado

`O artigo investiga o problema de planejamento de rotas em redes rodoviárias dinâmicas e dependentes do tempo, considerando simultaneamente padrões históricos de tráfego, atualizações de tráfego em tempo real e preferências ou restrições dos usuários. O desafio central é manter consultas eficientes mesmo quando o peso das arestas sofre alterações dinâmicas.`

### Objetivo do estudo

`Propor o Time-Dependent Customizable Route Planning (TDCRP), uma extensão do Customizable Route Planning capaz de incorporar mudanças dinâmicas ou dependentes do usuário nas métricas da rede e ainda responder rapidamente a consultas de caminho mínimo.`

### Método utilizado

`O método utiliza uma particionamento multinível da rede e uma fase de customização dependente da métrica. São realizadas buscas de perfil para calcular atalhos dependentes do tempo nos grafos de sobreposição. Na fase de consulta, o algoritmo utiliza uma variante bidirecional do algoritmo de Dijkstra sobre o grafo de busca reduzido. Para limitar a complexidade funcional dos atalhos nos níveis superiores, os autores aproximam os arcos de sobreposição durante a customização.`

### Contexto, amostra ou dados

`A avaliação utiliza redes rodoviárias dependentes do tempo da Alemanha, da Europa Ocidental e de Berlin/Brandenburg. A instância da Alemanha possui aproximadamente 4,7 milhões de vértices e 10,8 milhões de arestas; a da Europa possui cerca de 18 milhões de vértices e 42,2 milhões de arestas; e a de Berlin/Brandenburg possui aproximadamente 443 mil vértices e 988 mil arestas. Os dados incluem padrões históricos de tráfego e funções de tempo de viagem dependentes do tempo.`

### Principais resultados

`O TDCRP permite integrar alterações de tráfego e preferências de usuários sem reconstruir toda a estrutura de roteamento. A consulta utiliza uma busca bidirecional baseada em Dijkstra e apresenta tempos de consulta na ordem de milissegundos nas redes avaliadas. O estudo demonstra ainda que a complexidade funcional dos atalhos cresce significativamente nos níveis superiores da hierarquia e pode ultrapassar a capacidade de memória disponível. A aproximação dos arcos de sobreposição reduz esse custo e permite consultas rápidas, porém com soluções próximas do ótimo.`

### Limitações apresentadas

`O principal problema estrutural identificado é o crescimento da complexidade dos perfis de tempo nos níveis superiores dos grafos de sobreposição, tornando algumas estruturas inviáveis em memória. Para contornar essa limitação, os autores utilizam aproximação dos atalhos, de modo que o resultado final deixa de ser garantidamente exato em todos os casos. O artigo também não apresenta uma expressão assintótica única que caracterize o custo total do TDCRP em função de n e m como faz Constantinou et al. para o TD-Dijkstra.`

### Contribuição para o nosso artigo

`É a principal referência do corpus para analisar a dimensão de escalabilidade e o papel do Dijkstra Bidirecional em redes rodoviárias dependentes do tempo. O estudo mostra estruturalmente que a representação temporal das arestas pode aumentar significativamente o consumo de memória e que mecanismos hierárquicos são utilizados para restringir o espaço efetivamente pesquisado.`

### Comentário crítico

`O artigo é muito relevante para escalabilidade, mas deve ser interpretado com cuidado na comparação das variantes. O Dijkstra Bidirecional aparece como componente da fase de consulta do TDCRP, e não como uma análise isolada da complexidade assintótica do algoritmo bidirecional. Além disso, a aproximação dos atalhos introduz uma diferença importante em relação ao objetivo de caminho mínimo exatamente ótimo.`

### Citação literal opcional

> `Não utilizada nesta etapa.`

Página: `—`

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.

---

# Artigo 3 — Heni, Coelho e Renaud (2019)

### Identificação do artigo

- Referência completa: `HENI, Hamza; COELHO, Leandro C.; RENAUD, Jacques. Determining Time-Dependent Minimum Cost Paths under Several Objectives. Computers & Operations Research, v. 105, p. 102–117, 2019. DOI: 10.1016/j.cor.2019.01.007.`
- DOI ou URL: `https://doi.org/10.1016/j.cor.2019.01.007`
- Base de origem: `ScienceDirect (Elsevier)`
- Leitor responsável: `Grupo 4`
- Data da leitura: `07/10/2026`

## Fichamento

### Problema investigado

`O artigo estuda o problema de caminho mínimo de custo dependente do tempo com múltiplos componentes de custo, denominado TDMCP-SO. O custo de uma aresta depende não apenas da distância, mas também de consumo de combustível, emissões de gases de efeito estufa, custo do motorista e congestionamento, todos influenciados pela variação da velocidade ao longo do tempo.`

### Objetivo do estudo

`Desenvolver limites inferiores e superiores dependentes do tempo e métodos baseados em Dijkstra para determinar caminhos de menor custo em redes rodoviárias com velocidades variáveis, preservando a consistência FIFO e considerando diferentes componentes de custo.`

### Método utilizado

`O estudo formaliza uma rede direcionada dependente do tempo G=(V,A,Z,S), define funções de tempo e custo dependentes do instante de partida e utiliza o modelo Flow Speed Model (FSM) para garantir a propriedade FIFO. São desenvolvidas três adaptações do Dijkstra label-setting: TD-Dijkstra-LTM, TD-Dijkstra-LTM-STTF e TD-Dijkstra-FSM. Os autores também desenvolvem limites inferiores e superiores para reduzir o esforço computacional.`

### Contexto, amostra ou dados

`Os experimentos utilizam dados reais do sistema rodoviário de Québec City. São consideradas 80 instâncias de benchmark em uma rede com mais de 17.000 nós e um conjunto de aproximadamente 24 milhões de observações de velocidade. O estudo considera diferentes velocidades ao longo do dia e diferentes cargas transportadas.`

### Principais resultados

`O artigo apresenta expressões explícitas de complexidade. O Dijkstra original é caracterizado por O(m log n). Para o TD-Dijkstra-LTM, a complexidade é O(m log n + n). Para o TD-Dijkstra-LTM-STTF, é O(m log n + nC), em que C representa o número de passos usados pelo procedimento STTF. Para o TD-Dijkstra-FSM, a complexidade é O(m log n + nK), em que K representa o número máximo de períodos de tempo examinados pela função de custo. Os autores também demonstram que a consideração explícita da propriedade FIFO permite calcular limites dependentes do tempo de forma eficiente.`

### Limitações apresentadas

`O artigo não apresenta uma seção específica dedicada ao uso de memória e não fornece um limite assintótico independente para memória. A formulação depende da consistência FIFO e de uma discretização temporal para representar a variação da velocidade. Além disso, apesar de trabalhar com uma rede urbana real de grande porte, a avaliação está concentrada nos dados e condições de Québec City.`

### Contribuição para o nosso artigo

`O artigo fornece uma das análises mais detalhadas do corpus para relacionar complexidade assintótica, dinâmica temporal e escalabilidade do TD-Dijkstra. Em especial, a expressão O(m log n + nK) do método FSM permite comparar diretamente o impacto da dimensão temporal K com o custo do Dijkstra clássico.`

### Comentário crítico

`O estudo possui forte valor teórico, principalmente pela explicitação das diferentes componentes da complexidade. Entretanto, seu problema de otimização é mais abrangente que o caminho mínimo baseado exclusivamente em tempo, pois incorpora emissões, combustível e custos do motorista. Portanto, na síntese do Grupo 4, essa ampliação do modelo deve ser identificada para evitar uma comparação direta entre problemas com objetivos diferentes. O artigo também contém avaliação computacional, que deve ser utilizada na revisão apenas como evidência apresentada pelos autores sobre escalabilidade e desempenho, e não como implementação do grupo.`

### Citação literal opcional

> `Não utilizada nesta etapa.`

Página: `—`

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.

---

# Artigo 4 — Sun, Li e Liu (2023)

### Identificação do artigo

- Referência completa: `SUN, Yanming; LI, Jie; LIU, Shixian. Study on the Shortest Reliable Path of Stochastic Time-Dependent Transportation Networks considering Waiting Time at Signalized Intersections. Journal of Advanced Transportation, v. 2023, Article ID 8298068, 14 p., 2023. DOI: 10.1155/2023/8298068.`
- DOI ou URL: `https://doi.org/10.1155/2023/8298068`
- Base de origem: `Wiley Online Library`
- Leitor responsável: `Grupo 4`
- Data da leitura: `07/10/2026`

## Fichamento

### Problema investigado

`O artigo investiga o problema do caminho mínimo confiável em redes urbanas estocásticas e dependentes do tempo, considerando a incerteza dos tempos de viagem e, adicionalmente, o tempo de espera causado por interseções semaforizadas. O objetivo é obter uma rota que permaneça confiável mesmo quando os tempos de viagem variam.`

### Objetivo do estudo

`Modelar matematicamente o tempo de espera em interseções semaforizadas, transformar a rede estocástica dependente do tempo em uma rede determinística dependente do tempo e propor um algoritmo de caminho mínimo baseado em Dijkstra que considere os atrasos nas interseções.`

### Método utilizado

`O estudo formula uma função periódica de espera em interseções semaforizadas e um modelo de caminho mínimo confiável baseado em uma abordagem min-max. Em seguida, demonstra por indução matemática que uma rede de tráfego estocástica e dependente do tempo pode ser transformada em uma rede determinística dependente do tempo. Por fim, aplica um algoritmo de caminho mínimo baseado em Dijkstra à rede transformada, incorporando o tempo de espera nas interseções.`

### Contexto, amostra ou dados

`O modelo considera redes rodoviárias urbanas com n nós e m ligações, cujos tempos de viagem variam ao longo do tempo e apresentam incerteza. O artigo utiliza uma rede modelada para demonstrar o comportamento do método e apresenta experimentos numéricos com diferentes tempos de partida e condições de viagem. O estudo não utiliza uma grande rede urbana real com escala comparável às instâncias de Baum ou Heni.`

### Principais resultados

`O artigo demonstra matematicamente que o tempo de espera em uma interseção semaforizada pode ser representado por uma função periódica contínua e não diferenciável. Também demonstra que uma rede estocástica dependente do tempo pode ser reduzida a uma rede determinística dependente do tempo. O algoritmo baseado em Dijkstra considera explicitamente o atraso das interseções e não exige o conhecimento da distribuição probabilística dos tempos de viagem, utilizando apenas intervalos de incerteza derivados de dados históricos e experiência dos decisores. A abordagem produz caminhos com maior confiabilidade temporal no modelo analisado.`

### Limitações apresentadas

`Os próprios autores reconhecem que o modelo não considera os tempos de luz amarela e de todos os vermelhos nas interseções. Também não é analisado o efeito de volumes de tráfego dinâmicos em tempo real sobre o tempo de viagem. Os autores apontam a aplicação do algoritmo a redes de tráfego maiores como uma possibilidade de pesquisa futura. Na versão consultada, não foi identificada uma expressão assintótica explícita de complexidade de tempo ou de memória que permita compará-lo diretamente, nesse aspecto, com Constantinou et al. e Heni et al.`

### Contribuição para o nosso artigo

`O artigo contribui principalmente para a dimensão estrutural da rede dinâmica. Ele demonstra como fenômenos urbanos adicionais, como atrasos semafóricos e incerteza temporal, podem ser incorporados matematicamente ao problema de caminho mínimo antes da aplicação de um algoritmo baseado em Dijkstra. Dessa forma, ajuda a caracterizar como a modelagem temporal altera o problema de caminho mínimo, mesmo sem apresentar uma expressão assintótica comparável às dos demais estudos.`

### Comentário crítico

`O ponto forte do artigo é o formalismo matemático aplicado a um fenômeno específico das redes urbanas: o atraso em interseções semaforizadas. Sua principal fragilidade para a pergunta do Grupo 4 é a ausência de uma análise assintótica explícita de tempo e memória e a limitação da avaliação a uma rede de menor escala. Assim, sua maior contribuição para a revisão está na modelagem estrutural da dinâmica temporal e da confiabilidade, enquanto Constantinou e Heni são mais diretamente úteis para a comparação de complexidade.`

### Citação literal opcional

> `Não utilizada nesta etapa.`

Página: `—`

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
- [x] Toda citação literal contém página.