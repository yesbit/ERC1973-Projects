# Requirement checklist for implementation 

## ERC 1973 Contract

Make sure to use the ERC 1973 contract along with any open zepplin dependencies. Currently, you will have to extract the code form the EIP itself. Once you have the code base, there are two ways in which you can develop your application:

* Using Truffle (recommended) - use ERC 1973 as one of your smart contracts. You can then import the ERC 1973 into your other contracts OR create an interface to interact with it. 

* Using Remix 

# Test Cases 

Test cases are mandatory for any implementation.

* Truffle: add javascript test cases to your truffle suite 

* Remix: add Rospten (or any other test network) transactions in your repo and verify your contracts in Etherscan