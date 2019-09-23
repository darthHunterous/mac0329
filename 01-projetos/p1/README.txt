Integrantes do grupo:
	-Édio Cerati Neto - NUSP 9762678
	-Caio Calisto Gaede Hirakawa - NUSP 7590899
	-Arthur Sakayan Vieira de Melo - NUSP 10297647 


    O circuito da ULA projetado no Logisim foi baseado em 3 outros subcircuitos principais:
-Um subcircuito de comparação da entrada A com 0, devolvendo 1 na flag o1 se o número binário A é estritamente menor que zero, 1 na flag o2 se A é igual a zero e 1 na flag o3 se A é estritamente maior que zero.
-Um subcircuito de aritmética, que apresenta como saída a soma R dos números binários de 8 bits A e B, também indicando na flag o1 se ocorreu overflow ou não.
-Um subcircuito que complementa o binário B em caso de subtração, ativada pelo seletor s0, retornando o inverso de cada um de seus bits. O s0 também consta como entrada para o carry-in inicial no componente aritmético, ou seja, com s0 == 1, temos a notação do complemento de dois do número inserido em B, logo, a subtração A-B é transformada na soma de A+(-B), uma vez que a aritmética entre binários permite diretamente apenas a soma entre binários.
    A unidade aritmética, que soma números com 8 bits, por sua vez, é composta por 8 unidades somadoras de bits par a par, que recebem os valores correspondentes das mesmas posições de A e B (ai e bi) junto com um carry-in e com base nisso, determina a saída da soma junto com o carry-out correspondente.
    Na implementação efetuada, o seletor s1 tornou-se desnecessário, logo mudá-lo não implica em diferenças na execução da soma ou comparação que são efetuadas simultaneamente. O questionamento em aula em relação a essa diferença na implementação foi realizado e aprovado.
