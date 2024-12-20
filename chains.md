# CountChain: A Decentralized Oracle Network for Counting Systems


## Overview
Blockchain integration in industries like online advertising is hindered by its connectivity limitations to off-chain data. These industries heavily rely on precise counting systems for collecting and analyzing off-chain data. This requires mechanisms, often called oracles, to feed off-chain data into smart contracts. However, current oracle solutions are ill-suited for counting systems since the oracles do not know when to expect the data, posing a significant challenge.

To address this, we present CountChain, a decentralized oracle network for counting systems. In CountChain, data is received by all oracle nodes, and any node can submit a proposition request. Each proposition contains enough data to evaluate the occurrence of an event. Only randomly selected nodes participate in a game to evaluate the truthfulness of each proposition by providing proof and some stake. Finally, the propositions with the outcome of True increment the counter in a smart contract. Thus, instead of a contract calling oracles for data, in CountChain, the oracles call a smart contract when the data is available. Furthermore, we present a formal analysis and experimental evaluation of the system's parameters on over half a million data points to obtain optimal system parameters. In such conditions, our game-theoretical analysis demonstrates that a Nash equilibrium exists wherein all rational parties participate with honesty.

## More Information
1. [Publication](https://arxiv.org/abs/2409.11592){:target="_blank"}

# AdChain: Decentralized Header Bidding


## Overview
Due to the involvement of multiple intermediaries without trusted parties, lack of proper regulations, and a complicated supply chain, ad impression discrepancy affects online advertising. This issue causes up to $82 billion annual revenue loss for honest parties. The loss can be significantly reduced with a precise and trusted decentralized mechanism. This paper presents AdChain, a decentralized, distributed, and verifiable solution that detects and minimizes online advertisement impression discrepancies. AdChain establishes trust by employing multiple independent agents to receive and record log-level data, along with a consensus protocol to validate each ad data. AdChain is scalable, efficient, and compatible with the current infrastructure. Our experimental evaluation, using over half a million ad data points, identifies system parameters that achieve 98% accuracy, reducing the ad discrepancy rate from 20% to 2%. Our cost analysis shows that active nodes on AdChain can generate profits comparable to miners on major blockchain networks like Bitcoin.
## More Information
1. [Publication](https://arxiv.org/abs/2410.16141){:target="_blank"}

