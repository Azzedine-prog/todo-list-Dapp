<a href="https://github.com/mortennobel/cpp-cheatsheet"><img align="right" src="https://camo.githubusercontent.com/38ef81f8aca64bb9a64448d0d70f1308ef5341ab/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f72696768745f6461726b626c75655f3132313632312e706e67" alt="Fork me on GitHub" data-canonical-src="https://s3.amazonaws.com/github/ribbons/forkme_right_darkblue_121621.png"></a>

## Smart Contract TO do List :
## introduction:
Now a decentralized System works similarly, except you use a framework to contact a Blockchain network instead of a Server. Keeping this in mind, let’s get started! A Blockchain is essentially a Peer-to-Peer system, Ethereum included. There are many networks out there, but we will stick to Ethereum. Ehtereums run Smart Contracts, which are written in Solidity. If you have done any amount of Object-Oriented Programming before, Solidity will be easy to get on. For this tutorial you will need Web3.js, Truffle and Ganache. A quick introduction to all of this: Web3.js is used to communicate with your Blockchain, Truffle is used to interface with your solidity code, push it to the chain, test your smart contracts et al. and Ganache is used to run a local Blockchain to deploy your code to, since deploying to the Ethereum Virtual Network costs money (Ether) in the form of Gas.
# ToDo List INPT DApp
A todo list powered by Ethereum smart contracts. User can optionally deposit prize for each task which will get it back in his prize account or will be punished by not being able to withdraw the prize back to his account during the punishment period.
## Contents
- [team members](#team)
- [Screenshots](docs/screenshots.md)
- [Installation](#installation)

## team:
"INPT (national institute of posts and telecommunicatis) students"
- SOULTANA AICHA.
- NOUHAILA AYAR.
- YOUSSEF QAISSOUMI.
- AZZEDINE LAKHDAR.
## Installation
0. Install required packages.
```
npm install -g ganache-cli truffle
```
1. Run a `ganache-cli` service.
```
ganache-cli
## Or fill out .env file parameters for deploying contract on Rinkeby testnet
# cp sample.env .env
# nano .env
## Optionally you can run ganache localy with provided mnemonic phrase
# . .env
# ganache-cli --mnemonic "$MNEMONIC"
```
2. Navigate to `blockchain` directory and type below command and enter.
```
cd blockchain
npm install
truffle migrate --reset --compile-all --network development
## Deploy project on Rinkeby testnet
# truffle migrate --reset --compile-all --network rinkeby
```
3. Then navigate to `client` directory to enter below commands.
```
cd ../client
npm install
npm run serve
## Build production files
# npm run build
```
4. Open [http://localhost:8080/](http://localhost:8080/) URL to interact with the contract. **MetaMask** extension should be installed on your browser and you need to select the network which match with where the contract is being deployed. Furthermore you can import your generated accounts in Truffle to cover the fees.
