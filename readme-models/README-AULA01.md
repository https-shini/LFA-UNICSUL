<h1 align="center">📝 Aula 1 — Apresentação e Visão Geral</h1>

<p align="center">
  <a href="../README.md">Home</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-resumo">Resumo</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-conteúdo-abordado">Conteúdo</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-exercício">Exercício</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-materiais-da-aula">Materiais</a>
</p>

---

## 📜 Resumo
Esta aula introdutória estabelece o cenário para a disciplina de Linguagens Formais e Autômatos (LFA), apresentando a ementa, os objetivos, a metodologia de ensino e o sistema de avaliação. É um ponto de partida essencial para entender o escopo do curso e a sua estrutura, além de fornecer os recursos de apoio.

## 🔍 Conteúdo abordado
-   **Ementa da Disciplina:** O curso se propõe a estudar os fundamentos de linguagens formais e autômatos, abordando conceitos como alfabetos, palavras, linguagens e gramáticas, culminando na construção de autômatos finitos e Máquinas de Turing.
-   **Objetivos de Aprendizagem:**
    -   **Cognitivos:** Compreender as definições e propriedades dos modelos matemáticos de computação.
    -   **Habilidades:** Ser capaz de especificar linguagens através de autômatos e gramáticas, correlacionando a teoria com a prática da Ciência da Computação.
    -   **Atitudes:** Desenvolver pensamento abstrato, analítico e iniciativa na solução de problemas.
-   **Estratégia de Ensino:** Aulas expositivas com multimídia, exercícios complementares, atividades em grupo e a utilização da plataforma Blackboard como ambiente de apoio.
-   **Sistema de Avaliação:**
    -   Nota A1 (Prova Regimental): 5,0 pontos.
    -   Nota A2 (Outras avaliações): 5,0 pontos, distribuídos entre atividades online e uma avaliação parcial.
    -   A aprovação direta ocorre com `A1 + A2 >= 6,0`. Caso contrário, há a possibilidade de Avaliação Final (AF) para substituir a menor nota e buscar a aprovação.
-   **Bibliografia:** Listagem de bibliografia básica e complementar, incluindo livros e artigos online, que servem de base para o conteúdo do curso.

---

## 💻 Exercício
### Descrição
Dado um alfabeto `Σ = {a, b, c, 0, 1, #}`, construa 5 sentenças (palavras) com 6 símbolos (letras) que sigam as regras abaixo:
1.  Começar com 'a' ou 'b'.
2.  Terminar com '0' ou '1'.
3.  Conter pelo menos um '#' em qualquer posição, exceto no início ou no fim.
4.  Não pode ter 'c' adjacente a '#'.
5.  Ter 6 símbolos no total.

### Resolução
Aqui está a validação das 5 sentenças propostas, com a análise de cada uma:

1.  `a#ac10`
    -   **Começa com 'a'**: ✅ Válido.
    -   **Termina com '0'**: ✅ Válido.
    -   **Contém '#' na 2ª posição**: ✅ Válido.
    -   **Não há 'c' adjacente a '#'**: ✅ Válido.
    -   **6 símbolos**: ✅ Válido.
    -   **Status**: **Válido**.

2.  `a#b0c1`
    -   **Começa com 'a'**: ✅ Válido.
    -   **Termina com '1'**: ✅ Válido.
    -   **Contém '#' na 2ª posição**: ✅ Válido.
    -   **Não há 'c' adjacente a '#'**: ✅ Válido.
    -   **6 símbolos**: ✅ Válido.
    -   **Status**: **Válido**.

3.  `bcb#a0`
    -   **Começa com 'b'**: ✅ Válido.
    -   **Termina com '0'**: ✅ Válido.
    -   **Contém '#' na 4ª posição**: ✅ Válido.
    -   **Não há 'c' adjacente a '#'**: ❌ **Inválido**. O caractere 'c' está adjacente ao '#'.
    -   **6 símbolos**: ✅ Válido.
    -   **Status**: **Inválido**.

4.  `aa#1c1`
    -   **Começa com 'a'**: ✅ Válido.
    -   **Termina com '1'**: ✅ Válido.
    -   **Contém '#' na 3ª posição**: ✅ Válido.
    -   **Não há 'c' adjacente a '#'**: ✅ Válido.
    -   **6 símbolos**: ✅ Válido.
    -   **Status**: **Válido**.

5.  `bb#0c0`
    -   **Começa com 'b'**: ✅ Válido.
    -   **Termina com '0'**: ✅ Válido.
    -   **Contém '#' na 3ª posição**: ✅ Válido.
    -   **Não há 'c' adjacente a '#'**: ✅ Válido.
    -   **6 símbolos**: ✅ Válido.
    -   **Status**: **Válido**.

---

## 📎 Materiais da Aula
-   [**PDF da Aula 1**](slides/Aula01_Apresentacao_LFA.pdf)
