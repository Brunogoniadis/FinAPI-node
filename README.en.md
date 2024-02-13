[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/Brunogoniadis/FinAPI-node/blob/main/README.en.md)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](https://github.com/Brunogoniadis/FinAPI-node/blob/main/README.md)

# FinApi

## Description

FinApi is a banking management API built with Express in Node.js. The API offers basic functionalities for managing bank accounts, allowing operations such as customer registration, deposits, withdrawals, statement inquiry, customer information update, and account deletion.

This project uses local variables instead of a database for temporary storage of customer data and banking transactions.

## Key Features

1. **Customer Registration**
   - Route: `POST /account`
   - Description: Allows registering a new customer with a unique CPF and an associated name. Each created customer receives a unique identifier (UUID) for their account.

2. **Statement Inquiry**
   - Route: `GET /statement`
   - Description: Returns the complete statement of transactions for a specific customer identified by CPF. Requires the customer's CPF to be passed in the request header.

3. **Deposit**
   - Route: `POST /deposit`
   - Description: Allows a customer to make a deposit into their bank account. The customer can specify a description for the deposit and the amount to be deposited.

4. **Withdrawal**
   - Route: `POST /withdraw`
   - Description: Allows a customer to make a withdrawal from their bank account, provided there are sufficient funds. The customer can specify the amount to be withdrawn.

5. **Statement Inquiry by Date**
   - Route: `GET /statement/date`
   - Description: Returns the statement of transactions for a specific customer on a specific date. The customer is identified by CPF, and the date is passed as a query parameter in the URL.

6. **Customer Information Update**
   - Route: `PUT /account`
   - Description: Allows a customer to update their registration information, such as the name associated with the account. The customer is identified by CPF.

7. **Customer Information Inquiry**
   - Route: `GET /account`
   - Description: Returns customer information, including CPF and name associated with the account. The customer is identified by CPF.

8. **Account Deletion**
   - Route: `DELETE /account`
   - Description: Allows a customer to delete their bank account. After deletion, all data associated with the account is removed from the system.

## How to Use

1. Clone this repository.
2. Install dependencies using `npm install`.
3. Start the server locally using `npm start`.
4. Access the API routes as described above.

## Dependencies

- Express
- uuid

## Project Structure

- `index.js`: Entry point of the application, contains middleware used in the application and API routes.

## Contribution

Contributions are welcome. Feel free to open issues or pull requests for improvements, bug fixes, or new features.

## Author

- [Bruno Goniadis Lima](https://github.com/Brunogoniadis/) - Author

## License

This project is licensed under the [MIT License](https://github.com/Brunogoniadis/FinAPI-node?tab=MIT-1-ov-file#readme).
