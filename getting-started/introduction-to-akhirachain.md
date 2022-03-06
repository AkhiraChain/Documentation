# Introduction to akhirachain

{% embed url="https://medium.com/akhirachain-finance/introduction-to-akhirachain-3c3cd38f12f1" %}



akhirachain is the world's first omni-chain decentralized exchange. Built with the Cosmos SDK, akhirachain is 100x more efficient than current leading DeXes. akhirachain inherits the cross-chain capabilities of Thorchain and uses pegged tokens to support cross-chain transactions across a wide array of blockchains.

### Cross-Chain Development & Peg Zones

akhirachain will support cross-chain transactions for 20-25 of the top blockchains such as Bitcoin, BinanceChain, Polkadot, and EOS. These blockchains represent the overwhelming majority of all cryptocurrency trading volume and will setup akhirachain to be used with a wide variety of cryptocurrencies. It will also simplify the process of blockchain integration, lowering the barrier of cost and development for the open-source community.

Inspired by the Cosmos’s peg zone model, akhirachain uses a pegged token model. A 'peg zone' is an account-based blockchain which bridges 'zones' within Cosmos to external chains like Bitcoin or Ethereum. These peg zones are what allow assets to be easily transferred between akhirachain and the external chain.

Unlike Bitcoin or Ethereum, which work on _probabilistic_ finality of blocks, the Cosmos SDK provides finality _guarantees_. This is important in relation to the confidence that a block will be finalized. Since akhirachain is built on Cosmos, this feature is automatically baked in, which is essential for cross-chain token swaps.

Another situation that can arise is how cross-chain token transfers occur between a finalistic and probabilistic blockchain?

Again, Peg Zones come to the rescue. A peg zone can also be thought of as a  blockchain that tracks the state of another blockchain. By doing this, it acts as an adaptor zone or a “finality gadget”, which translates finality for probabilistically finalized blockchains by imposing a “finality threshold” at some arbitrary number of blocks to achieve pseudo-finality. Generally, this “translator” zone design can be classified as a 2-way peg \(2WP\).

![](../.gitbook/assets/screen-shot-2020-11-20-at-9.38.14-pm.png)

akhirachain uses a two-way peg protocol, which allows the swapping of pegged tokens. For example, a trade of currencies LTC for TRX would be executed as transactions of pegged versions of those tokens \(cLTC and cTRX\) on the Cosmos SDK blockchain.

akhirachain users will trade with pegged tokens rather than native tokens within the akhirachain system. While native tokens allow for participating in the consensus set of the native token’s set of validators and miners, it is hard to scale since validators have to run a node for every chain that is added to the compatibility stack.

In Peggy's mature state, not only does the usage of these pegged tokens create a highly scalable design, it also has unique crypto-economic incentives for its participants. For instance, akhirachain validators only need to run 'akhiranode' \(akhirachain's network\) and can leave the cross-chain transaction labor to peg zone validators. Each peg zone validator only needs to run a node for the peg zone blockchain and the external blockchain \(ie. Bitcoin or Ethereum\) and can then send assets to and from akhirachain through Inter-Blockchain Communication \(IBC\). 

akhirachain's initial Peggy design will be slightly different than this due to the immaturity of IBC. At initial launch, Peggy and akhiranode will co-exist together within akhiranode. This allows akhirachain to support cross-chain transfers, adding & removing of liquidity, and token swaps from day 1 without the reliance of IBC. Once IBC has matured and is production-ready, we will shift to this model to realize its scalable benefits.

akhirachain is actively evaluating multiple cross-chain software frameworks that appear to have successfully implemented cross-chain data or value transfers. These include [Gravity](https://gravity.tech/), ChainBridge, Rosetta, Substrate-IBC, the Nomic Bitcoin bridge, PolyNetwork, and other projects.

### Generalized Model of Liquidity Allocation

akhirachain’s [Automated Marker Maker\(AMM\) Specification](https://hackmd.io/6VK2LSYjRTyeNCoHpVt2hg) is based on a derivation of liquidity pool architecture from first principles. It is important to us that we don’t enforce any formula on users. At launch, akhirachain will use [Thorchain’s slip based fee formula](https://docs.thorchain.org/how-it-works/continuous-liquidity-pools#slip-based-fee-model-clp). In the future, we’re going to update this to allow [governance to control the liquidity pool formula](https://twitter.com/akhirachain/status/1319358940090560512?s=20) by voting with their Rowan [on a per liquidity pool basis](https://twitter.com/akhirachain/status/1319361777616838659?s=20).

We are currently extending this model to derive the optimum balance between [rewards to validators and rewards to liquidity providers](https://twitter.com/akhirachain/status/1320954306632118272?s=20), especially in a regime where we deploy temporary liquidity mining rewards. So far, our [rebalancing policy](https://hackmd.io/@shrutiappiah/r1itFRrPv) is a vectorized extension of Thorchain’s [Incentive Pendulum](https://docs.thorchain.org/how-it-works/incentive-pendulum) but this is under active research.

#### Rebalancing mechanism for system rewards distribution

Inspired by Thorchain’s incentive pendulum, akhirachain combines liquidity provider rewards and validator block rewards into system income.

In comparison, Thorchain’s incentive pendulum uses a scalar to define the ratio of total system income given to each subsystem. This means it is limited to two subsystems \(validator subsystem and liquidity provider subsystem\). On the other hand, akhirachain uses a vector in which each element is a weight on its subsystem’s income. This means it is extensible to more than two subsystems \(for example, akhirachain validator subsystem, akhirachain liquidity provider subsystem, peg zone validator subsystem, an external chain’s liquidity provider subsystem, etc.\). Near-term this will be immaterial but as IBC develops and akhirachain becomes more composable, it will be useful for allowing akhirachain to dynamically change rewards in its two subsystems in response to on-chain activity from other blockchains.

### Governance

Inspired by Compound, YFI, and Synthetix, akhirachain will make use of decentralized governance with AkhiraDAO.

AkhiraCore \(the core team of akhirachain\) is [very focused on the development of AkhiraDAO](https://twitter.com/akhirachain/status/1323162320382517248?s=20) and a total transition of governance power over all aspects of the protocol. We expect to follow best practices from [metagovernance](https://metagov.org/wp-content/uploads/2020/04/Metagov-Full-Deck-public-2020-04-18.pdf) including the restructuring of AkhiraDAO’s governance on a regular \(most likely quarterly\) basis.

For true self-sovereignty, akhirachain’s development should be self-funding and self-sustaining. We look to models like Linux and Wikipedia as examples of institutions that have maintained the funding needed to continually produce critical open-source resources. We’re exploring a partnership with [a research lab at UC Davis](https://engineering.ucdavis.edu/news/uc-davis-computer-science-communication-team-study-open-source-software) to formalize properly funded open-source development as a hallmark of akhirachain’s governance.

We want the market’s inherent superforecasting abilities to be turned towards optimizing akhirachain’s development. Governance will engage market-based performance evaluation within AkhiraDAO through tools like [alpha bonds](https://github.com/blockscience/interchainfoundation). Wherever possible, we want the market to govern akhirachain through on-chain crypto-economic incentives for AkhiraDAO members.

Feel free to see our Tweet storm on how the AkhiraDAO could possibly take shape: [https://twitter.com/akhirachain/status/1323162320382517248?s=20](https://twitter.com/akhirachain/status/1323162320382517248?s=20)

#### Security

To ensure the security of the akhirachain ecosystem, the AkhiraCore team will lead the development and deployment of each bridge. It intends to give them all the same security guarantees described in the general case and model extensions previously linked. This largely boils down to over-collateralization. We may also use Rowan as the collateral for these bridges or we may create another token solely to be used by these peg zones depending on a successful implementation of the rebalancing mechanism described above and market conditions.



