# Connectivity Tokens Architecture

This README provides a brief overview of the Micro Vision Architecture UML diagram. The architecture is composed of several key components, which are organized into a cloud provider and the Ethereum network.

## Cloud Provider

The cloud provider hosts the following components:

1. **Public FrontEnd**: The user interface of the solution, built using open-source frontend frameworks like Angular, Vue.js, or React.js. It can be deployed on a storage solution or an HTTP server.

2. **Back Office - Private Frontend**: The administrative web interface of the solution, also built using open-source frontend frameworks. It can also be deployed on a storage solution or an HTTP server.

3. **API Node - Core API**: The main REST APIs used by the solution. Both the Public FrontEnd and Back Office communicate with the Core API using REST.

4. **Message Oriented Middleware (MOM)**: Provides asynchronous processing using solutions like Apache Kafka, AWS SQS, or AMQP. It communicates with the Core API through async events.

5. **Identity Provider**: Handles authentication and authorization using off-the-shelf solutions like Keycloak based on open standards like XAML, OpenID.

6. **Relational Database**: A database solution such as Postgres or MySQL, used for common relational database functionalities.

7. **Storage**: Cloud storage solutions like AWS S3 or Google Storage for storing files and auditable information.

## Ethereum Network

The Ethereum network consists of the following smart contracts:

1. **MultiSignature**: A multisignature smart contract.
2. **TokenSmartContract**: A token smart contract.

These smart contracts interact with the Core API in the cloud provider.

The UML diagram provides a visual representation of these components and their relationships.
