---
layout: article
titles:
  # @start locale config
  en      : &EN       About
  en-GB   : *EN
  en-US   : *EN
  en-CA   : *EN
  en-AU   : *EN
  zh-Hans : &ZH_HANS  关于
  zh      : *ZH_HANS
  zh-CN   : *ZH_HANS
  zh-SG   : *ZH_HANS
  zh-Hant : &ZH_HANT  關於
  zh-TW   : *ZH_HANT
  zh-HK   : *ZH_HANT
  ko      : &KO       소개
  ko-KR   : *KO
  fr      : &FR       À propos
  fr-BE   : *FR
  fr-CA   : *FR
  fr-CH   : *FR
  fr-FR   : *FR
  fr-LU   : *FR
  # @end locale config
key: page-about
---

### About me
<table border="0">
  <tr>
    <td width="75%">
      <p><b>Company: Eigen Labs</b></p>
      <p><b>Email: zhoululu789 at gmail.com </b></p>
      <p><b>Social Media:
        <a href="https://www.linkedin.com/in/lulu-zhou-303824170/">LinkedIn</a>
      </b></p>
    </td>
    <td width="25%">
      <img src="./pictures/my_photo.png" width="100%">      
    </td>
  </tr>
</table>

### Publications:
[View on Google Scholar](https://scholar.google.com/citations?user=Hx-AeMwAAAAJ&hl=en)
1. Sprints: Intermittent Blockchain PoW Mining (USENIX'24), M Mirkin, L Zhou, I Eyal, F Zhang [[pdf]](https://eprint.iacr.org/2023/626)
2. Real-Time Recursive Routing in Payment Channel Network: A Bidding-based Design (WiOpt'22), J Liu, C Chen, L Zhou, Z Fang [[pdf]](https://dl.ifip.org/db/conf/wiopt/wiopt2022/1570807019.pdf)
3. CrudiTEE: A Stick-and-Carrot Approach to Building Trustworthy Cryptocurrency Wallets with TEEs (AFT’24), L Zhou, Z Liu, F Zhang, and M Reiter [[pdf]](https://drops.dagstuhl.de/storage/00lipics/lipics-vol316-aft2024/LIPIcs.AFT.2024.16/LIPIcs.AFT.2024.16.pdf) [[slides]](https://github.com/luluzhou1/luluzhou1.github.io/blob/master/CrudiTEE_Crypto_wallet.pdf)
4. Mechanism Design for ZK-Rollup Prover Markets, W Wang, L Zhou, A Yaish, F Zhang, B Fisch, and B Livshits [[pdf]](https://arxiv.org/html/2404.06495v1)


<!---*
### Other links:
* [CV](https://github.com/luluzhou1/luluzhou1.github.io/blob/master/Resume_Lulu_Zhou_2024_Oct.pdf)
* [LinkedIn](https://www.linkedin.com/in/lulu-zhou-303824170/)
 [Twitter](https://twitter.com/LuluZhou14) -->

### Projects related to blockchain
1. Ethereum Fast Confirmation Rule
   * Implemented the Ethereum Fast Confirmation Rule, tested its security and performance using real Ethereum data collected from the Beacon API, and authored blog posts to explain the rule and test results clearly.
   * Advanced research and promoted the adoption of the Fast Confirmation Rule, enhancing the security of Ethereum.
2. ZK Proof Accelerator
   * Modified the snarkjs and ffjavascript packages to implement dynamic caching for ZK-Login.
   * Accelerated the MSM process in ZK proof by 15\% and reduced the total proof generation time by 3\%.
  
3. TEE Wallet
   * Developed a Trusted Execution Environment (TEE)-based wallet for secure secret key management, employing OAuth to ensure an accountable authorization process.
   * Enhanced security using insurance and bounty incentives, and evaluated the solution's effectiveness using a MDP model.
  
4. Sprints
   * Developed "Sprints," a blockchain protocol combining PoW and PoD to reduce ecological impact while maintaining security.
   * Validated its security through performance testing with patched Bitcoin clients.

5. Transaction Relay Strategy
   * Analyzed optimal transaction relaying in Payment Channel Networks (PCNs) using MDP to optimize relay policies.
   * Developed an algorithm for optimal relay strategies in PCNs, assessing the impact on network performance.

1. Analysis of blockchain mining strategy based on MDP
  * This project aims to analyse the best way to mining in proof of work blockchain in order to make maximum profit.
  * [View the project](https://github.com/doris-lessing/Selfish-Mining-Simulator)
  * [View my thesis](https://github.com/doris-lessing/Blockchain_attack_MDP) (This page shows main idea and results, thesis in the repository was written in Chinese.)

### Projects related to data science:
  
1. Image processing algorithms implements
  * This project is meant to implements some classical alogorithms in image processing to get a deeper understanding of them. 
  * [View the project of image transformation](https://github.com/zhangyilang/ImageTransform)
  * [View the project of threshholding and interpulation](https://github.com/doris-lessing/image-processing)
  
2. Spark project: Turkey's population data analysis
  * Analyse a large dataset using Spark. 
  * [View the project](https://github.com/doris-lessing/spark_project)
  
3. Social network analysis on Bilibili
  * Crawled data from bilibili.com, analyzed the social network of bilibili.
  * [View the paper](https://github.com/doris-lessing/Social_Network_Mining_on_Bilibili/blob/master/Social%20network%20analysis%20and%20reference%20system%20construction%20on%20Bilibili.pdf)
    
4. Social network analysis in Chinese rural primary schools
  * We collected questionnaires about the background and social relationships of 227 primary school students when teaching as volunteers. This project focuses on the social network among the students.
  * [View the project](https://github.com/doris-lessing/social-network-mining)