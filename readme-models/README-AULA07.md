<h1 align="center">📝 Aula 7 — Análise de Gramáticas BNF</h1>

<p align="center">
  <a href="../README.md">Home</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-resumo">Resumo</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-conteúdo-abordado">Conteúdo</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-exercício-prático">Exercício Prático</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-materiais-da-aula">Materiais</a>
</p>

---

## 📜 Resumo
Esta aula se concentra no estudo prático das gramáticas formais, utilizando a **Notação de Backus-Naur (BNF)** para definir e validar sentenças em uma linguagem. O foco é aplicar as regras de produção para construir e verificar a validade de palavras, compreendendo como as gramáticas regem a estrutura da linguagem.

## 🔍 Conteúdo abordado
### 1. Notação de Backus-Naur (BNF)
* **Definição:** A BNF é uma notação para representar as regras de produção de uma gramática livre de contexto.
* **Estrutura:**
    * Variáveis não-terminais são delimitadas por `< >`.
    * A regra de produção `A → a` é substituída por `A ::= a`.
    * O símbolo `|` é usado para separar produções alternativas.

### 2. Gramática para Identificadores
* Uma gramática comum para a definição de identificadores em linguagens de programação especifica que um `id` deve começar com uma letra e pode ser seguido por outras letras, dígitos ou o caractere de sublinhado.

---

## 💻 Exercício Prático
### Descrição

G5 ={{id}, {letter}, {digit}, {a, b, ..., z, A, B, ..., Z, 0, 1, ..., 9, _ }, P, <id>} <br>

Produções: <br>
<id> ::= <letter> | <id><letter> | <id><digit> | <id>_ <br>
<letter> ::= a | b | ... | z | A | B | ... | Z <br>
<digit> ::= 0 | 1 | ... | 9 <br>

Dada a seguinte gramática para a criação de identificadores, complete as tarefas abaixo.

**Gramática:**

**Tarefas:**
1.  Construa as seguintes sentenças: `some_var1`, `X99`, `name_`
2.  Valide se a sentença `123abc` é válida segundo essa gramática.

### Resolução

**1. Construção das Sentenças**
As sentenças são construídas aplicando as regras de produção sequencialmente, começando pelo símbolo inicial `<id>`. Todas as sentenças fornecidas são válidas, pois seguem a regra de começar com uma letra.

* `some_var1`
    -   `<id> ::= <letter> ('s')`
    -   `<id> ::= <id><letter> ('o')`
    -   `<id> ::= <id><letter> ('m')`
    -   `<id> ::= <id><letter> ('e')`
    -   `<id> ::= <id>_`
    -   `<id> ::= <id><letter> ('v')`
    -   `<id> ::= <id><letter> ('a')`
    -   `<id> ::= <id><letter> ('r')`
    -   `<id> ::= <id><digit> ('1')`

* `X99`
    -   `<id> ::= <letter> ('X')`
    -   `<id> ::= <id><digit> ('9')`
    -   `<id> ::= <id><digit> ('9')`

* `name_`
    -   `<id> ::= <letter> ('n')`
    -   `<id> ::= <id><letter> ('a')`
    -   `<id> ::= <id><letter> ('m')`
    -   `<id> ::= <id><letter> ('e')`
    -   `<id> ::= <id>_`

**2. Validação da Sentença `123abc`**
A sentença `123abc` **não é válida**.
* De acordo com a regra de produção `<id> ::= <letter> | <id><letter> | <id><digit> | <id>_`, uma identificação (`<id>`) deve obrigatoriamente começar com uma `<letter>`.
* A sentença `123abc` começa com o dígito `1`.
* Portanto, a sentença viola a regra fundamental de que um identificador deve iniciar com uma letra.

---

## 📎 Materiais da Aula
-   Não há um material de aula específico para esta unidade. O conteúdo acima é baseado em conceitos de Gramáticas e BNF, abordados na disciplina.
