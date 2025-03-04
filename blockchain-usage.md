# Blockchain Usage in KRJPLMod

## Introduction
KRJPLMod includes built-in blockchain support, allowing developers to create decentralized applications (DApps), interact with smart contracts, and implement secure, transparent transactions. This guide covers how to integrate blockchain functionality into KRJPLMod applications.

## 1. Setting Up Blockchain in KRJPLMod
To begin using blockchain features, initialize a blockchain-enabled project:
```bash
krjplmod new blockchain_project --blockchain
cd blockchain_project
```
This sets up the necessary files and dependencies.

## 2. Connecting to a Blockchain Network
KRJPLMod supports multiple blockchain networks, including Ethereum, Binance Smart Chain, and custom chains:
```krjplmod
let blockchain = blockchain.connect("ethereum");
```
This establishes a connection to the Ethereum network.

## 3. Creating and Deploying Smart Contracts
Define a simple smart contract:
```krjplmod
contract Token {
    let balance = {};

    fn mint(to, amount) {
        balance[to] += amount;
    }

    fn transfer(from, to, amount) {
        if balance[from] >= amount {
            balance[from] -= amount;
            balance[to] += amount;
        }
    }
}
```
Deploy the contract:
```krjplmod
blockchain.deploy(Token);
```

## 4. Interacting with Smart Contracts
Call a smart contract function:
```krjplmod
blockchain.call(Token.mint("0xUserAddress", 100));
```
Retrieve contract data:
```krjplmod
let userBalance = blockchain.query(Token.balance["0xUserAddress"]);
web.p("User balance: " + userBalance);
```

## 5. Handling Blockchain Transactions
Send cryptocurrency transactions:
```krjplmod
let tx = blockchain.transaction("0xRecipient", 1.5, "ETH");
tx.send();
```
Verify transaction status:
```krjplmod
if tx.confirmed() {
    web.p("Transaction successful!");
} else {
    web.p("Transaction pending...");
}
```

## 6. Decentralized File Storage
Store data securely on a decentralized storage network:
```krjplmod
let fileHash = blockchain.store_file("document.pdf");
web.p("Stored file hash: " + fileHash);
```
Retrieve files:
```krjplmod
blockchain.get_file(fileHash, "download.pdf");
```

## 7. NFT Creation and Trading
Create an NFT:
```krjplmod
let nft = blockchain.create_nft("My Art", "art.png");
```
List NFT for sale:
```krjplmod
blockchain.list_nft(nft, 2.5, "ETH");
```

## 8. Web3 Integration
Enable Web3 authentication:
```krjplmod
let user = blockchain.web3_login();
web.p("Logged in as: " + user.address);
```

## Conclusion
KRJPLMod makes blockchain development **faster, easier, and more secure** than any other programming language. Next, explore:
- [Cloud Services](cloud_services.md)
- [Advanced Features](../docs/advanced_features.md)

Start building **decentralized applications with KRJPLMod** today!

