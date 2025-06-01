Cartão 7: Sobre os Bancos de Dados Padrão do MySQL

O MySQL, ao ser instalado, cria automaticamente alguns bancos de dados padrão que auxiliam no gerenciamento, monitoramento e exemplos de aprendizagem. Cada um possui funções específicas:

A) information_schema database
Explicação Detalhada:
O information_schema é um banco de dados virtual que armazena metadados – ou seja, dados sobre os dados – como a estrutura de tabelas, colunas, permissões e relacionamentos de todos os bancos de dados presentes no sistema. Ele não contém os dados em si, mas informações sobre a organização do sistema.

Exemplo Prático:
Um desenvolvedor que deseja automatizar a documentação do sistema pode consultar o information_schema para obter informações sobre todas as tabelas e colunas existentes, facilitando a criação de relatórios.

Exemplo Lúdico:
Pense no information_schema como o catálogo de uma biblioteca que descreve cada coleção, a localização exata de cada livro, o autor e o assunto, sem conter o próprio conteúdo dos livros.

B) mysql database

O banco de dados mysql contém todas as informações relacionadas à administração do MySQL. Ele armazena dados essenciais como contas de usuários, privilégios, permissões e configurações internas do servidor.

Exemplo Prático:
Quando um administrador adiciona ou altera usuários e suas permissões, essas informações são registradas no banco de dados mysql. Por exemplo, a criação de um novo usuário com acesso controlado utiliza dados armazenados aqui.

Exemplo Lúdico:
Imagine um diretório administrativo de uma escola, onde estão registradas todas as informações dos funcionários e suas responsabilidades. Esse diretório é fundamental para o bom funcionamento e a organização da instituição.

C) performance_schema database

O performance_schema coleta estatísticas detalhadas e métricas sobre o desempenho do servidor MySQL. Ele monitora consultas, o uso de recursos e outros aspectos que ajudam na identificação e solução de problemas de desempenho.

Exemplo Prático:
Um DBA (Administrador de Banco de Dados) pode usar o performance_schema para identificar gargalos em consultas SQL, ajustando índices e configurações do servidor para otimizar o desempenho.

Exemplo Lúdico:
Pense nele como um treinador esportivo que coleta estatísticas dos jogadores durante um jogo – tempo de resposta, velocidade e eficiência – para depois ajustar a estratégia e melhorar a performance do time.

D) sakila database

O sakila é um banco de dados de exemplo fornecido pelo MySQL. Ele simula um sistema de locadora de filmes, contendo tabelas sobre filmes, atores, clientes e aluguéis, e serve como material didático para praticar comandos e aprender sobre modelagem de dados.

Exemplo Prático:
Instrutores e estudantes de SQL podem utilizar o banco sakila para praticar consultas, junções e modelagem de dados sem a necessidade de criar um banco de dados do zero.

Exemplo Lúdico:
Imagine uma locadora de vídeos fictícia, onde você pode experimentar o gerenciamento de filmes e clientes sem impactar um negócio real – um cenário de prática seguro para aprender e testar novas ideias.

E) sys database

O sys é um banco de dados que reúne informações consolidadas e simplificadas sobre o desempenho e a configuração do MySQL. Ele utiliza os dados coletados pelo performance_schema, apresentando-os de forma mais acessível e amigável para auxiliar no diagnóstico e na administração do sistema.

Exemplo Prático:
Administradores usam o banco sys para visualizar dashboards e relatórios resumidos do estado do servidor, ajudando a identificar rapidamente problemas de performance ou configurações incorretas.

Exemplo Lúdico:
Imagine um painel de controle moderno em um avião, que apresenta os principais indicadores de desempenho (como velocidade, altitude e status dos sistemas), ajudando o piloto a entender rapidamente a condição do voo.

F) world database

O world é outro banco de dados de exemplo que contém informações geográficas sobre países, cidades e idiomas. Ele é frequentemente usado para demonstrar consultas com relacionamentos geográficos e para fins educacionais.

Exemplo Prático:
Estudantes de SQL podem utilizar o banco world para praticar consultas que cruzem dados de países, como listar cidades de um determinado país ou comparar estatísticas entre nações.

Exemplo Lúdico:
Pense no world como um atlas interativo, onde cada país e cidade estão registrados – é como ter um mapa do mundo com detalhes precisos, perfeito para explorar e aprender sobre geografia usando consultas de dados
