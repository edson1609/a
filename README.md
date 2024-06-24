# ## Curso Completo de SQL Server

### Módulo 1: Introdução ao SQL Server
**Objetivo:** Familiarizar-se com o SQL Server, sua interface e comandos básicos.

#### Aula 1: Instalação e Configuração
- **Tópicos:**
  - Download e instalação do SQL Server.
  - Configuração inicial.
  - Conexão com o SQL Server Management Studio (SSMS).
- **Exercício:**
  - Instale o SQL Server e configure uma conexão no SSMS.

#### Aula 2: Conceitos Básicos
- **Tópicos:**
  - Bancos de dados e tabelas.
  - Tipos de dados.
  - Comandos SQL básicos (SELECT, INSERT, UPDATE, DELETE).
- **Exercício:**
  - Crie um banco de dados e uma tabela simples.
  - Insira, atualize e exclua registros na tabela.

### Módulo 2: Manipulação de Dados
**Objetivo:** Aprender a manipular dados em tabelas SQL.

#### Aula 3: Consultas Básicas
- **Tópicos:**
  - SELECT e WHERE.
  - Operadores lógicos.
- **Exercício:**
  - Crie consultas simples usando SELECT e WHERE.

#### Aula 4: Funções de Agregação
- **Tópicos:**
  - Funções COUNT, SUM, AVG, MAX, MIN.
  - Agrupamento de dados com GROUP BY.
- **Exercício:**
  - Crie consultas usando funções de agregação e agrupamento.

#### Aula 5: Junções (Joins)
- **Tópicos:**
  - INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL JOIN.
- **Exercício:**
  - Crie consultas utilizando diferentes tipos de JOIN.

### Módulo 3: Administração de Banco de Dados
**Objetivo:** Entender a administração e manutenção de bancos de dados.

#### Aula 6: Criação e Alteração de Tabelas
- **Tópicos:**
  - CREATE TABLE e ALTER TABLE.
  - Tipos de constraints (PRIMARY KEY, FOREIGN KEY, UNIQUE, CHECK, DEFAULT).
- **Exercício:**
  - Crie e altere tabelas usando diferentes tipos de constraints.

#### Aula 7: Índices e Views
- **Tópicos:**
  - Criação e utilização de índices.
  - Criação e utilização de views.
- **Exercício:**
  - Crie índices e views em suas tabelas.

#### Aula 8: Procedimentos Armazenados e Triggers
- **Tópicos:**
  - Criação e execução de procedimentos armazenados.
  - Criação e uso de triggers.
- **Exercício:**
  - Crie procedimentos armazenados e triggers simples.

### Módulo 4: Otimização e Segurança
**Objetivo:** Aprender técnicas de otimização de consultas e práticas de segurança.

#### Aula 9: Otimização de Consultas
- **Tópicos:**
  - Análise de planos de execução.
  - Técnicas de otimização.
- **Exercício:**
  - Analise e otimize consultas complexas.

#### Aula 10: Segurança de Dados
- **Tópicos:**
  - Gerenciamento de usuários e permissões.
  - Backup e restauração de bancos de dados.
- **Exercício:**
  - Configure usuários com diferentes permissões.
  - Realize backups e restaurações.

### Módulo 5: Projetos Práticos
**Objetivo:** Aplicar o conhecimento adquirido em projetos práticos.

#### Projeto 1: Sistema de Gerenciamento de Vendas
- **Descrição:**
  - **Objetivo:** Criar um sistema para gerenciar vendas de uma loja.
  - **Funcionalidades:**
    - Cadastro de clientes e produtos.
    - Registro de vendas com detalhes de itens comprados.
    - Relatórios de vendas por período e por cliente.
  - **Requisitos Técnicos:**
    - Utilização de pelo menos três tabelas relacionais.
    - Implementação de pelo menos um procedimento armazenado para gerar relatórios.
    - Utilização de índices para otimizar consultas de busca de produtos.
  
#### Projeto 2: Sistema de Biblioteca
- **Descrição:**
  - **Objetivo:** Desenvolver um sistema para gerenciar um acervo de uma biblioteca.
  - **Funcionalidades:**
    - Cadastro de livros, autores e usuários.
    - Controle de empréstimos e devoluções.
    - Geração de relatórios de livros mais emprestados e usuários com mais empréstimos.
  - **Requisitos Técnicos:**
    - Utilização de pelo menos quatro tabelas relacionais.
    - Criação de views para facilitar a visualização de informações dos livros emprestados.
    - Implementação de triggers para atualização automática de contadores.

#### Projeto 3: Sistema de Reservas de Hotel
- **Descrição:**
  - **Objetivo:** Construir um sistema para gestão de reservas de quartos de hotel.
  - **Funcionalidades:**
    - Cadastro de clientes e quartos disponíveis.
    - Reservas de quartos com cálculo de preço e controle de disponibilidade.
    - Relatórios de ocupação por período e histórico de reservas.
  - **Requisitos Técnicos:**
    - Utilização de pelo menos duas tabelas principais (Clientes e Reservas).
    - Utilização de procedimentos armazenados para calcular preços de reservas.
    - Implementação de índices para otimizar consultas de disponibilidade de quartos.

### Tabela Principal: "Vendas"

#### Estrutura da Tabela "Vendas"
```sql
CREATE TABLE Vendas (
    VendaID INT PRIMARY KEY IDENTITY,
    ClienteID INT,
    ProdutoID INT,
    Quantidade INT,
    PrecoUnitario DECIMAL(10, 2),
    DataVenda DATE,
    CONSTRAINT FK_Cliente FOREIGN KEY (ClienteID) REFERENCES Clientes(ClienteID),
    CONSTRAINT FK_Produto FOREIGN KEY (ProdutoID) REFERENCES Produtos(ProdutoID)
);
```

### Exercícios Práticos

#### Exercícios Fáceis (50)

1. Corrija a seguinte consulta:
    ```sql
    SELECT * FROM Vendas WHERE ClienteID = 5
    ```
2. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda) VALUES (1, 2, 3, 15.00, '2023-01-01)
    ```
3. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 4 WHERE VendaID = 10
    ```
4. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ProdutoID = 3
    ```
5. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, SUM(PrecoUnitario * Quantidade) FROM Vendas GROUP BY ClienteID
    ```
6. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (1, 2, 3, 15.00, '2023-01-01');
    ```
7. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET PrecoUnitario = 20.00 WHERE VendaID = 5
    ```
8. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE VendaID  = 6
    ```
9. Corrija a seguinte consulta:
    ```sql
    SELECT * FROM Vendas WHERE DataVenda > '2023-01-01
    ```
10. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda) VALUE (1, 2, 3, 15.00, '2023-01-01')
    ```
11. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, SUM(Quantidade) FROM Vendas GROUP BY ClienteID
    ```
12. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 5 WHERE VendaID = 4
    ```
13. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID = 2
    ```
14. Corrija a seguinte consulta:
    ```sql
    SELECT * FROM Vendas WHERE PrecoUnitario >= 10.00
    ```
15. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (2, 3, 2, 20.00, '2023-02-01');
    ```
16. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET DataVenda = '2023-03-01' WHERE VendaID = 8
    ```
17. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ProdutoID = 1
    ```
18. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, SUM(PrecoUnitario) FROM Vendas GROUP BY ClienteID
    ```
19. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda) VALUE (3, 4, 1, 25.00, '2023-04-01')
    ```
20. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET PrecoUnitario = 30.00 WHERE VendaID = 2
    ```
21. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE VendaID = 9
    ```
22. Corrija a seguinte consulta:
    ```sql
    SELECT * FROM Vendas WHERE DataVenda < '2023-05-01'
    ```
23. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (4, 5, 3, 35.00, '2023-06-01');
    ```
24. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 2 WHERE VendaID = 3
    ```
25. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID = 1
    ```
26. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, SUM(PrecoUnitario * Quantidade) FROM Vendas GROUP BY ClienteID
    ```
27. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (5, 6, 4, 40.00, '2023-07-01');
    ```
28. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET DataVenda = '2023-08-01' WHERE VendaID = 7
    ```
29. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ProdutoID = 2
    ```
30. Corrija a seguinte consulta:
    ```sql
    SELECT * FROM Vendas WHERE PrecoUnitario > 50.00
    ```
31. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda) VALUE (6, 7, 1, 45.00, '2023-09-01')
    ```
32. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 3 WHERE VendaID = 5
    ```
33. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE VendaID = 1
    ```
34. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, COUNT(*) FROM Vendas GROUP BY ClienteID
    ```
35. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda) VALUES (7, 8, 2, 50.00, '2023-10-01');
    ```
36. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET PrecoUnitario = 55.00 WHERE VendaID = 6
    ```
37. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID = 3
    ```
38. Corrija a seguinte consulta:
    ```sql
    SELECT * FROM Vendas WHERE DataVenda >= '2023-11-01'
    ```
39. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (8, 9, 3, 60.00, '2023-12-01');
    ```
40. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 4 WHERE VendaID = 2
    ```
41. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ProdutoID = 3
    ```
42. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, AVG(PrecoUnitario) FROM Vendas GROUP BY ClienteID
    ```
43. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (9, 10, 1, 65.00, '2024-01-01');
    ```
44. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET PrecoUnitario = 70.00 WHERE VendaID = 4
    ```
45. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID = 4
    ```
46. Corrija a seguinte consulta:
    ```sql
    SELECT * FROM Vendas WHERE PrecoUnitario < 100.00
    ```
47. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (10, 11, 2, 75.00, '2024-02-01');
    ```
48. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 1 WHERE VendaID = 3
    ```
49. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ProdutoID = 4
    ```
50. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, MAX(DataVenda) FROM Vendas GROUP BY ClienteID
    ```

#### Exercícios Médios (50)

1. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, SUM(Quantidade) FROM Vendas GROUP BY ProdutoID
    ```
2. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (1, 2, 3, 15.00, '2023-01-01'
    ```
3. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 5, WHERE VendaID = 1
    ```
4. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE DataVenda BETWEEN '2023-01-01' AND '2023-12-31'
    ```
5. Corrija a seguinte consulta:
    ```sql
    SELECT * FROM Vendas WHERE PrecoUnitario = 20
    ```
6. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (1, 2, 3, 15.00, '2023-01-01');
    ```
7. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 6 WHERE VendaID  = 3
    ```
8. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID = (SELECT ClienteID FROM Clientes WHERE Nome = 'João')
    ```
9. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, COUNT(*), AVG(PrecoUnitario) FROM Vendas GROUP BY ClienteID
    ```
10. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda) VALUES (1, 2, 3, 15.00, '2023-01-01';
    ```
11. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, SUM(PrecoUnitario * Quantidade) FROM Vendas GROUP BY ClienteID
    ```
12. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 7 WHERE VendaID = 4
    ```
13. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID IS NOT NULL
    ```
14. Corrija a seguinte consulta:
    ```sql
    SELECT * FROM Vendas WHERE DataVenda = '2023-01-01'
    ```
15. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (2, 3, 2, 20.00, '2023-02-01');
    ```
16. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 2 WHERE VendaID  = 5
    ```
17. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID = (SELECT ClienteID FROM Clientes WHERE Nome = 'Maria')
    ```
18. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, AVG(PrecoUnitario) FROM Vendas GROUP BY ProdutoID
    ```
19. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (3, 4, 1, 25.00, '2023-04-01');
    ```
20. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 8 WHERE VendaID = 6
    ```
21. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE DataVenda IN ('2023-01-01', '2023-02-01')
    ```
22. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, SUM(Quantidade * PrecoUnitario) FROM Vendas
    ```
23. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (4, 5, 3, 35.00, '2023-06-01');
    ```
24. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET DataVenda = '2023-07-01' WHERE VendaID = 8
    ```
25. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID IN (1, 2, 3)
    ```
26. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, MAX(Quantidade) FROM Vendas GROUP BY ProdutoID
    ```
27. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (5, 6, 4, 40.00, '2023-08-01');
    ```
28. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 3 WHERE VendaID  = 9
    ```
29. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE DataVenda = '2023-09-01'
    ```
30. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, COUNT(*), SUM(Quantidade) FROM Vendas GROUP BY ProdutoID
    ```
31. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda) VALUES (6, 7, 1, 45.00, '2023-10-01';
    ```
32. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET PrecoUnitario = 50.00 WHERE VendaID = 2
    ```
33. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID = (SELECT ClienteID FROM Clientes WHERE Nome = 'Carlos')
    ```
34. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, COUNT(*) FROM Vendas GROUP BY ClienteID
    ```
35. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (7, 8, 2, 50.00, '2023-11-01');
    ```
36. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 4 WHERE VendaID  = 10
    ```
37. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE DataVenda = '2023-12-01'
    ```
38. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, SUM(Quantidade) FROM Vendas
    ```
39. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (8, 9, 3, 60.00, '2024-01-01');
    ```
40. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET PrecoUnitario = 65.00 WHERE VendaID = 3
    ```
41. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID = (SELECT ClienteID FROM Clientes WHERE Nome = 'Ana')
    ```
42. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, AVG(Quantidade) FROM Vendas GROUP BY ProdutoID
    ```
43. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (9, 10, 1, 65.00, '2024-02-01');
    ```
44. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 1 WHERE VendaID = 4
    ```
45. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE DataVenda IS NULL
    ```
46. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, SUM(PrecoUnitario * Quantidade) FROM Vendas
    ```
47. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (10, 11, 2, 75.00, '2024-03-01');
    ```
48. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET PrecoUnitario = 70.00 WHERE VendaID = 5
    ```
49. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID IN (SELECT ClienteID FROM Clientes WHERE Nome LIKE 'J%')
    ```
50. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, MAX(DataVenda) FROM Vendas GROUP BY ClienteID
    ```

#### Exercícios Difíceis (50)

1. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, SUM(Quantidade), AVG(PrecoUnitario) FROM Vendas GROUP BY ProdutoID
    ```
2. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (1, 2, 3, 15.00, '2023-01-01';
    ```
3. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 10 WHERE VendaID = 1
    ```
4. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE DataVenda BETWEEN '2023-01-01' AND '2023-12-31'
    ```
5. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, COUNT(*), SUM(Quantidade) FROM Vendas GROUP BY ClienteID
    ```
6. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (2, 3, 2, 20.00, '2023-02-01');
    ```
7. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 12 WHERE VendaID  = 3
    ```
8. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID = (SELECT ClienteID FROM Clientes WHERE Nome = 'Pedro')
    ```
9. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, SUM(PrecoUnitario * Quantidade) FROM Vendas GROUP BY ProdutoID
    ```
10. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda) VALUES (1, 2, 3, 15.00, '2023-01-01';
    ```
11. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, SUM(Quantidade) FROM Vendas GROUP BY ClienteID, ProdutoID
    ```
12. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 8 WHERE VendaID  = 4
    ```
13. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE DataVenda BETWEEN '2023-01-01' AND '2023-12-31'
    ```
14. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, COUNT(*), AVG(PrecoUnitario) FROM Vendas GROUP BY ClienteID
    ```
15. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (3, 4, 1, 25.00, '2023-04-01');
    ```
16. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 14 WHERE VendaID  = 5
    ```
17. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID = (SELECT ClienteID FROM Clientes WHERE Nome = 'Lucas')
    ```
18. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, COUNT(*), SUM(PrecoUnitario) FROM Vendas GROUP BY ClienteID
    ```
19. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (4, 5, 3, 35.00, '2023-06-01');
    ```
20. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 16 WHERE VendaID  = 6
    ```
21. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE DataVenda BETWEEN '2023-01-01' AND '2023-12-31'
    ```
22. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, COUNT(*), AVG(PrecoUnitario) FROM Vendas GROUP BY ProdutoID
    ```
23. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (5, 6, 4, 40.00, '2023-08-01');
    ```
24. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade

 = 18 WHERE VendaID  = 7
    ```
25. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE DataVenda IS NOT NULL
    ```
26. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, COUNT(*), SUM(Quantidade) FROM Vendas GROUP BY ClienteID
    ```
27. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (6, 7, 1, 45.00, '2023-10-01');
    ```
28. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 20 WHERE VendaID  = 8
    ```
29. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE DataVenda IS NOT NULL
    ```
30. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, COUNT(*), SUM(Quantidade) FROM Vendas GROUP BY ProdutoID
    ```
31. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda) VALUES (7, 8, 2, 50.00, '2023-11-01';
    ```
32. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 22 WHERE VendaID  = 9
    ```
33. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID = (SELECT ClienteID FROM Clientes WHERE Nome = 'Paulo')
    ```
34. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, COUNT(*), SUM(PrecoUnitario) FROM Vendas GROUP BY ProdutoID
    ```
35. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (8, 9, 3, 60.00, '2024-01-01');
    ```
36. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 24 WHERE VendaID  = 10
    ```
37. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE DataVenda IS NOT NULL
    ```
38. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, COUNT(*), SUM(Quantidade) FROM Vendas GROUP BY ClienteID
    ```
39. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (9, 10, 1, 65.00, '2024-02-01');
    ```
40. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 26 WHERE VendaID  = 11
    ```
41. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE DataVenda IS NOT NULL
    ```
42. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, COUNT(*), SUM(Quantidade) FROM Vendas GROUP BY ProdutoID
    ```
43. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (10, 11, 2, 75.00, '2024-03-01');
    ```
44. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 28 WHERE VendaID  = 12
    ```
45. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE ClienteID = (SELECT ClienteID FROM Clientes WHERE Nome = 'Mariana')
    ```
46. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, COUNT(*), SUM(Quantidade) FROM Vendas GROUP BY ClienteID
    ```
47. Corrija a seguinte consulta:
    ```sql
    INSERT INTO Vendas (ClienteID, ProdutoID, Quantidade, PrecoUnitario, DataVenda VALUES (11, 12, 1, 80.00, '2024-04-01');
    ```
48. Corrija a seguinte consulta:
    ```sql
    UPDATE Vendas SET Quantidade = 30 WHERE VendaID  = 13
    ```
49. Corrija a seguinte consulta:
    ```sql
    DELETE FROM Vendas WHERE DataVenda IS NOT NULL
    ```
50. Corrija a seguinte consulta:
    ```sql
    SELECT ClienteID, ProdutoID, COUNT(*), SUM(Quantidade) FROM Vendas GROUP BY ProdutoID
    ```

### Exercícios sobre agrupamento e ordenação de dados

#### Exercícios Fáceis (50)

1. Escreva uma consulta SQL para selecionar todas as colunas da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente.
2. Escreva uma consulta SQL para selecionar todas as colunas da tabela "Vendas" e ordená-las pelo campo "DataVenda" em ordem decrescente.
3. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente.
4. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente.
5. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda" da tabela "Vendas" e ordená-las pelo campo "DataVenda" em ordem decrescente.
6. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "ClienteID" em ordem crescente.
7. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente.
8. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade" da tabela "Vendas" e ordená-las pelo campo "Quantidade" em ordem crescente.
9. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem decrescente.
10. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "ProdutoID" em ordem crescente.
11. Escreva uma consulta SQL para selecionar as colunas "VendaID", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente.
12. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 10 linhas.
13. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado a 5 linhas.
14. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda" da tabela "Vendas" e ordená-las pelo campo "DataVenda" em ordem decrescente, limitando o resultado a 7 linhas.
15. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 3 linhas.
16. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 4 linhas.
17. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade" da tabela "Vendas" e ordená-las pelo campo "Quantidade" em ordem crescente, limitando o resultado a 6 linhas.
18. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem decrescente, limitando o resultado a 8 linhas.
19. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "ProdutoID" em ordem crescente, limitando o resultado a 9 linhas.
20. Escreva uma consulta SQL para selecionar as colunas "VendaID", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 2 linhas.
21. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 12 linhas.
22. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado a 15 linhas.
23. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda" da tabela

 "Vendas" e ordená-las pelo campo "DataVenda" em ordem decrescente, limitando o resultado a 20 linhas.
24. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 5 linhas.
25. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 10 linhas.
26. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade" da tabela "Vendas" e ordená-las pelo campo "Quantidade" em ordem crescente, limitando o resultado a 3 linhas.
27. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem decrescente, limitando o resultado a 7 linhas.
28. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "ProdutoID" em ordem crescente, limitando o resultado a 6 linhas.
29. Escreva uma consulta SQL para selecionar as colunas "VendaID", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 4 linhas.
30. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 2 linhas.
31. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado a 8 linhas.
32. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda" da tabela "Vendas" e ordená-las pelo campo "DataVenda" em ordem decrescente, limitando o resultado a 1 linha.
33. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 4 linhas.
34. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 5 linhas.
35. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade" da tabela "Vendas" e ordená-las pelo campo "Quantidade" em ordem crescente, limitando o resultado a 2 linhas.
36. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem decrescente, limitando o resultado a 3 linhas.
37. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "ProdutoID" em ordem crescente, limitando o resultado a 7 linhas.
38. Escreva uma consulta SQL para selecionar as colunas "VendaID", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 6 linhas.
39. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 9 linhas.
40. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado a 11 linhas.
41. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda" da tabela "Vendas" e ordená-las pelo campo "DataVenda" em ordem decrescente, limitando o resultado a 12 linhas.
42. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 13 linhas.
43. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 14 linhas.
44. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade" da tabela "Vendas" e ordená-las pelo campo "Quantidade" em ordem crescente, limitando o resultado a 15 linhas.
45. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem decrescente, limitando o resultado a 16 linhas.
46. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "ProdutoID" em ordem crescente, limitando o resultado a 17 linhas.
47. Escreva uma consulta SQL para selecionar as colunas "VendaID", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 18 linhas.
48. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 19 linhas.
49. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado a 20 linhas.
50. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda" da tabela "Vendas" e ordená-las pelo campo "DataVenda" em ordem decrescente, limitando o resultado a 21 linhas.

#### Exercícios Intermediários (50)

1. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 5 linhas, a partir da 10ª linha.
2. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado a 7 linhas, a partir da 3ª linha.
3. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda" da tabela "Vendas" e ordená-las pelo campo "DataVenda" em ordem decrescente, limitando o resultado a 10 linhas, a partir da 5ª linha.
4. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 8 linhas, a partir da 2ª linha.
5. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 6 linhas, a partir da 4ª linha.
6. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade" da tabela "Vendas" e ordená-las pelo campo "Quantidade" em ordem crescente, limitando o resultado a 9 linhas, a partir da 1ª linha.
7. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem decrescente, limitando o resultado a 12 linhas, a partir da 3ª linha.
8. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "ProdutoID" em ordem crescente, limitando o resultado a 10 linhas, a partir da 5ª linha.
9. Escreva uma consulta SQL para selecionar as colunas "VendaID", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 7 linhas, a partir da 2ª linha.
10. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 4 linhas, a partir da 6ª linha.
11. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado a 11 linhas, a partir da 8ª linha.
12. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda" da tabela "Vendas" e ordená-las pelo campo "

DataVenda" em ordem decrescente, limitando o resultado a 5 linhas, a partir da 7ª linha.
13. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 3 linhas, a partir da 9ª linha.
14. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 4 linhas, a partir da 11ª linha.
15. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade" da tabela "Vendas" e ordená-las pelo campo "Quantidade" em ordem crescente, limitando o resultado a 6 linhas, a partir da 3ª linha.
16. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem decrescente, limitando o resultado a 9 linhas, a partir da 5ª linha.
17. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "ProdutoID" em ordem crescente, limitando o resultado a 13 linhas, a partir da 10ª linha.
18. Escreva uma consulta SQL para selecionar as colunas "VendaID", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 8 linhas, a partir da 4ª linha.
19. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 5 linhas, a partir da 12ª linha.
20. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado a 9 linhas, a partir da 7ª linha.
21. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda" da tabela "Vendas" e ordená-las pelo campo "DataVenda" em ordem decrescente, limitando o resultado a 6 linhas, a partir da 8ª linha.
22. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 2 linhas, a partir da 13ª linha.
23. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 7 linhas, a partir da 6ª linha.
24. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade" da tabela "Vendas" e ordená-las pelo campo "Quantidade" em ordem crescente, limitando o resultado a 4 linhas, a partir da 11ª linha.
25. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem decrescente, limitando o resultado a 10 linhas, a partir da 15ª linha.
26. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "ProdutoID" em ordem crescente, limitando o resultado a 6 linhas, a partir da 14ª linha.
27. Escreva uma consulta SQL para selecionar as colunas "VendaID", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 3 linhas, a partir da 12ª linha.
28. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 4 linhas, a partir da 16ª linha.
29. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado a 5 linhas, a partir da 13ª linha.
30. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda" da tabela "Vendas" e ordená-las pelo campo "DataVenda" em ordem decrescente, limitando o resultado a 7 linhas, a partir da 11ª linha.
31. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 1 linha, a partir da 17ª linha.
32. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 4 linhas, a partir da 18ª linha.
33. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade" da tabela "Vendas" e ordená-las pelo campo "Quantidade" em ordem crescente, limitando o resultado a 2 linhas, a partir da 14ª linha.
34. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem decrescente, limitando o resultado a 5 linhas, a partir da 19ª linha.
35. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "ProdutoID" em ordem crescente, limitando o resultado a 6 linhas, a partir da 20ª linha.
36. Escreva uma consulta SQL para selecionar as colunas "VendaID", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 3 linhas, a partir da 21ª linha.
37. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 7 linhas, a partir da 22ª linha.
38. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado a 8 linhas, a partir da 23ª linha.
39. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda" da tabela "Vendas" e ordená-las pelo campo "DataVenda" em ordem decrescente, limitando o resultado a 5 linhas, a partir da 24ª linha.
40. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 6 linhas, a partir da 25ª linha.
41. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 2 linhas, a partir da 26ª linha.
42. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade" da tabela "Vendas" e ordená-las pelo campo "Quantidade" em ordem crescente, limitando o resultado a 9 linhas, a partir da 27ª linha.
43. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem decrescente, limitando o resultado a 8 linhas, a partir da 28ª linha.
44. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "ProdutoID" em ordem crescente, limitando o resultado a 3 linhas, a partir da 29ª linha.
45. Escreva uma consulta SQL para selecionar as colunas "VendaID", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 10 linhas, a partir da 30ª linha.
46. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 4 linhas, a partir da 31ª linha.
47. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado a 5 linhas, a partir da 32ª linha.
48.

 Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda" da tabela "Vendas" e ordená-las pelo campo "DataVenda" em ordem decrescente, limitando o resultado a 8 linhas, a partir da 33ª linha.
49. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 7 linhas, a partir da 34ª linha.
50. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 6 linhas, a partir da 35ª linha.

#### Exercícios Avançados (50)

1. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "Cidade" da tabela "Clientes" e ordená-las pelo campo "Cidade" em ordem crescente, limitando o resultado a 10 linhas.
2. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "CategoriaID" da tabela "Produtos" e ordená-las pelo campo "CategoriaID" em ordem decrescente, limitando o resultado a 15 linhas.
3. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda", "Quantidade" da tabela "Vendas" e ordená-las pelo campo "DataVenda" em ordem decrescente, limitando o resultado a 20 linhas.
4. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "Telefone" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 5 linhas.
5. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "PrecoUnitario" em ordem crescente, limitando o resultado a 10 linhas.
6. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 8 linhas.
7. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "Email" da tabela "Clientes" e ordená-las pelo campo "Email" em ordem crescente, limitando o resultado a 12 linhas.
8. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "QuantidadeEmEstoque" da tabela "Produtos" e ordená-las pelo campo "QuantidadeEmEstoque" em ordem decrescente, limitando o resultado a 7 linhas.
9. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda", "PrecoTotal" da tabela "Vendas" e ordená-las pelo campo "PrecoTotal" em ordem crescente, limitando o resultado a 6 linhas.
10. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "Endereco" da tabela "Clientes" e ordená-las pelo campo "Endereco" em ordem decrescente, limitando o resultado a 3 linhas.
11. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "FornecedorID" da tabela "Produtos" e ordená-las pelo campo "FornecedorID" em ordem crescente, limitando o resultado a 11 linhas.
12. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "Quantidade" em ordem decrescente, limitando o resultado a 14 linhas.
13. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "DataNascimento" da tabela "Clientes" e ordená-las pelo campo "DataNascimento" em ordem crescente, limitando o resultado a 9 linhas.
14. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "Peso" da tabela "Produtos" e ordená-las pelo campo "Peso" em ordem decrescente, limitando o resultado a 8 linhas.
15. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda", "Desconto" da tabela "Vendas" e ordená-las pelo campo "Desconto" em ordem crescente, limitando o resultado a 4 linhas.
16. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "Cidade" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem decrescente, limitando o resultado a 13 linhas.
17. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado a 10 linhas.
18. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade", "PrecoTotal" da tabela "Vendas" e ordená-las pelo campo "PrecoTotal" em ordem decrescente, limitando o resultado a 5 linhas.
19. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "Telefone" da tabela "Clientes" e ordená-las pelo campo "Telefone" em ordem crescente, limitando o resultado a 15 linhas.
20. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "CategoriaID" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado a 12 linhas.
21. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda", "Desconto" da tabela "Vendas" e ordená-las pelo campo "DataVenda" em ordem decrescente, limitando o resultado a 8 linhas.
22. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "Email" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 7 linhas.
23. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "QuantidadeEmEstoque" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem decrescente, limitando o resultado a 9 linhas.
24. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "Quantidade" em ordem crescente, limitando o resultado a 11 linhas.
25. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "DataNascimento" da tabela "Clientes" e ordená-las pelo campo "DataNascimento" em ordem decrescente, limitando o resultado a 6 linhas.
26. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "Peso" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado a 4 linhas.
27. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda", "PrecoTotal" da tabela "Vendas" e ordená-las pelo campo "PrecoTotal" em ordem crescente, limitando o resultado a 13 linhas.
28. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "Endereco" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 2 linhas.
29. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "FornecedorID" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem decrescente, limitando o resultado a 14 linhas.
30. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade", "Desconto" da tabela "Vendas" e ordená-las pelo campo "Quantidade" em ordem crescente, limitando o resultado a 3 linhas.
31. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "Cidade" da tabela "Clientes" e ordená-las pelo campo "Cidade" em ordem crescente, limitando o resultado a 8 linhas.
32. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 7 linhas.
33. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda", "Desconto" da tabela "Vendas" e ordená-las pelo campo "Desconto" em ordem decrescente, limitando o resultado a 5 linhas.
34. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "Email" da tabela "Clientes" e ordená-las pelo campo "Email" em ordem crescente, limitando o resultado a 12 linhas.
35. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "QuantidadeEmEstoque" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem crescente, limitando o resultado

 a 10 linhas.
36. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade", "PrecoTotal" da tabela "Vendas" e ordená-las pelo campo "Quantidade" em ordem decrescente, limitando o resultado a 4 linhas.
37. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "DataNascimento" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 9 linhas.
38. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "Peso" da tabela "Produtos" e ordená-las pelo campo "NomeProduto" em ordem decrescente, limitando o resultado a 11 linhas.
39. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "PrecoUnitario" em ordem crescente, limitando o resultado a 2 linhas.
40. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "Endereco" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem decrescente, limitando o resultado a 6 linhas.
41. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "FornecedorID" da tabela "Produtos" e ordená-las pelo campo "FornecedorID" em ordem crescente, limitando o resultado a 7 linhas.
42. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade", "Desconto" da tabela "Vendas" e ordená-las pelo campo "Desconto" em ordem crescente, limitando o resultado a 3 linhas.
43. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "Cidade" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem crescente, limitando o resultado a 8 linhas.
44. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "PrecoUnitario" da tabela "Produtos" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 12 linhas.
45. Escreva uma consulta SQL para selecionar as colunas "VendaID", "DataVenda", "Desconto" da tabela "Vendas" e ordená-las pelo campo "DataVenda" em ordem crescente, limitando o resultado a 6 linhas.
46. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "Email" da tabela "Clientes" e ordená-las pelo campo "Nome" em ordem decrescente, limitando o resultado a 9 linhas.
47. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "QuantidadeEmEstoque" da tabela "Produtos" e ordená-las pelo campo "QuantidadeEmEstoque" em ordem crescente, limitando o resultado a 4 linhas.
48. Escreva uma consulta SQL para selecionar as colunas "VendaID", "Quantidade", "PrecoUnitario" da tabela "Vendas" e ordená-las pelo campo "PrecoUnitario" em ordem decrescente, limitando o resultado a 11 linhas.
49. Escreva uma consulta SQL para selecionar as colunas "ClienteID", "Nome", "DataNascimento" da tabela "Clientes" e ordená-las pelo campo "DataNascimento" em ordem crescente, limitando o resultado a 7 linhas.
50. Escreva uma consulta SQL para selecionar as colunas "ProdutoID", "NomeProduto", "Peso" da tabela "Produtos" e ordená-las pelo campo "Peso" em ordem decrescente, limitando o resultado a 6 linhas.

#### Listas de clientes

1. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes".
2. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" e ordena pelo campo "Nome".
3. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Cidade" seja igual a "São Paulo".
4. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Idade" seja maior que 30.
5. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" comece com a letra "A".
6. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" termine com a letra "o".
7. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Idade" seja menor que 25.
8. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Cidade" não seja "Rio de Janeiro".
9. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Email" não contenha "gmail.com".
10. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" tenha exatamente 5 caracteres.
11. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Idade" seja entre 20 e 30.
12. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Cidade" seja "Belo Horizonte" ou "Curitiba".
13. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" não comece com a letra "J".
14. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Idade" não seja entre 18 e 35.
15. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" contenha a letra "e" e tenha mais de 6 caracteres.
16. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Cidade" seja "Brasília" e o campo "Idade" seja maior que 25.
17. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Email" não termine com "yahoo.com".
18. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" tenha pelo menos 4 caracteres e comece com a letra "M".
19. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Idade" seja menor que 18 ou maior que 40.
20. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Cidade" seja "Recife" e o campo "Nome" comece com a letra "L".
21. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Email" contenha "hotmail.com" e tenha mais de 10 caracteres.
22. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" tenha exatamente 3 caracteres e o campo "Cidade" seja "Fortaleza".
23. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Idade" seja entre 25 e 35 e o campo "Email" termine com "gmail.com".
24. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Cidade" seja "Salvador" ou "Porto Alegre" e o campo "Idade" seja menor que 30.
25. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" comece com a letra "R" e o campo "Idade" seja maior que 28.
26. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Email" não contenha "outlook.com" e tenha mais de 12 caracteres.
27. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" termine com a letra "a" e tenha menos de 7 caracteres.
28. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Idade" seja menor que 20 ou maior que 50.
29. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Cidade" seja "Campinas" e o campo "Nome" não comece com a letra "T".
30. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Email" termine com "icloud.com" e tenha menos de 8 caracteres.
31. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" contenha a letra "r" e tenha exatamente 5 caracteres.
32. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Idade" seja entre 22 e 29 e o campo "Cidade" seja "Florianópolis".
33. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" não contenha a letra "i" e tenha pelo menos 6 caracteres.
34. Escreva uma

 consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Cidade" seja "São Paulo" e o campo "Idade" seja maior que 27.
35. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Email" contenha "gmail.com" e tenha exatamente 12 caracteres.
36. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" tenha menos de 4 caracteres e o campo "Cidade" não seja "Rio de Janeiro".
37. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Idade" seja menor que 19 ou maior que 45 e o campo "Cidade" seja "Curitiba".
38. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" comece com a letra "S" e tenha pelo menos 5 caracteres.
39. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Cidade" seja "Belo Horizonte" e o campo "Nome" termine com a letra "o".
40. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Email" contenha "yahoo.com" e tenha mais de 15 caracteres.
41. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" tenha exatamente 7 caracteres e o campo "Cidade" não seja "São Paulo".
42. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Idade" seja entre 23 e 33 e o campo "Nome" comece com a letra "P".
43. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" não contenha a letra "a" e tenha menos de 8 caracteres.
44. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Cidade" seja "Recife" e o campo "Idade" seja maior que 31.
45. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Email" termine com "hotmail.com" e tenha menos de 14 caracteres.
46. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" comece com a letra "D" e tenha exatamente 6 caracteres.
47. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Cidade" seja "Brasília" e o campo "Nome" termine com a letra "a".
48. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Idade" seja menor que 26 ou maior que 38 e o campo "Nome" tenha mais de 4 caracteres.
49. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Nome" contenha a letra "e" e o campo "Cidade" seja "Fortaleza".
50. Escreva uma consulta SQL que seleciona todos os registros da tabela "Clientes" onde o campo "Cidade" seja "Salvador" e o campo "Idade" seja menor que 22.

#### Listas de produtos

1. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos".
2. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" e ordena pelo campo "NomeProduto".
3. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja maior que 50.
4. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "QuantidadeEmEstoque" seja menor que 10.
5. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" comece com a letra "A".
6. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" termine com a letra "o".
7. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja entre 20 e 40.
8. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "QuantidadeEmEstoque" seja maior que 100.
9. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" tenha exatamente 5 caracteres.
10. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja menor que 15.
11. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" contenha a letra "e".
12. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "QuantidadeEmEstoque" seja entre 50 e 200.
13. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" não seja maior que 30.
14. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" não comece com a letra "B".
15. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "QuantidadeEmEstoque" não seja menor que 20.
16. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja maior que 25 e menor que 60.
17. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" tenha mais de 6 caracteres.
18. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "QuantidadeEmEstoque" seja menor que 5 ou maior que 150.
19. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja entre 10 e 50 e o campo "QuantidadeEmEstoque" seja maior que 30.
20. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" contenha a letra "a" e tenha exatamente 6 caracteres.
21. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "QuantidadeEmEstoque" seja menor que 8 ou maior que 80.
22. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja menor que 100 e o campo "NomeProduto" tenha mais de 4 caracteres.
23. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" tenha menos de 5 caracteres e o campo "QuantidadeEmEstoque" seja maior que 50.
24. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja maior que 70 e o campo "QuantidadeEmEstoque" seja menor que 30.
25. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" comece com a letra "C" e o campo "PrecoUnitario" seja menor que 20.
26. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "QuantidadeEmEstoque" seja entre 15 e 45 e o campo "NomeProduto" termine com a letra "s".
27. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja maior que 25 e o campo "NomeProduto" contenha a letra "o".
28. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" tenha exatamente 4 caracteres e o campo "QuantidadeEmEstoque" seja maior que 60.
29. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja menor que 40 e o campo "NomeProduto" tenha menos de 8 caracteres.
30. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" contenha a letra "s" e o campo "QuantidadeEmEstoque" seja menor que 20.
31. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja entre 50 e 100 e o campo "NomeProduto" não comece com a letra "P".
32. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" termine com a letra "o" e o campo "QuantidadeEmEstoque" seja maior que 10.
33. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja maior que 20 e o campo "NomeProduto" tenha mais de 5 caracteres.
34. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" conten

ha a letra "e" e tenha menos de 7 caracteres.
35. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "QuantidadeEmEstoque" seja menor que 25 e o campo "PrecoUnitario" seja maior que 60.
36. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" tenha mais de 8 caracteres e o campo "PrecoUnitario" seja menor que 50.
37. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja maior que 15 e o campo "QuantidadeEmEstoque" seja menor que 10.
38. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" termine com a letra "a" e tenha exatamente 7 caracteres.
39. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja menor que 30 e o campo "QuantidadeEmEstoque" seja entre 40 e 100.
40. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" contenha a letra "r" e o campo "PrecoUnitario" seja maior que 35.
41. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" tenha exatamente 3 caracteres e o campo "QuantidadeEmEstoque" seja maior que 20.
42. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja entre 5 e 25 e o campo "NomeProduto" contenha a letra "o".
43. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" tenha mais de 6 caracteres e o campo "QuantidadeEmEstoque" seja menor que 15.
44. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "QuantidadeEmEstoque" seja menor que 7 e o campo "PrecoUnitario" seja maior que 45.
45. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" termine com a letra "o" e o campo "QuantidadeEmEstoque" seja maior que 50.
46. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja menor que 10 e o campo "NomeProduto" tenha exatamente 8 caracteres.
47. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" tenha menos de 4 caracteres e o campo "QuantidadeEmEstoque" seja maior que 70.
48. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "QuantidadeEmEstoque" seja maior que 10 e o campo "PrecoUnitario" seja menor que 25.
49. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "PrecoUnitario" seja maior que 40 e o campo "QuantidadeEmEstoque" seja menor que 60.
50. Escreva uma consulta SQL que seleciona todos os registros da tabela "Produtos" onde o campo "NomeProduto" contenha a letra "e" e tenha exatamente 4 caracteres.

#### Listas de vendas

1. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas".
2. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" e ordena pelo campo "DataVenda".
3. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "Quantidade" seja maior que 5.
4. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "PrecoTotal" seja menor que 100.
5. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "DataVenda" seja entre '2023-01-01' e '2023-12-31'.
6. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "ClienteID" seja igual a 7.
7. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "ProdutoID" seja igual a 12.
8. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "PrecoTotal" seja maior que 200.
9. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "Quantidade" seja menor que 3.
10. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "DataVenda" seja maior que '2022-06-01'.
11. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "PrecoTotal" seja entre 50 e 150.
12. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "ClienteID" seja entre 5 e 15.
13. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "ProdutoID" seja maior que 10.
14. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "DataVenda" seja entre '2023-03-01' e '2023-05-31'.
15. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "ClienteID" seja menor que 10.
16. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "Quantidade" seja entre 2 e 8.
17. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "PrecoTotal" seja maior que 300.
18. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "DataVenda" seja menor que '2021-01-01'.
19. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "ClienteID" seja igual a 3 e o campo "ProdutoID" seja igual a 9.
20. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "Quantidade" seja menor que 1.
21. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "PrecoTotal" seja maior que 250 e o campo "DataVenda" seja maior que '2022-07-01'.
22. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "ClienteID" seja igual a 8 ou o campo "ProdutoID" seja igual a 15.
23. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "Quantidade" seja menor que 4 e o campo "PrecoTotal" seja maior que 100.
24. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "DataVenda" seja maior que '2020-05-01' e o campo "PrecoTotal" seja menor que 50.
25. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "ClienteID" seja entre 1 e 5 e o campo "ProdutoID" seja maior que 8.
26. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "Quantidade" seja entre 1 e 3 e o campo "DataVenda" seja menor que '2022-11-01'.
27. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "PrecoTotal" seja maior que 150 e o campo "ClienteID" seja menor que 10.
28. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "DataVenda" seja entre '2023-02-01' e '2023-10-31' e o campo "ProdutoID" seja igual a 6.
29. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "Quantidade" seja maior que 10 e o campo "PrecoTotal" seja menor que 500.
30. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "ClienteID" seja igual a 4 e o campo "PrecoTotal" seja maior que 100.
31. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "DataVenda" seja menor que '2019-12-31' e o campo "Quantidade" seja menor que 2.
32. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas" onde o campo "PrecoTotal" seja maior que 80 e o campo "ClienteID" seja entre 6 e 12.
33. Escreva uma consulta SQL que seleciona todos os registros da tabela "Vendas
