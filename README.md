# Complexidade e Escalabilidade de Dijkstra em Redes Urbanas Dinâmicas

Repositório do **Grupo 4** para o projeto de pesquisa da disciplina **Computabilidade e Complexidade de Algoritmos**.

## 👥 Integrantes do Grupo

* Gabriel Souza de Carvalho
* Pedro Henrique dos Santos
* Carlos Eduardo Laera Prado
* Brayan Allan Nagatani Campos de Almeida
* João Marcelo El Hafi Batista

## 👩‍🏫 Orientadora

**Profa. Dra. Andréa Ono Sakai**

## 🎯 Tema

**Complexidade e escalabilidade de Dijkstra e suas variantes dependentes do tempo em redes urbanas.**

O trabalho concentra-se na análise teórica do algoritmo de Dijkstra e de suas variantes **Dijkstra Dependente do Tempo** e **Dijkstra Bidirecional**, considerando redes urbanas com tráfego variável.

## 🎯 Objetivo Geral

Analisar, com base na literatura científica, a complexidade, o uso de memória e a escalabilidade do algoritmo de Dijkstra e de suas variantes Dependente do Tempo e Bidirecional na busca pelo caminho mínimo em redes urbanas dinâmicas com tráfego variável.

## ❓ Pergunta de Pesquisa

> Como a literatura caracteriza a complexidade, o uso de memória e a escalabilidade do algoritmo de Dijkstra e de suas variantes Dependente do Tempo e Bidirecional na busca pelo caminho mínimo em redes urbanas dinâmicas?

## 🔎 Escopo da Pesquisa

O projeto possui caráter **exclusivamente bibliográfico e teórico**. A análise está direcionada à literatura científica sobre:

* algoritmo de Dijkstra;
* Dijkstra Dependente do Tempo (TD-Dijkstra);
* Dijkstra Bidirecional;
* problema do caminho mínimo;
* redes urbanas dinâmicas e tráfego dependente do tempo;
* complexidade assintótica;
* uso de memória;
* escalabilidade;
* comportamento estrutural dos grafos.

O estudo considera principalmente as variáveis estruturais:

$$
n = |V|
$$

representando o número de vértices da rede,

$$
m = |E|
$$

representando o número de arestas, e

$$
K
$$

representando o número de intervalos temporais utilizados na modelagem do tráfego dependente do tempo.

## 🚫 Critérios de Delimitação

Para manter o escopo definido pelo Grupo 4, a pesquisa **não aborda**:

* desenvolvimento ou implementação de software;
* desenvolvimento de sistemas de roteamento;
* benchmarks de código;
* simulações computacionais como contribuição central;
* engenharia de hardware;
* algoritmo A* e suas variantes;
* Problema do Caixeiro Viajante (TSP);
* Problema de Roteamento de Veículos (VRP);
* planejamento de múltiplas entregas.

O foco permanece no **problema do caminho mínimo** em redes urbanas dinâmicas e na análise teórica de complexidade, memória e escalabilidade.

## 📚 Metodologia Bibliográfica

A revisão bibliográfica foi estruturada em etapas de planejamento, busca, triagem e seleção de estudos.

Foram utilizadas quatro bases de dados:

* **IEEE Xplore**
* **ACM Digital Library**
* **ScienceDirect (Elsevier)**
* **Google Acadêmico**

Foram definidas três strings booleanas de busca e aplicados critérios de inclusão e exclusão para selecionar os trabalhos mais aderentes ao tema.

### Fluxo da triagem

$$
2533\text{ resultados brutos}
\rightarrow
130\text{ duplicatas}
\rightarrow
2403\text{ registros únicos}
$$

$$
2403
\rightarrow
2325\text{ excluídos}
+
65\text{ dúvidas}
+
13\text{ potenciais}
$$

$$
13
\rightarrow
9\text{ excluídos}
+
4\text{ artigos definitivos}
$$

## 📖 Artigos Selecionados

O conjunto definitivo da revisão é composto por quatro trabalhos:

1. **Constantinou et al. (2016)** — *Shortest Path Routing in Transportation Networks with Time-Dependent Road Speeds*.
2. **Baum et al. (2016)** — *Dynamic Time-Dependent Route Planning in Road Networks with User Preferences*.
3. **Heni et al. (2019)** — *Determining Time-Dependent Minimum Cost Paths under Several Objectives*.
4. **Sun et al. (2023)** — *Study on the Shortest Reliable Path of Stochastic Time-Dependent Transportation Networks Considering Waiting Time at Signalized Intersections*.

## 📊 Foco da Análise

A etapa de análise do projeto será concentrada na comparação teórica dos estudos selecionados, considerando principalmente:

| Dimensão                  | Foco                                                                    |
| ------------------------- | ----------------------------------------------------------------------- |
| **Complexidade de tempo** | Ordem assintótica e dependência de \(n\), \(m\) e \(K\)                 |
| **Uso de memória**        | Estruturas necessárias para representar e processar o grafo             |
| **Escalabilidade**        | Comportamento à medida que o tamanho e a dinâmica da rede aumentam      |
| **Estrutura temporal**    | Impacto dos pesos das arestas dependentes do tempo                      |
| **Variantes**             | Diferenças entre Dijkstra clássico, TD-Dijkstra e Dijkstra Bidirecional |

## 📂 Organização do Repositório

```text
/
├── docs/
│   ├── a_Escolha_do_Tema.md
│   ├── b_Levantamento_Bibliografico_Preliminar.md
│   └── c_objetivo_geral_e_especificos.md
│
└── README.md
```

A pasta `/docs` concentra os documentos acadêmicos, registros metodológicos e etapas de desenvolvimento da pesquisa.

O repositório **não tem como objetivo armazenar uma implementação do algoritmo ou um sistema de roteamento**. Seu propósito é documentar o desenvolvimento da pesquisa bibliográfica e da análise teórica.

## 🧠 Próximas Etapas

Após a definição do corpus bibliográfico, o grupo dará continuidade à pesquisa com:

* fichamento teórico dos quatro artigos selecionados;
* extração das formulações matemáticas relevantes;
* identificação das complexidades assintóticas;
* análise do uso de memória;
* análise da escalabilidade;
* construção de uma matriz comparativa entre Dijkstra, TD-Dijkstra e Dijkstra Bidirecional;
* elaboração da discussão e das considerações finais.

---

**Grupo 4 — Ciência da Computação 6° Semestre Noite**
**Computabilidade e Complexidade de Algoritmos**
