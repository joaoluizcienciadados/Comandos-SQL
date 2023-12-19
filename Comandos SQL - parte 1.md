#### SELECT
**Função**: Recupera dados de uma ou mais tabelas.<br>
**Exemplo**:<br>
```SQL
SELECT nome, idade
FROM usuarios;
```
***
#### INSERT
**Função**: Insere novos dados em uma tabela.<br>
**Exemplo**:<br>
```SQL
INSERT INTO usuarios (nome, idade)
VALUES ('João', 25);
```
***
#### UPDATE
**Função**: Atualiza dados existentes em uma tabela. <br>
**Exemplo**:<br>
```SQL
UPDATE usuarios
SET idade = 26
WHERE nome = 'João';
```
***
#### DELETE
**Função**: Exclui dados de uma tabela.<br>
**Exemplo**:<br>
```SQL
DELETE FROM usuarios
WHERE nome = 'João';
```
***
#### CREATE TABLE
**Função**: Cria uma nova tabela no banco de dados.<br>
**Exemplo**:<br>
```SQL
CREATE TABLE alunos (<br>
  id INT PRIMARY KEY,<br>
  nome VARCHAR(50),<br>
  idade INT<br>
);
```
***
#### ALTER TABLE
**Função**: Modifica uma tabela existente (adiciona, remove ou modifica colunas).<br>
**Exemplo**:<br>
```SQL
ALTER TABLE alunos
ADD COLUMN curso VARCHAR(50);
```
***
#### DROP TABLE
**Função**: Exclui uma tabela do banco de dados.<br>
**Exemplo**:<br>
```SQL
DROP TABLE alunos;
```
***
#### SELECT DISTINCT<br>
**Função**: Retorna valores distintos de uma coluna.<br>
**Exemplo**:<br>
```SQL
SELECT DISTINCT cidade
FROM clientes;
```
***
#### WHERE<br>
**Função**: Filtra os resultados com base em uma condição.<br>
**Exemplo**:<br>
```SQL
SELECT *
FROM produtos
WHERE preco > 50;
```
***
#### ORDER BY<br>
**Função**: Ordena os resultados por uma ou mais colunas.<br>
**Exemplo**:<br>
```SQL
SELECT nome, idade
FROM usuarios
ORDER BY idade DESC;
```
***
#### GROUP BY<br>
**Função**: Agrupa os resultados com base em uma ou mais colunas.<br>
**Exemplo**:<br>
```SQL
SELECT cidade, COUNT(*)
FROM clientes
GROUP BY cidade;
```
***
#### HAVING<br>
**Função**: Filtra os resultados de um GROUP BY com base em uma condição.<br>
**Exemplo**:<br>
```SQL
SELECT cidade, COUNT(*)
FROM clientes
GROUP BY cidade
HAVING COUNT(*) > 1;
```
