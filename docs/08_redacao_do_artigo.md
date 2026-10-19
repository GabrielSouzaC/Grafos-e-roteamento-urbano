# Etapa 8 Redação do artigo

# Título

**Complexidade, uso de memória e escalabilidade do algoritmo de Dijkstra e suas variantes em redes urbanas dinâmicas: uma revisão bibliográfica**

## Palavras-chave

Algoritmo de Dijkstra; caminho mínimo; redes urbanas dinâmicas; complexidade algorítmica; escalabilidade.

## Introdução

A Teoria dos Grafos oferece modelos matemáticos para representar redes de transporte, nas quais os cruzamentos podem ser representados por vértices e os segmentos de vias por arestas. Nesse contexto, o problema do caminho mínimo consiste em determinar um percurso de menor custo entre uma origem e um destino. O algoritmo de Dijkstra é uma abordagem clássica para esse problema, mas sua aplicação a redes urbanas exige atenção às características dos custos associados às vias, especialmente quando os tempos de deslocamento variam conforme as condições de tráfego.

Em uma rede urbana dinâmica, o custo de percorrer uma aresta pode depender do instante de partida, da velocidade do veículo, do congestionamento e de outros fatores temporais. Dessa forma, o problema deixa de ser descrito apenas por pesos constantes e passa a exigir modelos que representem a variação dos tempos de viagem ao longo do dia. Constantinou et al. (2016), por exemplo, investigam redes nas quais as velocidades das vias variam por intervalo temporal, enquanto Heni, Coelho e Renaud (2019) consideram custos de transporte dependentes do tempo e associados a diferentes componentes, como emissões, combustível e custos operacionais.

Duas variantes relevantes nesse contexto são o Dijkstra Dependente do Tempo (TD-Dijkstra) e o Dijkstra Bidirecional. A primeira incorpora a dependência temporal dos custos durante a busca pelo caminho mínimo. A segunda executa buscas a partir da origem e do destino, reduzindo o espaço explorado em determinadas condições. Baum et al. (2016) integram uma variante bidirecional de Dijkstra a uma estrutura multinível de roteamento dependente do tempo, demonstrando como a organização estrutural da rede pode contribuir para consultas eficientes. Já Sun, Li e Liu (2023) investigam como a incerteza dos tempos de viagem e os atrasos em cruzamentos semaforizados podem ser incorporados matematicamente ao problema do caminho mínimo confiável.

Apesar dessas contribuições, os estudos selecionados não apresentam a mesma profundidade para todas as dimensões relevantes à análise algorítmica. Alguns fornecem expressões explícitas de complexidade assintótica, enquanto outros enfatizam a estrutura da rede, o consumo de memória ou a formulação matemática das condições de tráfego. Essa diferença dificulta a comparação direta entre as variantes e evidencia a necessidade de distinguir os resultados formalmente demonstrados das conclusões obtidas por avaliações computacionais relatadas pelos próprios autores.

Diante disso, este artigo tem como objetivo **analisar, com base na literatura científica, a complexidade, o uso de memória e a escalabilidade do algoritmo de Dijkstra e de suas variantes Dependente do Tempo e Bidirecional na busca pelo caminho mínimo em redes urbanas dinâmicas com tráfego variável**.

## Metodologia

Este trabalho caracteriza-se como uma revisão bibliográfica de abordagem qualitativa, com busca e seleção de estudos organizadas por critérios explícitos de inclusão e exclusão. O processo de identificação e seleção foi estruturado em etapas de planejamento, deduplicação, triagem por título e resumo, leitura dos artigos elegíveis e síntese comparativa, seguindo a lógica de transparência de seleção recomendada pelo PRISMA 2020 (Page et al., 2021).

As buscas foram registradas em quatro bases: Google Acadêmico, ACM Digital Library, ScienceDirect e IEEE Xplore. Foram utilizadas três strings booleanas, combinando termos referentes ao algoritmo de Dijkstra, à dependência temporal, ao caminho mínimo, à complexidade, ao uso de memória e à escalabilidade. As consultas registradas foram realizadas em 10 de setembro de 2026, com o período de publicação delimitado entre 2016 e 2026, inclusive.

As strings utilizadas foram:

1. `("Dijkstra's algorithm" OR "Dijkstra*") AND ("time-dependent" OR "dynamic traffic") AND ("shortest path")`

2. `("bidirectional Dijkstra" OR "time-dependent Dijkstra") AND ("complexity" OR "scalability" OR "memory") AND ("urban network*" OR "routing")`

3. `("Dijkstra") AND ("dependente do tempo" OR "bidirecional" OR "tráfego dinâmico") AND ("caminho mínimo" OR "escalabilidade")`

Foram considerados elegíveis artigos científicos revisados por pares, publicados em português ou inglês, com texto completo disponível e pertinência direta ao problema do caminho mínimo em redes urbanas dinâmicas. A inclusão exigiu relação central com o algoritmo de Dijkstra, o TD-Dijkstra ou o Dijkstra Bidirecional, além de contribuição relevante para a análise teórica, matemática ou estrutural de complexidade, memória ou escalabilidade.

Foram excluídos trabalhos focados em A* e suas variantes, problemas de múltiplas entregas, Problema do Caixeiro Viajante (TSP), Problema de Roteamento de Veículos (VRP), implementação de software como contribuição central sem análise teórica suficiente, estudos fora do contexto de redes urbanas dinâmicas, duplicatas e documentos sem revisão por pares ou sem texto completo disponível para avaliação.

As contagens registradas pelo grupo totalizaram aproximadamente 2.533 resultados brutos: cerca de 2.400 no Google Acadêmico, 60 na ScienceDirect, 70 na ACM Digital Library e 3 na IEEE Xplore. Após a deduplicação de 130 registros, permaneceram 2.403 registros únicos. Na triagem por título e resumo, 2.325 foram classificados para exclusão, 65 foram inicialmente registrados como casos duvidosos e 13 foram selecionados como candidatos à leitura integral. Após a aplicação dos critérios de elegibilidade na etapa final, quatro artigos foram mantidos no corpus e nove foram excluídos.

A análise dos quatro estudos foi organizada por três eixos: (1) modelagem do caminho mínimo em redes dinâmicas; (2) complexidade assintótica e escalabilidade; e (3) uso de memória, limitações estruturais e lacunas teóricas. Para cada eixo, foram comparados objetivos, métodos, resultados, hipóteses e limitações. A síntese distingue expressões matemáticas de complexidade fornecidas pelos autores de resultados empíricos relatados nos estudos. Não foram realizadas implementações, benchmarks próprios ou simulações pelo grupo.

## Revisão da literatura

### Eixo 1: Modelagem do caminho mínimo em redes urbanas dinâmicas

A dependência temporal dos pesos das arestas é uma característica central dos problemas de caminho mínimo em redes urbanas dinâmicas. Em redes estáticas, o custo de uma aresta é considerado constante durante uma consulta. Em redes dependentes do tempo, o tempo de viagem pode variar conforme o instante de partida, tornando necessário avaliar o custo da aresta de acordo com o momento em que o veículo chega a ela.

Constantinou et al. (2016) abordam o problema do caminho mínimo em termos de tempo de viagem. Os autores consideram velocidades que variam por intervalo temporal e desenvolvem procedimentos para calcular o tempo de travessia das vias a partir do instante de partida. O trabalho apresenta uma formulação matemática para o cálculo do tempo de viagem e sua integração ao Dijkstra Dependente do Tempo. A propriedade FIFO, segundo a qual a ordem de chegada de veículos que partem em instantes diferentes não é invertida pela função de chegada considerada, tem papel relevante nas garantias de otimalidade do modelo.

Heni, Coelho e Renaud (2019) ampliam a análise ao tratar de caminhos mínimos de custo dependente do tempo sob vários componentes de custo. A função considerada incorpora fatores como emissões de gases de efeito estufa, consumo de combustível e custos do motorista, sujeitos a alterações do tráfego, do horário e da carga transportada. Os autores desenvolvem modelos de cálculo de custo e variantes do Dijkstra label-setting para representar essas dependências. O trabalho também destaca a importância da consistência FIFO para a construção de limites dependentes do tempo e para a aplicação das abordagens propostas.

Baum et al. (2016), por sua vez, investigam o roteamento dependente do tempo com padrões históricos de tráfego, atualizações de tráfego em tempo real e preferências dos usuários. A abordagem TDCRP (Time-Dependent Customizable Route Planning) organiza a rede em níveis e utiliza grafos de sobreposição para reduzir o espaço explorado nas consultas. Na fase de consulta, uma variante bidirecional de Dijkstra é executada sobre o grafo de busca reduzido. Assim, o trabalho relaciona a dependência temporal dos custos à organização estrutural do grafo e à escalabilidade do roteamento.

Sun, Li e Liu (2023) tratam de outra característica do tráfego urbano: a incerteza dos tempos de viagem e os atrasos provocados por interseções semaforizadas. Os autores formulam uma função periódica para representar o tempo de espera e apresentam uma transformação matemática que permite reduzir uma rede estocástica dependente do tempo a uma rede determinística dependente do tempo, sobre a qual pode ser aplicada uma abordagem de caminho mínimo baseada em Dijkstra. A contribuição está na inclusão formal dos atrasos semafóricos e da confiabilidade temporal na modelagem da rede.

Os quatro trabalhos convergem ao reconhecer que a dinâmica temporal exige uma representação mais elaborada dos custos das arestas do que aquela utilizada em uma rede estática. Entretanto, diferem quanto ao objetivo de otimização, às hipóteses adotadas e à forma de representar o tráfego. Constantinou et al. concentram-se no tempo de viagem; Heni et al. consideram diferentes componentes de custo; Baum et al. priorizam a atualização eficiente de métricas em uma estrutura multinível; e Sun et al. incorporam a incerteza temporal e a espera em semáforos.

Essas diferenças precisam ser consideradas na comparação. Embora todos os estudos utilizem ou adaptem abordagens baseadas em Dijkstra, seus resultados não correspondem necessariamente ao mesmo problema matemático. A modelagem adotada influencia as funções de custo, as condições de validade dos algoritmos e as garantias de otimalidade.

### Eixo 2: Complexidade assintótica e escalabilidade

A complexidade assintótica permite caracterizar o crescimento do custo computacional à medida que o tamanho do grafo aumenta. Para essa análise, são utilizadas as variáveis \(n=|V|\), correspondente ao número de vértices, e \(m=|E|\), correspondente ao número de arestas. Nas redes dependentes do tempo, a quantidade de intervalos temporais ou o número de períodos examinados também pode influenciar o custo dos procedimentos de cálculo das arestas.

Constantinou et al. (2016) apresentam uma análise explícita da complexidade do TD-Dijkstra. Como o procedimento ATT para determinar o tempo de travessia de uma aresta possui complexidade \(O(K)\), a implementação simples do algoritmo apresenta complexidade:

\[
O(n^2+mK).
\]

Os autores também discutem uma implementação com Fibonacci heap, cuja complexidade é:

\[
O(n\log n+mK).
\]

Essas expressões mostram que a escolha da estrutura de dados altera a parcela relacionada à seleção de vértices, enquanto o termo \(mK\) representa o custo adicional associado à avaliação temporal das arestas. Portanto, o número de intervalos temporais pode influenciar diretamente a complexidade do algoritmo.

Heni, Coelho e Renaud (2019) também apresentam expressões explícitas para diferentes procedimentos baseados no Dijkstra label-setting. O algoritmo clássico, sob a estrutura de dados considerada pelos autores, apresenta complexidade \(O(m\log n)\). Para as variantes dependentes do tempo, os autores apresentam:

\[
O(m\log n+n)
\]

para TD-Dijkstra-LTM,

\[
O(m\log n+nC)
\]

para TD-Dijkstra-LTM-STTF, e

\[
O(m\log n+nK)
\]

para TD-Dijkstra-FSM.

Nessas expressões, \(C\) representa a quantidade de passos utilizados pelo procedimento STTF, enquanto \(K\) representa o número máximo de períodos temporais examinados pela função de cálculo de custo FSM. Embora essas variáveis estejam relacionadas ao processamento temporal, seus significados específicos dependem dos procedimentos descritos no artigo e não devem ser tratados automaticamente como parâmetros idênticos.

Além disso, as expressões de Heni et al. precisam ser interpretadas dentro do problema de custo dependente do tempo sob vários componentes de custo. O trabalho apresenta métodos de cálculo e limites inferior e superior para obter soluções de boa qualidade; não se deve interpretar suas expressões como uma garantia de complexidade para qualquer formulação possível de caminho mínimo multiobjetivo.

Baum et al. (2016) fornecem uma contribuição complementar ao investigar a escalabilidade de uma estrutura multinível em redes rodoviárias extensas. A avaliação relatada pelos autores inclui instâncias da Alemanha, da Europa Ocidental e de Berlin/Brandenburg. No caso europeu, a rede contém aproximadamente 18 milhões de vértices e 42 milhões de arestas. A dimensão da rede permite discutir os desafios estruturais associados ao roteamento em escala continental. Entretanto, o trabalho não apresenta uma única expressão assintótica que possa ser colocada diretamente lado a lado com as expressões de Constantinou et al. e Heni et al. para representar todo o custo do TDCRP.

Sun, Li e Liu (2023) apresentam formulação matemática e resultados numéricos para o problema do caminho mínimo confiável em redes estocásticas dependentes do tempo. Porém, o artigo não fornece uma expressão assintótica de complexidade de tempo comparável às apresentadas pelos dois estudos anteriores, nem uma expressão geral de memória. Dessa forma, sua contribuição para este eixo está principalmente na modelagem do problema e no tratamento dos atrasos semafóricos.

A comparação revela que Constantinou et al. (2016) e Heni et al. (2019) são as referências mais diretas do corpus para a extração de expressões assintóticas. Baum et al. (2016) contribuem especialmente com evidências sobre escalabilidade estrutural de redes de grande porte, enquanto Sun et al. (2023) ampliam a modelagem temporal sem oferecer a mesma caracterização assintótica.

É importante ressaltar que não há uma comparação uniforme entre as variantes nas mesmas condições de rede, função de custo e estrutura de dados. Assim, as expressões devem ser discutidas de acordo com suas hipóteses originais, sem concluir que uma variante é universalmente superior apenas pela forma de sua expressão assintótica.

### Eixo 3: Uso de memória, limitações estruturais e lacunas teóricas

O uso de memória é uma dimensão essencial para o estudo da escalabilidade, especialmente quando os custos das arestas são representados por funções temporais. Em tais situações, o espaço necessário para armazenar informações pode depender não apenas do número de vértices e arestas, mas também da complexidade das funções de custo e dos perfis temporais.

Baum et al. (2016) apresentam a evidência mais direta dessa limitação no corpus. A abordagem TDCRP utiliza grafos de sobreposição cujos atalhos podem representar trajetos extensos e, consequentemente, apresentar funções temporais com um número elevado de pontos de quebra. Nos níveis superiores da hierarquia, a complexidade dessas funções cresce significativamente. Os autores relatam que, para a instância europeia, o cálculo exato dos perfis não pôde prosseguir além do quarto nível porque os 64 GiB de memória principal disponíveis eram insuficientes para armazenar todos os rótulos de perfil.

Para contornar esse problema, os autores simplificam os perfis temporais por meio de aproximações com erro controlado. Essa estratégia reduz a quantidade de pontos de quebra, o espaço necessário para armazenar os perfis e o custo de customização. Como consequência, o sistema consegue realizar consultas rápidas e próximas do ótimo, mas não garante exatidão absoluta em todos os casos quando são utilizados perfis aproximados. Trata-se de um compromisso entre memória, tempo de processamento e qualidade da solução.

Constantinou et al. (2016) apresentam a complexidade temporal dos procedimentos considerados, incluindo a influência do parâmetro \(K\), mas não fornecem uma expressão assintótica independente e comparável para o consumo de memória. Heni et al. (2019) também formalizam a complexidade temporal de diferentes variantes, sem estabelecer um limite geral de memória que possa ser diretamente comparado ao resultado estrutural apresentado por Baum et al. Sun et al. (2023), por sua vez, concentram-se na modelagem estocástica e nos atrasos semafóricos, sem apresentar uma expressão assintótica geral para memória.

Essa diferença de cobertura é um resultado importante da revisão: a ausência de uma expressão de memória em determinados artigos não significa que esses algoritmos não consumam memória, mas limita a possibilidade de comparação quantitativa com base apenas nos resultados publicados. Da mesma forma, a presença de avaliações computacionais nos artigos não substitui uma análise assintótica formal quando o objetivo é caracterizar o crescimento do custo em função das dimensões do problema.

A principal lacuna identificada é a ausência, no corpus selecionado, de uma comparação teórica uniforme que analise simultaneamente complexidade de tempo, consumo de memória, escalabilidade e garantias de otimalidade para Dijkstra clássico, TD-Dijkstra e Dijkstra Bidirecional sob as mesmas hipóteses de rede. Os estudos apresentam contribuições complementares, mas cada um enfatiza um aspecto diferente: complexidade assintótica, estrutura de roteamento multinível, formulação de custos ou confiabilidade temporal.

Essa lacuna também exige cuidado ao interpretar a comparação. O Dijkstra Bidirecional aparece no trabalho de Baum et al. como parte de uma estrutura multinível, de modo que não pode ser considerado isoladamente responsável pelo desempenho relatado. De maneira semelhante, os resultados sobre TD-Dijkstra variam de acordo com a função de custo, a representação temporal e o procedimento de avaliação das arestas.

### Síntese crítica

A análise dos quatro artigos indica que a literatura aborda o caminho mínimo em redes urbanas dinâmicas por diferentes perspectivas matemáticas e estruturais. Constantinou et al. (2016) oferecem uma análise explícita da complexidade do TD-Dijkstra, evidenciando a influência do número de intervalos temporais. Heni, Coelho e Renaud (2019) ampliam essa análise para diferentes modelos de custo dependente do tempo e apresentam expressões assintóticas para variantes label-setting. Baum et al. (2016) demonstram que a complexidade dos perfis temporais pode constituir um gargalo de memória em redes de grande porte, recorrendo a aproximações para tornar viáveis a customização e as consultas. Sun, Li e Liu (2023) contribuem com a formalização da incerteza temporal e dos atrasos semafóricos, mas não fornecem uma expressão assintótica comparável para tempo e memória.

Portanto, a principal tendência identificada é o aumento da importância da representação temporal e da estrutura da rede na análise da complexidade e da escalabilidade. Ao mesmo tempo, a cobertura desigual das dimensões pesquisadas impede uma classificação absoluta das variantes. A comparação mais defensável consiste em distinguir as expressões matemáticas explicitamente apresentadas, os resultados de escalabilidade relatados pelos autores e as dimensões para as quais não foram encontradas medidas teóricas comparáveis. O corpus permite caracterizar avanços e limitações, mas não sustenta uma conclusão universal de superioridade de uma variante sobre as demais.

## Considerações finais

Este artigo teve como objetivo analisar como a literatura científica caracteriza a complexidade, o uso de memória e a escalabilidade de Dijkstra e de suas variantes Dependente do Tempo e Bidirecional na busca pelo caminho mínimo em redes urbanas dinâmicas. A análise dos quatro estudos selecionados permitiu identificar contribuições complementares e uma lacuna relevante na comparação teórica dessas dimensões.

Em relação à complexidade de tempo, Constantinou et al. (2016) apresentam expressões explícitas para o TD-Dijkstra, incluindo \(O(n^2+mK)\) na implementação simples e \(O(n\log n+mK)\) com Fibonacci heap. Heni et al. (2019) também fornecem expressões assintóticas para diferentes variantes dependentes do tempo, demonstrando que o custo adicional depende do procedimento de cálculo de custos e da quantidade de períodos temporais examinados. Essas expressões, contudo, estão vinculadas a hipóteses e formulações específicas e não devem ser comparadas sem considerar os diferentes modelos de custo.

Quanto à escalabilidade, Baum et al. (2016) mostram que uma estrutura multinível pode reduzir o espaço pesquisado durante as consultas, mas também evidenciam que a complexidade dos perfis temporais dos atalhos pode gerar limitações severas de memória. O emprego de aproximações permite reduzir esse custo e realizar consultas próximas do ótimo. Sun et al. (2023) contribuem ao demonstrar como a incerteza temporal e a espera em semáforos podem ser incorporadas ao modelo, embora não apresentem uma análise assintótica de tempo e memória comparável à dos outros estudos.

A resposta à pergunta de pesquisa é, portanto, que a literatura caracteriza a complexidade, a memória e a escalabilidade de maneiras complementares, mas não uniformes. Alguns trabalhos formalizam a complexidade de tempo; outros demonstram limitações de memória ou propõem modelos temporais mais abrangentes. A ausência de uma análise comum para as três dimensões impede uma comparação definitiva entre Dijkstra clássico, TD-Dijkstra e Dijkstra Bidirecional sob todas as condições consideradas.

Como limitação desta revisão, o corpus é composto por apenas quatro estudos, e os trabalhos selecionados diferem quanto ao modelo temporal, à função de custo e à profundidade da análise assintótica. Além disso, a quantidade de resultados inicialmente recuperados exigiu uma triagem rigorosa, e as contagens das buscas foram registradas como aproximações. Essas características recomendam interpretar as conclusões como uma síntese do corpus selecionado, e não como uma caracterização exaustiva de toda a literatura existente.

Como continuidade acadêmica, recomenda-se aprofundar a extração das hipóteses matemáticas de cada variante, construir uma matriz que mantenha separadas as expressões de complexidade, os resultados de memória explicitamente relatados e as evidências de escalabilidade, e identificar quais dimensões permanecem sem formulação teórica nos artigos selecionados. Essas atividades podem ampliar a compreensão das limitações estruturais das variantes sem exigir implementação ou experimentação própria.

## Resumo

Este artigo analisa a complexidade, o uso de memória e a escalabilidade do algoritmo de Dijkstra e de suas variantes Dependente do Tempo e Bidirecional na busca pelo caminho mínimo em redes urbanas dinâmicas. Foi realizada uma revisão bibliográfica com busca sistematizada em quatro bases acadêmicas, aplicando critérios de inclusão e exclusão relacionados ao período de publicação, revisão por pares, pertinência temática e análise teórica. O levantamento registrou aproximadamente 2.533 resultados brutos, dos quais quatro artigos foram mantidos após as etapas de triagem e leitura integral. A análise comparativa identificou expressões explícitas de complexidade para variantes dependentes do tempo, evidências de limitações de memória associadas à complexidade de perfis temporais e contribuições para a modelagem da incerteza e dos atrasos semafóricos. Os estudos, entretanto, apresentam diferentes hipóteses e não oferecem uma comparação uniforme das três dimensões. Conclui-se que a literatura permite caracterizar aspectos complementares de complexidade e escalabilidade, mas permanece uma lacuna quanto à comparação teórica conjunta de tempo, memória e garantias de otimalidade entre as variantes analisadas.

## Referências

BAUM, Moritz; DIBBELT, Julian; PAJOR, Thomas; WAGNER, Dorothea. Dynamic time-dependent route planning in road networks with user preferences. In: INTERNATIONAL SYMPOSIUM ON EXPERIMENTAL ALGORITHMS, 15., 2016, St. Petersburg. *Experimental Algorithms*. Cham: Springer, 2016. p. 33–49. (Lecture Notes in Computer Science, v. 9685). DOI: https://doi.org/10.1007/978-3-319-38851-9_3.

CONSTANTINOU, Costas K.; ELLINAS, Georgios; PANAYIOTOU, Christos G.; POLYCARPOU, Marios M. Shortest path routing in transportation networks with time-dependent road speeds. In: INTERNATIONAL CONFERENCE ON VEHICLE TECHNOLOGY AND INTELLIGENT TRANSPORT SYSTEMS, 2016. *Proceedings [...]*. [S. l.]: SciTePress, 2016. p. 91–98. DOI: https://doi.org/10.5220/0005807000910098.

HENI, Hamza; COELHO, Leandro C.; RENAUD, Jacques. Determining time-dependent minimum cost paths under several objectives. *Computers & Operations Research*, v. 105, p. 102–117, 2019. DOI: https://doi.org/10.1016/j.cor.2019.01.007.

PAGE, Matthew J. et al. The PRISMA 2020 statement: an updated guideline for reporting systematic reviews. *BMJ*, v. 372, n. 71, 2021. DOI: https://doi.org/10.1136/bmj.n71.

SUN, Yanming; LI, Jie; LIU, Shixian. Study on the shortest reliable path of stochastic time-dependent transportation networks considering waiting time at signalized intersections. *Journal of Advanced Transportation*, v. 2023, art. 8298068, 2023. DOI: https://doi.org/10.1155/2023/8298068.

## Checklist

- [x] A introdução termina com o objetivo.
- [x] A metodologia descreve o processo registrado pelo grupo.
- [x] A revisão compara os artigos.
- [x] A conclusão responde ao problema.
- [x] O resumo representa o texto completo.