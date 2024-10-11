# Sistema de Gerenciamento Imobiliário

Este projeto é um sistema básico de gerenciamento imobiliário. Ele permite cadastrar propriedades, clientes e agentes, bem como registrar transações de compra e aluguel de imóveis. O sistema também oferece consultas para visualizar propriedades disponíveis e transações realizadas.

## Funcionalidades

- **Gestão de Propriedades**: Cadastro de propriedades com informações como endereço, tipo (casa, apartamento, terreno), valor e status (disponível, vendido, alugado).
- **Gestão de Clientes**: Registro de clientes interessados em compra ou aluguel, com informações como nome, telefone, e-mail e tipo de interesse.
- **Gestão de Agentes**: Cadastro de agentes imobiliários, responsáveis pelas transações de venda e aluguel.
- **Gestão de Transações**: Registro de transações de compra e aluguel, associando clientes, agentes e propriedades, além de informações sobre a data e o tipo de transação.

## Estrutura do Banco de Dados

### Tabelas

- **Propriedades**:
  - `id`: Identificador único da propriedade.
  - `endereco`: Endereço da propriedade.
  - `tipo`: Tipo da propriedade (`casa`, `apartamento`, `terreno`).
  - `valor`: Valor da propriedade.
  - `status`: Status da propriedade (`disponível`, `vendido`, `alugado`).

- **Clientes**:
  - `id`: Identificador único do cliente.
  - `nome`: Nome completo do cliente.
  - `telefone`: Número de telefone do cliente.
  - `email`: E-mail do cliente.
  - `tipo_interesse`: Tipo de interesse do cliente (`compra` ou `aluguel`).

- **Agentes**:
  - `id`: Identificador único do agente.
  - `nome`: Nome do agente imobiliário.
  - `telefone`: Número de telefone do agente.
  - `email`: E-mail do agente.

- **Transações**:
  - `id`: Identificador único da transação.
  - `cliente_id`: Referência ao cliente que fez a transação.
  - `agente_id`: Referência ao agente responsável pela transação.
  - `propriedade_id`: Referência à propriedade envolvida na transação.
  - `data`: Data da transação.
  - `tipo_transacao`: Tipo da transação (`compra` ou `aluguel`).

## Consultas e Operações Disponíveis

### Consultas

1. **Listar todas as propriedades disponíveis**:
   - Exibe todas as propriedades cujo status está como "disponível".

2. **Listar todas as transações de compra**:
   - Mostra todas as transações que envolvem a compra de imóveis.

3. **Detalhes completos de uma transação**:
   - Exibe informações completas de uma transação, incluindo o nome do cliente, agente e o endereço da propriedade.

### Atualizações e Deleções

1. **Alterar o status de uma propriedade para "Vendido"**:
   - Após a conclusão de uma transação de compra, o status da propriedade é atualizado para "vendido".

2. **Atualizar as informações de um cliente**:
   - Permite modificar os dados de um cliente, como telefone ou e-mail.

3. **Remover um cliente ou uma propriedade**:
   - Exclui registros de clientes e propriedades que não estão mais envolvidos em transações.

## Como Usar

1. **Criar o Banco de Dados**:
   Execute o script SQL fornecido para criar o banco de dados e suas respectivas tabelas.

2. **Inserir Dados**:
   Insira dados de propriedades, clientes, agentes e transações conforme necessário.

3. **Consultar e Manipular Dados**:
   Utilize as consultas SQL fornecidas para visualizar e modificar os dados.

## Licença

Este projeto está licenciado sob a Licença MIT. Consulte o arquivo `LICENSE` para mais detalhes.

## Requisitos

- MySQL ou outro sistema de gerenciamento de banco de dados compatível com SQL.
- Ferramenta para execução de scripts SQL, como MySQL Workbench ou phpMyAdmin.
