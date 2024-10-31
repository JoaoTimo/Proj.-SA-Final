-- create database gerenTaref;

use gerenTaref;
/*
-- Administrador 
CREATE TABLE Administrador ( 
id_adm INT PRIMARY KEY AUTO_INCREMENT, 
nome_adm VARCHAR(100) NOT NULL, email VARCHAR(100) NOT NULL UNIQUE, 
senha_adm VARCHAR(100) NOT NULL, email_adm VARCHAR(100) NOT NULL, 
is_ativo BOOLEAN DEFAULT TRUE, 
criado_em TIMESTAMP DEFAULT CURRENT_TIMESTAMP 
);

-- Desenvolvedor 
CREATE TABLE Desenvolvedor ( 
id_dev INT PRIMARY KEY AUTO_INCREMENT, 
nome_dev VARCHAR(100) NOT NULL, email_dev VARCHAR(100) NOT NULL UNIQUE, 
senha_dev VARCHAR(100) NOT NULL, 
is_ativo BOOLEAN DEFAULT TRUE, 
criado_em TIMESTAMP DEFAULT CURRENT_TIMESTAMP 
);

-- Tabela usuário
 CREATE TABLE Usuarios (
    user_id INT PRIMARY KEY AUTO_INCREMENT,
    nome_usu VARCHAR(50) NOT NULL UNIQUE,
    email_usu VARCHAR(100) NOT NULL UNIQUE,
    pass_usu VARCHAR(100) NOT NULL,
    status ENUM('Admin', 'Dev', 'Usuario') DEFAULT 'Usuario',
    status_ativo ENUM('ativo', 'bloqueado', 'inativo') DEFAULT 'ativo',
    tentativas INT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

*/
CREATE TABLE Tarefa ( 
id_tasks INT PRIMARY KEY AUTO_INCREMENT, 
name_tasks VARCHAR(100) NOT NULL, 
descricao_tasks VARCHAR(100) NOT NULL, 
task_type_id INT, 
qm_criou INT NOT NULL, -- Quem criou a tarefa 
-- FOREIGN KEY (qm_criou) REFERENCES Users(user_id), 
data_cria DATETIME DEFAULT CURRENT_TIMESTAMP  NOT NULL
); 
/*
 -- Permissão create TABLE Permissions ( permission_id INT PRIMARY KEY AUTO_INCREMENT, permission_name VARCHAR(50) NOT NULL UNIQUE -- Ex: 'admin', 'user' );

-- Associação de usuários e permissões CREATE TABLE UserPermissions ( user_id INT, permission_id INT, FOREIGN KEY (user_id) REFERENCES Users(user_id), FOREIGN KEY (permission_id) REFERENCES Permissions(permission_id), PRIMARY KEY (user_id, permission_id) );

-- Associações de Usuários e Tarefas CREATE TABLE UserTasks ( task_id INT, user_id INT, assigned_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP, FOREIGN KEY (task_id) REFERENCES Tasks(task_id), FOREIGN KEY (user_id) REFERENCES Users(user_id), PRIMARY KEY (task_id, user_id) );

-- Histórico de tarefas CREATE TABLE HistoricoTarefas ( historico_id INT PRIMARY KEY AUTO_INCREMENT, tarefa_id INT, alterado_por INT, descricao_alteracao TEXT, data_alteracao TIMESTAMP DEFAULT CURRENT_TIMESTAMP, FOREIGN KEY (tarefa_id) REFERENCES Tarefas(tarefa_id) ON DELETE CASCADE, FOREIGN KEY (alterado_por) REFERENCES Desenvolvedor(desenvolvedor_id) ON DELETE SET NULL ); 

 -- Usuários Bloqueados CREATE TABLE BlockedUsers ( user_id INT, blocked_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP, FOREIGN KEY (user_id) REFERENCES Users(user_id), PRIMARY KEY (user_id) );
Permissions e UserPermissions controlam o que cada usuário pode fazer no sistema. TaskTypes definem diferentes categorias de tarefas. Tasks armazena as tarefas com informações de tipo e criador. UserTasks associa usuários às tarefas. BlockedUsers armazena informações de usuários que foram bloqueados.

INSERT INTO Desenvolvedor (nome_dev, email_dev, senha_dev) VALUES ('João Silva', 'joao.silva@example.com', 'hashed_password');

INSERT INTO Administrador (nome_adm, email_adm, senha_adm) VALUES ('Maria Souza', 'maria.souza@example.com', 'hashed_password');
*/

