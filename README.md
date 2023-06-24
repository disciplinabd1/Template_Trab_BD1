# TRABALHO 01:  Surfistinha
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Fernanda Jaimara do Nascimento:fernandajaimara@gmail.com<br>
Lorenzo Peixoto:lo.peixoto@gmail.com<br>
Maressa Karen Henrique da Silva:khsmaressa@gmail.com<br>
Rafael Machado Souza:rafaelmachadosouza3@gmail.com<br>

### 2.INTRODUÇÃO E MOTIVAÇÃO<br>
Este documento contém a especificação do projeto do banco de dados Surfistinha. 
 
> A empresa "Surfistinha" objetiva providenciar aos surfistas um sistema eficiente e portável de aluguel de pranchas a fim de propiciar uma ótima experiência para os clientes. Várias pessoas querem surfar sem precisar comprar uma prancha e para isso contam com um serviço de aluguel. Para facilitar isso o sistema "surfistinha" proporciona uma interface online entre o cliente e a loja da empresa. Para realizar suas atividades, a empresa necessita de um sistema que armazene informações referentes aos clientes, cartão de crédito, pranchas e seus modelos e a locação das pranchas. O sistema deverá gerar relatórios que forneçam feedback para a gerência da empresa.
 
### 3.MINI-MUNDO<br>

Descrição do mini-mundo!

> Um cliente deseja um sistema onde possa alugar suas pranchas de forma online, nesse sistema uma prancha só pode ser alugada para um único cliente. Cada prancha não deve estar associada diretamente ao cliente e sim a locação. Uma locação pode comportar uma ou várias pranchas. Cada cliente pode ter um  ou vários cartões de crédito cadastrados, mas cada cartão só pode estar associado a um cliente. Por fim, cada cliente deve estar associado somente a uma única identificação de login, e o login deve ser exclusivo deste cliente. Cada LOCAÇÃO deve estar relacionada apenas a um único cartão de um determinado cliente (pois o sistema só permite compras por meio de cartão). Do CLIENTE devemos registrar as informações de código, nome, telefone e e-mail, já com relação a cada PRANCHA devemos registrar o código, status, nome e preço, cada prancha também deve ter um modelo e esse modelo precisa ter descrição e comprimento.  Com relação a cada CARTÃO devemos saber o número , bandeira e data de validade e o momento que o cartão foi inserido no sistema.  Sobre cada  LOCAÇÃO deve-se registrar um código, data/hora e tempo de locação da prancha. Com relação aos dados de LOGIN deve-se armazenar o username e password de cada usuário (mas estes não devem ser chaves de login). 

### 4.PROTOTIPAÇÃO, PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>

#### 4.1 RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>


![Alt text](https://github.com/disciplinabd1/Template_Trab_BD1/blob/master/images/prototipo_bd1.png?raw=true "Title")

![Arquivo PDF do Protótipo Balsamiq feito para Empresa Surfistinha](https://github.com/disciplinabd1/Template_Trab_BD1/blob/master/arquivos/SistemaSurfista_Fernanda_Lorenzo_Maressa_Rafael%20(1).pdf)
![Arquivo PDF do Protótipo Balsamiq feito para Empresa Surfistinha (adimistração)](https://github.com/disciplinabd1/Template_Trab_BD1/blob/master/arquivos/AdmSite.pdf)


#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
 
> A Empresa Surfistinha precisa inicialmente dos seguintes relatórios:

    * Relatório mostrando todas as pranchas do sistema. O relatório deve mostrar o código da prancha, o modelo e se a prancha está disponível ou alugada.
    * Relatório relacionando cliente, modelo de prancha, mostrando qual o modelo mais alugado por cada cliente. O relatório deve conter o nome do cliente, o nome do modelo de prancha mais alugado por ele e o total de vezes que ele alugou o modelo.
    * Relatório relacionando cliente e número de locações, o relatório deve conter nome do cliente, telefone e email, além do número de locações feito pelo cliente.
    * Relatório mostrando os dados referentes a cada prancha, descrição, comprimento, nome e quantidade de pranchas do referente modelo, além do número de locações de cada modelo.
    * Relatório relacionando cliente e o prazo mais utilizado por ele. O relatório deve mostrar o nome do cliente, o número de horas do prazo, e o total de vezes que o cliente requisitou o prazo.
 
 
#### 4.3 TABELA DE DADOS DO SISTEMA:
    
![Tabela de dados da Empresa Surfistinha](https://github.com/disciplinabd1/Template_Trab_BD1/blob/master/arquivos/Trabalho_BD1_tabela_de_dados.xlsx?raw=true "Tabela - Empresa Surfistinha")
    
    
### 5.MODELO CONCEITUAL<br>
        
![Alt text](https://github.com/disciplinabd1/Template_Trab_BD1/blob/master/images/modeloConceitual.png?raw=true "Modelo Conceitual")
    
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Micaely e Kailany]
    - login e cliente estao com a ordem invertida (ACATADO)
    - cliente poderia ser facilmente integrado com login, os atributos de login podia fazer parte de cliente (NÃO ACATADO)
    
    [Grupo02]: [Perseu]
    - Adicionar um ramo de cliente para locação, deixando claro a locação feita pelo cliente (NÃO ACATADO)


#### 5.2 Descrição dos dados 
    2) DETALHAMENTO DE ESPECIFICAÇÃO DAS ENTIDADES E RELACIONAMENTOS

    ##Entidades:

    LOGIN: Tabela que armazena informações relacionadas ao login que o cliente usará para logar no Sistema.
    Id: Campo que armazena a identificação única do login utilizado pelo cliente.
    username: Campo que contém o nome de usuário utilizado pelo cliente para logar no Sistema.
    password: Campo que armazena a senha que o cliente usará para logar no sistema.
    
    CLIENTE: Tabela que armazena os dados dos clientes.  
    id: Campo que armazena  a identificação unica do cliente.  
    Nome: Campo que armazena o nome do cliente.  
    Telefone: Campo que armazena o telefone do Cliente.  
    Email: Campo que armazena o email do cliente que vai alocar a prancha.
    
    CARTAO: Tabela que armazenas as informações referentes ao cartão que o cliente irá usar para efetuar a locação da prancha.
    id: Campo que armazena a identificação única do cartão utilizado para locar as pranchas.
    Numero: Campo que armazena o número do cartão.
    Bandeira: Campo que armazena a informação da bandeira do cartão.
    Data de  validade: Campo que armazena a data da validade da utilização do cartão.
    
    LOCAÇÃO: Tabela que armazena 
    id: Campo que armazena a identificação única da locação.
    data_hora: Campo que armazena a informação que contém a data/hora que a locação foi efetivada.
    
    PRANCHA: Tabela que armazena informações sobre as pranchas que estarão disponíveis para os clientes alugarem.
    id: Campo que armazena a identificação unica da prancha.
    Status: Campo que armazena a informação se a prancha está disponível para locação ou não.
    Preço: Campo que armazena o valor que será cobrado por hora que a prancha será locada.
    
    MODELO_PRANCHA: Tabela que armazena informações sobre quais são os tipos de pranchas que serão disponibilizadas pela loja para locação.
    id: Campo que armazena a identificação única do modelo de prancha.
    Descrição: Campo que contem um texto que descreve o Modelo da prancha e suas especificidades.
    Comprimento: Campo que contém a informação do tamanho da prancha.
    Nome: Campo que armazena o nome da prancha.<br>
    Foto: Campo que contem a URL com uma imagem do modelo da prancha.<br>

    ##Relacionamentos:

    Efetua(Cliente/Login)
    Ao se cadastrar no site o cliente efetuará um login.
    Um login só pode estar relacionado a um cliente.

    Possui(Cliente/Cartão)
    Um cliente pode ter um ou vários cartões cadastrados
    Um cartão é associado a um cliente

    Possibilita(Cartão/Locação): 
    Um cartão possibilita a locação das pranchas. 
    Para conseguir finalizar uma locação o cliente precisa ter um cartão.

    Loca(Locação/Prancha)
    Cada locação pode ter uma ou várias pranchas.
    Cada prancha pode estar relacionada a uma locação.

    Possui(Prancha/Modelo Prancha)
    Uma prancha é associada a um modelo de prancha.
    Um modelo de prancha pode estar associado a várias pranchas.


### 6.MODELO LÓGICO<br>

![Alt text](https://github.com/disciplinabd1/Template_Trab_BD1/blob/master/images/modelo-logico-bd1.jpeg?raw=true "Modelo Lógico")


### 7.MODELO FÍSICO<br>

     CREATE TABLE LOGIN_CLIENTE(
      ID SERIAL PRIMARY KEY,
      NOME VARCHAR(80),
      TELEFONE VARCHAR(15),
      EMAIL VARCHAR(50),
      USERNAME VARCHAR(15),
      PASSWORD VARCHAR(30)
     );

     CREATE TABLE CARTAO(
      ID SERIAL PRIMARY KEY,
      NUMERO BIGINT,
      BANDEIRA VARCHAR(15),
      DT_VALIDADE DATE,
      FK_LOGIN_CLIENTE_ID INTEGER,
      FOREIGN KEY(FK_LOGIN_CLIENTE_ID)REFERENCES LOGIN_CLIENTE(ID)
     );

     CREATE TABLE LOCACAO(
      ID SERIAL PRIMARY KEY,
      DATA_HORA TIMESTAMP,
      FK_CARTAO_ID INTEGER,
      FOREIGN KEY(FK_CARTAO_ID) REFERENCES CARTAO(ID)
     );

     CREATE TABLE MODELO_PRANCHA(
      ID SERIAL PRIMARY KEY,
      DESCRICAO VARCHAR(400),
      COMPRIMENTO REAL,
      NOME VARCHAR(30),
      FOTO VARCHAR(200)
     );

     CREATE TABLE PRANCHA(
      ID SERIAL PRIMARY KEY,
      PRECO REAL,
      FK_MODELO_PRANCHA_ID INTEGER,
      FOREIGN KEY(FK_MODELO_PRANCHA_ID) REFERENCES MODELO_PRANCHA(ID)
     );


     CREATE TABLE LOCACAO_PRANCHA (
       ID SERIAL PRIMARY KEY,
       FK_PRANCHA_ID INTEGER,
       FK_LOCACAO_ID INTEGER,
       TEMPO_LOCACAO INTEGER,
       FOREIGN KEY (FK_PRANCHA_ID) REFERENCES PRANCHA (ID),
       FOREIGN KEY (FK_LOCACAO_ID) REFERENCES LOCACAO (ID)
     );


       
### 8.INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>


    ---- INSERÇÃO NA TABELA LOGIN_CLIENTE ----
    INSERT INTO login_cliente(id, nome, telefone, email, username, password)
    VALUES
    (1, 'Raphael Ambrosius Costeau', '27997878387', 'rafinha@gmail.com', 'DumbDoomSpiral', 'DeusEstaMorto123'),
    (2, 'Fernanda Jamaira', '27993210213', 'chata@gmail.com', 'fernandaJaimara', 'faz_o_L_13'),
    (3, 'Mirosmar Francisco', '27993284533', 'miros@gmail.com', 'mirosmaFran', 'flamengo20'),
    (4, 'Luiz Inácio Da Silva', '27998483838', 'lulu@gmail.com', 'luluDaSilva', 'macacoLouco1'),
    (5, 'Pedro Pascal', '27994843881', 'joel@gmail.com', 'JoelPascal', 'corintia1000'),
    (6, 'Alexandre Fronta', '27998882828', 'lele@gmail.com', 'xandão10', 'xandao100'),
    (7, 'Rodrigo Santoro', '27999393999', 'xexes@gmail.com', 'rodriguin6Pack', 'luckyStrike12');

    ---- INSERÇÃO NA TABELA PRANCHA ----
    INSERT INTO prancha(ID, PRECO, FK_MODELO_PRANCHA_ID)
    VALUES(1, 50, 1),
    (2, 30, 2),
    (3, 50, 3),
    (4, 25, 4),
    (5, 40, 5),
    (6, 40, 6),
    (7, 30, 7);

    ---- INSERÇÃO NA TABELA CARTAO ----
    INSERT INTO cartao(id, numero, bandeira,dt_validade, fk_login_cliente_id)
    VALUES(1, 1234567891122344, 'VISA', '2024/06/12', 1),
    (2,1224347894321239, 'VISA', '2024/08/10', 2),
    (3, 9849439975744394, 'Mastercard', '2025/03/02', 3),
    (4, 2399349938849398, 'ELO', '2023/11/04', 4),
    (5, 2999388839933993, 'ALELO', '2024-05-05', 5),
    (6, 2999888888443992, 'Hipercard', '2025-06-07', 6),
    (7, 3994843338581039, 'Mastercard', '2024-08-09', 7);

    ---- INSERÇÃO NA TABELA LOCACAO_PRANCHA ----
    INSERT INTO LOCACAO_PRANCHA(ID, TEMPO_LOCACAO, STATUS, FK_LOCACAO_ID, FK_PRANCHA_ID)  
    VALUES	(1, 4, 'Alugada', 1, 3),  
    (2, 6, 'Alugada', 2, 2),  
    (3, 4, 'Disponivel', 3, 1),  
    (4, 6, 'Alugada', 4, 5),  
    (5, 4, 'Alugada', 6, 4),  
    (6, 8, 'Disponivel', 6, 6),  
    (7, 8, 'Alugada', 7, 7);  

    ---- INSERÇÃO NA TABELA LOCACAO ----
    INSERT INTO LOCACAO (data_hora,FK_CARTAO_ID) VALUES<br>
    ('12/06/2023 14:32:43', 2),
    ('2023-06-11 16:34:42',	2),
    ('2023-07-12 09:01:12',	3),
    ('2023-08-09 00:02:45',	5),
    ('2023-08-09 13:11:34', 4),
    ('2023-09-09 12:33:34',	6),
    ('2023-08-04 14:33:43',	7);

    ---- INSERÇÃO NA TABELA MODELO_PRANCHA ----
    INSERT INTO MODELO_PRANCHA (nome,descricao,comprimento,foto) VALUES<br>
    ('Longboard','É um tipo de prancha de surf caracterizada por sua grande extensão, variando entre 9 e 12 pés de comprimento, e uma largura que geralmente é maior que a de outras pranchas de surf.', 2.9, 'https://s-media-cache-ak0.pinimg.com/originals/fd/82/8d/fd828daf3d8630fe70bc7a9d31701aa7.jpg'),
    ('Shortboard','São pranchas menores, indicadas para pessoas que já tem um pouco de experiência no surf.',1.68,'https://th.bing.com/th/id/OIP.X1-ovzrhyQC9BPdwgb5jYQHaHa?pid=ImgDet&rs=1'),
    ('Funboard','São as pranchas mais recomendadas para iniciantes no Surf. Possuem bastante área distribuída por toda sua extensão.',2.29,'https://cdn.shopify.com/s/files/1/0206/5056/products/Green_Thumb_2048x.jpg?v=1506107831'),
    ('Fish','Essas pranchas são caracterizadas por sua forma única, que apresenta uma largura e volume maior na área do meio da prancha, além de uma rabeta em forma de swallow (andorinha), que é mais larga e curta do que as rabetas tradicionais.',1.63,'https://th.bing.com/th/id/R.2bf47c66a7d1dfa4327a843181f97c75?rik=vBnjsCocFmCtlw&pid=ImgRaw&r=0'),
    ('Evolution','É a melhor para aprender a surfar porque é a maior e grossa, além de muito estáveis.',1.83,'https://images.offerup.com/7u6Bx7vTuvHvQ-yVlLnn36R9NM4=/600x800/8eba/8eba4d5873f747d4bc273ebde96d1c58.jpg'),
    ('Gun', 'Pranchas maiores e com o bico arredondado que variam de 8 a 12 pés. Por ser bem comprida e pesada, é uma prancha estável e que entra na onda com mais facilidade.',3.05,'https://th.bing.com/th/id/OIP.Dw3Sw1SG-OUWSYWeCogaEgHaHa?pid=ImgDet&rs=1'),
    ('Softboard','Uma prancha softboard é uma prancha de surf feita com um núcleo de espuma macia e uma camada superior de material emborrachado, que fornece uma superfície antiderrapante e segura para o surfista ficar em pé. Essas pranchas são especialmente projetadas para iniciantes e surfistas intermediários, que estão aprendendo a surfar ou querem melhorar suas habilidades.',2.74,'https://th.bing.com/th/id/R.a578f11895e66c5045dc2ddf8e862a64?rik=ge07XvUSFls%2f3A&pid=ImgRaw&r=0');

 
### 9.TABELAS E PRINCIPAIS CONSULTAS<br>
    
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
https://colab.research.google.com/drive/1KcrMp_ruP2bqOZ3ssEwCbaCR5fvNI2QI#scrollTo=fKv8IJkLpVQG

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>

https://colab.research.google.com/drive/1KcrMp_ruP2bqOZ3ssEwCbaCR5fvNI2QI#scrollTo=gMAg-NgZroW-

#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)

**Consuta 1: Retorna dados dos cartões da bandeira Mastercard com vencimento depois de 2024.**

    SELECT *
    FROM CARTAO
    WHERE BANDEIRA = 'Mastercard' AND DT_VALIDADE > '2024-12-31';
    
**Consulta 2: Retorna as locações com status disponivel ou tempo de locação menor que 4.**

    SELECT *
    FROM LOCACAO_PRANCHA
    WHERE STATUS = 'Disponivel' OR TEMPO_LOCACAO < 5;
   
**Consulta 3: Retorna os itens que não estão disponíveis.**

    SELECT *
    FROM LOCACAO_PRANCHA
    WHERE NOT STATUS = 'Disponivel';
   
**Consulta 4: Retorna todos os registros da tabela CARTAO onde a bandeira é 'VISA' e a data de validade é posterior a 1º de janeiro de 2024, ou a bandeira é 'Mastercard' e a data de validade não é posterior a 1º de janeiro de 2025.**

    SELECT *
    FROM CARTAO
    WHERE (BANDEIRA = 'VISA' AND DT_VALIDADE >= '2024-01-01') OR (BANDEIRA = 'Mastercard' AND NOT DT_VALIDADE >= '2025-01-01');
  
**Consulta 5: Retorna os itens de MODELO_PRANCHA que tem um comprimento entre 2.5 a 3 ou que o nome termina com "board".**

    SELECT *
    FROM MODELO_PRANCHA
    WHERE (COMPRIMENTO >= 2.5 AND COMPRIMENTO <= 3.0) OR (NOME LIKE '%board');

**Consulta 6: Retorna as colunas ID e PRECO e renomeia o resultado como PRECO_AUMENTADO adicionando mais 10 em todos os itens.**

    SELECT ID, PRECO, PRECO + 10 AS PRECO_AUMENTADO
    FROM PRANCHA;
    
**Consulta 7: Retorna as colunas de ID e PRECO e renomeia o resultado como PRECO_REDUZIDO dinuido 5 de todos os itens**

    SELECT ID, PRECO, PRECO - 5 AS PRECO_REDUZIDO
    FROM PRANCHA;
    
 **Consulta 8: Retorna os itens que tem o tempo de locação multiplicado por 2 maior que 8 e o status como 'Alugado'**
 
    SELECT *
    FROM LOCACAO_PRANCHA
    WHERE TEMPO_LOCACAO * 2 > 8 AND STATUS = 'Alugada';
    
 **Consulta 9: Renomeia o ID como Identificador e o PRECO como PrecoUnitario.**
 
    SELECT ID AS Identificador, PRECO AS PrecoUnitario
    FROM PRANCHA;
    
 **Consulta 10: Selecionamos ID e PRECO da tabela PRANCHA e renomeamos a tabela MODELO_PRANCHA para 'M' e depois renomeamos a coluna NOME para 'nomeModelo'**
 
    SELECT P.ID, P.PRECO, M.NOME AS NomeModelo
    FROM PRANCHA P
    JOIN MODELO_PRANCHA M ON P.FK_MODELO_PRANCHA_ID = M.ID;
    
 **Consulta 11: Selecionamos o campo TEMPO_LOCACAO da tabela LOCACAO_PRANCHA e o campo PRECO da tabela PRANCHA depois renomeamos a tabela LOCACAO_PRANCHA para "LP" e o campo TEMPO_LOCACAO para "Tempo". Renomeamos também a tabela PRANCHA para "P" e o campo PRECO para "Valor" na seleção.**
 
    SELECT LP.TEMPO_LOCACAO AS Tempo, P.PRECO AS Valor
    FROM LOCACAO_PRANCHA LP
    JOIN PRANCHA P ON LP.FK_PRANCHA_ID = P.ID;
    

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização
https://colab.research.google.com/drive/1KcrMp_ruP2bqOZ3ssEwCbaCR5fvNI2QI#scrollTo=P4Q1vfLH2nAi

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    
    
**Consulta 1: Retorna o nome e o número do cartão de todos os clientes, ordenados pelo nome do cliente em ordem alfabética.**

     SELECT lc.NOME, c.NUMERO 
     FROM LOGIN_CLIENTE lc 
     INNER JOIN CARTAO c ON lc.ID = c.FK_LOGIN_CLIENTE_ID 
     ORDER BY lc.NOME ASC;

**Consulta 2: Retorna o nome e o preço de todas as pranchas, ordenadas pelo preço em ordem decrescente.**

     SELECT mp.NOME, p.PRECO
     FROM MODELO_PRANCHA mp
     NNER JOIN PRANCHA p ON mp.ID = p.FK_MODELO_PRANCHA_ID
     ORDER BY p.PRECO DESC;
     
**Consulta 3: Retorna o nome do cliente, o número do cartão e a data de locação, ordenados pela data de locação em ordem crescente.**

     SELECT lc.NOME, c.NUMERO, l.DATA_HORA
     FROM LOGIN_CLIENTE lc
     INNER JOIN CARTAO c ON lc.ID = c.FK_LOGIN_CLIENTE_ID
     INNER JOIN LOCACAO l ON c.ID = l.FK_CARTAO_ID
     ORDER BY l.DATA_HORA ASC;
          
**Consulta 4: Retorna o nome do cliente, número do cartão, nome da prancha e a data de locação para as locações que foram realizadas após uma determinada data, ordenadas pela data de locação em ordem decrescente.**

     SELECT lc.NOME, c.NUMERO, mp.NOME, l.DATA_HORA
     FROM LOGIN_CLIENTE lc
     INNER JOIN CARTAO c ON lc.ID = c.FK_LOGIN_CLIENTE_ID
     INNER JOIN LOCACAO l ON c.ID = l.FK_CARTAO_ID
     INNER JOIN LOCACAO_PRANCHA lp ON l.ID = lp.FK_LOCACAO_ID
     INNER JOIN PRANCHA p ON lp.FK_PRANCHA_ID = p.ID
     INNER JOIN MODELO_PRANCHA mp ON p.FK_MODELO_PRANCHA_ID = mp.ID
     WHERE l.DATA_HORA > '2023-06-01'
     ORDER BY l.DATA_HORA DESC;
     
**Consulta 5: Retorna todas as informações de locações ativas, incluindo o nome do cliente, número do cartão, nome da prancha, data de locação e tempo de locação.**

     SELECT lc.NOME AS nome_cliente, c.NUMERO AS numero_cartao, mp.NOME AS nome_prancha, l.DATA_HORA, lp.TEMPO_LOCACAO
     FROM LOGIN_CLIENTE lc
     INNER JOIN CARTAO c ON lc.ID = c.FK_LOGIN_CLIENTE_ID
     INNER JOIN LOCACAO l ON c.ID = l.FK_CARTAO_ID
     INNER JOIN LOCACAO_PRANCHA lp ON l.ID = lp.FK_LOCACAO_ID
     INNER JOIN PRANCHA p ON lp.FK_PRANCHA_ID = p.ID
     INNER JOIN MODELO_PRANCHA mp ON p.FK_MODELO_PRANCHA_ID = mp.ID
     WHERE lp.STATUS = 'Alugada';
     
**Consulta 6: Retorna o nome do cliente e a data de locação para todas as locações ordenadas pelo nome do cliente em ordem alfabética.**

     SELECT lc.NOME, l.DATA_HORA
     FROM LOGIN_CLIENTE lc
     INNER JOIN CARTAO c ON lc.ID = c.FK_LOGIN_CLIENTE_ID
     ORDER BY lc.NOME ASC;
     
#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção
https://colab.research.google.com/drive/1KcrMp_ruP2bqOZ3ssEwCbaCR5fvNI2QI#scrollTo=R6CSq8BvrwtD

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>

**VIEW 1: Essa VIEW seleciona as colunas ID, NOME, DESCRICAO, COMPRIMENTO e STATUS, mostrando os modelos das pranchas e se estão disponíveis para locação. Utiliza-se um LEFT JOIN entre a tabela MODELO_PRANCHA e as tabelas PRANCHA e LOCACAO_PRANCHA para verificar se existe uma prancha associada ao modelo e se essa prancha não está alugada.**

    CREATE VIEW vw_pranchasDisponiveis AS
    SELECT mp.ID, mp.NOME, mp.DESCRICAO, mp.COMPRIMENTO, lp.STATUS
    FROM MODELO_PRANCHA mp
    LEFT JOIN PRANCHA p ON mp.ID = p.FK_MODELO_PRANCHA_ID
    LEFT JOIN LOCACAO_PRANCHA lp ON p.ID = lp.FK_PRANCHA_ID
    WHERE (lp.STATUS IS NULL OR lp.STATUS <> 'Alugada');
    
  Consulta:
    
    SELECT *
    FROM vw_pranchasDisponiveis;
    
 **VIEW 2: Retorna as locações ativas de pranchas, incluindo o ID, tempo de locação, status, data e hora da locação, e nome do modelo da prancha. Ela é construída através de junções INNER JOIN entre as tabelas LOCACAO_PRANCHA, LOCACAO, PRANCHA e MODELO_PRANCHA, onde são relacionados os IDs correspondentes. Além disso, é aplicado um filtro para mostrar apenas as locações com status 'Alugada'.**
 
    CREATE VIEW vw_locacoes_ativas AS
    SELECT lp.ID, lp.TEMPO_LOCACAO, lp.STATUS, l.DATA_HORA, m.NOME AS MODELO_PRANCHA
    FROM LOCACAO_PRANCHA lp
    INNER JOIN LOCACAO l ON lp.FK_LOCACAO_ID = l.ID
    INNER JOIN PRANCHA p ON lp.FK_PRANCHA_ID = p.ID
    INNER JOIN MODELO_PRANCHA m ON p.FK_MODELO_PRANCHA_ID = m.ID
    WHERE lp.STATUS = 'Alugada';
    
  Consulta:
  
    SELECT *
    FROM vw_locacoes_ativas;
    
**VIEW 3: Nesta VIEW, é realizada uma junção INNER JOIN entre as tabelas LOGIN_CLIENTE e CARTAO, relacionando os registros através do ID do cliente através da coluna FK_LOGIN_CLIENTE_ID. O comando WHERE filtra os registros com data de validade até 2024.**

    CREATE VIEW vw_cartoesValidadeAcabando AS
    SELECT lc.NOME, c.BANDEIRA, c.DT_VALIDADE
    FROM LOGIN_CLIENTE lc
    INNER JOIN CARTAO c ON lc.ID = c.FK_LOGIN_CLIENTE_ID
    WHERE c.DT_VALIDADE <= '2024-12-31';
    
  Consulta:
  
    SELECT *
    FROM vw_cartoesValidadeAcabando;
    
**VIEW 4: Nesta VIEW, usamos a junção LEFT JOIN entre as tabelas LOGIN_CLIENTE e LOCACAO, relacionando os registros através da coluna FK_CARTAO_ID. O comando GROUP BY agrupa os registros pelo nome da pessoa. A função COUNT() é utilizada para contar o número de locações realizadas por cada pessoa.**

    CREATE VIEW vw_totalLocacoes AS
    SELECT lc.NOME, COUNT(l.ID) AS TOTAL_LOCACOES
    FROM LOGIN_CLIENTE lc
    LEFT JOIN LOCACAO l ON lc.ID = l.FK_CARTAO_ID
    GROUP BY lc.NOME;
    
  Consulta:
  
    SELECT *
    FROM vw_TotalLocacoes;
    
**VIEW 5: Realizamos junções INNER JOIN entre as tabelas LOGIN_CLIENTE, CARTAO, LOCACAO e LOCACAO_PRANCHA para obter as informações dos clientes, cartões, locações e locações de prancha. A cláusula WHERE é usada para filtrar apenas os registros com tempo de locação igual ou menor que 4.**

    CREATE VIEW vw_clientes_tempo_locacao AS
    SELECT lc.NOME, lc.TELEFONE, lc.EMAIL
    FROM LOGIN_CLIENTE lc
    INNER JOIN CARTAO c ON lc.ID = c.FK_LOGIN_CLIENTE_ID
    INNER JOIN LOCACAO l ON c.ID = l.FK_CARTAO_ID
    INNER JOIN LOCACAO_PRANCHA lp ON l.ID = lp.FK_LOCACAO_ID
    WHERE lp.TEMPO_LOCACAO <= 4;
  
  Consulta: 
 
    SELECT *
    FROM vw_clientes_tempo_locacao;
  
**VIEW 6: Realizamos um INNER JOIN entre as tabelas MODELO_PRANCHA e PRANCHA para obter as informações do nome do modelo da prancha e o preço correspondente. .**

    CREATE VIEW vw_pranchaPreco AS
    SELECT mp.NOME AS MODELO_PRANCHA, p.PRECO
    FROM MODELO_PRANCHA mp
    INNER JOIN PRANCHA p ON mp.ID = p.FK_MODELO_PRANCHA_ID;
    
  Consulta:
  
    SELECT *
    FROM vw_pranchaPreco;
    

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção
     
**Subconsulta 1: Retorna o nome dos clientes que possuem uma locação ativa.**
       
**Subconsulta 2: Retorna Subconsulta para obter o número de pranchas disponíveis para locação.**
       
**Subconsulta 3: Retorna o número de locações ativas por cliente.**

**Subconsulta 4: Retorna o nome dos clientes que alugaram pranchas e a média de tempo de locação por cliente.**



### 10 RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 03: Itens 10 e 11<br>
<br>
<br>




### 12 FORMATACAO NO GIT:<br> 
https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
    
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/
#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

    
### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


