# Desafio de Modelagem de Banco de Dados - Sistema de Clientes e Entregas

## Descrição do Projeto

Este projeto tem como objetivo a modelagem de um banco de dados para gerenciar informações de **clientes** (Pessoa Jurídica e Pessoa Física), **pagamentos** e **entregas**. O modelo foi implementado utilizando **MySQL** e inclui as principais funcionalidades para cadastrar clientes, registrar formas de pagamento e acompanhar o status de entregas.

### Objetivos do Desafio:

- **Cliente**: O sistema deve permitir o cadastro de clientes do tipo Pessoa Jurídica (PJ) ou Pessoa Física (PF). Um cliente não pode ter ambas as informações (PJ e PF) ao mesmo tempo.
- **Pagamento**: O sistema deve permitir o cadastro de múltiplas formas de pagamento para cada cliente (ex: Cartão de Crédito, Boleto, Transferência).
- **Entrega**: A entrega deve ser registrada com um status (Em andamento, Entregue, Cancelado) e um código de rastreio único.

### Estrutura do Banco de Dados

A modelagem de dados foi realizada utilizando um **Diagrama Entidade-Relacionamento (EER)**, que pode ser visualizado através do MySQL Workbench. As principais entidades e seus relacionamentos são:

- **Cliente**: Armazena informações sobre o cliente, com distinção entre Pessoa Física (PF) e Pessoa Jurídica (PJ).
- **Pagamento**: Cada cliente pode ter múltiplos registros de pagamento.
- **Entrega**: Cada cliente pode ter várias entregas associadas, com status e código de rastreio.
