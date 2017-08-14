---
title: FiD Technical
tags: whitepaper-section
order: 10
headings:
  - Credit Protocol Smart Contracts
  - Friend in Debt Use Case Authority Contract
  - Market Handler
  - Front End
date: 2017-08-14 15:44:37
---


# FiD Technical:

## Credit Protocol Smart Contracts

The Credit Protocol smart contracts form the base contracts on which FiD runs.  FiD is more or less an unrestricted UCAC running on top of the CP.  Ergo, all of the above descriptions of the mechanisms behind the CP, apply to FiD.  

Foundation forms the core of user interaction with FiD.  This means that in order to use FiD you will need to have a FoundationID.  These are easy to create through the Foundation Manager UI and currently free.  

## Friend in Debt Use Case Authority Contract

The FiD UCAC is simply a UCAC without any rules.  This means that it is open to the general public and has no limits on the amounts of debt that can pass through it.

The FiD UCAC will allow any CP Token Holder to stake their tokens and bid for hosting user transactions, to be paid in ETH. The FiD UCAC will automatically choose the lowest-priced transactions for its user, ensuring that costs are as low as possible. Therefore, users of FiD must pay a transaction price in ETH unless there are free transactions available. While owning ETH is a necessity for using current versions of FiD, in future releases BlockMason plans to develop methods for onboarding new users who don’t possess ETH wallets, significantly growing the potential customer base.

## Market Handler

The Friend in Debt UCAC implements a smart bidding system, allowing CP Token stakers to bid for supporting FiD user transactions.  In practice, CP token stakers will bid a specific amount of ETH that they’d like to charge for the transaction.  The lowest bid (cheapest for FiD users) will win, if that bid has transaction capacity remaining.  

Initially Blockmason will be staking a portion of tokens set aside for FiD transactions, making those transactions free.  In the future, BlockMason will evaluate whether to continue this practice, use fewer CPT tokens, or raise the price of these transactions.

## Front End

The front end for Friend In Debt is written using Purescript. Purescript is a strongly, statically typed language with expressive types. Purescript compiles to javascript. Purescript is very similar to Haskell. We like Purescript because of its advanced type system lets us prototype and iterate much faster. These qualities ensure writing code in Purescript is ultimately easier, more fun, and significantly less prone to bugs.

The front end allows for users to easily interact with smart contract functionality without requiring the technical expertise of being able to use raw smart contract functions. It also serves to display data in an easy to view user friendly manner.

LUKE FRONT END PICS

For more information on the front end, why not try it out?  Friend in Debt beta is already available for a test drive. Please find the appropriate links on our website at [http://friendindebt.com](http://friendindebt.com)
