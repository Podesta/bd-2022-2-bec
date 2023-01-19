## [Tópico T29] - Modelo Entidade Relacionamento (MER) - DB Delivery: Requisitos de dados
###### *by Prof. Plinio Sa Leitao-Junior (INF/UFG)*

### Perfis de interesse (user profiles)

Cliente
Fornecedor
Entregador
Financeira

### Demanda Informacional

#### Cliente

1. Quais os métodos de pagamento?
1. Quais os fornecedores para certa categoria de produtos?
1. Quais as categorias de produtos?
1. Qual o tempo previsto para a entrega de certo pedido?
1. Quais fornecedores de certa categoria de produtos recebem pedidos em certo horário?
1. Quais os cupons de desconto disponíveis para certos fornecedores?
1. Quais os fornecedores com entrega grátis?
1. Quais as avaliações de um certo fornecedor?

#### Fornecedor

1. Quais os produtos disponíveis para entrega?
1. Quais as avaliações dos mesus clientes?
1. Qual o faturamento em certo período?
1. Que entregas foram realizadas dentro do tempo previsto?
1. Quais bairros com maior volume de entregas?
1. Qual a 

#### Entregador




Necessidade de divisão de entidades como entregador, restaurante, alimento, rotas, usuários, pagamentos, envios.
Necessidade de escolha de qual modelagem faz mais sentido visto que o sistema tem algumas prioridades como velocidade do banco e suas queries, necessidade de integridade de dados, necessidade de auditoria para conseguir ter informações de quem enviou para quem e o que enviou de forma fácil. Além de precisar lidar com algumas peculiaridades de geolocalização que dependendo de como feitas podem dar dor de cabeça.
