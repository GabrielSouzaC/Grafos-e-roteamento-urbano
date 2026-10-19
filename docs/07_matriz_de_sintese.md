# Etapa 7 Matriz de síntese e organização da revisão

## Solicitação

Compare os artigos e organize a revisão por temas ou eixos. Não produza apenas uma sequência de resumos.

## Eixos da revisão

1. `Modelagem do caminho mínimo em redes urbanas dinâmicas: pesos dependentes do tempo, propriedade FIFO e condições de otimalidade.`
2. `Complexidade assintótica e escalabilidade: influência do tamanho do grafo e da representação temporal dos custos.`
3. `Uso de memória, limitações estruturais e lacunas na análise teórica das variantes de Dijkstra.`

## Matriz de síntese

| Eixo | Artigos relacionados | Convergências | Divergências | Limitações | Lacunas |
|---|---|---|---|---|---|
| Modelagem do caminho mínimo em redes urbanas dinâmicas | Constantinou et al. (2016); Baum et al. (2016); Heni et al. (2019); Sun et al. (2023) | Os quatro trabalhos tratam de problemas de caminho mínimo em redes cujos custos ou tempos de viagem variam conforme o tempo. Todos adaptam ou utilizam abordagens baseadas em Dijkstra para considerar características temporais da rede. | Constantinou et al. modelam velocidades variáveis nas vias; Baum et al. incorporam perfis históricos, atualizações de tráfego e preferências dos usuários; Heni et al. consideram custos associados a diferentes objetivos, incluindo emissões e custos operacionais; Sun et al. tratam da incerteza dos tempos de viagem e da espera em interseções semaforizadas. | Os modelos utilizam hipóteses diferentes para representar os custos e as condições temporais. Em particular, a formulação FIFO e o tipo de função de custo influenciam a aplicabilidade e as garantias dos métodos. | Falta uma comparação entre os quatro modelos sob hipóteses matemáticas comuns, permitindo separar o efeito da variante do algoritmo do efeito da própria modelagem da rede. |
| Complexidade assintótica e escalabilidade | Constantinou et al. (2016); Baum et al. (2016); Heni et al. (2019); Sun et al. (2023) | Os trabalhos evidenciam que a dinâmica temporal pode aumentar o custo da busca ou exigir estruturas e operações adicionais. A complexidade depende não apenas do grafo, mas também da representação temporal dos custos e da abordagem adotada. | Constantinou et al. apresentam as expressões \(O(n^2+mK)\) e \(O(n\log n+mK)\) para o TD-Dijkstra, conforme a estrutura de dados utilizada. Heni et al. apresentam complexidades diferentes para variantes de Dijkstra adaptadas aos respectivos modelos de custo. Baum et al. concentram-se na escalabilidade de um método multinível e apresentam avaliações em redes extensas. Sun et al. priorizam a formulação matemática do caminho mínimo confiável, sem apresentar uma expressão assintótica comparável às dos demais. | As expressões de complexidade referem-se a problemas, procedimentos e hipóteses distintos. Os resultados de Heni et al. devem ser interpretados considerando a formulação multiobjetivo e o cálculo de limites de custo, não como uma garantia de complexidade polinomial para toda formulação exata do problema. As avaliações de escalabilidade de Baum et al. dependem da estrutura hierárquica utilizada. | Não há uma análise assintótica comparativa única para Dijkstra clássico, TD-Dijkstra e Dijkstra Bidirecional nas mesmas condições de rede. A influência dos intervalos temporais também é definida de maneiras diferentes entre os modelos. |
| Uso de memória e limitações estruturais | Principalmente Baum et al. (2016), com contribuições complementares de Constantinou et al. (2016), Heni et al. (2019) e Sun et al. (2023) | Os artigos mostram que a representação dos custos temporais e a complexidade das funções associadas às arestas podem afetar a viabilidade e a escalabilidade das abordagens de caminho mínimo. | Baum et al. discutem diretamente o crescimento da complexidade funcional dos atalhos e seu impacto na memória, utilizando aproximações para tornar o método viável. Constantinou et al. explicitam o custo temporal da consulta, mas não apresentam uma análise assintótica independente de memória. Heni et al. fornecem expressões de complexidade de tempo, sem estabelecer uma expressão geral comparável para memória. Sun et al. não apresentam uma análise assintótica explícita de memória. | As dimensões de memória não são quantificadas de maneira uniforme nos quatro estudos. No método de Baum et al., a aproximação dos perfis reduz o custo de armazenamento, mas resulta em consultas próximas do ótimo, não necessariamente exatas em todos os casos. Sun et al. também reconhecem restrições no modelo de tráfego e a necessidade de avaliar redes maiores. | A principal lacuna é a ausência de uma comparação teórica sistemática do uso de memória das variantes de Dijkstra em redes urbanas dinâmicas. Também falta uma análise integrada que relacione complexidade de tempo, memória, estrutura temporal e garantias de otimalidade sob um mesmo conjunto de hipóteses. |

## Roteiro da revisão da literatura

### Eixo 1 — Modelagem do caminho mínimo em redes urbanas dinâmicas

- **Ideia principal:** `A variação temporal dos custos das arestas modifica a formulação do problema do caminho mínimo e exige que o instante de partida e as condições da rede sejam considerados na determinação do trajeto. A propriedade FIFO é relevante para as garantias de otimalidade e para a aplicação de métodos label-setting baseados em Dijkstra.`

- **Evidências que serão usadas:** `Constantinou et al. (2016) apresentam um modelo de velocidades dependentes do tempo e procedimentos para calcular o tempo de travessia das vias. Baum et al. (2016) integram padrões históricos de tráfego, atualizações de tráfego e preferências dos usuários. Heni et al. (2019) formulam custos dependentes do tempo sob múltiplos objetivos e discutem a consistência FIFO. Sun et al. (2023) incorporam matematicamente a espera em interseções semaforizadas e transformam uma rede estocástica dependente do tempo em uma representação determinística dependente do tempo.`

- **Comparação entre estudos:** `Os artigos convergem ao reconhecer que o custo de uma aresta pode depender do instante de partida, mas diferem na função de custo considerada, na representação da incerteza e no tratamento de fenômenos urbanos. Constantinou et al. concentram-se no tempo de viagem; Heni et al. ampliam a função de custo; Baum et al. enfatizam atualizações dinâmicas e preferências; Sun et al. consideram a confiabilidade e os atrasos semafóricos.`

- **Ligação com o problema:** `Esse eixo estabelece as condições sob as quais a complexidade e a escalabilidade podem ser analisadas. Ele também explica por que os resultados dos artigos não devem ser comparados sem considerar as diferenças entre suas formulações matemáticas.`

### Eixo 2 — Complexidade assintótica e escalabilidade

- **Ideia principal:** `A análise de complexidade deve considerar o número de vértices n, o número de arestas m e a representação temporal dos custos. O custo adicional decorrente da dinâmica temporal depende das operações necessárias para calcular e processar funções ou intervalos de tempo, além das estruturas utilizadas na busca.`

- **Evidências que serão usadas:** `Constantinou et al. (2016) apresentam O(n² + mK) para uma implementação simples do TD-Dijkstra e O(n log n + mK) quando se utiliza uma Fibonacci heap. Heni et al. (2019) apresentam O(m log n + n), O(m log n + nC) e O(m log n + nK) para variantes relacionadas aos diferentes métodos de cálculo de custo, sendo C o número de passos utilizados pelo procedimento STTF e K o número máximo de períodos examinados pelo procedimento FSM. Baum et al. (2016) investigam a escalabilidade de um método multinível em redes rodoviárias extensas, enquanto Sun et al. (2023) desenvolvem e avaliam uma formulação de caminho mínimo confiável sem apresentar uma expressão assintótica comparável.`

- **Comparação entre estudos:** `Constantinou et al. e Heni et al. fornecem expressões explícitas de complexidade, mas os termos temporais e os procedimentos analisados não são idênticos. Baum et al. oferecem evidências sobre escalabilidade estrutural e desempenho de consultas por meio de uma abordagem multinível. Sun et al. contribuem principalmente para a formulação matemática do problema e para a incorporação de restrições temporais urbanas.`

- **Ligação com o problema:** `Esse eixo responde diretamente à dimensão de complexidade da pergunta de pesquisa e permite identificar quais artigos fornecem resultados assintóticos explícitos, quais avaliam escalabilidade por meio de suas estruturas e quais deixam essa dimensão sem quantificação formal.`

### Eixo 3 — Uso de memória, limitações estruturais e lacunas

- **Ideia principal:** `O uso de memória está associado à representação das funções de custo e dos perfis temporais, especialmente em métodos que armazenam atalhos ou informações para acelerar consultas. A escalabilidade depende, portanto, tanto do tamanho do grafo quanto da complexidade das estruturas temporais utilizadas.`

- **Evidências que serão usadas:** `Baum et al. (2016) mostram que a complexidade dos perfis temporais nos níveis superiores dos grafos de sobreposição pode impedir o cálculo exato por falta de memória. Os autores utilizam aproximações para reduzir esse consumo e viabilizar consultas rápidas próximas do ótimo. Constantinou et al. (2016) e Heni et al. (2019) fornecem resultados de complexidade de tempo, mas não estabelecem uma expressão geral de complexidade de memória comparável à análise estrutural de Baum et al. Sun et al. (2023) também não apresenta uma expressão assintótica explícita para o consumo de memória.`

- **Comparação entre estudos:** `Baum et al. são a referência mais direta para discutir a memória como limitação estrutural da representação temporal. Os outros três trabalhos contribuem para a compreensão da formulação temporal e da complexidade de tempo, mas não permitem uma comparação quantitativa uniforme do consumo de memória.`

- **Ligação com o problema:** `Esse eixo evidencia que a literatura selecionada não oferece uma resposta uniforme para as três dimensões da pergunta de pesquisa. Ele também permite identificar lacunas específicas, especialmente a falta de uma análise comparativa do consumo de memória e de uma avaliação assintótica comum às variantes consideradas.`

## Síntese crítica provisória

`A literatura selecionada converge na constatação de que redes urbanas dinâmicas exigem modelos de caminho mínimo que considerem a variação temporal dos custos e que essa representação influencia a complexidade e a escalabilidade dos métodos baseados em Dijkstra. Constantinou et al. (2016) e Heni et al. (2019) oferecem as expressões assintóticas mais explícitas para variantes dependentes do tempo, embora aplicadas a modelos e procedimentos diferentes. Baum et al. (2016) evidenciam que a complexidade funcional dos perfis temporais pode tornar o consumo de memória um limitador da escalabilidade, recorrendo a aproximações para viabilizar consultas eficientes. Sun et al. (2023) ampliam a modelagem ao incorporar incerteza temporal e espera em cruzamentos semaforizados, mas não apresentam uma análise assintótica comparável de tempo e memória. Como lacuna principal, os quatro estudos não fornecem uma comparação teórica uniforme entre Dijkstra clássico, TD-Dijkstra e Dijkstra Bidirecional que contemple simultaneamente complexidade, memória, escalabilidade e garantias de otimalidade. A revisão deverá, portanto, preservar as diferenças de formulação entre os artigos e distinguir resultados formais de complexidade de evidências de desempenho relatadas pelos próprios autores.`

## Checklist

- [x] Os artigos foram agrupados por ideias.
- [x] Há comparações entre estudos.
- [x] As divergências foram registradas.
- [x] As lacunas são específicas e sustentadas pelas leituras.