### AS
**Função**: usado para atribuir um alias (apelido) a uma tabela ou a uma coluna em uma consulta.  
**Exemplo**:
```sql
SELECT { coluna }
FROM { tabela } AS { apelido }
WHERE { apelido }.{ coluna } = { valor };
```
___
### LIMIT
**Função**: usado no SQL para limitar o número de registros retornados por uma consulta.  
**Exemplo**:
```sql
SELECT { coluna }
FROM { tabela }
LIMIT { quantidade } OFFSET { quantidade };
```
___

### DISTINCT
**Função**: usado para omitir dados duplicados de uma tabela.
**Exemplo**:
```sql
SELECT DISTINCT { coluna }
FROM { tabela }
```
___
### WHERE
**Função**: usado para extrair apenas alguns dados de acordo com sua condição.  
**Exemplo**:
```sql
SELECT { coluna } FROM { tabela } WHERE { condição }
SELECT { coluna }
FROM { tabela }
WHERE LastName = 'miller' AND firstName = 'anna'
```
OBS: Operadores para as condições:
```
= ---------> IGUAL
> ---------> MAIOR QUE
< ---------> MENOR QUE
>= --------> MAIOR QUE OU IGUAL
<= --------> MENOR QUE OU IGUAL
<> --------> DIFERENTE DE
AND -------> OPERADOR 'E'
OR --------> OPERADOR 'OU'
```
___
### COUNT
**Função**: usado para retornar a quantidade de linhas de acordo com a sua condição.  
**Exemplo**:
```sql
SELECT COUNT(*)
FROM { tabela }
```
___
### TOP
**Função**: usado para filtrar (limitar) o que é retornado de um SELECT.  
**Exemplo**:
```sql
SELECT TOP 10 *
FROM { tabela }
```
___
### BETWEEN
**Função**: usado para encontrar valor, entre um valor mínimo e um valor máximo.  
**Exemplo**:
```sql
SELECT { coluna }
FROM { tabela }
WHERE { coluna } BETWEEN 100 AND 200;
```
Para fazer o contrário, basta utilizar o NOT.
```sql
SELECT { coluna }
FROM { tabela }
WHERE { coluna } NOT BETWEEN 100 AND 200;
```
___
### IN
**Função**: é usado em conjunto com o WHERE, para verificar se um valor corresponde com qualquer valor passado na lista de valores.  

Caso queira o contrário da sua condição, utilize o NOT.  
**Exemplo**:
```sql
SELECT { coluna }
FROM { tabela }
WHERE { coluna } IN(valor1, valor2, valor3);
```
___
### LIKE
**Função**: usado para encontrar um dado específico com fragmentos do nome.  
**Exemplo**:
```sql
SELECT { coluna }
FROM { tabela }
WHERE { coluna } LIKE '___';
```
___

### CREATE TABLE
**Função**:usado para criar uma tabela para o banco de dados e utilizar algumas restrições.    

Principais tipos de restrições que podem ser aplicadas:  

NOT NULL - Não permite nulos  
UNIQUE - Força que todos os valores em uma coluna sejam diferentes  
PRIMARY KEY - Uma junção de NOT NULL e UNIQUE  
FOREIGN KEY - Identifica únicamente uma linha em outra tabela.  
CHECK - Força uma condição específica em uma coluna  
DEFAULT - Força um valor padrão quando nenhum valor é passado  

**Exemplo**:
```sql
CREATE TABLE { nome da tabela } (
{ nome da coluna } INT PRIMARY KEY,
{ nome da coluna } VARCHAR() NOT NULL,
{ nome da coluna } INT DEFAULT { valor }, 
{ nome da coluna } INT FOREIGN KEY REFERENCES { coluna de outra tabela }
```
___
### INSERT INTO
**Função**: O comando INSERT INTO é utilizado para inserir dados em uma tabela.  

Inserindo dados de uma tabela em uma tabela existente:

```sql
INSERT INTO { nova tabela }(nova coluna)
SELECT { coluna existente }
FROM { tabela }
```
Inserindo dados:
```sql
INSERT INTO { nome da tabela }(coluna1, coluna2)
VALUES(valor1, valor2)
```
Copiar dados de uma tabela e inserir numa tabela existente:
```sql
SELECT * INTO { NOVA TABELA }
FROM { TABELA }
```
___

