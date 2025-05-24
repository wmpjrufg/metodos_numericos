---
layout: page
title: 1 - Otimização
---

<!--Don't delete this script-->
<script src = "https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id = "MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
<!--Don't delete this script-->

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

<h3>Montando a solução:</h3>

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
        <td style="width: 90%;">\[ 0 \leq x \leq 25 \;\; 0 \leq y \leq 15 \]</td>
        <td style="width: 10%;"><p align = "right" id = "eq3">(3)</p></td>
    </tr>
</table>

<p align="center" id="tab2"><b>Tabela 2.</b> Avaliação de pontos de projeto para o problema de otimização e restrições.</p>
<table style="width:100%">
    <thead>
        <tr>
            <th>Solução</th>
            <th><i>x</i></th>
            <th><i>y</i/</th>
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

<p align = "justify">
Considerando as simulações realizadas na <a href="#tab2" style="color: #2e6da4; font-weight: bold;">Tabela 2</a>, a solução que apresentou o melhor desempenho foi a <strong>Solução 2</strong>, atingindo um lucro total de <strong>R$ 575.000</strong> respeitando a restrição de capacidade produtiva (2.400 horas mensais).
</p>