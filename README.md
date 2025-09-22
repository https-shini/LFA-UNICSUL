<h1 align="center">🧠 Linguagens Formais e Autômatos (LFA)</h1>

<p align="center">
  <a href="#-sobre-a-disciplina">Sobre</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-conteúdo-programático">Conteúdo</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-aulas-e-recursos">Aulas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-licença">Licença</a>
</p>

---

## 📖 Sobre a disciplina
A disciplina de **Linguagens Formais e Autômatos** explora os modelos matemáticos e as teorias que formam a base da ciência da computação. O curso aprofunda a compreensão de como as linguagens, tanto naturais quanto de programação, podem ser definidas, estruturadas e processadas por máquinas, com aplicações diretas em áreas como o desenvolvimento de compiladores e a inteligência artificial.

### 🎯 Objetivos de aprendizagem
- **Cognitivos:** Compreender as definições e propriedades de modelos computacionais como linguagens, autômatos e gramáticas.
- **Habilidades:** Ser capaz de especificar linguagens usando autômatos e gramáticas, além de correlacionar a teoria com aplicações práticas na computação.
- **Atitudes:** Desenvolver um pensamento abstrato, analítico e criativo para a solução de problemas complexos.

**Professor:** Prof. Jose Claudio Sousa <br>
**Curso:** Ciência da Computação – Universidade Cruzeiro do Sul

---

## 📚 Conteúdo programático
O conteúdo da disciplina é organizado de forma a construir o conhecimento de maneira progressiva, partindo dos conceitos básicos até a Hierarquia de Chomsky e a análise sintática.

1.  **Unidades 1-2:** Fundamentos de Linguagens Formais, Palavras, Grafos e Expressões Regulares.
2.  **Unidades 3-4:** Autômatos Finitos (AFD e AFN) e a Hierarquia de Chomsky.
3.  **Unidades 5-6:** Gramáticas Livres de Contexto (GLC) e Algoritmos de Análise Sintática.
4.  **Unidades 7+:** Linguagens Recursivamente Enumeráveis, Máquinas de Turing e Avaliações.

---

## 📝 Aulas e Recursos
As aulas a seguir formam a espinha dorsal do curso, cobrindo os tópicos essenciais da disciplina.

### 📝 **Aula 1: Apresentação e Visão Geral**
Apresentação da disciplina, incluindo ementa, objetivos, metodologia de ensino, sistema de avaliação e bibliografia. Este material define o escopo do curso e as expectativas de aprendizado.

👉 [Acessar o conteúdo completo da Aula 1.](readme-models/README-AULA01.md)

### 📝 **Aula 2: Conceitos Iniciais e Grafos**
Introdução aos elementos fundamentais da teoria de linguagens formais, como **símbolos**, **alfabetos**, **palavras** e **linguagens**. A aula também detalha operações como **prefixo**, **sufixo**, **subpalavra**, **concatenação** e **potência**. A seção final introduz a **teoria de grafos**, que será utilizada como base para a representação de autômatos.

👉 [Acessar o conteúdo completo da Aula 2.](readme-models/README-AULA02.md)

### 📝 **Aula 3: Expressões Regulares e Autômatos Finitos Determinísticos (AFD)**
Foco nos mecanismos de descrição e reconhecimento de linguagens. A aula define **Expressões Regulares (ER)** como um formalismo para descrever linguagens regulares. Em seguida, introduz **Autômatos Finitos (AF)** como modelos matemáticos para reconhecer essas linguagens. O **Autômato Finito Determinístico (AFD)** é formalizado como uma 5-tupla `M = (Σ, Q, δ, q0, F)`, com seus componentes e regras de computação.

👉 [Acessar o conteúdo completo da Aula 3.](readme-models/README-AULA03.md)

### 📝 **Aula 4: Hierarquia de Chomsky e Gramáticas Regulares**
Esta aula apresenta a **Hierarquia de Chomsky**, uma classificação fundamental das gramáticas formais. Aprofunda-se no **Tipo 3: Gramáticas Regulares**, explicando o formato de suas produções e a relação com as Linguagens Regulares e Autômatos Finitos. Os outros tipos da hierarquia (Tipo 2, 1 e 0) são brevemente apresentados para contextualização.

👉 [Acessar o conteúdo completo da Aula 4.](readme-models/README-AULA04.md)

### 📝 **Aula 5: Conversão de Expressões Regulares (ER) para AFN/AFD**
Explora a relação prática entre Expressões Regulares e Autômatos Finitos. A aula detalha dois algoritmos cruciais: a **Construção de Thompson**, que traduz uma ER para um Autômato Finito Não Determinístico (AFN) com ε-transições, e o **Método da Construção de Subconjuntos**, que converte um AFN para um AFD equivalente.

👉 [Acessar o conteúdo completo da Aula 5.](readme-models/README-AULA05.md)

### 📝 **Aula 6: Gramáticas Livres de Contexto (GLC) e Análise Sintática**
Foco no **Tipo 2: Gramáticas Livres de Contexto (GLC)**, essenciais para a definição de linguagens de programação. O material introduz conceitos como **Árvore de Derivação**, **Árvore Sintática Abstrata (AST)** e **Gramáticas Ambíguas**. Por fim, são explicadas as estratégias de análise sintática **Top-Down** e **Bottom-Up**, com um exemplo detalhado do algoritmo **LL(1)**.

👉 [Acessar o conteúdo completo da Aula 6.](readme-models/README-AULA06.md)

### 📝 **Aula 7: Análise de Gramáticas BNF**
Uma aula prática dedicada ao estudo da **Notação de Backus-Naur (BNF)**, uma forma de representar gramáticas formais. O foco está na aplicação das regras de produção para construir e validar sentenças de uma linguagem, como identificadores em linguagens de programação, garantindo que elas sigam a estrutura gramatical definida.

👉 [Acessar o conteúdo completo da Aula 7.](readme-models/README-AULA07.md)

---

## 📄 Licença
Todo o material deste repositório está sob a **Licença MIT**. Consulte o arquivo `LICENSE` para mais detalhes sobre permissões e restrições.

---

> *Este repositório é um guia para o estudo de Linguagens Formais e Autômatos, servindo como recurso de consulta e apoio ao aprendizado contínuo.*
