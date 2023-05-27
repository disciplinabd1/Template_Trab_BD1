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
Neste ponto a codificação não e necessária, somente as ideias de telas devem ser criadas, o princípio aqui é pensar na criação da interface para identificar possíveis informações a serem armazenadas ou descartadas <br>

Sugestão: https://balsamiq.com/products/mockups/<br>

![Alt text](https://github.com/discipbd1/trab01/blob/master/balsamiq.png?raw=true "Title")
![Arquivo PDF do Protótipo Balsamiq feito para Empresa Surfistinha](https://github.com/disciplinabd1/Template_Trab_BD1/blob/master/arquivos/SistemaSurfista_Fernanda_Lorenzo_Maressa_Rafael%20(1).pdf)
![Arquivo PDF do Protótipo Balsamiq feito para Empresa Surfistinha (adimistração)](https://github.com/disciplinabd1/Template_Trab_BD1/blob/master/arquivos/AdmSite.pdf)
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
    
> A Empresa Surfistinha precisa inicialmente dos seguintes relatórios:

* Relatório mostrando todas as pranchas do sistema. O relatório deve mostrar o código da prancha, o modelo e se a prancha está disponível ou alugada.
* Relatório relacionando cliente, modelo de prancha, mostrando qual o modelo mais alugado por cada cliente. O relatório deve conter o nome do cliente, o nome do modelo de prancha mais alugado por ele e o total de vezes que ele alugou o modelo.
* Relatório relacionando cliente e número de locações, o relatório deve conter nome do cliente, telefone e email, além do número de locações feito pelo cliente.
* Relatório mostrando os dados referentes a cada prancha, descrição, comprimento, nome e quantidade de pranchas do referente modelo, além do número de locações de cada modelo.
* Relatório relacionando cliente e o prazo mais utilizado por ele. O relatório deve mostrar o nome do cliente, o número de horas do prazo, e o total de vezes que o cliente requisitou o prazo.
 
 
#### 4.3 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    
![Exemplo de Tabela de dados da Empresa Devcom](https://github.com/discipbd1/trab01/blob/master/arquivos/TabelaEmpresaDevCom_sample.xlsx?raw=true "Tabela - Empresa Devcom")
    
    
### 5.MODELO CONCEITUAL<br>
    A) Utilizar a Notação adequada (Preferencialmente utilizar o BR Modelo 3)
    B) O mínimo de entidades do modelo conceitual pare este trabalho será igual a 3 e o Máximo 5.
        * informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)       
    C) Principais fluxos de informação/entidades do sistema (mínimo 3). <br>Dica: normalmente estes fluxos estão associados as tabelas que conterão maior quantidade de dados 
    D) Qualidade e Clareza
        Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas (Aplicar os conceitos de normalização abordados).   
        
![Alt text](https://github.com/discipbd1/trab01/blob/master/images/Y?raw=true "Modelo Conceitual")
    
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Nomes dos que participaram na avaliação]
    [Grupo02]: [Nomes dos que participaram na avaliação]

#### 5.2 Descrição dos dados 
    2) DETALHAMENTO DE ESPECIFICAÇÃO DAS ENTIDADES E RELACIONAMENTOS

Entidades:<br />

LOGIN: Tabela que armazena informações relacionadas ao login que o cliente usará para logar no Sistema.<br>
Id: Campo que armazena a identificação única do login utilizado pelo cliente.<br>
username: Campo que contém o nome de usuário utilizado pelo cliente para logar no Sistema.<br>
password: Campo que armazena a senha que o cliente usará para logar no sistema.<br>
<br>
CLIENTE: Tabela que armazena os dados dos clientes.  
id: Campo que armazena  a identificação unica do cliente.  
Nome: Campo que armazena o nome do cliente.  
Telefone: Campo que armazena o telefone do Cliente.  
Email: Campo que armazena o email do cliente que vai alocar a prancha.
<br>
CARTAO: Tabela que armazenas as informações referentes ao cartão que o cliente irá usar para efetuar a locação da prancha.<br>
Código: Campo que armazena a identificação única do cartão utilizado para locar as pranchas.<br>
Numero: Campo que armazena o número do cartão.<br>
Bandeira: Campo que armazena a informação da bandeira do cartão.<br>
Data de  validade: Campo que armazena a data da validade da utilização do cartão.<br>
<br>
LOCAÇÃO: Tabela que armazena 
id: Campo que armazena a identificação única da locação.<br>
data_hora: Campo que armazena a informação que contém a data/hora que a locação foi efetivada.<br>

<br />
PRANCHA: Tabela que armazena informações sobre as pranchas que estarão disponíveis para os clientes alugarem.<br>
Código: Campo que armazena a identificação unica da prancha.<br>
Status: Campo que armazena a informação se a prancha está disponível para locação ou não.<br>
Preço: Campo que armazena o valor que será cobrado por hora que a prancha será locada.<br>
 <br>
MODELO_PRANCHA: Tabela que armazena informações sobre quais são os tipos de pranchas que serão disponibilizadas pela loja para locação.<br>
Código: Campo que armazena a identificação única do modelo de prancha.<br>
Descrição: Campo que contem um texto que descreve o Modelo da prancha e suas especificidades.<br>
Comprimento: Campo que contém a informação do tamanho da prancha.<br>
Nome: Campo que armazena o nome da prancha.<br>
Foto: Campo que contem a URL com uma imagem do modelo da prancha.<br>

**Relacionamentos:

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


### 6	MODELO LÓGICO<br>
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas em SQL/DDL 
        (criação de tabelas, alterações, etc..) 
        
       
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físico
        (Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL

###### INSERÇÃO NA TABELA LOGIN_CLIENTE
INSERT INTO login_cliente(id, nome, telefone, email, username, password)<br />
VALUES<br />
(1, 'Raphael Ambrosius Costeau', '27997878387', 'rafinha@gmail.com', 'DumbDoomSpiral', 'DeusEstaMorto123'),<br />
(2, 'Fernanda Jamaira', '27993210213', 'chata@gmail.com', 'fernandaJaimara', 'faz_o_L_13'),<br />
(3, 'Mirosmar Francisco', '27993284533', 'miros@gmail.com', 'mirosmaFran', 'flamengo20'),<br />
(4, 'Luiz Inácio Da Silva', '27998483838', 'lulu@gmail.com', 'luluDaSilva', 'macacoLouco1'),<br />
(5, 'Pedro Pascal', '27994843881', 'joel@gmail.com', 'JoelPascal', 'corintia1000'),<br />
(6, 'Alexandre Fronta', '27998882828', 'lele@gmail.com', 'xandão10', 'xandao100'),<br />
(7, 'Rodrigo Santoro', '27999393999', 'xexes@gmail.com', 'rodriguin6Pack', 'luckyStrike12');<br />

###### INSERÇÃO NA TABELA PRANCHA
INSERT INTO prancha(ID, PRECO, FK_MODELO_PRANCHA_ID)<br />
VALUES(1, 50, 1),<br />
(2, 30, 2),<br />
(3, 50, 3),<br />
(4, 25, 4),<br />
(5, 40, 5),<br />
(6, 40, 6),<br />
(7, 30, 7);<br />
  
###### INSERÇÃO NA TABELA CARTAO
INSERT INTO cartao(id, numero, bandeira,dt_validade, fk_login_cliente_id)<br />
VALUES(1, 1234567891122344, 'VISA', '2024/06/12', 1),<br />
(2,1224347894321239, 'VISA', '2024/08/10', 2),<br />
(3, 9849439975744394, 'Mastercard', '2025/03/02', 3),<br />
(4, 2399349938849398, 'ELO', '2023/11/04', 4),<br />
(5, 2999388839933993, 'ALELO', '2024-05-05', 5),<br />
(6, 2999888888443992, 'Hipercard', '2025-06-07', 6)<br />
(7, 3994843338581039, 'Mastercard', '2024-08-09', 7);<br />
  
###### INSERÇÃO NA TABELA LOCACAO_PRANCHA
INSERT INTO LOCACAO_PRANCHA(ID, TEMPO_LOCACAO, STATUS, FK_LOCACAO_ID, FK_PRANCHA_ID)  
VALUES	(1, 4, 'Alugada', 1, 3),  
(2, 6, 'Alugada', 2, 2),  
(3, 4, 'Disponivel', 3, 1),  
(4, 6, 'Alugada', 4, 5),  
(5, 4, 'Alugada', 6, 4),  
(6, 8, 'Disponivel', 6, 6),  
(7, 8, 'Alugada', 7, 7);  
  
###### INSERÇÃO NA TABELA LOCACAO
INSERT INTO LOCACAO (data_hora,FK_CARTAO_ID) VALUES
('12/06/2023 14:32:43', 2),  
('2023-06-11 16:34:42',	2),  
('2023-07-12 09:01:12',	3),  
('2023-08-09 00:02:45',	5),  
('2023-08-09 13:11:34', 4),  
('2023-09-09 12:33:34',	6),  
('2023-08-04 14:33:43',	7);  

###### INSERÇÃO NA TABELA MODELO_PRANCHA
INSERT INTO MODELO_PRANCHA (nome,descricao,comprimento,foto) VALUES  
('Longboard','É um tipo de prancha de surf caracterizada por sua grande extensão, variando entre 9 e 12 pés de comprimento, e uma largura que geralmente é maior que a de outras pranchas de surf.', 2.9, 'https://s-media-cache-ak0.pinimg.com/originals/fd/82/8d/fd828daf3d8630fe70bc7a9d31701aa7.jpg'),  
('Shortboard','São pranchas menores, indicadas para pessoas que já tem um pouco de experiência no surf.',1.68,'https://th.bing.com/th/id/OIP.X1-ovzrhyQC9BPdwgb5jYQHaHa?pid=ImgDet&rs=1'),  
('Funboard','São as pranchas mais recomendadas para iniciantes no Surf. Possuem bastante área distribuída por toda sua extensão.',2.29,'https://cdn.shopify.com/s/files/1/0206/5056/products/Green_Thumb_2048x.jpg?v=1506107831'),  
('Fish','Essas pranchas são caracterizadas por sua forma única, que apresenta uma largura e volume maior na área do meio da prancha, além de uma rabeta em forma de swallow (andorinha), que é mais larga e curta do que as rabetas tradicionais.',1.63,'https://th.bing.com/th/id/R.2bf47c66a7d1dfa4327a843181f97c75?rik=vBnjsCocFmCtlw&pid=ImgRaw&r=0'),  
('Evolution','É a melhor para aprender a surfar porque é a maior e grossa, além de muito estáveis.',1.83,'https://images.offerup.com/7u6Bx7vTuvHvQ-yVlLnn36R9NM4=/600x800/8eba/8eba4d5873f747d4bc273ebde96d1c58.jpg'),  
('Gun', 'Pranchas maiores e com o bico arredondado que variam de 8 a 12 pés. Por ser bem comprida e pesada, é uma prancha estável e que entra na onda com mais facilidade.',3.05,'https://th.bing.com/th/id/OIP.Dw3Sw1SG-OUWSYWeCogaEgHaHa?pid=ImgDet&rs=1'),  
('Softboard','Uma prancha softboard é uma prancha de surf feita com um núcleo de espuma macia e uma camada superior de material emborrachado, que fornece uma superfície antiderrapante e segura para o surfista ficar em pé. Essas pranchas são especialmente projetadas para iniciantes e surfistas intermediários, que estão aprendendo a surfar ou querem melhorar suas habilidades.',2.74,'https://th.bing.com/th/id/R.a578f11895e66c5045dc2ddf8e862a64?rik=ge07XvUSFls%2f3A&pid=ImgRaw&r=0');  
### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
SELECT * FROM login_cliente  
SELECT * FROM cartao  
SELECT * FROM locacao  
SELECT * FROM prancha  
SELECT * FROM locacao_prancha  
SELECT * FROM modelo_prancha  

># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção

># Marco de Entrega 02: Do item 9.2 até o ítem 9.10<br>

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


