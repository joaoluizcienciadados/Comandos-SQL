### JOIN  

**Função**: O comando JOIN é usado para combinar dados de duas ou mais tabelas. Existem vários tipos de JOINs, cada um com seu próprio propósito.  
**Exemplo**:

```SQL  
SELECT  
    clientes.nome,  
    produtos.nome,  
    produtos.preco  
FROM  
    clientes  
    JOIN produtos  
        ON clientes.id = produtos.cliente_id;   
```
**Explicação**: Este comando irá retornar os nomes dos clientes, os nomes dos produtos e os preços dos produtos que foram comprados 
por esses clientes.  
___
### CASE


**Função**: O comando CASE é usado para realizar testes e ações condicionais. Ele pode ser usado para retornar diferentes valores dependendo 
do resultado de um teste.
**Exemplo**:
```SQL
SELECT
    nome,
    CASE
        WHEN idade > 18 THEN 'Adulto'
        WHEN idade > 12 THEN 'Adolescente'
        ELSE 'Criança'
    END AS idade_categoria
FROM
    clientes;
```
**Explicação**: Este comando irá retornar a categoria de idade de cada cliente.
___
### SUBQUERY

O comando SUBQUERY é usado para executar uma consulta dentro de outra consulta. 
Ele pode ser usado para obter dados de uma tabela ou conjunto de tabelas que não são diretamente acessíveis pela consulta principal.

Exemplo:

```SQL
SELECT
    nome,
    cidade
FROM
    clientes
WHERE
    cidade IN (
        SELECT
            cidade
        FROM
            cidades
        WHERE
            populacao > 1000000
    );
```
**Explicação**: Este comando irá retornar os nomes e as cidades dos clientes que moram em cidades com população superior a 1 milhão de habitantes.  
___
### UNION  

**Função**: O comando UNION é usado para combinar os resultados de duas ou mais consultas. Ele pode ser usado para combinar dados de tabelas 
diferentes ou para combinar resultados de consultas que retornam dados semelhantes.  

**Exemplo**:  

```SQL  
SELECT  
    nome,  
    idade  
FROM  
    clientes  
UNION  
SELECT  
    nome,  
    idade  
FROM  
    funcionários;  
```
**Explicação**: Este comando irá retornar os nomes e as idades de todos os clientes e funcionários.  
___
### INTERSECT

**Função**: O comando INTERSECT é usado para retornar apenas as linhas que estão presentes em ambas as consultas.  
**Exemplo**:  

```SQL  
SELECT  
    nome,  
    idade  
FROM  
    clientes  
INTERSECT  
SELECT  
    nome,  
    idade  
FROM  
    funcionários;
```  
**Explicação**: Este comando irá retornar os nomes e as idades dos clientes que também são funcionários.  
___
### EXCEPT  

**Função**:O comando EXCEPT é usado para retornar apenas as linhas que estão presentes na primeira consulta, mas não na segunda.  
**Exemplo**:  

```sql
SELECT  
    nome,  
    idade  
FROM  
    clientes  
EXCEPT  
SELECT  
    nome,  
    idade  
FROM  
    funcionários;
```

**Explicação**: Este comando irá retornar os nomes e as idades dos clientes que não são funcionários.

