# FAQ

## What is ROWAN and what is eROWAN?

**ROWAN** will be the functional token of the akhirachain network. akhirachain derives its internal asset price from CLPs and uses ROWAN as the settlement token. Traders must directly or indirectly purchase Rowan in order to execute trades against CLPs. For example, the USDC:BTC internal price is calculated using the USDC:RWN and RWN:BTC CLPs. ROWAN can be used for a variety of different actions within the akhirachain ecosystem, including: 

* To stake a node and earn block rewards
* To delegate to a staked node and earn a commission of block rewards.
* To execute a swap from one token to another. Swaps will cost fees, of which are paid via ROWAN.
* To add liquidity to a pool and earn swap fees accrued within that pool. 

For more details on the usage of ROWAN, please refer here \(Casey to input medium article\). 

**eROWAN** is the equivalent token of ROWAN on the Ethereum network. Users are able to transfer their ROWAN to eROWAN between the Ethereum and akhirachain networks via Peggy. 

## How can I acquire ROWAN and/or eROWAN?

\(Taylor to fill out\)

## How can I setup a akhirachain address in order to acquire ROWAN and use the akhirachain-DEX?

There are a few different ways you can setup a akhirachain address. This address is needed to be able to acquire any akhirachain native token \(including ROWAN and all pegged tokens in the akhirachain ecosystem\). In order to get a akhirachain address, you can:

1. Use the akhirachain-DEX-UI and use our Keplr Wallet integration to setup a new akhirachain address. For directions on this, please refer to our instructions here. \(Casey to input link\).
2. Use [ruby](https://www.ruby-lang.org/en/documentation/installation/) to run the below two commands:
   1. `rake "keys:generate:mnemonic"` - This will generate a mnemonic for you.
      1. **Important:** write this mnemonic phrase in a safe place. It is the only way to recover your account if you ever forget your password.
   2. Take this generated key and run: `rake "keys:import[<moniker>]"`
      1. This will give you your newly generate akhirachain address.

## How can I view my eROWAN in my MetaMask Wallet?

\(Taylor to fill out\)

## How can I convert my eROWAN to ROWAN?

In order to convert your eROWAN to ROWAN, you will use Peggy. Find out more information about Peggy [here](https://docs.akhirachain.finance/core-concepts/al-jabaal). In order to utilize this functionality, we have put a front-end in place for you to easily convert your Ethereum assets into akhirachain assets \(in this case, your eROWAN into ROWAN\).  For step-by-step directions on how to do this via our Front-end portal, reference here \(Casey to input link to FE guide here\). 

## Where can I acquire ROWAN?

\(Taylor to fill out\)

