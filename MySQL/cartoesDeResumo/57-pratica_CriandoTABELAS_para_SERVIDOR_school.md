Quero que analise, particione e explique detalhadamente cada query envolvida na criação das tabelas para o servidor 'school' a seguir:

CREATE TABLE students (
studentid INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
firstname VARCHAR(40) NOT NULL,
lastname VARCHAR(40) NOT NULL,
class VARCHAR(20),
age INT(3)
);

CREATE TABLE teachers (
teacherid INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
name VARCHAR(80) NOT NULL,
phone VARCHAR(10)
);

CREATE TABLE subjects (
subjectid INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
title VARCHAR(50) NOT NULL
);