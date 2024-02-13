[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/Brunogoniadis/FinAPI-node/blob/main/README.md)

# FinApi

## Descrição

FinApi em uma API de gerenciamento bancário feita com Express em Node.js. A API oferece funcionalidades básicas para o gerenciamento de contas bancárias, permitindo operações como cadastro de clientes, depósitos, saques, consulta de extrato, atualização de informações do cliente e exclusão de conta.

Este projeto utiliza variáveis locais em vez de um banco de dados para armazenamento temporário de dados dos clientes e transações bancárias.

## Funcionalidades Principais

1. **Cadastro de Cliente**
   - Rota: `POST /account`
   - Descrição: Permite cadastrar um novo cliente com um CPF único e um nome associado. Cada cliente criado recebe um identificador único (UUID) para sua conta.

2. **Consulta de Extrato**
   - Rota: `GET /statement`
   - Descrição: Retorna o extrato completo de transações de um cliente específico, identificado pelo CPF. Requer que o CPF do cliente seja passado no header da requisição.

3. **Depósito em Conta**
   - Rota: `POST /deposit`
   - Descrição: Permite que um cliente faça um depósito em sua conta bancária. O cliente pode especificar uma descrição para o depósito e o valor a ser depositado.

4. **Saque em Conta**
   - Rota: `POST /withdraw`
   - Descrição: Permite que um cliente faça um saque de sua conta bancária, desde que haja fundos suficientes. O cliente pode especificar o valor a ser sacado.

5. **Consulta de Extrato por Data**
   - Rota: `GET /statement/date`
   - Descrição: Retorna o extrato de transações de um cliente específico em uma data específica. O cliente é identificado pelo CPF e a data é passada como um parâmetro de consulta na URL.

6. **Atualização de Informações do Cliente**
   - Rota: `PUT /account`
   - Descrição: Permite que um cliente atualize suas informações cadastrais, como o nome associado à conta. O cliente é identificado pelo CPF.

7. **Consulta de Informações do Cliente**
   - Rota: `GET /account`
   - Descrição: Retorna as informações do cliente, incluindo CPF e nome associado à conta. O cliente é identificado pelo CPF.

8. **Exclusão de Conta do Cliente**
   - Rota: `DELETE /account`
   - Descrição: Permite que um cliente exclua sua conta bancária. Após a exclusão, todos os dados associados à conta são removidos do sistema.

## Como Usar

1. Clone este repositório.
2. Instale as dependências usando `npm install`.
3. Inicie o servidor localmente usando `npm start`.
4. Acesse as rotas da API conforme descrito acima.

## Dependências

- Express
- uuid

## Estrutura do Projeto

- `index.js`: Ponto de entrada da aplicação, contém os middlewares utilizados na aplicação e rotas da API.

## Contribuição

Contribuições são bem-vindas. Fique à vontade para abrir issues ou pull requests para melhorias, correções de bugs, ou novas funcionalidades.

## Autor

- [Bruno Goniadis Lima](https://github.com/Brunogoniadis/) - Autor

## Licença

Este projeto está licenciado sob a [MIT](https://github.com/Brunogoniadis/FinAPI-node?tab=MIT-1-ov-file#readme).
