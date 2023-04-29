
<p align="center">
  <p align="center">
    <img src="https://avatars3.githubusercontent.com/u/53176002?s=200&v=4" height="100" alt="Blockcore" />
  </p>
  <h3 align="center">
   Blockcore White Paper
  </h3>
</p>

## Table of contents
*   [Introduction](#introduction)
*   [Architecture](#architecture)
*   [Scalability](#scalability)
*   [Technical details](#technical-details)
*   [Roadmap](#roadmap)
*   [Team](#team)
*   [Legal and regulatory considerations](#legal-and-regulatory-considerations)
*   [Release Process](#release-process)
*   [Conclusion](#conclusion)
*   [References](#references)


# **Introduction**

**W**elcome to Blockcore's white paper for its cutting-edge and open-source blockchain project. The aim of Blockcore is to create free and open-source solutions for modern decentralized societies with the vision to "decentralize everything". By providing the building blocks for decentralized societies, Blockcore's software can make existing centralized systems redundant. Decentralization in the context of Blockcore refers to distributing power, control, and authority away from centralized organizations, giving individuals and communities greater control over data, assets, and decision-making. Blockcore's vision aligns with the principles of Web5, which advocates for a more decentralized and user-centric internet.

Blockcore’s team of experienced blockchain developers and engineers took this initiative with the mission of empowering users to build unique blockchain solutions using a wide range of software tools, including Block Explorer, Block Indexing, Block Analytics, Wallets, API Wallet Service, Atomic Swaps, Developer Tooling, and Documentation.

The Blockcore’s platform offers a decentralized web node and decentralized identifiers, all designed to enhance the capabilities of the platform and to make it accessible to a wide range of users. Blockcore's objectives include continuing the development of the C# Stratis full node, maintaining the C# Bitcoin full node, supporting projects and teams using the underlying technology, extending the technology by building developer and user tools, providing a forum for developers and teams to collaborate and to improve the technology, and building relationships with potential sponsors and partners to boost the pace of development.

Blockcore's guiding principles emphasize collaboration, contribution to open-source software, making it easy for everyone to contribute to the ecosystem, and encouraging projects to adopt Blockcore technology to strengthen the platform. We believe that our platform, Blockcore, can drive innovation and foster a collaborative environment for blockchain development. Committed to staying at the forefront of Bitcoin and blockchain technology through continuous development and improvements, let us endeavor together for what we can accomplish through Blockcore and blockchain technology.

# **Architecture**

Blockcore is an ecosystem composed of different parts, with blockchain node software as its foundation.

![image](https://user-images.githubusercontent.com/6504337/234680656-7bbd9b24-c16a-4035-bca4-6c8c0c826637.png)


This software is used to run a UTXO-based blockchain with Bitcoins Script language, similar to Bitcoin, with added support for Proof-of-Stake, and it also supports Proof-of-Work blockchains. Each node has the full data of the blockchain, which normally does not contain much additional data other than limited OP_RETURN data, and nodes are not exposed to public consumption.

The indexer is responsible for building a queryable database of the history of the blockchain, for specific addresses, transactions, and blocks. On top of the indexer, Blockcore has built various user interface surfaces, such as the explorer, which allows insight into the blockchain, including rich lists, network nodes, known public addresses, and more.

Blockcore also offers different software options for users, including a non-custodial wallet that runs in the web browser and is distributed on add-ons stores for easy discovery, installation, and automatic updates. This extension relies on the indexer to access blockchain data. The Blockcore Hub is a full-node wallet, which is the optimal wallet for advanced users performing Proof-of-Stake operations, as it downloads the entire blockchain for improved privacy.

Blockcore also offers a tipping-bot software called Blockcore Tipbot, which allows users to give and receive tips in the form of coins and tokens easily. The tipbot is a custodial service, meaning that the keys do not belong to the individual users, so it is only recommended for smaller amounts. Users can withdraw from their tipbot balance into Blockcore Hub or Blockcore Extension wallets.

Additionally, Blockcore offers a server software called Blockcore Vault, which allows for distributed data storage and sharing. The software implements open standards for decentralized identity (DID) and can store a user's verifiable credentials, including private direct messages, NFTs, receipts from purchases, favorite music, videos, and more. The software supports both public (unencrypted) and private (encrypted) information to be hosted.

Meanwhile, Blockcore has cross-system documentation for all of its software, in combination with tooling for generating new blockchains and more. It also runs a community provided and supported server infrastructure of blockchain nodes, tipbots, indexers, explorers, and more.

# **Scalability**
Blockcore, a novel approach to addressing the scalability issue in cryptocurrencies, offers multiple solutions to the limitations of traditional blockchain systems like Bitcoin. These solutions work together to mitigate the problems associated with transaction volumes, block sizes, and centralization of mining power to make the platform more attractive for businesses and organizations. Here is a summary of the key features that address these issues:

1. Configurable private blockchains: Blockcore allows organizations to create and to manage their own private blockchains, tailoring block sizes to suit their specific needs and available resources. This customization enables businesses to optimize their blockchain's performance without being constrained by a single, global blockchain.

2. Host chain and dedicated ledgers: Blockcore operates on a host chain from which businesses can deploy their own ledgers based on their specific requirements. This structure provides the versatility of an extensive 2.0 platform combined with the full control of a private chain, which is secured by the host blockchain but managed by the owning organization.

3. Proof-of-Stake consensus: Blockcore employs a Proof-of-Stake (PoS) consensus mechanism, aligning the interests of end-users (businesses) and network security providers (full nodes). This allows businesses to run their own nodes without the overheads associated with specialized mining hardware, reducing the barriers to entry and preventing centralization of mining power.

4. Anti-bloat measures: To ensure the main chain remains lightweight and efficient, Blockcore implements a series of measures to combat bloating. This ensures that the host chain's primary purpose is to secure child chains, keeping the overall system streamlined and manageable.

In summary, Blockcore addresses the scalability and the centralization issues faced by traditional blockchain systems like Bitcoin through the use of configurable private blockchains, a host chain with dedicated ledgers, a PoS consensus mechanism, and anti-bloat measures. These features make Blockcore an attractive option for businesses and organizations seeking a more efficient, secure, and adaptable blockchain solution.


# **Technical Details**

Blockcore is a versatile and flexible platform for building Layer 1 consensus networks based on the Bitcoin protocol. This platform is built on .NET and is entirely written in C#. It provides a wide range of tooling to support user's blockchain, including a Block Explorer, Block Indexing, Block Analytics, Wallets, API Wallet Service, Atomic Swaps, Developer Tooling, and Documentation. Blockcore aims to maintain an alternative C# Bitcoin implementation based on the NBitcoin and Stratis projects.

Blockcore is a blockchain platform that supports both Proof of Work (PoW) and Proof of Stake (PoS) consensus mechanisms. PoW is used to mine new blocks during the initial stage of the network, while PoS is used to validate new blocks and to secure the network over time. In Blockcore, PoW and PoS are combined in a hybrid consensus mechanism, which enables the network to benefit from the advantages of both approaches. The PoW component of the consensus mechanism is used to create new blocks, while the PoS component is used to validate the new blocks and to secure the network.

In the PoW component, miners compete to solve a cryptographic puzzle to create new blocks. The difficulty of the puzzle is adjusted dynamically to maintain a consistent block time. The PoW component is designed as ASIC-resistant, which ensures that miners with specialized hardware do not gain an unfair advantage over other miners.

In the PoS component, validators are chosen based on the amount of tokens they hold and the duration of time they are willing to stake their tokens. Validators are responsible for validating new blocks and securing the network. In PoS, the more tokens a validator holds and stakes, the higher the chance of being chosen as a validator. Blockcore's PoS mechanism uses a variant of the delegated proof-of-stake (DPoS) approach, in which validators are elected by token holders through a voting process. The DPoS approach ensures the network is controlled by a small group of trusted validators increasing the network's security and the scalability.

Blockcore's blockchain architecture is designed as modular and flexible, allowing developers to customize the consensus mechanism to meet the specific needs of their use case. The platform provides a range of APIs and SDKs that enable developers to build and to deploy blockchain applications easily. With its hybrid PoW/PoS consensus mechanism, Blockcore provides a secure and scalable network for developers to build blockchain applications while maintaining an alternative C# Bitcoin implementation.

### What Are PoW and PoS?

Proof of Work (PoW) and Proof of Stake (PoS) are two consensus algorithms used in blockchain networks to validate transactions and to create new blocks.

Proof of Work (PoW) was a revolutionary concept when introduced in Bitcoin, as it provided a novel solution to the Byzantine Generals' Problem, ensuring consensus and trust in a decentralized network without the need for a central authority. The PoW algorithm relies on miners contributing computational power to solve complex mathematical puzzles, which helps maintain the security and the integrity of the blockchain. This process incentivizes miners through block rewards and transaction fees, encouraging honest behavior and fostering a robust network. Additionally, the PoW algorithm makes it computationally expensive to alter the blockchain's history, further enhancing the security and the immutability of the system. PoW laid the foundation for the growth of the cryptocurrency ecosystem and inspired many innovations in blockchain technology.

Proof of Stake (PoS) emerged as an alternative consensus mechanism, building on the foundations laid by Proof of Work while introducing new innovations. PoS is designed to provide consensus and to maintain the security of a decentralized network by having validators, or stakeholders participate in the process of creating new blocks. In PoS, validators are chosen based on the amount of cryptocurrency they hold and "stake" as collateral. This approach incentivizes validators to act honestly, as they have a vested interest in the network's success and risk losing their stake if they behave maliciously. By making it costly for validators to acquire a majority stake in the network, PoS helps maintain the security and the decentralization of the system. Furthermore, PoS lowers the barriers to entry for participation, as it does not require specialized or high-performance hardware, only a stable device with an internet connection and the minimum staking requirements. This fosters a more accessible validator ecosystem, encouraging a wide range of community members to contribute to the network's growth and development.

Overall, the main difference between PoW and PoS is the way the new blocks are created and validated. PoW relies on computational power, while PoS relies on ownership and stake in the network.

### Definitions and Explanations

#### Coinbase

It is a special transaction that is produced by the miners (the producers of PoW blocks) and contains information about the block.

#### Coinstake

This is a special transaction that is produced by the stakers (the producers of PoS blocks) and contains the transactions' inputs and outputs of coins used to create a block. A coinstake's input can be split in to several outputs, this is to reduce the size of a staking output. Splitting a big output to many smaller outputs increases the chance of producing new blocks.  

#### Stake Mine Confirmations

They are the minimum confirmations required for a coin to be good enough to participate in staking. They must be equal or greater than MaxReorg, and this is to discourage attackers to stake in isolation and then to force a reorg.

#### MaxReorg

It is the long reorganization protection or the maximal length of reorganization that a node is willing to accept. The reason to prevent long reorganization is to prevent "history attack" or simply stating to prevent the reuse of old spent coins from creating a longer chain in isolation and to cause large reorgs.

Honest nodes will not switch to a chain that has forked earlier than MaxReorg, and because stake mine confirmations will not allow to reuse coins before MaxReorg then staking in isolation cannot cause long reorganizations.

#### Coin Maturity

It is the number of confirmations a newly found coinstake needs to be buried under before it can be spent (not to be confused with stake mine confirmations for staking).

#### Proven Headers
 
These are headers that contain all the information that is needed to validate a coinstake. Proven headers are used as a `headers first` approach, where the node will first download the headers of blocks. Only if the header is valid then the node will fetch the entire block for full validation. The full Proven Headers specification can be found [here](/Features/ProvenHeaders.md)

#### Target Difficulty

It is defined as the difficulty target for the next block, or how hard it will be to find the next valid Kernel to satisfy the target difficulty.

#### Kernel Hash

It is a sha256 hash created from a number of parameters corresponding to the coinstake. A valid stake kernel hash satisfies the target difficulty.

#### Target Spacing

Target spacing is the expected block time in seconds, or how often we expect the network to produce a block. The target spacing is multiples of the Mask.  

#### Future Drift

Future drift is maximal allowed block's timestamp difference over adjusted time. We set the future drift to be a fixed value of 15 seconds which is close to the Mask value.

#### Mask

It is a bit mask for the coinstake header's timestamp, and it is used to decrease granularity of timestamp. This corresponds to the number of blocks that can be produced in a given time span. For example, if the bit mask is 15 (0x0000000F) then a valid coinstake's timestamp must be divisible by 16.

#### Stake Modifiers

A stake modifier forms a chain of hashes made from the previous stake modifier and the kernel all the way back to the first PoS block.
It is used to introduce an additional input parameter to the Kernel calculations, in order to scramble computation to make it extremely difficult to pre-compute future proof-of-stake.

### How It Works on Blockcore

#### Hashing a Valid Kernel

In Proof of Stake (PoS) cryptocurrencies, the staking process is an essential part of maintaining the network's security and functionality. Instead of relying on the energy-intensive Proof of Work (PoW) system, PoS selects validators (those who can create new blocks) based on the amount of cryptocurrency they hold and are willing to "stake" as collateral.

The heart of the staking process is finding a valid coinstake, which occurs when the timestamp mask is valid. The process involves iterating over a node's stakeable outputs (matured outputs beyond MaxReorg) and hashing each output with several parameters to create the kernel. The goal is to find a kernel hash that is below a certain target to be considered valid. The target is adjusted by a factor proportional to the number of coins in a UTXO (unspent transaction output), called the weighted target. This gives a better chance for bigger outputs to find a valid kernel hash and to create a block.

Here is a summary of the process:

1. A node iterates over its stakeable outputs, hashing each output with the parameters: previous StakeModifier, output hash, output position, and new coinstake current time.
2. This produces a kernel hash.
3. The target is calculated, which is the number the kernel hash needs to be below to be considered valid.
4. The target is adjusted based on the number of coins in a UTXO, creating the weighted target.
5. If the kernel hash is below the weighted target, the coinstake is considered valid and is used to create a new block.

This staking process ensures the PoS system remains secure and decentralized. The more coins users hold, the more likely they are to create a valid coinstake and to participate in the validation process. This incentivizes users to support the network, to maintain consensus, and to prevent malicious behavior.

#### The Importance of Synchronizying Time Correctly (Future Drift)

Each node has a consensus rule of a fixed interval of 15 seconds that will enforce how far in the future it will accept blocks. Blocks with a timestamp that is 15 seconds further than local nodes' current datetime are not rejected, but such rejected blocks are not considered invalid. In case our local node just had the wrong time in comparison to the network and the network accepted such a block, our local node would fork away form the network consensus. Therefore, it is crucial that nodes on the network to participate in full consensus rules validation and are on the same UTC datetime. To achieve this, we use the computer's local current time, and double check it against all connected peers' datetime (when a peer first connects, it will advertise its current UTC datetime) giving the datetime samples for outbound nodes 3x more weight in the measurements. This is also to prevent a certain attack on a node, where an attacker initiates many inbound connections and effects our local nodes' average time. If the local time and peers' average time do not match, the node will print out a warning message and defaults to the peers' time.

#### Block Signatures (Why Sign a Block With the Private Key Owning the UTXO?)

The coinstake that finds a valid kernel and thus is selected to create a block is used to proof ownership of the UTXO by providing the signature that spends the outputs. However, such an output does not have cryptographic strong link to the block itself, meaning an attacker can take the valid coinstake utxo and can put it in another block, which the attacker has created and propagates that to the network. The attacker could then censor transactions at will. By signing the block with the same key that owns the UTXO, peers can validate if the block is created by the owner of the coinstake. The block signature is attached at the end of the serialized block and is not a part of the header hash.

#### How is the Next Difficulty Target Calculated?

The calculation of the next target is based on the last target value and the block time (a.k.a. spacing). For example, it is the difference in timestamp of this block and its immediate predecessor. Meanwhile, the target changes every block, and it is adjusted down. for instance, it shifts towards harder to reach or more difficult if the time to mine last block is lower than the target block time. It is adjusted up if it takes longer than the target block time. The adjustments take place in a way the target is moving towards the target-spacing exponentially (expected block time), so even a major change in the mining power on the network is fixed by retargeting relatively fast.

#### Changes Made in POSv4

The following changes are made in POSv4:

- The first change is the removal of the timestamp from the transaction serialization. This makes PoS transactions serialize the same as Bitcoin transactions. The benefit is that it is easier to use various blockchain tools that are made for Bitcoin. That timestamp was used in the kernel hash; however, the kernel hash was defaulting to the header timestamp so there was no need to serialize the timestamp also in each transaction.

- The second change is the removal of the coinstake time from the kernel hash calculations. When checking the kernel validity, a few parameters are hashed together to find a valid kernel. Previously the timestamp of the utxo that was being spent was also included in that hash.
However, it did not provide additional value because the previous outpoint was used, and that made it unique.

#### Coldstaking (Multisig Staking) 

Coldstaking is a mechanism that eliminates the need to keep the coins in a hot wallet. When setting up coldstaking, a user generates two wallets or two different private keys. One key is only used for staking or creating other coinstakes, and the other key is used for spending the coins. Cold staking still requires a fully synchronized node running and connected to the network. The full Coldstaking specification can be found [here](/Features/ColdStaking.md).

### Weaknesses

#### NAS (Nothing at Stake)

Nothing-at-stake is a theoretical security issue in proof-of-stake consensus systems in which validators have a financial incentive to mine on every fork of the blockchain that takes place. This is disruptive to consensus and potentially makes the system more vulnerable to attacks. Assuming the majority of staking power (coins at stake) are honest, an attacker who exercises NAS can make it very difficult for honest nodes to know what the chain with the total honest staking power is (even if the attacker stakes on forks with less total stake, this can confuse nodes in IBD). However, this attack is not obvious to execute as an attacker would have to be economically invested in the chain in order to execute the attack and will be risking the value of the attacker's coins.

https://golden.com/wiki/Nothing-at-stake_problem
https://medium.com/coinmonks/understanding-proof-of-stake-the-nothing-at-stake-theory-1f0d71bc027

#### Stake Grinding
 
Stake grinding is a class of attack in which a validator performs some computation or takes some other steps to try to bias the randomness in his or her favour. In a stake grinding attack, the attacker has a small amount of stake and goes through the history of the blockchain and finds places, where his or her stake wins a block. In order to consecutively win, the attacker modifies the next block header until some of his or her stakes win once again. https://dyor-crypto.fandom.com/wiki/Grinding_Attack
  
#### The IBD problem

Proof of stake networks are more vulnerable during Initial Block Download (IBD). During initial synchronization a local node will find peers to synchronize the consensus history. If a fake chain is presented, as a fake chain is any chain that is not the chain accepted by the majority of stakers, a local node will not rewind away from the fake chain if its fork is beyond the maxreorg parameter and will result in the local node being stuck on the incorrect chain. To address this issue the local node uses checkpoints, regularly hard coding into the software of the appropiate chain. A node only accepts outgoing connections to mitigate that attack during IBD.

#### Known Issues of PoS

PoS is considered less decentralized than PoW due to the following factors:
- Complexity: If the PoS protocol is more complex, more unknown attacks may be found. 
- The IBD problem: This means in some cases users need to use some external trust in order to find the best chain.
- In case of a 51% attack: A user's intervention is needed like checkpoints in order to recover.
- IBD: the reliance on checkpoints is for IBD.
- Time synchronization: This is the requirement a majority of nodes have for the correct global time.


# **Roadmap**

Short-term goals are as follow:
- To release Blockcore with new features and improvements, such as Schnorr signatures and Taproot integration.
- To launch Blockcore's mainnet with a hybrid PoW/PoS consensus mechanism.
- To development an improved Block Explorer with advanced search capabilities and real-time transaction data.
- To integrate additional blockchains to the Blockcore platform to expand its interoperability.
- To expand the Blockcore developer community through hackathons, bounties, and developer conferences.

Milestones are enumerated below:
- The completion of Schnorr signatures and Taproot integration in Q3 2023.
- The launch of Blockcore's mainnet in Q4 2023.
- The release of the improved Block Explorer in Q1 2024.
- The integration of additional blockchains to the Blockcore platform throughout 2024.
- The expansion of the developer community through hackathons, bounties, and developer conferences throughout 2024.

Long-term goals are as follow:
- To develop a decentralized application (Dapp) ecosystem on the Blockcore platform.
- To continue improvement of the hybrid PoW/PoS consensus mechanism for increased security and scalability.
- To expand the Blockcore's ecosystem through partnerships and collaborations with other blockchain projects.
- To integrate privacy features into the Blockcore's platform to enable anonymous transactions.
- To support hardware wallets and multi-signature wallets.

Milestones are listed below:
- The development of a Dapp ecosystem on the Blockcore's platform throughout 2024.
- The continuation of improvement of the hybrid PoW/PoS consensus mechanism throughout 2024 and beyond.
- The expansion of the Blockcore's ecosystem through partnerships and collaborations throughout 2024 and beyond.
- The integration of privacy features into the Blockcore's platform in 2025.
- The support provided for hardware wallets and multi-signature wallets in 2025.

Resources:
- Funding through a combination of coin sales, venture capital, and grants.
- Recruiting and retaining talented developers and engineers.
- Building partnerships with other blockchain projects and businesses.
- Collaborating with universities and research institutions to advance the technology.

# **Team**

Blockcore is an open-source project started by a talented group of blockchain developers and engineers, including Dan Gershony, Sondre Bjellås, David Gershony, Milad Raeisi and others. Each team member brings unique experience and expertise in blockchain development, software engineering, project management, and business strategy to the project.

Dan Gershony is a seasoned entrepreneur with extensive experience in blockchain technology, DApps, and DeFi. Sondre Bjellås is a software engineer and blockchain developer with a passion for open-source projects, and he has successfully launched the City Chain blockchain. David Gershony is a software engineer and blockchain developer with expertise in developing blockchain-based solutions for various industries. Milad Raeisi is a blockchain expert with experience in digital marketing and business development.

The team came together with the shared vision of creating a fully integrated platform for building custom blockchains that could support a wide range of use cases. They recognized the need for a comprehensive and user-friendly platform that would support the development of blockchain-based solutions for businesses and developers.

Blockcore's vision is to become the leading platform for blockchain development, providing a reliable and scalable infrastructure that enables businesses and developers to build and to deploy decentralized applications with ease. The team is committed to developing an open-source platform that is accessible, user-friendly, and customizable, with a focus on security, performance, and innovation. The team aims to empower the blockchain community with the tools and resources needed to succeed in this exciting and rapidly evolving field. The team always welcomes new community members, and it encourages developers and businesses to join in building the future of blockchain technology.

# **Legal and Regulatory Considerations**

Blockcore's official website (https://blockcore.net) contains its current terms and conditions, which users must adhere to when accessing or using the products or the services. As Blockcore continuously develops new software and features, the terms and the conditions are subject to change. To stay up to date on any modifications, users can refer to the rules change log, which is also available on the website. The log provides a record of any updates or changes made to the terms and the conditions, which helps users understand how these modifications may impact their use of Blockcore's products and services. It is important for users to review the rules change log periodically to ensure compliance with the current terms and conditions. By accessing or using Blockcore's products or services, users agree to bound by the current terms and conditions as posted on the website.

# **Release Process**

This process describes the steps that are required to go through the release of new and updated packages and software.

### RocksDB Native and NuGet Package

1: [https://github.com/block-core/blockcore-rocksdb-native](https://github.com/block-core/blockcore-rocksdb-native)

2: [https://github.com/block-core/blockcore-rocksdb](https://github.com/block-core/blockcore-rocksdb)

If there is a new release of RocksDB, then RocksDB native must be built and released. The next step is to build the NuGet package, then to release it when it is ready. After releasing on NuGet, at least a 10-minute wait is required before proceeding to ensure scanning, approval and indexing of the package are completed.

### Blockcore NuGet Packages

3: [https://github.com/block-core/blockcore](https://github.com/block-core/blockcore)

The main repository that contains the majority of our NuGet packages, must be updated to new version. After a build is completed from the `master` branch, then a new release will be added to the repository, in draft state. It is important to verify the NuGet packages locally by downloading and installing, if possible. To publish new version of NuGet packages to the NuGet website, simply users should edit the new draft release and publish it. This will automatically trigger a workflow that will publish the NuGet packages. Again, it is important to wait at least 10 minutes before proceeding, as the NuGet packages must be scanned for malware, approved and indexed.

### Blockcore Features

4: [https://github.com/block-core/blockcore-features](https://github.com/block-core/blockcore-features)

We maintain some custom features that extend the basic functionality, such as upgrading the version number, performing a build, and publishing the draft release. The source code has a reference to Blockcore NuGet packages in the pattern "1.1.\*", which means each build will always take the latest one available. There is no need to manually update NuGet packages from Visual Studio, except of course other third party packages that might need to be updated. It is mandatory to wait at least 10 minutes before proceeding, due to NuGet scanning, approval and indexing.

### Blockcore Reference Nodes

5: [https://github.com/block-core/blockcore-nodes](https://github.com/block-core/blockcore-nodes)

We maintain a multi-node that can be utilized to run all the Blockcore-based blockchains using a single package. This is to upgrade the version number, to perform a build, and to publish the draft release. The source code has reference to Blockcore NuGet packages in the pattern "1.1.\*", which means each build will always take the latest one available. There is no need to manually update NuGet packages from Visual Studio, except of course other third party packages that might need to be updated. When the draft release is published, the workflow will automatically build and publish container images to Docker Hub.

Image: [https://hub.docker.com/repository/docker/blockcore/node-multi](https://hub.docker.com/repository/docker/blockcore/node-multi)

### Blockcore Indexer

6: [https://github.com/block-core/blockcore-indexer](https://github.com/block-core/blockcore-indexer)

Users should add any new network NuGet packages, if new blockchains have been added. When the draft release is published, the workflow will automatically build and publish container images to Docker Hub.

Image: [https://hub.docker.com/repository/docker/blockcore/indexer](https://hub.docker.com/repository/docker/blockcore/indexer)

### Blockcore Explorer

7: [https://github.com/block-core/blockcore-explorer](https://github.com/block-core/blockcore-explorer)

Users should update the version and verify if there is any NPM packages that should be updated on the UI project. When the draft release is published, the workflow will automatically build and publish container images to Docker Hub. The Explorer does not depend on the network NuGet packages and does not need to be updated for every new blockchain.

Image: [https://hub.docker.com/repository/docker/blockcore/explorer](https://hub.docker.com/repository/docker/blockcore/explorer)

### Blockcore TipBot

8: [https://github.com/block-core/blockcore-tipbot](https://github.com/block-core/blockcore-tipbot)

The TipBot is hosted by Blockcore as a community service, but we advice teams to use their own dedicated tipbot for individual blockchains. The TipBot does not depend on the network NuGet packages and does not need to be updated for every new blockchain.

### Blockcore Hub

9: [https://github.com/block-core/blockcore-hub](https://github.com/block-core/blockcore-hub)

Blockcore Hub requires the multi-node to be released first, it embeds the full node software. Users should upgrade packages and version, then publish the draft release after build is complete.

### Chains Configurations

10: [https://github.com/block-core/chaininfo](https://github.com/block-core/chaininfo)

The Blockcore software utilizes a hosted server for configuration. This makes it possible to update configurations of software without re-installations and updated releases. It is the responsibility of individual blockchains to maintain their own configurations, but the Blockcore team will support and help with instructions. The configurations are published on the website: [https://chains.blockcore.net/](https://chains.blockcore.net/).


# **Conclusion**

In conclusion, this whitepaper provides a comprehensive overview of the Blockcore blockchain platform, which utilizes both proof-of-work (PoW) and proof-of-stake (PoS) consensus algorithms. The Blockcore platform has been designed with the goal of providing a secure, scalable, and decentralized blockchain infrastructure that can support a wide range of decentralized applications.

One of the core principles of the Blockcore's platform is the commitment to open-source development, which is reflected in the platform's architecture, codebase, and community-driven governance model. By leveraging the power of open-source development, the Blockcore community is able to collaborate and to innovate more effectively, resulting in a more robust and resilient blockchain ecosystem.

Moving forward, the Blockcore community is dedicated to continuing to improve and to enhance the platform through ongoing research, development, and community engagement. We believe that by working together and leveraging the collective expertise of the community, we can build a truly decentralized and resilient blockchain infrastructure that will enable the next generation of decentralized applications and services.

# **References**

#### Older White Papers  
POS Whitepaper - [pos.pdf](/pos-whitepapers/pos.pdf)  
POSv2 Whitepaper - [posv2.pdf](/pos-whitepapers/posv2.pdf)  
POSv3 Whitepaper - [posv3.pdf](/pos-whitepapers/posv3.pdf)  

#### Additional References  
https://en.bitcoin.it/wiki/Proof_of_Stake  
Bitcointalk discussion on the issues of POS https://bitcointalk.org/index.php?topic=1382241.0  
https://github.com/libbitcoin/libbitcoin-system/wiki/Proof-of-Stake-Fallacy  
http://earlz.net/view/2017/07/27/1904/the-missing-explanation-of-proof-of-stake-version  
https://www.reddit.com/r/Bitcoin/comments/1oi7su/criticisms_of_proofofstake/  
https://blog.ethereum.org/2014/07/05/stake/  
https://eprint.iacr.org/2018/248.pdf  
http://tselab.stanford.edu/downloads/PoS_LC_SBC2020.pdf  


#  **Updated:** 
April 28, 2023 

#  **Version:** 
Draft 1
