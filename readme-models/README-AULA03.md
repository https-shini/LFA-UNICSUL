<h1 align="center">📝 Aula 3 — Expressões Regulares e Autômatos Finitos Determinísticos (AFD)</h1>

<p align="center">
  <a href="../README.md">Home</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-resumo">Resumo</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-conteúdo-abordado">Conteúdo</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-exercício-prático">Exercício Prático</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-materiais-da-aula">Materiais</a>
</p>

---

## 📜 Resumo
Esta aula aprofunda a relação entre Expressões Regulares (ER) e Autômatos Finitos (AF). As ERs são apresentadas como uma forma concisa de descrever linguagens regulares, enquanto os autômatos são formalismos matemáticos que as reconhecem. O foco principal é a estrutura, a definição formal e o funcionamento dos Autômatos Finitos Determinísticos (AFD).

## 🔍 Conteúdo abordado
### 1. Expressões Regulares (ER)
* **O que são?** As expressões regulares são formalismos denotacionais usados para descrever linguagens regulares. Elas permitem que se infira como construir ("gerar") as palavras de uma linguagem.
* **Operações Fundamentais:**
    * **União (`r U s`):** A união de duas linguagens.
    * **Concatenação (`r.s`):** A junção de duas linguagens.
    * **Fecho de Kleene (`r*`):** Representa zero ou mais repetições de uma expressão.

### 2. Autômatos Finitos (AF)
* **Reconhecedores de Linguagem:** São modelos matemáticos que atuam como reconhecedores de linguagens, verificando se uma palavra pertence ou não a um conjunto de sentenças válidas.
* **Sistema de Estados Finitos:** Podem ser vistos como sistemas de estados finitos, compostos por um conjunto de estados e transições. A disciplina diferencia três tipos:
    * **Determinístico:** Para cada estado e símbolo lido, o sistema assume um **único** estado de destino bem definido.
    * **Não Determinístico:** Para cada estado e símbolo lido, o sistema pode assumir um **conjunto** de estados alternativos.
    * **Com Movimento Vazio (ε-transição):** Permite a transição entre estados sem a leitura de nenhum símbolo de entrada.

### 3. Autômato Finito Determinístico (AFD)
* **Modelo Computacional:** Um AFD é compreendido como uma máquina abstrata composta por três partes:
    * **Fita:** Onde a palavra de entrada é armazenada. A fita é finita, dividida em células e lida da esquerda para a direita.
    * **Unidade de Controle:** Reflete o estado atual da máquina e tem um número finito de estados predefinidos.
    * **Função de Transição (δ):** A "lógica" do autômato. É responsável por comandar as leituras e determinar o próximo estado com base no estado atual e no símbolo lido.
* **Definição Formal:** Um AFD é formalmente representado por uma 5-tupla ordenada:
    `M = (Σ, Q, δ, q0, F)`
    * `Σ`: O alfabeto de entrada.
    * `Q`: O conjunto finito de estados.
    * `δ`: A função de transição. Ex: `δ(p, a) = q`.
    * `q0`: O estado inicial.
    * `F`: O conjunto de estados finais (ou de aceitação).
* **Computação e Aceitação:** A computação consiste na aplicação sucessiva da função de transição para cada símbolo da palavra. Uma palavra é **aceita** se o autômato termina em um estado final após processar toda a entrada.

---

## 💻 Exercício Prático
### Descrição
Com base no Autômato Finito Determinístico (AFD) `M1` apresentado no material da aula (Slide 20), realize as seguintes tarefas:
1.  Defina formalmente o autômato `M1` (a 5-tupla).
2.  Trace a computação da palavra `ababa` para determinar se ela é aceita ou rejeitada.

### Resolução

**1. Definição Formal do AFD M1**
O autômato `M1` é definido como:
`M1 = ({a,b}, {q0, q1, q2, qf}, δ, q0, {qf})`

* **`Σ` (Alfabeto):** `{a, b}`
* **`Q` (Estados):** `{q0, q1, q2, qf}`
* **`δ` (Função de Transição):**
    | Estado | a | b |
    |:---:|:---:|:---:|
    | `q0` | `q1` | `q2` |
    | `q1` | `qf` | `q2` |
    | `q2` | `q1` | `qf` |
    | `qf` | `qf` | `qf` |
  
* **`q0` (Estado Inicial):** `q0`
* **`F` (Estados Finais):** `{qf}`

**2. Traçando a Computação da Palavra `ababa`**
A computação processa a palavra `ababa` símbolo por símbolo, iniciando no estado `q0`.

* **Estado inicial:** `q0`
* **Lê 'a'**: De `q0` para `q1`.
* **Lê 'b'**: De `q1` para `q2`.
* **Lê 'a'**: De `q2` para `q1`.
* **Lê 'b'**: De `q1` para `q2`.
* **Lê 'a'**: De `q2` para `q1`.
* **Fim da palavra**. A computação termina no estado `q1`.

O estado final da computação (`q1`) **não** é um estado de aceitação (`qf`). Portanto, a palavra `ababa` é **rejeitada** por `M1`.

---

## 📎 Materiais da Aula
-   [**PDF da Aula 3**](slides/Aula03_ER-AFD.pdf)
