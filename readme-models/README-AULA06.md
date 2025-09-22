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
    subgraph Derivação
        E_0[E]
        E_0 --> E_1[E]
        E_0 --> op1[+]
        E_0 --> T_0[T]
        
        E_1 --> T_1[T]
        
        T_1 --> F_0[F]
        
        F_0 --> p_open[(]
        F_0 --> E_2[E]
        F_0 --> p_close[)]
        
        E_2 --> T_2[T]
        E_2 --> op2[*]
        E_2 --> F_1[F]
        
        T_2 --> F_2[F]
        
        F_2 --> id1[id]
        
        F_1 --> id2[id]
        
        T_0 --> F_3[F]
        F_3 --> id3[id]
        
        style E_0 fill:#A0D2EB, stroke:#3A86FF
        style E_1 fill:#A0D2EB, stroke:#3A86FF
        style E_2 fill:#A0D2EB, stroke:#3A86FF
        style T_0 fill:#A0D2EB, stroke:#3A86FF
        style T_1 fill:#A0D2EB, stroke:#3A86FF
        style T_2 fill:#A0D2EB, stroke:#3A86FF
        style F_0 fill:#A0D2EB, stroke:#3A86FF
        style F_1 fill:#A0D2EB, stroke:#3A86FF
        style F_2 fill:#A0D2EB, stroke:#3A86FF
        style F_3 fill:#A0D2EB, stroke:#3A86FF
        style id1 fill:#EBEB9B, stroke:#F7C852
        style id2 fill:#EBEB9B, stroke:#F7C852
        style id3 fill:#EBEB9B, stroke:#F7C852
        style op1 fill:#EBEB9B, stroke:#F7C852
        style op2 fill:#EBEB9B, stroke:#F7C852
        style p_open fill:#EBEB9B, stroke:#F7C852
        style p_close fill:#EBEB9B, stroke:#F7C852
        
        E_0 -.-> E_1
        E_0 -.-> T_0
        E_1 -.-> T_1
        T_1 -.-> F_0
        F_0 -.-> p_open
        F_0 -.-> E_2
        F_0 -.-> p_close
        E_2 -.-> T_2
        E_2 -.-> F_1
        T_2 -.-> F_2
        F_2 -.-> id1
        F_1 -.-> id2
        T_0 -.-> F_3
        F_3 -.-> id3
    end
```
## 📎 Materiais da Aula
-   [**PDF da Aula 6 - Gramáticas Livres de Contexto (GLC) e Análise Sintática**](slides/Aula06_GLC.pdf)
