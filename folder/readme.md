# DESAFIO DIO - Refinando um Projeto Conceitual de Banco de Dados - E-COMMERCE

### Descrição:
O esquema deverá ser adicionado a um repositório do Github para futura avaliação do desafio de projeto. Adicione ao Readme a descrição do projeto conceitual para fornecer o contexto sobre seu esquema.

### Objetivo: 
Refine o modelo apresentado acrescentando os seguintes pontos:

* Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações  
* Pagamento – Pode ter cadastrado mais de uma forma de pagamento  
* Entrega – Possui status e código de rastreio;


## O que foi feito por mim?


Este é o Modelo Entidade-Relacionamento (MER) feito para o banco de dados da nossa loja fictícia de E-Commerce. O MER, como ensinado pela Juliana, é uma representação gráfica das entidades (tabelas) do banco de dados e seus relacionamentos. Esse modelo foi criado para fornecer uma visão abrangente das principais entidades do sistema e como elas se relacionam entre si.

#### Entidades descritas no modelo:
* Cliente: Representa os clientes registrados em nossa loja virtual. Cada cliente possui informações pessoais, como nome, e-mail e endereço, e também possui um identificador único chamado de "cliente_id".   
* Produto: Essa entidade contém informações sobre os produtos oferecidos em nossa loja. Cada produto é identificado por um "produto_id" exclusivo e possui atributos como nome, descrição, preço e estoque.  
* Pedido: A entidade "Pedido" registra todas as transações de compra realizadas pelos clientes. Cada pedido é identificado por um "pedido_id" único e contém informações sobre a data da compra, status de entrega e o total da compra.  
* Entrega: Essa entidade armazena informações sobre o processo de entrega dos pedidos. Cada entrega está vinculada a um pedido e possui dados como o código de rastreamento, endereço de entrega e data estimada de entrega.  
* Transportadora: Representa as empresas de transporte que fornecem serviços de entrega para nossos pedidos. Cada transportadora é identificada por um "transportadora_id" exclusivo e possui informações como nome, CNPJ e telefone de contato.  

#### Relacionamentos:
* Cliente -> Pedido: Cada cliente pode realizar vários pedidos na loja. Essa relação é representada pelo relacionamento um-para-muitos entre as entidades "Cliente" e "Pedido". Um cliente pode estar associado a vários pedidos, mas cada pedido pertence a apenas um cliente.

* Pedido -> Produto: Cada pedido é composto por vários produtos. Essa relação é representada pelo relacionamento muitos-para-muitos entre as entidades "Pedido" e "Produto". Um pedido pode conter vários produtos, e um produto pode estar presente em vários pedidos.

* Pedido -> Entrega: Cada pedido está associado a uma entrega. Essa relação é representada pelo relacionamento um-para-um entre as entidades "Pedido" e "Entrega". Cada pedido tem uma única entrega relacionada a ele, e cada entrega está vinculada a apenas um pedido.

* Entrega -> Transportadora: Cada entrega é realizada por uma transportadora. Essa relação é representada pelo relacionamento muitos-para-um entre as entidades "Entrega" e "Transportadora". Várias entregas podem ser realizadas por uma mesma transportadora, mas cada entrega está vinculada a apenas uma transportadora.
