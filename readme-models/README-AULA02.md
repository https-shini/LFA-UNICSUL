<h1 align="center">📝 Aula 2 — Conceitos Iniciais e Grafos</h1>

<p align="center">
  <a href="../README.md">Home</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-resumo">Resumo</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-conteúdo-abordado">Conteúdo</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-exercício-prático">Exercício Prático</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-materiais-da-aula">Materiais</a>
</p>

---

## 📜 Resumo
Esta aula estabelece a base teórica para o estudo da teoria de linguagens formais, definindo os componentes essenciais de uma linguagem e as operações fundamentais que podem ser realizadas com elas. Além disso, introduz a teoria de grafos, que é um formalismo utilizado para a representação de autômatos.

## 🔍 Conteúdo abordado
-   **Conceitos Básicos de Linguagens Formais:**
    -   **Símbolo:** Uma entidade abstrata, indivisível, como uma letra, dígito ou caractere especial. Constituem os blocos de construção das linguagens.
    -   **Alfabeto (Σ):** Um conjunto finito de símbolos. Exemplos: `Σ = {0, 1}` para binários ou `Σ = {a, b, c}`.
    -   **Sentença (ou Palavra):** Uma sequência finita de símbolos de um alfabeto. O tamanho de uma sentença `w` é denotado por `|w|`. A sentença vazia é representada por `ε`.
    -   **Linguagem:** Um conjunto de sentenças válidas definidas por um conjunto de regras (gramática).
-   **Operações sobre Palavras:**
    -   **Prefixo:** Qualquer sequência inicial de símbolos de uma palavra. Exemplo: os prefixos de `abc` são `ε`, `a`, `ab`, `abc`.
    -   **Sufixo:** Qualquer sequência final de símbolos de uma palavra. Exemplo: os sufixos de `abc` são `ε`, `c`, `bc`, `abc`.
    -   **Subpalavra:** Qualquer sequência de símbolos contíguos. Inclui todos os prefixos e sufixos.
    -   **Concatenação:** A operação de unir duas palavras. É associativa. Exemplo: se `v = ab` e `w = c`, então `vw = abc`.
    -   **Potência em Palavra (`w^n`):** Concatenação sucessiva de uma palavra por `n` vezes. Por convenção, `w^0 = ε` (palavra vazia).
-   **Teoria de Grafos:** Introdução aos grafos como um conjunto de vértices (nós) e arestas (ligações).
    -   **Tipos de Grafo:** Diferenciação entre **grafos não-direcionados** (arestas sem sentido) e **grafos direcionados** (arestas com sentido, representadas por setas).
    -   **Conceitos:** Explora noções como grau de um nó, subgrafo, caminho (sequência de nós conectados por arestas) e ciclo (um caminho que começa e termina no mesmo nó).

---

## 💻 Exercício Prático
### Descrição
Dado o conceito de prefixo, sufixo e subpalavra, complete a análise para a palavra "automato".

### Resolução

**Palavra:** `automato`

#### Prefixo
Um prefixo é qualquer sequência inicial de símbolos.
* **Lista fornecida:** `ε, a, au, aut, auto, autom, automa, automat, automato`
* **Análise:** A lista está **correta**, pois inclui a palavra vazia (`ε`) e todas as sequências iniciais da palavra `automato`.

#### Sufixo
Um sufixo é qualquer sequência final de símbolos.
* **Lista fornecida:** `o, to, ato, mato, omato, tomatos, utomato, automato`
* **Análise:** A lista contém um erro. A palavra `tomatos` não é um sufixo de `automato`. O correto seria `tomato`.
* **Lista corrigida:** `ε, o, to, ato, mato, omato, tomato, utomato, automato`

#### Subpalavras
Uma subpalavra é qualquer sequência contígua de símbolos.
* **Lista fornecida:** `toma`, `omat`, `tomat`
* **Análise:** Nenhuma das palavras fornecidas (`toma`, `omat`, `tomat`) é uma subpalavra da palavra `automato`. As letras em `automato` são `a-u-t-o-m-a-t-o`. As sequências de letras `toma`, `omat` e `tomat` não aparecem de forma contígua.
* **Exemplos de subpalavras corretas:** `ut`, `to`, `om`, `ma`, `at`, `mato`.

---

## 📎 Materiais da Aula
-   [**PDF da Aula 2 - Conceitos Iniciais e Grafos**](slides/Aula02_Prefixo-Sufixo-Subpalavra.pdf)
