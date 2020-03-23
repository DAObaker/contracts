![DAObaker banner](images/Github%20banner.png)

# DAO Baker

**_Self-amending DAO for Staking Economy_**
> An upgradeable, on-chain staking validator for the Tezos community earning staking rewards. Additional features include peer-to-peer participation and automation of the entire baking process and governance voting.

Note: this is an evolving experiment and a proof of concept.
This standard Decentralised Autonomous Organisation (DAO) Baker is written in Michelson and runs on the Tezos blockchain.

[![Vault Contract](https://img.shields.io/badge/vault%20contract-2.0-blue
)](https://carthagenet.tzstats.com/KT1J7VKG2JubhZKczCdktQGRhcieTRHbvJfa)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Telegram](https://img.shields.io/badge/community-telegram-blueviolet
)](https://t.me/daobaker)


## Overview 

DAO Baker is an earnest effort by **[Block Swap](https://blockswap.xyz)** to decentralise the **Tezos (XTZ) staking (aka baking)** process through a set of self-enforcing smart contracts. This provides block by block transparency and auditability, thus minimising reliance on centralised discretionary staking providers.

The purpose is to address the user experience and inefficiency plaguing the current staking process that limits the benefit  to niche technical crypto users. Our solution intends to provide a mainstream user experience for Tezos staking.
DAO Baker is a 100% open source project.

## Table of Contents
- [Overview](#overview)
- [Modules](#Modules)
- [Contract Details](#vault)
- [More Information](#more-information)
- [Disclaimer](#Additional-Disclaimers)

## Modules

### Vault - Monetary Management
- Delegation
- Bonds (security deposit)
- Rewards & Payouts

### Protocol Politician  - Governance 
- Registration & Profile 
- Baker Rights & Management (TBA) 
- Community Index (TBA)

### Relay Node - Bakery
- BDE (TBA)
- Validator Infrastructure (TBA)

## More Information

Have any questions or feedback? Join the conversation on the [Telegram channel](https://t.me/daobaker/). Also, see the "DAO Baker" [article series](https://medium.com/@blockswap_hq/) for our primary thesis and some of the motivations, features, and design decisions of the DAO Baker.


## Vault

![Vault](https://i.ibb.co/h87mLK0/nitromethane-burning-inside-of-a-whoosh-bottle-in-super-slow-motion.gif)

### Account Management   

The current implementation of the **Vault** works as follows:

Allows users to make **_deposits and stake XTZ by simply sending XTZ to the contract_**, and the contract will automate the account generation and rewards allocation to that address. Account addresses are counterfactual based on the initial user deposit key and can be safely deployed by anyone using the vault contract. A user can make withdrawals partially or completely. When withdrawn completely, the user automatically redeems and transfers the account balance XTZ to the originated address. A user may cancel the delegation at any time should they wish and withdraw their balance with accumulated rewards.

There is also an account recovery option built-in "**Escape Hatch**". This can be used in the event that a user has lost access to their account or the contract has been compromised. Additional features will be rolled out in phases for the **Vault**, such as the ability to receive custom periodical payouts and portfolio management features.


#### [See deployed contract here](https://carthagenet.tzstats.com/KT1J7VKG2JubhZKczCdktQGRhcieTRHbvJfa)

| Key Functions|  Description |
| --- | --- |
|  `deposit` | Allows the user to **deposit XTZ** (multiples of 1 XTZ) to the contract account. In the case of new users, the contract will automatically generate and assign an account for them.|
| `withdrawal` | Allows the user to **withdraw XTZ** at any time by using the contract withdrawal function (multiples of 1 XTZ). In case of performing a _complete withdrawal_, the account will get closed.|
| `close_account` | Handles the **final settlement of the account** and also gets triggered in the event of a complete withdrawal of XTZ from the account.|
| `distribute` | Handles the **payout of staking rewards** to designated accounts and also handles final settlement on account closing events. |


## Licensing

The DAO Baker is a free software: you can redistribute it and/or modify it under the terms of the MIT License.
The DAO Baker is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the MIT License for more details.
A copy of the MIT License is included along with the DAO framework. See LICENSE.

### Additional Disclaimers

NEITHER THE SOFTWARE NOR ITS CREATORS PROVIDE LEGAL ADVICE AND THIS CODE WAS NOT CREATED TO PROVIDE LEGAL ADVICE OR AS A SUBSTITUTE FOR LEGAL ADVICE. BY USING THIS CODE YOU ALSO AGREE:

a. The creators of the Software and its contributors are not your lawyers.

b. The Software is not a lawyer.

c. Your use of the Software does not, in and of itself, create a legally binding contract in any jurisdiction and does not establish a lawyer-client relationship. Your communication with a non-lawyer will not be subject to the attorney-client privilege and (depending on your jurisdiction) may not be entitled to protection as confidential communication.

d. The dissemination, distribution, or usage of this software shall not constitute the provision of legal advice within your jurisdiction. Unless you are legally authorized and licensed to do so, you will not use the Software to provide or assist in the provision of legal advice.

e. You acknowledge and understand that each jurisdiction has its own particular rules regarding the practice of law. IF YOU USE THIS SOFTWARE TO PROVIDE LEGAL ADVICE YOU MAY BE SUBJECT TO CIVIL AND CRIMINAL LIABILITY. PRACTICING LAW WITHOUT A LICENSE IS A VIOLATION OF CRIMINAL LAW IN SOME JURISDICTIONS. CONSULT A LAWYER LICENSED IN YOUR JURISDICTION IF YOU HAVE ANY QUESTIONS ABOUT WHAT DOES OR DOES NOT CONSTITUTE THE PRACTICE OF LAW.

f. The providers of this software neither warrant nor guarantee this software shall meet the requirements of any particular legal system to form a legally binding contract, nor it it their intention to directly or indirectly facilitate or encourage the unauthorized practice of law.

g. You agree that in order for you to form a legally binding contract that you shall seek legal advice from an appropriately qualified and experienced lawyer within your jurisdiction.
