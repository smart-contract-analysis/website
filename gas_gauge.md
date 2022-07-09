# Gas Gauge: A Security Analysis Tool for Smart Contract Out-of-Gas Vulnerabilities


## Overview
In recent years, we have witnessed a dramatic increase in the adoption and application of smart contracts in a variety of contexts. However, security vulnerabilities pose a significant challenge to the continued adoption of smart contracts. An important and pervasive class of security vulnerabilities that afflicts Ethereum smart contracts is the gas limit DoS on a contract via unbounded operations. These vulnerabilities result in a failed transaction with an "out-of-gas" error and are often present in contracts containing loops whose bounds are affected by end- user input. To address this issue, we present Gas Gauge, a tool aimed at detecting Out-of-Gas DoS vulnerabilities in Ethereum smart contracts. The Gas Gauge tool has three major components: The Detection Phase, Identification Phase, and Correction Phase. The Detection Phase component consists of an accurate static analysis approach that finds and summarizes all the loops in a smart contract. The Identification Phase component uses a white-box fuzzing approach to generate a set of inputs that causes the contract to run out of gas. Lastly, the Correction Phase component uses static analysis and run-time verification to predict the maximum loop bounds consistent with allowable gas usage and suggest appropriate repairs to the tool’s users. Each part of Gas Gauge can be used separately or all together to detect, identify and help repair contracts vulnerable to Out-of-Gas DoS vulnerabilities. 

Gas Gauge was tested on 1,000 real-world solidity smart contracts. When compared to seven state-of-the-art tools, we show that Gas Gauge is the most effective (i.e., has no false positives and false negatives) while being competitive in terms of efficiency.
## More Information
1. [Publication](https://arxiv.org/pdf/2112.14771){:target="_blank"}
2. [Code](https://gasgauge.github.io/){:target="_blank"}
