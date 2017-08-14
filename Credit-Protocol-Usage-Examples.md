---
title: Credit Protocol Usage Examples
tags: whitepaper-section
order: 3
headings:
  - University Meal Vouchers
  - Microfinancing
  - Retail Gift Cards
  - Consumer Loans
  - Airline Miles Vendor Loyalty Credit Card Points
  - Friend In Debt
date: 2017-08-14 15:44:44
---


# Credit Protocol Usage Examples:

The simplest way to imagine the Credit Protocol is as a mechanism for the creation, tracking, and settlement of IOUs. At a basic level, IOUs are no different than currency. The earliest forms of cash were little more than standardized IOUs for some amount of precious metal, such as gold or silver, or a commodity like stored grain. *Therefore, by allowing individual users to create and manipulate customized IOUs, CP effectively democratizes the digital issuance of currency.*

> Therefore, by allowing individual users to create and manipulate customized IOUs, CP effectively democratizes the digital issuance of currency.

Off the blockchain, there already exist a massive range of use cases for IOUs—they exist between vendors and buyers in the form of accounts receivable, retailers and consumers in the form of gift cards, or airlines and flyers in the form of miles. Sometimes, these IOUs are denominated in a fiat currency issued by a government; other times, the IOUs exist only as an arbitrary currency designed by its issuer. Either type of IOU has value, so long as the two parties trust that one party may redeem the currency for something else of agreed upon worth. CP is the foundational tool that enables this massive range of use cases, available to and developable by anyone owning our product-use tokens.[^1]

We envision a vast and diverse array of applications to be built atop BlockMason’s Credit Protocol, with tremendously varied functionality. Below, we examine just a few usage examples for the Credit Protocol—the first targets for our Bounty Program (see explanation below)—as well as our first exciting CP-based application: __Friend in Debt__ ([Try It Now](http://fiddy.io)).

We invite everyone interested in the Credit Protocol to check out our code at [our github repository](https://github.com/blockmason).

## University Meal Vouchers

Imagine a school wants to implement a meal plan for its students. First, the school purchases sufficient CP tokens to cover the amount of transactions they expect to occur within the system. Then, the school whitelists students’ FoundationIDs, preventing anyone other than a university student from executing transactions through the UCAC. The UCAC is designed to only allow transactions between the school and students, preventing students from trading tokens between each other on any sort of underground market. The Meal Voucher system uses its allotted free CP transfers (proportional to the number of CP tokens purchased by the school) to allow students to settle debts without cost on the CP network. Students then pay for a meal plan, let’s say $300 a month. Students pay the school in cash or digital currency, and the school sends the student 60 meal tokens. Each time the students visit the cafeteria, they tap their phone to machine that records their purchase, spending one meal token to buy their food. The school’s UCAC allows *only* these types of transactions to be settled between specific on-campus food venues and students of the school.

![School voucher checkout system](/cp-whitepaper/images/image_2.png)

## Microfinancing

A microloan system may be developed in the same manner as the meal voucher system described above. The creator of the Use Case Authority Contract, in this case the lender, could write a contract that limits the amount of individual debts per borrower, requires multiple borrowers for one loan (e.g. for individuals from the same community or village), makes the pool of borrowers jointly liable, and includes a built-in interest and payback schedule.

Microfinancing of this type is an extremely powerful tool, especially for communities without access to traditional banking. It enables liquid movement of debt and complex economic development previously unavailable to areas of the world outside the reach of large financial institutions. These developments could include small business development loans, low-interest payday loans, or crowdsourced repayment of community debts, such as rebuilding a business after a fire or paying medical expenses after an accident.

## Retail Gift Cards

Another obvious use of the Credit Protocol is an application to manage retail gift cards. Consumers may purchase store credits and send those credits to any FoundationID (including his or her own), creating a debt between the retailer and the recipient of those credits. When the recipient uses his or her credits to redeem a product or service, it settles that debt.

Alternatively, a user could purchase from a retailer a redeemable code that allows access to funds already written into the Use Case Authority Contract. This digital ecosystem of debt and credit movement between retailers and consumers allows for the simple creation of entities like Visa Cash Cards, or all-purpose credits that can be deposited in a specific gift card account.

Because gift card usage is generally very similar between vendors, one can imagine a single unified application for managing any number of gift cards, allowing users to gift their friends credits which could then be assigned to specific stores of their choosing.

## Consumer Loans

While securing a consumer loan currently requires wading through significant red tape and bureaucratic infrastructure, the Credit Protocol could vastly simplify the process of acquiring such a loan. Because blockchain ledgers are both public and secure, users could employ dapps to track their debts exactly, facilitate debt repayment through third party organizations, and be absolutely certain that payment has been received, avoiding any of the numerous scams or problems plaguing those operating in the debting world.

Such a system could also make use of the underlying debt data stored in the Credit Protocol to evaluate individual borrower’s credit and debt repayment history. A UCAC could further verify a borrower’s claims against information associated with that user’s FoundationID to determine their legitimacy.

Get a suspicious phone call claiming you’re behind on your car payments? Hang up and check the blockchain to confirm your payment *instantly*.

## Airline Miles / Vendor Loyalty / Credit Card Points

Airline miles and vendor loyalty points are yet another form of debt that exists between the airline or vendor and their customers. Airlines issues miles in the form of their own currency (e.g. debt) as a reward for fliers based on their patronage. Users then settle the debt by claiming a product or service based on the point system established by the airline or vendor.

This vendor loyalty system highlights a particularly interesting property of the Credit Protocol: debts need not be recorded as fiat currency, such as USD, or cryptocurrency, such as ETH. Users may write UCACs to accept arbitrary values and currencies so long as:
  1. they map redemption values to redemption methods
  2. the customer base values the newly generated currency, such as airline miles or credit card points.

![air miles received](/cp-whitepaper/images/image_3.png)

## Friend In Debt

Here, we’ve saved the best for last.

Friend in Debt is our first full-fledged (__and functional!__) implementation of the Credit Protocol, a social tool for users to track and issue debts amongst friends, family members, and individuals in their community. Its potential applications and use cases are vast and powerful, and we look forward to presenting Friend in Debt in further detail later in this Whitepaper.

Or, to jump straight into the economic revolution, explore Friend in Debt here: [fiddy.io](http://fiddy.io)

*[IOU]: I owe you. A document acknowledging a debt.

[^1]: PLEASE NOTE: Some applications built upon CP may be subject to regulation in some jurisdictions.  Developers building upon CP are responsible for determining which apps are subject to regulation and for complying as appropriate.
