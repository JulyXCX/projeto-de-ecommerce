# Esquema Conceitual de E-commerce

Este projeto representa um esquema conceitual de banco de dados para um sistema de e-commerce. O modelo abrange as principais entidades e relacionamentos, com refinamentos específicos para atender às funcionalidades detalhadas no desafio.

## Entidades e Relacionamentos

### Fornecedor
- Representa os fornecedores dos produtos vendidos na plataforma.
- **Relacionamentos**:
  - Um fornecedor pode fornecer vários produtos (1:N).
  - Cada produto é fornecido por apenas um fornecedor.

### Produto
- Representa os itens disponíveis para venda.
- **Relacionamentos**:
  - Cada produto possui um registro único no estoque (1:1).
  - Um produto pode estar presente em vários pedidos (N:N, resolvido pela entidade associativa **Itens do Pedido**).

### Estoque
- Armazena a quantidade de produtos disponíveis.
- **Relacionamentos**:
  - Cada produto possui um registro único no estoque (1:1).

### Cliente
- Representa os usuários cadastrados, podendo ser **PF** (Pessoa Física) ou **PJ** (Pessoa Jurídica).
- **Relacionamentos**:
  - Um cliente pode realizar vários pedidos (1:N).
  - Um cliente pode cadastrar várias formas de pagamento (1:N).

### Pedido
- Representa as compras realizadas pelos clientes.
- Relacionamentos:
  - Cada pedido pertence a um único cliente (N:1).
  - Um pedido pode conter vários itens (1:N), detalhados por **Itens do Pedido**.
  - Cada pedido possui uma única entrega (1:1).

### Itens do Pedido
- Detalha os produtos incluídos em cada pedido, incluindo quantidade e preço unitário.
- Relacionamentos:
  - Cada item refere-se a um único pedido (N:1).
  - Cada item refere-se a um único produto (N:1).

### Pagamento
- Representa as formas de pagamento cadastradas, como cartão de crédito, débito, boleto e Pix.
- **Relacionamentos**:
  - Cada forma de pagamento pertence a um único cliente (N:1).

### Entrega
- Representa o processo de entrega de um pedido, com informações sobre status e código de rastreio.
- **Relacionamentos**:
  - Cada entrega está associada a um único pedido (1:1).

## Estrutura do Banco de Dados
![EER - Ecommerce - projeto DIO](https://github.com/user-attachments/assets/e898b515-d71b-48fe-9e75-9946404f9f3b)

## Como usar este projeto
1. Clone este repositório:
   ```bash
   git clone <URL_DO_REPOSITORIO>
