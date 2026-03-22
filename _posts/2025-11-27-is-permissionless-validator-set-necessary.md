---
title: Are permissionless validator sets truly necessary?  
tags: 
- permissionless
- cryptoeconomic security
---

If a system is backed by a large amount of stake, is an open validator set essential, or just a design choice? The answer depends on **what kind of faults** the protocol needs to defend against. Different categories of faults can be prevented by different forms of assumptions, and the role of stake and validator-set design changes depending on the assumptions.

## Threshold assumptions are reliable when the validator set is permissionless

BFT protocols rely on threshold assumptions (e.g., less than one-third of validators being malicious), which can be fragile if the validator set is permissioned, even when the total stake is large. A single well-capitalized adversary can simulate many validator identities and contribute large collateral. A validator set may *look* diverse and well-backed, but the entire set might effectively be controlled by one entity.

In BFT protocols, **stake functions primarily as Sybil resistance**, rather than directly guaranteeing safety via cryptoeconomic penalties (explained in the next section). The real guarantee comes from the diversification of validator identities, and permissionless entry is what makes that diversification credible: since honest validators are free to join, malicious validators are unlikely to take up too much of the total participants.

## Cryptoeconomic security provides direct guarantees through stake

When we move from threshold-based trust to **cryptoeconomic security**, the calculus changes.

Cryptoeconomic security is very effective for defending against **objectively attributable faults** [1]. These are faults where the evidence of misbehavior is direct and undisputed (for example, double signing or incorrect state transitions). These faults allow the protocol to apply slashing automatically and objectively to the validator’s collateral.

In this regime, what matters is the **absolute value of slashable collateral**, not the decentralization of the validators. A single entity holding all the stake is not inherently dangerous if:

1. misbehavior directly triggers slashing, and  
2. the stake is large enough that the attack is irrational to perform.

This means that cryptoeconomic security can safely rely on permissioned validator committees or even fully centralized service providers.

This mirrors how the non-crypto world works. People regularly trust banks and large tech companies not because they are decentralized, but because:

1. these entities hold large assets, and  
2. the legal system can punish them if they misbehave.

Cryptoeconomic systems strengthen this model by automating the punishment. When a fault is objectively attributable, the protocol can slash instantly without relying on courts, regulators, or human judgment. This makes cryptoeconomic security *stronger* than traditional legal enforcement for this category of faults.

## The limits of cryptoeconomic security

Not all faults are objectively attributable [1]. Some are **intersubjectively attributable** or even **non-attributable**. Here is a brief description of the three kinds of faults:

- **Objectively attributable** faults can be objectively proven, for example:  
  - invalid execution  
  - double signing  

- **Intersubjectively attributable** faults can be identified by a shared social consensus among active observers of the system, for example:  
  - censorship (under synchrony assumptions)  
  - liveness failures (under synchrony assumptions)  

- **Non-attributable** faults cannot be reliably attributed by participants other than the victim, for example:  
  - privacy violations  
  - censorship (without synchrony assumptions)  
  - liveness failures (without synchrony assumptions)  

If faults cannot be reliably attributed, then slashing cannot be applied. Therefore, cryptoeconomic security is only achievable for **attributable faults**, but it cannot address **non-attributable faults**. To handle non-attributable faults, protocols must rely on **BFT threshold assumptions**. And for these assumptions to be meaningful, the validator set must be permissionless so honest validators can join freely and keep the malicious fraction below the threshold.

## Conclusion

In summary, different fault categories require different validator-set designs, as shown below:

| Fault Type                          | Cryptoeconomic Security (Slashing) | BFT Threshold Assumption | Decentralized Validator Set |
|------------------------------------|-------------------------------------|---------------------------|------------------------------|
| **Objectively attributable faults** | Effective                           | Also works                | Helpful |
| **Intersubjectively attributable faults** | Effective with intersubjective slashing | Also works | Helpful |
| **Non-attributable faults**        | Not enforceable                     | Required                  | Necessary |

This leads to the final takeaway:

- For properties depending on threshold trust assumptions, it is not enough to show that the validator set is backed by large stakes. The validator set must be permissionless so honest validators can join and ensure malicious participation remains below the threshold.  
- For properties depending on cryptoeconomic security, a large slashable stake can be sufficient even if the validator set is permissioned or centralized. The total value at risk matters more than decentralization.

## Reference

[1] Eigen Token Whitepaper, https://docs.eigencloud.xyz/assets/files/EIGEN_Token_Whitepaper-0df8e17b7efa052fd2a22e1ade9c6f69.pdf
