## [Tópico T16b] - Álgebra Relacional - Exercícios
###### *by Prof. Plinio Sa Leitao-Junior (INF/UFG)*

Para apoiar os exercícios e exemplo sobre as operações da Álgebra Relacional, considere a ilustração abaixo do **BD Empresa**.

<img src="../media/fig-mr-2.jpg" width="450">

Escreva em álgebra relacional as seguintes consultas:

1. Qual o nome dos projetos que o funcionário "João B Silva" trabalha em?<br>

JOAO_CPF ← π <sub>Cpf</sub> ( σ <sub>Pnome='Joao' AND Minicial='B' AND Unome='Silva'</sub> (FUNCIONARIO) )<br>
JOAO_PNR ← π <sub>Pnr</sub> ( JOAO_CPF ⨝ <sub>Cpf = Fcpf</sub> TRABALHA_EM )<br>
<< expressão para nome dos projetos ?? >><br>

**JOAO_CPF**
|Cpf|
|-|
|12345678966|

**JOAO_PNR**
|Pnr|
|-|
|1|
|2|

JOAO_CPF ← π <sub>Cpf</sub> ( σ <sub>Pnome='Joao' AND Minicial='B' AND Unome='Silva'</sub> (FUNCIONARIO) )<br>
JOAO_PNR ← π <sub>Pnr</sub> ( JOAO_CPF ⨝ <sub>Cpf = Fcpf</sub> TRABALHA_EM )<br>
RESULT ← π <sub>Projnome</sub> ( JOAO_PNR ⨝ <sub>Pnr = Projnumero</sub> PROJETO )<br>

1. Qual o nome das pessoas que trabalham em pelo menos um dos projetos que o funcionário "João B Silva" trabalha em?<br>

1. Qual o nome das pessoas que não trabalham em qualquer dos projetos que o funcionário "João B Silva" trabalha em? Pessoas que não trabalham em qualquer projeto ESTÃO INCLUÍDAS no resultado da consulta.<br>

ρ CPF_JOAO ( π Cpf (σ <sub>Pnome="João" AND Minicial="B" AND Unome="Silva"</sub> (FUNCIONARIO) ) )<br>
ρ PROJ_JOAO (π Pnr (TRABALHA_EM &#8904; <sub>Fcpf=Cpf</sub> CPF_JOAO) )<br>
ρ GOLD_CPF (Cpf)( (π Fcpf (PROJ_JOAO * TRABALHA_EM) ) - CPF_JOAO )<br>
π <sub>Pnome, Minicial, Unome</sub> ( GOLD_CPF * FUNCIONARIO )

4. Qual o nome das pessoas em que todos os projetos que trabalham em estão entre os projetos que o funcionário "João B Silva" trabalha em? Pessoas que não trabalham em qualquer projeto NÃO ESTÃO INCLUÍDAS no resultado da consulta.<br>

IMPORTANTE: Use a sintaxe da Álgebra Relacional conforme os exemplos apresentados até então.
