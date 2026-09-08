# Etapa (a) — Escolha do Tema

> **Como preencher:** este documento deve ser preenchido **em conjunto pelo grupo**, mas com registro individualizado da contribuição de cada integrante. Substitua os campos entre `[ ]` pelas informações do seu grupo. Não apague as instruções em itálico — elas ajudam na avaliação do orientador.

---

## 1. Identificação do Grupo

| Campo | Informação |
|---|---|
| Curso / Disciplina | Ciência da Computação |
| Projeto de Pesquisa / IC | Roteamento de Entregas Urbanas |
| Orientador(a) | Dra. Andrea Ono Sakai |
| Data de entrega desta etapa | 18/08/2026 |
| Integrantes do grupo | Gabriel Souza de Carvalho, Pedro Henrique dos Santos, Carlos Eduardo Laera Prado, Brayan Allan Nagatani Campos de Almeida |

---

## 2. Tema Escolhido

### 2.1 Área geral de interesse
*Qual grande área do conhecimento/disciplina motivou a escolha (ex.: complexidade dos algoritmos, classes de problemas P, NP, Algoritmos Gulosos, Programação Dinâmica, Divisão e conquista)?*

A área geral de interesse que motivou a escolha deste trabalho concentra-se na Teoria dos Grafos, na Otimização Combinatória e no estudo dos Algoritmos Gulosos. A escolha foi impulsionada diretamente pela experiência e pelos resultados obtidos no desenvolvimento do nosso projeto prático do semestre anterior, que consistiu na criação de um sistema interativo de roteamento logístico para entregas urbanas.Naquele contexto, aplicamos o Algoritmo de Dijkstra — um clássico representante da classe dos algoritmos gulosos — para resolver o Problema do Caminho Mínimo (Shortest Path Problem). A necessidade de garantir a eficiência do sistema nos levou a estudar a fundo a complexidade computacional dos algoritmos de busca em grafos, implementando otimizações estruturais como Filas de Prioridade (Min-Heap) para alcançar um desempenho de O((V + E) \log V).Essa vivência prática de modelar cruzamentos reais como vértices e ruas como arestas ponderadas geograficamente despertou o interesse do grupo em aprofundar a pesquisa. O objetivo agora é expandir nossa base teórica para compreender como algoritmos gulosos e heurísticas lidam com restrições do mundo real em redes urbanas, explorando as limitações do Dijkstra clássico frente a variáveis dinâmicas de tráfego e restrições de infraestrutura.

### 2.2 Tema delimitado (versão final)
*Escreva o tema já delimitado, de forma específica — não o tema amplo. Lembre-se: o tema deve ser enunciado em 1 a 2 frases, como um assunto (ainda não é uma pergunta de pesquisa, isso vem na etapa "c").*

Tema: A análise bibliográfica de estratégias de otimização para roteamento logístico urbano, com foco nas extensões teóricas do Algoritmo de Dijkstra. O estudo investiga, por meio da literatura, a incorporação de restrições viárias estáticas e variáveis dinâmicas de tráfego, visando identificar propostas de melhoria conceitual para modelos de grafos puramente geográficos.

### 2.3 Do amplo ao específico
*Mostre o raciocínio de delimitação — como vocês chegaram do tema amplo ao tema específico.*

| Tema amplo (ponto de partida) | Tema delimitado (ponto de chegada) |
|---|---|
| Teoria dos Grafos e Otimização Combinatória aplicadas a algoritmos de busca de caminho mínimo. | A análise bibliográfica das extensões teóricas do Algoritmo de Dijkstra para roteamento logístico urbano, incorporando restrições viárias estáticas e métricas dinâmicas de tráfego. |

---

## 3. Justificativa da Escolha

### 3.1 Relevância
*Por que esse tema é importante ou atual? Para quem ele importa (academia, mercado, sociedade)?*

A otimização do roteamento urbano é altamente atual devido ao avanço do e-commerce e aos desafios de mobilidade. Para o mercado logístico, evoluir algoritmos como o Dijkstra reduz custos e otimiza o tempo nas entregas de "última milha". Na academia, o tema é relevante por conectar a abstração da Teoria dos Grafos às restrições viárias dinâmicas do mundo real. Para a sociedade, rotas mais inteligentes reduzem congestionamentos e emissões de carbono, demonstrando o impacto socioambiental positivo da computação.

### 3.2 Viabilidade
*O grupo avaliou se tem tempo, recursos, acesso a dados/fontes e domínio mínimo do assunto para desenvolver esse tema até o fim do projeto?*

| Critério | Avaliação (Sim/Parcial/Não) | Observação |
|---|---|---|
| Tempo disponível é suficiente | Sim | O escopo restringe-se à pesquisa bibliográfica de literatura selecionada (3 a 4 artigos-chave), o que é perfeitamente exequível dentro do nosso cronograma do semestre letivo. |

| Há acesso a fontes/dados necessários | Sim | Nós já mapeamos preliminarmente os três artigos-alvo e suas temáticas, e todos estão disponíveis para acesso em bases de dados acadêmicas (como IEEE, ACM ou Google Scholar). |

| O grupo já tem domínio mínimo do tema | Parcial | Embora eu e meus colegas já tenhamos desenvolvido a base do sistema com o Dijkstra clássico, ainda precisamos aprofundar nossos conhecimentos teóricos nas modelagens matemáticas que lidam com variáveis dinâmicas de trânsito e restrições urbanas. |       

| Recursos técnicos necessários estão disponíveis | Sim | Como a nossa pesquisa atual tem caráter exclusivamente teórico-bibliográfico, os recursos necessários limitam-se a computadores, acesso à internet e gerenciadores de referências, que nós já possuímos. |

### 3.3 Originalidade / Não-redundância
*O grupo verificou rapidamente (via um levantamento preliminar) se o tema já é excessivamente explorado ou se existe um ângulo próprio a ser explorado?*

Sim. Embora o Algoritmo de Dijkstra clássico seja um assunto amplamente documentado e consolidado na literatura, o nosso levantamento preliminar demonstrou que a modelagem de suas extensões dinâmicas para cenários urbanos hiperconectados oferece excelentes oportunidades de investigação. O nosso "ângulo próprio" reside em analisar a literatura não de forma genérica, mas com um olhar focado na transição estrutural do modelo: investigar como a teoria resolve a evolução de um grafo puramente geográfico para um grafo influenciado por estressores viários (como tempos de semáforo e previsões de tráfego em tempo real). Como já vivenciamos as limitações do modelo básico na prática, a nossa revisão ganha um caráter crítico e direcionado para a identificação de estratégias reais de otimização logística.

---

## 4. Validação com o Orientador

| Campo | Informação |
|---|---|
| Data da conversa/validação | 18/08/2026 |
| Tema aprovado pelo orientador? | Sim com ajustes |
| Observações ou ajustes solicitados pelo orientador | A professora validou o nosso escopo, reforçando que o trabalho consistirá exclusivamente na busca e montagem da base de artigos, sem qualquer etapa de implantação de código. Ela nos orientou a realizar pesquisas teóricas mais aprofundadas sobre o tema na literatura, dando destaque especial ao embasamento sobre algoritmos gulosos e como suas extensões se aplicam ao nosso cenário. |

---

## 5. Contribuição Individual dos Integrantes

> **Importante:** cada integrante deve descrever, com suas próprias palavras, o que efetivamente fez nesta etapa. Contribuições genéricas como "ajudei em tudo" não serão aceitas. Use verbos de ação e seja específico (ex.: "pesquisei 5 temas candidatos e apresentei prós/contras ao grupo").

### Integrante 1 — Gabriel Souza de Carvalho
- **O que fez nesta etapa:** Conduzi a redação e estruturação da Área de Interesse e da Justificativa da pesquisa, articulando a transição do nosso projeto prático anterior (código) para a abordagem exclusivamente teórica exigida para este semestre.
- **Tempo dedicado (aprox.):** 1h30m
- **Evidência da contribuição** Redação direta do texto das seções 2.1 e 3.1 no documento final do grupo durante o horário de aula.

### Integrante 2 — Pedro Henrique dos Santos
- **O que fez nesta etapa:** Realizei o levantamento preliminar dos três artigos acadêmicos (estado da arte, restrições urbanas e caso real da J&T Express) e estruturei a matriz de Viabilidade e Originalidade baseada nas fontes encontradas.
- **Tempo dedicado (aprox.):** 1h30m
- **Evidência da contribuição:** Apresentação dos resumos dos artigos selecionados e debate presencial com a equipe em sala de aula.

### Integrante 3 — Carlos Eduardo Laera Prado
- **O que fez nesta etapa:** Representei o grupo no alinhamento presencial/síncrono com a professora orientadora para apresentar o tema inicial, e fui o responsável por registrar as diretrizes de ajuste.
- **Tempo dedicado (aprox.):** 1h30m
- **Evidência da contribuição:** Conversas com a professora e preenchimento da seção 4 do documento.

### Integrante 4 — Brayan Allan Nagatani Campos de Almeida
- **O que fez nesta etapa:** Analisei o Pipeline da Pesquisa Bibliográfica fornecido pela professora e fui o responsável por afunilar o "Tema Amplo" para o "Tema Delimitado", garantindo que a nossa proposta estivesse estritamente alinhada com as etapas (a) e (b) do método exigido.
- **Tempo dedicado (aprox.):** 1h30m
- **Evidência da contribuição:** Estruturação da tabela de delimitação (do amplo ao específico) e revisão geral dos pontos preenchidos no formulário.

### 5.1 Quadro-resumo de participação

| Integrante | Contribuição principal | % estimado de participação nesta etapa |
|---|---|---|
| Gabriel Souza de Carvalho | Redação da área de interesse e justificativa do tema | 25% |
| Pedro Henrique dos Santos | Seleção dos artigos de referência e avaliação de viabilidade | 25% |
| Carlos Eduardo Laera Prado | Atendimento com a professora e registro dos ajustes do orientador | 25% |
| Brayan Allan Nagatani Campos de Almeida | Análise do método e delimitação do tema do amplo ao específico | 25% |

*A soma das porcentagens deve ser igual a 100%. Divergências de percepção sobre a participação devem ser discutidas em grupo antes do envio — o orientador pode solicitar esclarecimentos individuais em caso de disparidade relevante.*

---

## 6. Checklist Final da Etapa

- [x] Tema delimitado e redigido em 1-2 frases
- [x] Justificativa de relevância escrita
- [x] Viabilidade avaliada pelo grupo
- [x] Verificação preliminar de originalidade realizada
- [x] Tema validado com o orientador
- [x] Contribuição individual de cada integrante registrada
- [x] Quadro-resumo de participação preenchido (soma = 100%)

---


