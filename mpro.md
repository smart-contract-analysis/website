# MPro: Combining Static and Symbolic Analysis for Scalable Testing of Smart Contracts


## Overview
Smart contracts are executable programs that enable the building of a programmable trust mechanism between multiple entities without the need of a trusted third-party. At the time of this writing, there were over 10 million smart contracts deployed on the Ethereum networks and this number continues to grow at a rapid pace. Smart contracts are often written in a Turing-complete programming language called Solidity, which is not easy to audit for subtle errors. Further, since smart contracts are immutable, errors have led to attacks resulting in losses of cryptocurrency worth 100s of millions of USD and reputational damage. Unfortunately, manual security analyses do not scale with size and number of smart contracts. Automated and scalable mechanisms are essential if smart contracts are to gain mainstream acceptance. Researchers have developed several security scanners in the past couple of years. However, many of these analyzer either do not scale well, or if they do, produce many false positives. This issue is exacerbated when bugs are triggered only after a series of interactions with the functions of the contractunder test. A depth-n vulnerability, refers to a vulnerability that requires invoking a specific sequence of n functions to trigger. Depth-n vulnerabilities are time-consuming to detect by existing automated analyzers, because of the combinatorial explosion of sequences of functions that could be executed on smart contracts.


In this project, we present a technique to analyze depth-n vulnerabilities in an efficient and scalable way by combining symbolic execution and data dependency analysis. A significant advantage of combining symbolic with static analysis is that it scales much better than symbolic alone and does not have the problem of false positive that static analysis tools typically have. We have implemented our technique in a tool called MPro, a scalable and automated smart contract analyzer based on the existing symbolic analysis tool Mythril-Classic and the static analysis tool Slither. We analyzed 100 randomly chosen smart contracts on MPro and our evaluation shows that MPro is about n-times faster than Mythril-Classic for detecting depth- n vulnerabilities, while preserving all the detection capabilities of Mythril-Classic.


## More Information
1. [Publication](https://arxiv.org/pdf/1911.00570.pdf){:target="_blank"}
2. [Code](https://github.com/QuanZhang-William/M-Pro){:target="_blank"}
