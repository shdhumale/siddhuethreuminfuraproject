# siddhuethreuminfuraproject
This project shows the use of Infura to connect Ropsten Test Env using Solidity
Project Overview

This project demonstrates how to use Infura to connect to the Ropsten test network using Solidity.  It includes the basic setup for a Truffle project, a Solidity contract for sending money, and tests.

Directory Structure

The project has the following structure:

contracts/: Contains the Solidity source files:

Migrations.sol: A standard Truffle migration contract. 

SendMoney.sol: The core contract for sending Ether. 

migrations/: Contains JavaScript files for deploying contracts. 

test/: Contains JavaScript files for testing the contracts. 

truffle-config.js: Truffle configuration file (network settings, compiler settings, etc.). 

package.json: Node.js package file (dependencies, etc.). 

README.md: Basic project description. 

Key Files Explained

truffle-config.js: This file is crucial.

It sets up how Truffle connects to the Ethereum network. 

It defines network configurations (like development and ropsten). 

For Ropsten, it uses @truffle/hdwallet-provider to interact with Infura.  It's important to note that you'll need to replace "your metamask mnemonic" and <Your API Key> with your actual MetaMask seed phrase and Infura API key. 



It also specifies the Solidity compiler version. 
contracts/SendMoney.sol: This is the Solidity contract.

It has functions to send coins (sendCoin, sendAmount) and check balances (getSenderAmount, getReceiverAmount). 

It emits a Transfer event when coins are sent. 

migrations/2_SendMoney_migration.js: This migration file tells Truffle how to deploy the SendMoney contract to the blockchain. 

test/sendmoney.js: This file contains tests written using Truffle's testing framework. 

It tests the sendCoin function to ensure that Ether is transferred correctly between accounts. 

package.json: This file lists the project's dependencies, including @truffle/hdwallet-provider, which is used to sign transactions for Infura. 

How it Works

Connecting to Ropsten: The truffle-config.js file sets up the connection to the Ropsten test network through Infura. It uses a wallet provider to securely sign transactions. 

Deploying the Contract: Truffle migrations are used to deploy the SendMoney.sol contract to the Ropsten network. 

Sending Ether: The sendCoin and sendAmount functions in the SendMoney contract allow sending Ether between accounts. 

Testing: The test/sendmoney.js file verifies that the contract functions correctly, specifically that Ether is transferred as expected. 

Let me know if you'd like a more detailed explanation of any specific part of the code!
