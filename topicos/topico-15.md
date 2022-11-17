## [Tópico T15] - Ágebra Relacional (MR) - Vários comandos
###### *by Prof. Plinio Sa Leitao-Junior (INF/UFG)*

Seja abaixo uma [*ilustração para o banco de dados*](../media/fig-mr-2.jpg) **BD Empresa** [1], conforme Modelo Relacional (MR):

<img src="../media/fig-mr-2.jpg" width="400">

### Grupo 1:	fácil

1.	π <ins>Pnome, Unome</ins> (FUNCIONARIO)
1.	σ <ins>Sexo="F"</ins> (FUNCIONARIO)
1.	π <ins>Pnome, Unome</ins> ( σ <ins>Sexo="F"</ins> (FUNCIONARIO) )
1.	TRABALHA_EM  X  PROJETO
1.	FUNCIONARIO * ( ρ (cpf, Projnumero, Horas) (TRABALHA_EM) * PROJETO )
1.	ρ FUNC ( <ins>π Pnome, Unome<ins> ( σ <ins>Sexo="F"</ins> (FUNCIONARIO) ) )
1.	ρ FUNC (PrimeiroNome, UltimoNome) ( π <ins>Pnome, Unome</ins> ( σ <ins>Sexo="F"</ins> (FUNCIONARIO) ) )
