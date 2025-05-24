---
layout: page
title: 1 - Otimização
---

<!--Don't delete this script-->
<script src = "https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id = "MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
<!--Don't delete this script-->

<h1>1.1 - Introdução</h1>

<p align = "justify">
As técnicas de otimização consistem em métodos matemáticos para encontrar soluções ótimas sob restrições específicas, com aplicações em engenharia, ciências exatas e até mesmo ciências sociais.
<br><br>
Para ficar mais claro vamos avaliar um exemplo um problema de otimização em uma fábrica de tratores:
<br><br>
Uma fábrica produz dois modelos de tratores: (a) Trator Agrícola Colheitadeira (<i>x</i>); e (b) Trator Agrícola Pulverizador (<i>y</i>). Os dados de capacidade de produção da fábrica são dados conforme <a href="#tab1" style="color: #2e6da4; font-weight: bold;">Tabela 1</a>. Conforme os dados de capacidade detalhados a unidade produtiva possui uma capacidade máxima de 2.400 horas mensais de operação. O desafio operacional consiste em determinar a proporção ideal de produção entre esses dois modelos que maximize o lucro total,
</p>

<p align="center" id="tab1"><b>Tabela 1.</b> Dados de produção da fábrica.</p>
<table style="width:100%">
    <thead>
        <tr>
            <th>Recurso</th>
            <th>Trator Agrícola Colheitadeira (<i>x</i>)</th>
            <th>Trator Agrícola Pulverizador (<i>y</i>)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Lucro Unitário</td>
            <td>R$ 20.000</td>
            <td>R$ 35.000</td>
        </tr>
        <tr>
            <td>Horas de Montagem</td>
            <td>50 h/unidade</td>
            <td>80 h/unidade</td>
        </tr>
        <tr>
            <td>Demanda máxima</td>
            <td>25 unidades</td>
            <td>15 unidades</td>
        </tr>
    </tbody>
</table>

<h3>Solução:</h3>

<p align = "justify">
A <a href="#eq1" style="color: #2e6da4; font-weight: bold;">equação (1)</a> apresenta o equacionamento do objetivo, <a href="#eq2" style="color: #2e6da4; font-weight: bold;">equação (2)</a> a restrição de produção mensal em horas e <a href="#eq3" style="color: #2e6da4; font-weight: bold;">equação (3)</a> a restrição de produção mensal em unidades:
</p>

<table style="width:100%">
    <tr>
        <td style="width: 90%;">\[ l \left(x,y\right) = 20000 \cdot x + 35000 \cdot y \]</td>
        <td style="width: 10%;"><p align = "right" id = "eq1">(1)</p></td>
    </tr>
    <tr>
        <td style="width: 90%;">\[ g \left(x,y\right) = 50 \cdot x + 80 \cdot y \leq 2400 \]</td>
        <td style="width: 10%;"><p align = "right" id = "eq2">(2)</p></td>
    </tr>
    <tr>
        <td style="width: 90%;">\[ 0 \leq x \leq 25 ,\;\; 0 \leq y \leq 15 \]</td>
        <td style="width: 10%;"><p align = "right" id = "eq3">(3)</p></td>
    </tr>
</table>

<p align="center" id="tab2"><b>Tabela 2.</b> Avaliação de pontos de projeto para o problema de otimização e restrições.</p>
<table style="width:100%">
    <thead>
        <tr>
            <th>Solução</th>
            <th><i>x</i></th>
            <th><i>y</i></th>
            <th><i>l(x,y)</i></th>
            <th><i>g(x,y)</i></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>15</td>
            <td>10</td>
            <td>\[ l(15,10) = 20000 \cdot 15 + 35000 \cdot 10 = 650.000 \]</td>
            <td>\[ g(15,10) = 50 \cdot 15 + 80 \cdot 10 = 1.550 \leq 2.400 \]</td>
        </tr>
        <tr>
            <td>2</td>
            <td>20</td>
            <td>5</td>
            <td>\[ l(20,5) = 20000 \cdot 20 + 35000 \cdot 5 = 575.000 \]</td>
            <td>\[ g(20,5) = 50 \cdot 20 + 80 \cdot 5 = 1.400 \leq 2.400 \]</td>
        </tr>
        <tr>
            <td>3</td>
            <td>12</td>
            <td>15</td>
            <td>\[ l(12,15) = 20000 \cdot 12 + 35000 \cdot 15 = 765.000 \]</td>
            <td>\[ g(12,15) = 50 \cdot 12 + 80 \cdot 15 = 1.800 \leq 2.400 \]</td>
        </tr>
  </tbody>
</table>

<p align="justify">
Considerando as simulações realizadas na <a href="#tab2" style="color: #2e6da4; font-weight: bold;">Tabela 2</a>, a solução que apresentou o melhor desempenho (maximização do lucro!) foi a <strong>Solução 3</strong>, atingindo um lucro total de <strong>R$ 765.000</strong> respeitando a restrição de capacidade produtiva (2.400 horas mensais).
</p>

<h2>Termos da otimização</h2>

<ul>
    <li>
        <p align="justify">
            Função Objetivo: A função objetivo é a expressão matemática que se deseja maximizar ou minimizar no problema de otimização.
        </p>
    </li>
    <li>
        <p align="justify">
            Restrições: Definem os limites físicos, operacionais ou de recursos dentro dos quais a solução deve ser encontrada. Podem ser expressas como igualdades ou desigualdades matemáticas (≤, ≥ ou =) que limitam as combinações possíveis das variáveis de projeto.
        </p>
    </li>    
    <li>
        <p align="justify">
            Espaço de Projeto: Compreende todas as possíveis combinações de valores que as variáveis de projeto podem assumir, tanto as soluções viáveis (que satisfazem todas as restrições) quanto as inviáveis.
        </p>
    </li>
    <li>
        <p align="justify">
            Variáveis de Projeto: São os parâmetros controláveis do sistema que podem ser ajustados para otimizar a função objetivo. Representadas geralmente por <i>x<sub>1</sub></i>, <i>x<sub>2</sub></i>, ..., <i>x<sub>n</sub></i>. Podem ser contínuas (valores reais), discretas (valores inteiros) ou binárias (0 ou 1), dependendo da natureza do problema.
        </p>
    </li>
    <li>
        <p align="justify">
            Solução Ótima: É a combinação específica de valores das variáveis de projeto que fornece o melhor valor possível da função objetivo dentro da região viável. Pode ser única (ótimo global ou local) ou múltipla (quando existem várias combinações com o mesmo valor ótimo).
        </p>
    </li>
</ul>

<h2>Tipos de algoritmo</h2>

<p align="justify">
De forma geral o processo de busca de solução em um problema de otimização caracteriza-se como um método onde a solução é encontrada pelo processo iterativo da <a href="#eq4" style="color: #2e6da4; font-weight: bold;">equação (4)</a>.
</p>

<table style="width:100%">
    <tr>
        <td style="width: 90%;">\[ \mathbf{x}_{k+1} = \mathbf{x}_k + \alpha_k \cdot \mathbf{w}_k \]</td>
        <td style="width: 10%;"><p align = "right" id = "eq4">(4)</p></td>
    </tr>
</table>

<p align="justify">
Onde <i><strong>x<sub>k+1</sub></strong></i> é o vetor de variáveis na iteração <i>k+1</i>; <i><strong>x<sub>k</sub></strong></i> é o vetor de variáveis na iteração <i>k</i>, <i><strong>w<sub>k</sub></strong></i> é a função de atualização da direção de busca no espaço de projeto e <i>α<sub>k</sub></i> é o passo da direção de busca.
<br><br>
A diferença entre a grande maioria dos métodos numéricos de otimização está no parâmetro <i><strong>w<sub>k</sub></strong></i>, onde cada método terá seu processo de busca. Em linhas gerais os processos otimização tem duas fundamentações: (a) Processo determinístico (podendo ser baseados em derivada); e (b) Processo probabilístico.
</p>

<ol>
    <li>
        <strong>Processo determinístico</strong>:
        <ul>
            <li>Método do Gradiente Descendente</li>
            <li>Método de Newton</li>
            <li>Método Quasi-Newton (BFGS)</li>
        </ul>
    </li>
    <li>
        <strong>Processo probabilístico</strong>:
        <ul>
            <li>Algoritmos Genéticos</li>
            <li>Enxame de Partículas (PSO)</li>
            <li>Recozimento Simulado</li>
        </ul>
    </li>
</ol>

<h2>Forma geral do problema de otimização</h2>

<p align="justify">
Um problema geral de otimização assume a forma multiobjetivo (MOO) pois esta envolve várias funções objetivo que devem ser minimizadas ou maximizadas. Além disso, o problema geralmente possui uma série de restrições que igualdade o desigualdade que a solução ótima deverá respeitar, além das restrições laterais. A <a href="#eq5" style="color: #2e6da4; font-weight: bold;">equação (5)</a> apresenta o problema de otimização multiobjetivo em sua forma geral:
</p>

<table style="width:100%">
    <tr>
        <td style="width: 90%;">\[ \begin{cases} 
f_m(\mathbf{x}), & m=1,2,\ldots,M; \\ 
g_j(\mathbf{x}) \leq 0, & j=1,2,\ldots,J; \\ 
h_k(\mathbf{x}) = 0, & k=1,2,\ldots,K; \\ 
x_i^{(L)} \leq x_i \leq x_i^{(U)}, & i=1,2,\ldots,n. 
\end{cases} \]</td>
        <td style="width: 10%;"><p align = "right" id = "eq5">(5)</p></td>
    </tr>
</table>

<p align="justify">  
A formulação do problema envolve \(M\) funções objetivo, representadas por \(f(\mathbf{x}) = (f_1(\mathbf{x}), f_2(\mathbf{x}), ..., f_M(\mathbf{x}))^T\). Onde \(x_i\) representa as variáveis de projeto do problema de otimização \(n\) dimensional. O conjunto de restrições são definidas pelas inequações \(g_j\), equações \(h_k\) e pelas restrições laterais \(x_i^{(L)}\) e \(x_i^{(U)}\). Os limites \(x_i^{(L)}\) e \(x_i^{(U)}\) estabelecem o espaço de projeto \(\mathcal{D}\) . No caso de objetivos de maximização, eles são convertidos para problemas de minimização, para isso as funções de maximização são multiplicadas por menos um. A Figura 2.1 apresenta possíveis soluções de um problema multiobjetivo de duas dimensões considerando a diversidade de abordagens.
</p>

<h1>1.2 - Usando pacotes de otimização</h1>

<p align="justify">
O Python oferece poderosas ferramentas de otimização através do pacote <code>scipy.optimize</code>. A função <code>minimize</code> implementa diversos algoritmos numéricos para encontrar mínimos de funções não-lineares.
</p>

<table style="width:100%; border-collapse: collapse; border-radius: 10px; overflow: hidden;">
    <tr style="background-color: #4b86b4; color: white;">
        <td style="padding: 10px; border: 1px solid #ddd; font-weight: bold;">Importante</td>
    </tr>
    <!-- Linhas com azul claro alternado -->
    <tr style="background-color: #e7f2ff;">
        <td style="padding: 6px; border: 1px solid #ddd;"><p align="justify">Existem duas formas de criação de um problema de otimização, são elas: (a) maximização e (b) minimização. Neste material optou-se pela escrita das funções matemáticas do problema de otimização na forma de minimização. Para problemas de maximização basta multiplicar a função por -1.</p></td>
    </tr>
</table>