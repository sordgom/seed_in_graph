# NEAR Protocol NFT Minting with GraphQL
This project demonstrates how to use NEAR Protocol to mint NFTs and track ownership using GraphQL.

# Requirements
To use this project, you will need the following:

* A NEAR Protocol account and testnet tokens
* A deployed NFT contract
* A GraphQL schema to query and mutate data

# Installation
To install the necessary dependencies for this project, run the following command:

```
npm install
```

# Usage
Before running the GraphQL server, make sure that you have set the following environment variables:

`NEAR_NODE_URL`: the URL of the NEAR Protocol node to connect to
`NFT_CONTRACT_ADDRESS`: the address of the deployed NFT contract

To start the GraphQL server, run the following command:
```
npm start
```
This will start a GraphQL server at http://localhost:4000/graphql.

You can now use a GraphQL client (e.g., GraphQL Playground) to send queries to the server.

# Examples
Here are some example GraphQL queries that you can use to interact with the smart contract:

graphql
```
query {
  getToken(tokenId: "1") {
    tokenId
    owner {
      accountId
    }
  }
}

mutation {
  mintNFT(accountId: "user.testnet", tokenId: "2") {
    tokenId
    owner {
      accountId
    }
  }
}
```
These queries demonstrate how to get information about an NFT token and mint a new NFT.

# Contributions
Contributions to this project are welcome! If you find a bug or have an idea for a new feature, please open an issue or submit a pull request.
