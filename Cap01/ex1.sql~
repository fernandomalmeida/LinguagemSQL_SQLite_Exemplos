/*
 * Exercício 1 do Capítulo 1 do Livro Linguagem SQL - Fundamentos e Prática da Editora Saraiva
 * 
 * 1. São dados os esquemas:
 * 
 * Fatura (*numFatura*, codCliente)
 * Produto (*codProduto*, descricao)
 * Cliente(*codCliente*, nome, endereco, credito, tipo, CPF)
 * ItensFatura(*numFatura*, *codProduto*, quantidade, valor)
 * 
 * Utilizando comandos da SQL, realize as seguintes operações:
 */

-- 1.1. Crie todo o esquema.

CREATE TABLE Cliente (
	codCliente INT(11),
	nome CHAR(20) NOT NULL,
	endereco CHAR(50),
	credito INT(11),
	tipo CHAR(20),
	CPF INT(11),
	PRIMARY KEY (codCliente)
);

CREATE TABLE Produto (
	codProduto INT(11),
	descricao CHAR(50),
	PRIMARY KEY (codProduto)
);

CREATE TABLE Fatura (
	numFatura INT(11),
	codCliente INT(11),
	PRIMARY KEY (numFatura),
	FOREIGN KEY (codCliente) REFERENCES Cliente (codCliente)
);

CREATE TABLE ItensFatura (
	numFatura INT(11),
	codProduto INT(11),
	quantidade INT(11),
	valor INT(11),
	FOREIGN KEY (numFatura) REFERENCES Fatura (numFatura),
	FOREIGN KEY (codProduto) REFERENCES Produto (codProduto)
);

-- 1.2. Na tabela Cliente:
-- a) Inclua o campo histórico.

ALTER TABLE Cliente ADD historico CHAR(20);

-- b) Altere o campo nome para varchar(30)

-- Não tem CHANGE no SQLite
-- ALTER TABLE Cliente CHANGE nome nome CHAR(30) NOT NULL;

-- c) Exclua o campo crédito

-- Não tem DROP no SQLite
-- ALTER TABLE Cliente DROP credito;
