-- CREATE DATABASE gerenTaref;
USE gerenTaref;
/*
-- Criar Desenvolvedores e TiposTarefas antes
CREATE TABLE Desenvolvedores (
    id_dev INT PRIMARY KEY AUTO_INCREMENT,
    nome_dev VARCHAR(100) NOT NULL,
    email_dev VARCHAR(100) NOT NULL UNIQUE
);

CREATE TABLE TiposTarefas (
    id_type_task INT PRIMARY KEY AUTO_INCREMENT,
    nome_type_task VARCHAR(100) NOT NULL UNIQUE
);

-- Criar Usuarios
CREATE TABLE Usuarios (
    id_usu INT PRIMARY KEY AUTO_INCREMENT,
    nome_usu VARCHAR(100) NOT NULL,
    email_usu VARCHAR(100) NOT NULL UNIQUE,
    senha_usu VARCHAR(255) NOT NULL,
    stats ENUM('admin','analista','desenvolvedor','noFunc') DEFAULT 'noFunc',
    statusOp ENUM('ativo', 'bloqueado', 'inativo') DEFAULT 'ativo'
);

-- Criar Tarefas
CREATE TABLE Tarefas (
    id_task INT PRIMARY KEY AUTO_INCREMENT,
    descricao_task VARCHAR(100) NOT NULL,
    id_dev INT,
    id_type_task INT,
    data_conclusao date,
    stats ENUM('pendente', 'em andamento', 'concluída') DEFAULT 'pendente',
    FOREIGN KEY (id_dev) REFERENCES Desenvolvedores(id_dev),
    FOREIGN KEY (id_type_task) REFERENCES TiposTarefas(id_type_task)
);
*/
-- INSERT INTO Desenvolvedores (nome_dev, email_dev) VALUES ('Joao', 'joaovt@gmail.com');
-- INSERT INTO tipostarefas (nome_type_task) values ('Listar');
/*INSERT INTO tarefas (descricao_task, data_conclusao, stats)
VALUES ('asdadas','2001-12-28', 'em andamento');*/

