CREATE TABLE persona  ( 
    id      bigint(15) AUTO_INCREMENT NOT NULL,
    paterno varchar(100) NULL,
    materno varchar(100) NULL,
    nombres varchar(100) NULL,
    email   varchar(100) NULL,
    PRIMARY KEY(id));
    
    
CREATE TABLE usuario  ( 
    id          bigint(15) AUTO_INCREMENT NOT NULL,
    username    varchar(100) NULL,
    password varchar(100) NULL,
    estado      varchar(20) NULL,
    rol         varchar(100) NULL,
    id_persona  bigint(15) NULL,
    PRIMARY KEY(id));
    
ALTER TABLE usuario
    ADD CONSTRAINT REL_1
    FOREIGN KEY(id_persona)
    REFERENCES persona(id);
