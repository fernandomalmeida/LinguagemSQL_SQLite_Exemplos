/*
 * Exercício 2 do Capítulo 1 do Livro Linguagem SQL - Fundamentos e Prática da Editora Saraiva
 * 
 * Com os esquemas seguintes:
 * Cliente (*CPF*, nome, numConta, telefone, cidade)
 * Carro (*CHASSIS*, modelo, cor, ano, valor)
 * Aluguel (*CPF*, *CHASSIS*, dataEntrada, dataSaida, total)
 * 
 */

-- 2.1. Crie todo o esquema.

CREATE TABLE Cliente (
	CPF INT(11),
	nome CHAR(20),
	numConta INT(11),
	telefone CHAR(11),
	cidade CHAR(20),
	PRIMARY KEY (CPF)
);

CREATE TABLE Carro (
	CHASSIS CHAR(11),
	modelo CHAR(20),
	cor CHAR(20),
	ano INT(4),
	valor INT(11),
	PRIMARY KEY (CHASSIS)
);

CREATE TABLE Aluguel (
	CPF INT(11),
	CHASSIS CHAR(11),
	dataEntrada DATE,
	dataSaida DATE,
	total INT(11),
	FOREIGN KEY (CPF) REFERENCES Cliente (CPF),
	FOREIGN KEY (CHASSIS) REFERENCES Carro (CHASSIS)
);

-- 2.2. Com as tabelas do esquema do item 2, insire dados conforme apresentados.

INSERT INTO Cliente (CPF, nome, numConta, telefone, cidade) VALUES
	(111111, "Ana", "2317", "019", "Campinas"),
	(222222, "Fábio", "1711", "019", "Jundiaí"),
	(121111, "Maria", "7121", "011", "São Paulo"),
	(321222, "Flávio", "2211", "019", "Campinas"),
	(123111, "Fernando", "1123", "031", "Rio de Janeiro"),
	(217222, "Marta", "3211", "021", "Belo Horizonte");

INSERT INTO Carro (CHASSIS, modelo, cor, ano) VALUES
	("A21", "Uno", "Prata", 2003),
	("2AC", "Gol", "Preto", 2004),
	("33A", "Corsa", "Branco", 2005),
	("12C", "Uno", "Verde", 2001),
	("1C2", "Astra", "Prata", 2005),
	("22A", "Gol", "Prata", 2005);


INSERT INTO Aluguel (CPF, CHASSIS, dataEntrada, dataSaida) VALUES
	(111111, "33A", "21-07-2006", "05-08-2006"),
	(222222, "12C", "21-07-2006", ""),
	(222222, "33A", "23-07-2006", "06-08-2006"),
	(222222, "1C2", "24-07-2006", "");


-- 2.3. Utilizando comandos da linguagem SQL e com os dados indicados no iem 2.2:

-- a) Inclua uma linha na tabela Cliente e deixe um campo em branco.
INSERT INTO Cliente VALUES (121212, "Fabiano", NULL, "079", "Aracaju");

-- b) Inclua um registro na tabela Carro na seguinte ordem: (valor, cor, ano, CHASSIS, modelo).
INSERT INTO Carro (valor, cor, ano, CHASSIS, modelo) VALUES (12000, "Vermelha", 2013, "2A1", "Eclipse");

-- c) Inclua três tuplas, utilizando um só comando na tabela Aluguel.
INSERT INTO Aluguel (CPF, CHASSIS, dataEntrada) VALUES
	(121212, "2A1", "14-07-2013"),
	(121212, "1C2", "14-07-2013"),
	(121212, "33A", "14-07-2013");

-- d) Altere, na tabela Cliente, o campo telefone para 019.
UPDATE Cliente SET telefone = "019";

-- e) Altere um registro na tabela Cliente e modifique o nome para André.
UPDATE Cliente SET nome = "André" WHERE CPF = "111111";

-- f) Altere na tabela Cliente aqueles que possuem conta com número maior que 2000 para a cidade de Brasília.
UPDATE Cliente SET cidade = "Brasília" WHERE numConta > "2000";

-- g) Na tabela Carro, modifique todos os valores dos carros para 20.000.
UPDATE Carro SET valor = 20000;

-- h) Na tabela Carro, altere todos os modelos Uno e Corsa para a cor azul.
UPDATE Carro SET cor = "Azul" WHERE modelo = "Uno" OR modelo = "Corsa";

-- i) Altere um registro na tabela Aluguel;
UPDATE Aluguel SET total = "1000";

-- j) Na tabela Aluguel, altere todos os registros para que a data de saída fique em branco.
UPDATE Aluguel SET dataSaida = NULL;

-- k) Excluir, na tabela Cliente, aqueles da cidade de Campinas.
DELETE FROM Cliente WHERE cidade = "Campinas";

-- l) Excluir, na tabela Carro, os veículos dos anos 2003 e 2004.
DELETE FROM Carro WHERE ano = 2003 OR ano = 2004;

-- m) Excluir, na tabela Carro, o veículo de Chassis 22A.
DELETE FROM Carro WHERE CHASSIS = "22A";

-- n) Excluir um registro da tabela Cliente;
DELETE FROM Cliente WHERE cidade = "Rio de Janeiro";

-- o) Excluir um conjunto de tuplas da tabela Carro.
DELETE FROM Carro WHERE ano = 2005;

-- p) Excluir, na tabela Carro, o modelo Gol e de cor prata.
DELETE FROM Carro WHERE modelo = "Gol" AND cor = "Prata;

-- q) Excluir, na tabela Cliente, os clientes que possuam telefone 019 e morem em Campinas.
DELETE FROM Cliente WHERE telefone = "019" AND cidade = "Campinas";

-- r) Excluir, na tabela Carro, os veículos com valores inferiores a 2.000 e superiores a 1.000
DELETE FROM Carro WHERE valor < 2000 AND valor > 1000;

-- s) Excluia todos os dados da tabela Aluguel.
DELETE FROM Aluguel;
