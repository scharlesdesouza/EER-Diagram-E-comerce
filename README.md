# Sistema de E-commerce

## 📋 Descrição

Este projeto representa a modelagem de um sistema de e-commerce. O sistema é projetado para gerenciar fornecedores, clientes, produtos, pedidos, pagamentos e entregas de forma eficiente, além de permitir a integração com vendedores terceirizados.

---

## 🛠️ Funcionalidades

1. **Gestão de Fornecedores**:
   - Cadastro de fornecedores com dados de identificação (CNPJ, razão social).
   - Controle de produtos disponibilizados por fornecedores.

2. **Gestão de Vendedores Terceirizados**:
   - Cadastro de vendedores externos que podem ofertar produtos no sistema.

3. **Cadastro de Produtos**:
   - Registro detalhado de produtos, incluindo descrição, valor e quantidade em estoque.
   - Associação de produtos aos fornecedores e vendedores terceirizados.

4. **Gestão de Clientes**:
   - Cadastro de clientes com informações como CPF, endereço, e-mail e telefone.
   - Registro de histórico de pedidos realizados pelos clientes.

5. **Gestão de Pedidos**:
   - Criação de pedidos contendo:
     - Produtos solicitados e respectivas quantidades.
     - Dados do cliente e vendedor associado.
   - Associação dos pedidos aos pagamentos e entregas.

6. **Pagamentos**:
   - Registro de informações de pagamento de cada pedido, incluindo status e valor.

7. **Gestão de Entregas**:
   - Controle das entregas dos pedidos com registro de dados necessários.

---

## 🗂️ Estrutura do Modelo Conceitual

### Entidades Principais:

- **Fornecedor**:
  - `idFornecedor` (PK): Identificador único.
  - `razaoSocial`: Razão social do fornecedor.
  - `CNPJ`: Número do CNPJ.

- **Vendedor Terceirizado**:
  - `idTerceiro` (PK): Identificador único.
  - `razaoSocial`: Razão social do vendedor.
  - `CNPJ`: Número do CNPJ.

- **Produto**:
  - `idProduto` (PK): Identificador único.
  - `descricao`: Descrição detalhada do produto.
  - `valor`: Preço do produto.
  - `quantidadeEstoque`: Quantidade disponível no estoque.
  - Relacionamentos:
    - Pode ser fornecido por fornecedores ou disponibilizado por vendedores terceirizados.

- **Cliente**:
  - `idCliente` (PK): Identificador único.
  - `nome`: Nome completo do cliente.
  - `CPF`: Cadastro de Pessoa Física.
  - `telefone`, `email`: Contatos do cliente.
  - `endereco`: Endereço completo.

- **Pedido**:
  - `idPedido` (PK): Identificador único.
  - `dataPedido`: Data de realização do pedido.
  - Relacionamentos:
    - Associa cliente e os produtos solicitados.

- **Pagamento**:
  - `idPagamento` (PK): Identificador único.
  - `valorPagamento`: Valor total do pedido.
  - `statusPagamento`: Status do pagamento.

- **Entrega**:
  - `idEntrega` (PK): Identificador único.
  - Relacionamento com o pedido para controle do fluxo logístico.

- **Relacionamentos**:
  - **Produtos por Pedido**: Registra quais produtos estão associados a cada pedido e suas quantidades.
  - **Produtos por Fornecedor/Vendedor**: Determina quais fornecedores ou vendedores terceirizados oferecem cada produto.

---
