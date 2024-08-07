# Financial-Transaction-API# Financial Transaction Processing

This project is a MuleSoft application that processes financial transactions, including creating transactions, processing refunds, and reconciling accounts.

## Prerequisites

- MuleSoft Anypoint Studio
- Maven
- Java 8 or later

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/akshithachinthareddy/financial-transaction-processing.git
    cd financial-transaction-processing
    ```

2. Open the project in Anypoint Studio.

3. Run the application:
    ```sh
    mvn clean install
    ```

## Usage

1. Start the MuleSoft application in Anypoint Studio.

2. Access the API endpoints:
    - Create Transaction: `POST /api/transactions`
    - Process Refund: `POST /api/refunds`
    - Reconcile: `POST /api/reconcile`

### Example Requests

- **Create Transaction**

    ```sh
    curl -X POST http://localhost:8081/api/transactions \
    -H 'Content-Type: application/json' \
    -d '{
        "amount": 100.00,
        "currency": "USD",
        "description": "Payment for invoice #123"
    }'
    ```

- **Process Refund**

    ```sh
    curl -X POST http://localhost:8081/api/refunds \
    -H 'Content-Type: application/json' \
    -d '{
        "transactionId": "abc123",
        "amount": 100.00
    }'
    ```

- **Reconcile**

    ```sh
    curl -X POST http://localhost:8081/api/reconcile
    ```

## Tests

Run the MUnit tests:
    ```sh
    mvn test
    ```

### MUnit Tests

The project includes the following MUnit tests:

- **createTransactionFlowTest**: Tests the `createTransactionFlow` for successful transaction creation.
- **processRefundFlowTest**: Tests the `processRefundFlow` for successful refund processing.
- **reconcileFlowTest**: Tests the `reconcileFlow` for successful reconciliation.

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

