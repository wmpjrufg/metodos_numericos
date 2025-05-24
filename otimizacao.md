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
<table>
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
            <td>-</td>
        </tr>
        <tr>
            <td>Horas de Montagem</td>
            <td>50 h/unidade</td>
            <td>80 h/unidade</td>
        </tr>
    </tbody>
</table>

<h3>Montando a solução:</h3>

<p align = "justify">
A <a href="#eq1" style="color: #2e6da4; font-weight: bold;">equação (1)</a> apresenta o equacionamento do objetivo e <a href="#eq2" style="color: #2e6da4; font-weight: bold;">equação (2)</a> a restrição de produção:
</p>

<table style="width:100%">
    <tr>
        <td style="width: 90%;">\[ l \left(x,y\right) = 20000 \cdot x + 35000 \cdot y\]</td>
        <td style="width: 10%;"><p align = "right" id = "eq1">(1)</p></td>
    </tr>
    <tr>
        <td style="width: 90%;">\[ g \left(x,y\right) = 50 \cdot x + 80 \cdot y \leq 2400\]</td>
        <td style="width: 10%;"><p align = "right" id = "eq2">(2)</p></td>
    </tr>
</table>