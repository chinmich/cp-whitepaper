---
title: Cost & Economics
tags: whitepaper-section
order: 6
headings:
  - Cost & Economics
  - Plasma and Off Chain Transactions
  - UCACs Transaction Costs and Monopolies
  - Transaction Capacity Setting
date: 2017-08-14 15:44:41
---


# Cost & Economics

When BlockMason designed the Credit Protocol, we envisioned a revolutionary protocol with global reach, available to users free of charge. However, computing, data storage, and transaction execution all have a cost on the Ethereum blockchain. This cost is commonly referred to as *gas. *Therefore, because CP runs on the Ethereum blockchain, using the protocol inevitably incurs transaction costs. Additionally, compared to traditional applications using standard web hosting, storage prices are relatively high. While we believe that Ethereum’s global domination is inevitable, we also know that the average user need not necessarily understand Ethereum and its operation. Successful, scalable dapps will likely appear to users just as normal, web-based applications, with many layers between users and the Ethereum network.

## Plasma and Off-Chain Transactions

Right now, the entire blockchain community is grappling with the problem of balancing cost and network speed against security and longevity. Fortunately, it seems a number of improvements may be within our grasp. In particular, the recent announcement of Plasma demonstrates the Ethereum Foundation’s commitment to increasing network speed and decreasing transaction cost, paving the way for widespread adoption of consumer focused decentralized applications. Additionally, the Raiden Network, similar to Bitcoin’s proposed Lightning Network, has the promise to reduce transaction costs up to 7 times and process up to 1 million transactions per second. It does this by moving some transactions off the blockchain onto a peer-to-peer network, while still interacting with the Ethereum Network to retain security and longevity. In the event that the Raiden Network fails to be implemented, BlockMason will execute its own off-chain settlement feature and make it available to all users. Employing an off-chain solution allows CP to make fewer updates to the Ethereum blockchain, and thus reduce associated costs.

Most importantly, we believe that CP will be a significant factor in driving users to the Ethereum network. The protocol’s power and its low barrier to entry will draw customers from a new customer base unfamiliar with cryptocurrency. We also plan to design future versions of the CP that cover the cost of a new user’s transaction fees without their even needing to know about concepts like ether and gas.

## UCACs, Transaction Costs, and Monopolies

CP token holders receive the ability to conduct a defined number of transactions per day based on the number of tokens they hold (which can be fractional).  While holders may choose to employ their tokens in CP dapps they personally use, in order enable their own transactions, token holders may also pursue various developer pathways as well. For example, holders could stake a dapp that they control, ensuring their users have an existing pathway to process a defined number of transactions, either for a fee set by the holder or free of charge.  

Token holders also might choose to stake their funds in other CP dapps to provide further transaction capacity for the dapp’s users, whether for free or for compensation. For example, a UCAC may include a bidding system to encourage CP Token holders to provide pathways for their users. While these bidding systems could be written in a variety of ways, entirely up to the UCAC creator, one solution would be an open ETH marketplace in which the lowest cost transaction pathway would "win" and be “sold” to the user of the dapp.

Such a market need not necessarily evaluate pathways based on associated fees. Instead, software may choose pathways based on other factors such as the reputation of users, which could be determined by institutions completely unrelated to the Credit Protocol. For example, an environmental agency could certify on the blockchain that a CP token stakeholder has taken an action that had a positive or negative effect on the environment. The dapp could then choose to process or not process transactions through that user’s pathways based on this reputation. Once identity characteristics are evaluated on the blockchain, such scenarios, in which contracts evaluate a user’s viability for interaction, are near infinite.

Lastly, because UCACs may restrict which users stake their CP Tokens to a particular contract, it is possible for CP Token holders to create virtual monopolies for that contract. To illustrate, a company may build a dapp that employs the Credit Protocol, but only allow their own organization to stake CP Tokens to that dapp. Therefore, the company could charge any price they want for transactions within that dapp without worrying about price competition from other CP stakeholders.

These are merely some of the possible actions and strategies that CP token holders can pursue as they use the tokens.

## Transaction Capacity Setting

Each CP Token will allow its owner to process a specified amount of transactions per day. The amount of transactions allowed per CP Token will be dynamically adjusted so that total network transactions account for 85% of the network’s capacity for transactions.

This algorithm monitoring and adjusting transaction capacity may only ever increase the total number of transactions allowed per CP Token; it can never decrease it.  This mechanism guarantees that available transaction capacity will grow with increasing network usage, while preventing purchasers from losing the total number of transactions allotted to them by their initial token purchase. It is akin to the expansion of broadband capacity as network usage increased with the popularity of online digital video and gaming.
