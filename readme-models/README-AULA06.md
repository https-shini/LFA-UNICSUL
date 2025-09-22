<h1 align="center">📝 Aula 6 — Gramáticas Livres de Contexto (GLC) e Análise Sintática</h1>

<p align="center">
  <a href="../README.md">Home</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-resumo">Resumo</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-conteúdo-abordado">Conteúdo</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-exercício-prático">Exercício Prático</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-materiais-da-aula">Materiais</a>
</p>

---

## 📜 Resumo
Esta aula se aprofunda nas Gramáticas Livres de Contexto (GLC), que são fundamentais para definir a sintaxe de linguagens de programação. O material explora as representações gráficas das derivações, o conceito de ambiguidade e as principais estratégias de análise sintática. As GLCs são essenciais para tarefas como o balanceamento de parênteses e a manipulação de expressões aritméticas.

## 🔍 Conteúdo abordado
### 1. Gramáticas Livres de Contexto (GLC)
* **Definição Formal:** Uma GLC é representada por uma quádrupla `G(V, T, P, S)`:
    * `V`: conjunto de símbolos Não-Terminais.
    * `T`: conjunto de símbolos terminais, que correspondem ao alfabeto da linguagem.
    * `P`: conjunto das regras de produção da gramática.
    * `S`: a variável inicial (raiz da gramática).
* **Conceito:** A principal característica é que a variável em derivação não depende de símbolos que a antecedem ou a sucedem, tornando-a "livre de contexto".

### 2. Árvore de Derivação
* **Representação Gráfica:** É uma forma útil de mostrar as derivações de uma GLC através de uma estrutura hierárquica.
* **Estrutura da Árvore:**
    * A **raiz** é o símbolo inicial da gramática.
    * Os **nós internos** são variáveis (não-terminais).
    * As **folhas** são os símbolos terminais e não-vazios.
* **Funcionalidade:** Proporciona uma melhor visualização da estrutura da sentença e facilita a representação interna em compiladores e interpretadores.

### 3. Gramática Ambígua
* **Definição:** Uma gramática é considerada ambígua se uma mesma palavra pode ser gerada por duas ou mais árvores de derivação diferentes. Isso ocorre devido a diferentes escolhas de derivação, seja à esquerda ou à direita.

### 4. Estratégias de Análise Sintática
* **Análise Top-Down (Descendente):** Constrói a árvore de derivação a partir do símbolo inicial (raiz) e a expande em direção às folhas. Um exemplo é o algoritmo **LL(1)**, que usa uma pilha e um símbolo de *lookahead* para prever a derivação.
* **Análise Bottom-Up (Redutiva):** Constrói a árvore no sentido inverso, a partir das palavras de entrada (folhas) até o símbolo inicial. A cada passo, uma sequência de símbolos é reduzida a um não-terminal.

---

## 💻 Exercício Prático
### Descrição
Considere a gramática abaixo e construa a árvore de derivação completa para a *string* `(id * id) + id`.

**Gramática:**
E → E + T | T <br>
T → T * F | F <br>
F → ( E ) | id <br>

### Resolução
Para derivar a string `(id * id) + id`, seguimos as regras de produção a partir do símbolo inicial `E`.

**Árvore de Derivação:**

```mermaid
graph TD
    E((E)) --> E_plus_T["E + T"]
    E_plus_T --> E_left["E"]
    E_plus_T --> plus["+"]
    E_plus_T --> T_right["T"]

    E_left --> T_left["T"]
    T_left --> F_left["F"]
    F_left --> paren_expr["( E )"]
    paren_expr --> open["("]
    paren_expr --> E_inside["E"]
    paren_expr --> close[")"]

    E_inside --> T_star_F["T * F"]
    T_star_F --> T_inside["T"]
    T_star_F --> star["*"]
    T_star_F --> F_inside["F"]

    T_inside --> F_inside_id["F"]
    F_inside_id --> id_1["id"]

    F_inside --> id_2["id"]

    T_right --> F_right["F"]
    F_right --> id_3["id"]
```

## 📎 Materiais da Aula
-   [**PDF da Aula 6 - Gramáticas Livres de Contexto (GLC) e Análise Sintática**](slides/Aula06_GLC.pdf)
