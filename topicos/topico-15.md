## [Tópico T15] - Ágebra Relacional (MR) - Vários comandos
###### *by Prof. Plinio Sa Leitao-Junior (INF/UFG)*

Seja abaixo uma [*ilustração para o banco de dados*](../media/fig-mr-2.jpg) **BD Empresa** [1], conforme Modelo Relacional (MR):

<img src="../media/fig-mr-2.jpg" width="400">

### Grupo 1: Fácil

-	π <sub>Pnome, Unome</sub> (FUNCIONARIO)
-	σ <sub>Sexo="F"</sub> (FUNCIONARIO)
-	π <sub>Pnome, Unome</sub> ( σ <sub>Sexo="F"</sub> (FUNCIONARIO) )
-	TRABALHA_EM  X  PROJETO
- ρ FUNC ( π Pnome, Unome ( σ <sub>Sexo="F"</sub> (FUNCIONARIO) ) )
- ρ FUNC (PrimeiroNome, UltimoNome) ( π <sub>Pnome, Unome</sub> ( σ <sub>Sexo="F"</sub> (FUNCIONARIO) ) )

### Grupo 2: Simples

- TRABALHA_EM &#8904; <sub>Fcpf=cpf</sub>  FUNCIONARIO
- FUNCIONARIO * ( ρ (cpf, Projnumero, Horas) (TRABALHA_EM) * PROJETO )
- π <sub>Cpf_supervisor</sub> (FUNCIONARIO) ∪ π <sub>Cpf_gerente</sub> (DEPARTAMENTO)
- π <sub>Cpf_supervisor</sub> (FUNCIONARIO) ∩ π <sub>Cpf_gerente</sub> (DEPARTAMENTO)
- π <sub>Cpf_supervisor</sub> (FUNCIONARIO) – π <sub>Cpf_gerente</sub> (DEPARTAMENTO)
- ...

### _Under Construction_
