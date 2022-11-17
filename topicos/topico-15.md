## [Tópico T15] - Ágebra Relacional (MR) - Vários comandos
###### *by Prof. Plinio Sa Leitao-Junior (INF/UFG)*

Seja abaixo uma [*ilustração para o banco de dados*](../media/fig-mr-2.jpg) **BD Empresa** [1], conforme Modelo Relacional (MR):

<img src="../media/fig-mr-2.jpg" width="400">

### Grupo 1: Fácil

-	π <sub>Pnome, Unome</sub> (FUNCIONARIO)
-	σ <sub>Sexo="F"</sub> (FUNCIONARIO)
-	π <sub>Pnome, Unome</sub> ( σ <sub>Sexo="F"</sub> (FUNCIONARIO) )
-	TRABALHA_EM  X  PROJETO
- FUNCIONARIO * ( ρ (cpf, Projnumero, Horas) (TRABALHA_EM) * PROJETO )
- ρ FUNC ( π Pnome, Unome ( σ <sub>Sexo="F"</sub> (FUNCIONARIO) ) )
- ρ FUNC (PrimeiroNome, UltimoNome) ( π <sub>Pnome, Unome</sub> ( σ <sub>Sexo="F"</sub> (FUNCIONARIO) ) )

### Grupo 2: Simples

8)	TRABALHA_EM JJ Fcpf=cpf  FUNCIONARIO
9)	π Cpf_supervisor (FUNCIONARIO)  π Cpf_gerente (DEPARTAMENTO)
10) 	π Cpf_supervisor (FUNCIONARIO)  π Cpf_gerente (DEPARTAMENTO)
11) 	π Cpf_supervisor (FUNCIONARIO) –  π Cpf_gerente (DEPARTAMENTO)

### _Under Construction_
