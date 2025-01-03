# OficinaGerenciamentoOS

## Descrição do Projeto

Este projeto é um esquema de banco de dados desenvolvido para gerenciar ordens de serviço (OS) em uma oficina mecânica. O sistema é projetado para registrar clientes, veículos, mecânicos, equipes, serviços, peças e as ordens de serviço em execução, fornecendo uma base estruturada e otimizada para as operações de gerenciamento.

O banco de dados foi modelado para atender às necessidades descritas no desafio, considerando todos os detalhes da narrativa fornecida.

---

## Estrutura do Banco de Dados

O banco de dados contém as seguintes tabelas principais:

### Tabelas
1. **Cliente**: Armazena informações dos clientes da oficina.
2. **Veículo**: Registra os veículos trazidos pelos clientes.
3. **Mecânico**: Contém dados dos mecânicos e suas especialidades.
4. **Equipe**: Representa equipes de mecânicos responsáveis pela execução das ordens de serviço.
5. **Mecanico_Equipe**: Relacionamento entre mecânicos e equipes.
6. **Serviço**: Lista os serviços disponíveis, com valores de mão de obra associados.
7. **Peça**: Registra as peças disponíveis, com seus respectivos valores.
8. **Ordem_Serviço**: Contém os dados principais das ordens de serviço, como status e valores totais.
9. **Servico_OS**: Relaciona serviços a ordens de serviço, incluindo quantidade.
10. **Peca_OS**: Relaciona peças a ordens de serviço, incluindo quantidade.

---

## Relacionamentos

- **Cliente** (1:N) **Veículo**  
- **Veículo** (1:N) **Ordem_Serviço**  
- **Equipe** (1:N) **Ordem_Serviço**  
- **Equipe** (N:M) **Mecânico**  
- **Ordem_Serviço** (N:M) **Serviço**  
- **Ordem_Serviço** (N:M) **Peça**

---

## Scripts do Projeto

- ```schema.sql```: Script SQL para criação do banco de dados e tabelas.
- ```README.md```: Este documento explicando a estrutura e os objetivos do projeto.

---

## Como Utilizar

1. Clone o repositório:
   ```
   git clone https://github.com/seu-usuario/OficinaGerenciamentoOS.git
   ```
2. Importe o arquivo ```schema.sql``` no seu sistema de banco de dados:
   ```
   mysql -u usuario -p < schema.sql
   ```
3. Configure e teste o banco de dados, adicionando dados fictícios para simular o uso do sistema.

---

## Próximos Passos

- Adicionar scripts para popular as tabelas com dados fictícios.
- Implementar queries SQL para relatórios, como:
  - Listar ordens de serviço em andamento.
  - Consultar serviços mais frequentes.
  - Identificar peças mais utilizadas.

---

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.

---

## Autor

Projeto desenvolvido como parte de um desafio de criação de banco de dados. Para dúvidas ou sugestões, entre em contato comigo através do GitHub.
