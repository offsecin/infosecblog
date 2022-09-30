
Hey Readers,

Thanks for checking in.

For a long time, I have been planning to get started with Web3 security as I feel this is the most exciting domain that we are about to witness in the next generation of information security.

I am planning to mention the notes and resources here so that they might help others who are willing to get started in this domain.

This is my first blog about Web3, so please find the below resources that will give you an overview of what the Web3 learning curve might look like. I will go into detail on most of the topics (that I feel are worth mentioning here) as I get the chance.

- https://twitter.com/adrianhetman/status/1475550508354093072?lang=en
- https://github.com/Anugrahsr/Awesome-web3-Security
- https://sm4rty.medium.com/roadmap-for-web3-smart-contract-hacking-2022-229e4e1565f9

So, let's get started with a book called `Mastering Ethereum`. The following section would cover the following important notes about these topics that might be from different resources: 

# Day 1 of Mastering Ethereum

### Chapter 1: What is Ethereum?

- Ethereum is an open source, globally decentral‐ized computing infrastructure that executes programs called smart contracts. It uses a blockchain to synchronize and store the system’s state changes, along with a crypto‐currency called ether to meter and constrain execution resource costs.

- Ethereum is a deterministic but practically unbounded state machine, consisting of a globally accessible singleton state and a virtual machine that applies changes to that state.
- A general purpose Blockchain.
- Ethereum is also a distributed state machine.Ethereum tracks the state transitions of a general-purpose data
store, i.e., a store that can hold any data expressible as a key–value tuple.

Note:Unlike Bitcoin which has a very limited scripting language, Ethereum is designed to be a general-purpose programmable blockchain that runs a virtual machine capable of executing code of arbitrary and unbounded complexity. Where Bitcoin’s Script lan‐ guage is, intentionally, constrained to simple true/false evaluation of spending condi‐ tions, Ethereum’s language is Turing complete, meaning that Ethereum can straightforwardly function as a general-purpose computer.

#### Components of a Blockchain
- A peer-to-peer network
- Messages in the form of transactions
- A set of consensus rules governing rules for a valid transactions
- A state machine that processes transactions according to the consensus rules
- A chain of cryptographically secured blocks that acts as a journal of all the verified and accepted state transitions
- A consensus algorithm that decentralizes control over the blockchain
- A scheme to economically secure the state machine in an open environment

##### GAS 

Ethereum’s ability to execute a stored program, in a state machine called the Ethereum Virtual Machine, while reading and writing data to memory makes it a Turing- complete system and therefore a UTM (Universal Turing machine). Ethereum can compute any algorithm that can be computed by any Turing machine, given the limitations of finite memory.

##### UTM : 

To avoid DOS attacks/infinite loops due to unexptected transactions, Ethereum introduced a mechanism called `gas`.Each instruction has a predetermined cost in units of gas. When a transaction triggers the execution of a smart contract, it must include an amount of gas that sets the upper limit of what can be consumed running the smart contract. The EVM will terminate execution if the amount of gas consumed by com‐ putation exceeds the gas available in the transaction. Gas is the mechanism Ethereum uses to allow Turing-complete computation while limiting the resources that any pro‐ gram can consume.
Gas can only be purchased as part of a transaction, and can only be bought with ether.Gas is purchased for the transaction, the computation is executed, and any unused gas is refunded back to the sender of the transaction.


##### DApps :  
Dapps is a set of contracts and a web interface using the ethereum’s infrastructure.


