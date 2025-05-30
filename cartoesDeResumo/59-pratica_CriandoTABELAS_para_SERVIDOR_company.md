Cartão Explicativo 1: Criação da Tabela employees

CREATE TABLE employees (
  employeeid INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(80) NOT NULL,
  jobtitle VARCHAR(50) NOT NULL,
  salary FLOAT
);

Análise e Particionamento Detalhado

    - CREATE TABLE employees
    - Função: Inicia a criação de uma nova tabela com o nome employees.
    - Contexto: Esta tabela armazenará os registros referentes aos funcionários da empresa.
  
- employeeid INT NOT NULL PRIMARY KEY AUTO_INCREMENT

  - employeeid: Nome da coluna destinada a identificar cada funcionário de maneira única.
  - INT: Define que o tipo de dado é numérico inteiro.

  - NOT NULL: Garante que esta coluna não aceite valores nulos; cada registro DEVE ter um ID.
  - PRIMARY KEY: Designa essa coluna como a chave primária, ou seja, o identificador único da
    tabela.

  - AUTO_INCREMENT: Faz com que o valor seja incrementado automaticamente a cada novo registro
    inserido, evitando conflitos e garantindo unicidade

- name VARCHAR(80) NOT NULL

  - name: Nome da coluna para armazenar o nome do funcionário.

  - VARCHAR(80): Define um campo textual com até 80 caracteres.

  - NOT NULL: Impede a inserção de registros sem o nome do funcionário.

- jobtitle VARCHAR(50) NOT NULL

  - jobtitle: Armazena o cargo ou título profissional do funcionário.

  - VARCHAR(50): Campo textual com até 50 caracteres.

  - NOT NULL: Exige que o cargo seja informado para cada registro.

  - salary FLOAT

  - salary: Coluna para armazenar o salário do funcionário.

  - FLOAT: Tipo de dado numérico que permite números com casas decimais, adequado para valores
    monetários, embora em ambientes reais muitas vezes se usem tipos com precisão extra (DECIMAL).

  - ; (ponto e vírgula):

  - Finaliza a instrução SQL, sinalizando que a query está completa.
  
Exemplo Prático na Realidade:
Imagine que uma empresa deseja gerenciar seus colaboradores de forma automatizada. Ao criar a tabela employees, o sistema começará a armazenar informações como o identificador único (gerado automaticamente), o nome, o cargo desempenhado (como gerente, analista, etc.) e o salário de cada funcionário. Dessa forma, ao inserir um novo colaborador, não é necessário digitar manualmente o ID, pois ele é definido automaticamente.

Exemplo Lúdico
Pense na tabela employees como um registro digital de uma equipe de futebol.
- employeeid: É o número da camisa, único para cada jogador.
- name: É o nome do jogador.
- jobtitle: É a posição ou função em campo (como atacante, zagueiro, etc.).
- salary: Representa o valor que o jogador recebe por suas atuações.
Assim, cada “ficha” do jogador (registro) é preenchida automaticamente com um número (camisa) e informações essenciais, garantindo que todos os jogadores sejam identificados e organizados.

Cartão Explicativo 2: Criação da Tabela clients

CREATE TABLE clients (
  clientid INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(80) NOT NULL,
  phone VARCHAR(15),
  address VARCHAR(150)
);

Análise e Particionamento Detalhado

- CREATE TABLE clients
  - Função: Inicia a criação de uma nova tabela denominada clients, que armazenará os registros dos clientes da empresa.

clientid INT NOT NULL PRIMARY KEY AUTO_INCREMENT
  - clientid: Identificador único para cada cliente.
  - INT NOT NULL: Valor numérico, obrigatório para cada registro.
  - PRIMARY KEY AUTO_INCREMENT: Garante unicidade e incrementa automaticamente o valor, evitando a necessidade de inserção manual para cada novo cliente.

name VARCHAR(80) NOT NULL
  - name: Coluna para armazenar o nome do cliente.
  - VARCHAR(80): Campo textual com capacidade para até 80 caracteres.
  - NOT NULL: Exige a informação do nome para cada registro.

phone VARCHAR(15)
  - phone: Coluna para armazenar o telefone do cliente.
  - VARCHAR(15): Campo textual que permite números, hífens ou outros caracteres, com até 15 caracteres.
  - Nota: Não é obrigatório (não há NOT NULL), permitindo que registros sejam inseridos sem essa informação.

address VARCHAR(150)
  - address: Armazena o endereço do cliente.
  - VARCHAR(150): Campo textual com até 150 caracteres, permitindo uma descrição detalhada.
  - Nota: Também não é obrigatório.

; (ponto e vírgula):
  - Indica o final da query

Exemplo Prático na Realidade:
Considere uma empresa cujo objetivo é registrar e manter contato com seus clientes. Ao criar a tabela clients, o sistema passa a armazenar cada cliente com um ID único, seu nome obrigatório e, opcionalmente, seu telefone e endereço. Essa estrutura possibilita a consulta para enviar promoções, realizar cobranças ou registrar histórico de compras.

Exemplo Lúdico:
Imagine a tabela clients como um catálogo de clientes de uma loja de música.
- clientid: Seria como o número único de cada cliente no cadastro, como um “código de cliente”.
- name: O nome do cliente, indispensável para identificação.
- phone: O contato para possíveis ligações ou mensagens sobre lançamentos musicais.
- address: O endereço onde são enviadas revistas ou catálogos promocionais.

Assim, cada “ficha” do cliente é organizada para facilitar o acompanhamento, da mesma forma que um catálogo organizado permite identificar e contatar cada entusiasta da música.

Cartão Explicativo 3: Criação da Tabela projects

CREATE TABLE projects (
  projectid INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
  title VARCHAR(200) NOT NULL,
  clientid INT,
  employeeid INT,
  startdate DATETIME,
  enddate DATETIME
);

Análise e Particionamento Detalhado
CREATE TABLE projects
  - Função: Cria uma nova tabela chamada projects, destinada a armazenar informações sobre os projetos desenvolvidos na empresa.

projectid INT NOT NULL PRIMARY KEY AUTO_INCREMENT
  - projectid: Coluna que atua como identificador único para cada projeto.
  - INT NOT NULL: Tipo numérico, obrigatório em cada registro.
  - PRIMARY KEY AUTO_INCREMENT: Garante que cada projeto receba um identificador único automaticamente, com incremento sucessivo.
  
title VARCHAR(200) NOT NULL
  - title: Designa o título ou nome do projeto.
  - VARCHAR(200): Campo textual com capacidade para até 200 caracteres, permitindo títulos descritivos.
  - NOT NULL: Exige que o título seja informado em cada registro, pois é fundamental para identificar o projeto

clientid INT
- clientid: Armazena um número que, normalmente, se relaciona ao identificador de um cliente (possivelmente a tabela clients).
- Tipo: Inteiro.
- Nota: Não possui NOT NULL, o que permite que um projeto seja registrado sem vinculação imediata a um cliente (ou pode ser definido posteriormente).

employeeid INT
  - employeeid: Armazena o identificador de um funcionário (geralmente vinculado à tabela employees) que esteja gerenciando ou participando do projeto.
  - Tipo: Inteiro.
  - Nota: Também opcional – possibilita relacionar o projeto a um colaborador.

startdate DATETIME
  - startdate: Indica a data e hora de início do projeto.
  - DATETIME: Tipo que armazena data e hora completas, permitindo um registro preciso do momento em que o projeto foi iniciado.

enddate DATETIME
  - enddate: Registra a data e hora para a conclusão (ou prazo final) do projeto.
  - Tipo: DATETIME, possibilitando planejar e acompanhar o término das atividades.

; (ponto e vírgula):
  - Encerra a query.

Exemplo Prático na Realidade:
Em uma empresa que gerencia diversos projetos, a tabela projects é essencial para controlar cada projeto com seu título e período de execução. Quando um novo projeto é iniciado, o sistema cria um registro com um ID único, o nome do projeto e os detalhes sobre seus responsáveis (cliente e funcionário). As colunas startdate e enddate permitem acompanhar o cronograma de execução e o andamento das atividades.

Exemplo Lúdico:
Imagine a tabela projects como um quadro de avisos em um escritório de projetos.
- projectid: É o número único de cada anúncio, garantindo que cada projeto tenha uma identificação distinta.
- title: O título chamativo do projeto, como “Reestruturação do Site” ou “Lançamento de Novo Produto”.
- clientid: Representa o “cartão de visita” do cliente que contratou o serviço, possibilitando uma referência cruzada com o cadastro dos clientes.
- employeeid: É como o “supervisor” indicado que ficará responsável pelo projeto, útil para que todos saibam quem lidera a iniciativa.
- startdate e enddate: São as datas que marcam o início e o fim do projeto, como se o anúncio tivesse um prazo definido, permitindo que o quadro seja atualizado conforme os projetos evoluem.

Essa organização facilita o gerenciamento do fluxo de trabalho dentro da empresa.
