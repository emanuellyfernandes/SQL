<h1 align="center">SQL :books:</h1>

<h3>É uma linguagem padrão para se trabalhar com bancos de dados.</h3>

https://www.youtube.com/watch?v=rbH0B3mFsLI


* (*) = serve para selecionar todas as colunas e linhas da tabela
* WHERE = cria filtros nas tabelas
* AS = da nome nas colunas
* LIMIT = limitar  o numero de linhas de uma tabel
* ORDER BY = ordenar do menor para o maior
* ORDER BY DESC = do maior ao menor
<br>

* COUNT = retorna a quantidade total de valores de uma coluna
* COUNT(*) = retorna a quantidade total de linhas de uma tabela.. nao ignora valores nulos
* COUNT (DISTINCT) = retorna a quantidade distinta de valores de uma tabela (quantos tipos diferentes eu tenho)
<br>

* SUM = retorna a soma total de valores de uma coluna
* AVG =  retorna a média de valores de uma coluna
* MIN = retorna o valor mínimo de uma coluna
* MAX = retorna o valor maximo de uma coluna
<br>

* GROUP BY = criar agrupamentos ou resumos das tabelas principais
<br>

* TABELA DIMENSÃO = Contém caracterpisticas de um determinado elemento: lojas, produtos, funcionários, clientes,etc
   nenhum dos elementos principais irá se repetir

* TABELA FATO = vai registrar os fatos ou acontecimentos de uma empresa/negócio de um determinado periodo de tempo (vendas, devoluções,trocas,chamados,despesas,receitas,etc)
<br>

* INNER JOIN = permite relacionar tabela A com a tabela B e criar uma nova tabela C que é a junção das duas

<br>


<details>
   <summary><strong>EXEMPLOS</strong></summary>
   <br>


        SELECT Nome, Sobrenome, Estado
        FROM Clientes
        WHERE Estado = 'São Paulo';

<br>

        CREATE TABLE Funcionários{ /* criar tabela + nome da tabela */
        ID INT
        Nome VARCHAR{100}
        }
<br>

        SELECT * FROM actor;       -> actor nome da tabela
   <br>



        ou SELECT * FROM sacquila.actor     -> sacquila nome do banco de dados
   
   <br>



        SELECT Col1, Col2
        FROM (nome da tabela);             -> selecionar colunas específicas
<br>


        SELECT 
           Col1 AS "Coluna 1"
           Col2 AS "Coluna 2"
        FROM (nome da tabela);
<br>


        SELECT
            Nome 
            Setor
        FROM (nome da tabela) 
        WHERE setor = 'energia';
        LIMIT 2;   --> limitar o numero de linhas de uma tabela

<br>
        SELECT Nome FROM Resultados;    -> selecionar a coluna de nome que está na tabela resultado
<br>
        ORDER BY Col3;   ----> permite ordenar uma tabela a partir de uma coluna de forma ascendente
<br>
        ORDER BY Col3 DESC; ----> ordena do maior ao menor.
<br>
        SELECT 
            COUNT (DISTINCT Escolaridade)
            FROM clientes;   ----> contar a quantidade de clientes
<br>
        SELECT 
           COUNT (Nome)
           FROM clientes;   ----> contar a quantidade de clientes
<br>

       SELECT 
           sexo
           COUNT(*) AS 'quantidade de clientes'
       FROM clientes
       GROUP BY sexo;

<br>
       SELECT
          tabela_A.Coluna1,
          tabela_B.Coluna2,
          tabela_B.Coluna3
       FROM
          tabela_A
       INNER JOIN tabela_B
          ON tabela_A.id_chave_estrangeira = Tabela_B.id_chave_primaria
   
  </details>
