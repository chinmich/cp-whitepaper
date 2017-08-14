---
title: CP Technical
tags: whitepaper-section
order: 5
headings:
  - Foundation Technical
  - Credit Protocol Data Smart Contract
  - Credit Protocol Smart Contract
  - Flux Capacitor Smart Contract
  - Use Case Authority Contracts
  - Multiple Users and Bidding
  - Staking Smart Contract
  - Tech Considerations
  - Nameprep for FoundationIDs
  - Storage Costs
  - Expandability
date: 2017-08-14 15:44:42
---


# CP Technical

**Luke graphic**

## Foundation Technical

For a more detailed explanation of Foundation please, see the Foundation whitepaper here: [http://blockmason.io/foundation_whitepaper.pdf](http://blockmason.io/foundation_whitepaper.pdf)

View the Foundation documents here: [http://blockmason.io/projects/foundation/documentation/](http://blockmason.io/projects/foundation/documentation/)

BlockMason created Foundation after experimenting with an earlier, unreleased version of the Credit Protocol. During the development process, we encountered a number of technical issues related to identity and wallet integration that no current application on the Ethereum network could solve. How would you proceed, for instance, if one wanted to access a CP backed dapp on your desktop instead of on your phone? Would you need to unsecurely email yourself your private Ethereum key? Should you try to type it into another wallet to import it? If you decided to use a new Ethereum address with the CP, how could you integrate that new address into the application?

Through endless coding, sleepless nights, and extensive trial and error, we realized that we required a unifying mechanism to link Ethereum addresses on one’s phone and desktop. From the ashes of our earliest CP development, Foundation rose like a phoenix—a phoenix whose primary purpose is to allow all of your addresses to identify as *you*.

Foundation’s interface facilitates a clean and easy ID creation process. All that is required is an Ethereum address not currently associated with another Foundation ID. It’s that simple. Once a user has created a FoundationID, he or she may then choose to add any other addresses he or she currently owns from an address already associated with the Foundation ID, via the Foundation smart contract.

This unified FoundationID is required to use the Credit Protocol. It allows users to maintain one identity with the ability to access the CP from any device and any dapp browser.

**Foundation Manager screenshots.**

## Credit Protocol Data Smart Contract

The Credit Protocol Data smart contract is the core contract which stores data about all relationships between entities, as well as their debts and credits. It holds two main data structs:  *Relationships* and *Debts*.  

*Relationships* tracks relationships between two entities.  To form a debt between two entities, those two entities must be demarcated as "connected."  *Relation**ships* also tracks pending relationships, as users are required to confirm relation requests.

*Debts* keeps track of debts between one user and another.  It executes tasks like tracking debts, holding pending debts, and recording in which currency particular debts are denominated.

## Credit Protocol Smart Contract

The Credit Protocol smart contract reads and manipulates the Credit Protocol data contract. This contracts functions include: reading user’s debts, pending debts, sending debts, confirming debts, reading friends lists, adding friends, removing friends, etc.   

The Credit Protocol smart contract is the only address authorized to manipulate information stored in the Credit Protocol data smart contract.

Users may only interface with the Credit Protocol smart contract via the Flux Capacitor contract (described below).  

## Flux Capacitor Smart Contract

The Flux Capacitor contract is the contract with which users interact.  The user never actually interacts directly with the UCACs.  Flux Capacitor functions mimic the core CP contract functions, with the exception that each function also takes the address of a UCAC.  The Flux Capacitor functions check the calls from the user against the UCAC at the UCAC address to make sure parameter values specified by the user are valid for that specific UCAC.  

The Flux Capacitor contract also checks the Staking contract to record the amount of tokens a CP Token holder is staking and for which contracts those tokens are declared. The Flux Capacitor contract also notes total remaining capacity for transactions allowed within a given time period for that user’s staked tokens. The contract then updates the CP Token staker’s transaction capacity and calls the corresponding function in the CP Data smart contract.

It is easiest to think of the Flux Capacitor as an enforcer. It administrates the parameters of a UCAC and limits transaction capacity according to the amount of CP Tokens a user has staked for a given UCAC.

## Use Case Authority Contracts

UCAC’s contain the exact same function calls as those listed in the Flux Capacitor contract.  Each function only returns a boolean of true or false.  The Flux Capacitor contract calls on the UCAC with the exact function name as denoted in the Flux Capacitor to check if the transaction is valid.  

As an example, the Flux Capacitor function *newDebt *would call a UCAC’s *newDebt* function with the exact same parameters: *bytes32 myId, bytes32 friendId, bytes32 currencyCode, int amount, bytes32 _desc, *and the UCAC would return true or false to verify if this was a valid transaction. Therefore, if a UCAC allows EUR, but not USD, and a user attempts to pass USD through the Flux Capacitor contract, it would return false.  A false return would cause the call to newDebt in the Flux Capicitator to fail.  

A UCAC’s reason for returning true or false answers are limitless.  Their only requirement is that they maintain the same function names and parameters inputs as the functions in Flux Capacitor.  If they do not have the same function names and parameters, then calls to those Flux Capacitor functions will throw.  

## Multiple Users and Bidding

Multiple users can stake CP tokens for the same UCAC, if allowed.  If a dapp is sufficiently popular, hundreds or thousands of users may stake CP tokens to help support its transactions.

A UCAC may also be written to allow CP token holders to compete for transactions through that UCAC. For example, two users may stake their tokens for the same UCAC, offering their allotted transactions to users of the UCAC at two different prices. The dapp can then evaluate which bid is least expensive, and offer the price to the user before sending the CP transaction through that pathway.

## Staking Smart Contract

The Staking contract stores information about how many tokens a user stakes to a specific UCAC, powering the transactions of a UCAC.  When a user attempts to execute a function for a UCAC, the Flux Capacitor then queries the Staking contract for information about how many tokens the user has staked to power the transactions of that UCAC.

The Staking contract also watches for changes in a user’s CP tokens to guarantee that the user is not trying to cheat the system to acquire free transactions.

## **Tech Considerations**

### Nameprep for FoundationIDs

FoundationIDs integrated with CP will be usable only if adhering to a nameprep standard that exclusively supports lowercase letters and numbers. This restriction means that FoundationIDs containing any symbol other than lowercase a-z and 0-9 will not be usable with the CP.

### Storage Costs

Storing data on the Ethereum blockchain is expensive. In order to make CP low cost for users, BlockMason’s ongoing maintenance and support include updating and optimizing our product to reduce costs. Cost minimization is an ongoing process that involves the use of systems like IPFS and other off-chain storage solutions. We carefully select variable types to minimize storage costs and also consciously examine the benefits of storing specific data on or off the blockchain.

### Expandability

While we are already excited about the current version of CP, we are committed to providing robust maintenance and support, including fixes and expanded functionality in periodic version upgrades, as with any quality software-based service. With maintenance and support in mind, we have compartmentalized the Foundation smart contract to separate storage variables from actual functionality. This allows us to upgrade the protocol’s functionality while maintaining all existing storage, saving the cost of porting that storage into new contracts. We will implement this same compartmentalization method for all CP smart contracts.

One powerful feature of building applications atop the Ethereum blockchain is its public ledger storage. Because the CP smart contract is accessible to anyone on the Ethereum network, future developers may easily build applications atop the existing CP infrastructure. This transparency allows for the creation of dynamic new debt payment models using the existing CP data and functionality, including platforms for micro loans, consumer loans, and business to business credit lines.
