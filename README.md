# Backend & Blockchain Developer Exam

Programming exam for backend and blockchain developers.

# Summary

Create an API server using Node.js runtime that allows user registration/login and integrates on a deployed Solidity smart contract on Ethereum's testnet to store and retrieve numeric values.

### Tasks
1. Create a server application using any Node.js framework.
2. Design a database structure that will allow user registration and login using API tokens.
3. Create a POST /register endpoint that accepts a user's username, email, and password.
  - Upon registration a web3 wallet must also be created and linked to the user's account via foreign key.
  - Wallet's public key must be stored in plain-text format on the database, but the private key should be encrypted.
4. Create a POST /login endpoint to allow users to request for API tokens.
  - Users are not allowed to have 2 or more valid API token at a time.
5. Create a PUT /logout endpoint to revoke the user's API token.
6. Deploy the Storage.sol smart contract on Ethereum's Ropsten Test Network.
7. Use either web3.js or ethers.js to interface the Storage.sol smart contract deployed on Ropsten on the Node.js server.
8. Create a POST /store endpoint that accepts the key "data" from the request body and will have any number value, then pass it on to the deployed smart contract.
  - Users should be authenticated. Only allow users with a valid API token.
9. Create a GET /retrieve endpoint that accepts the key "data" as a query param, then retrieve it's value from the deployed smart contract.

Plus points if the entire server application is Dockerized.

Push the code on a public repository also named "backend-blockchain-exam" under your own GitHub account. Send the repository link with the complete solution to the examiner not later that 3 days.