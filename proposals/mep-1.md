<pre>
  MEP: 1
  Title: Purpose and Guidelines
  Status: Living
  Type: Process
  Created: 2023-04-20
</pre>

# MEP 1: Purpose and Guidelines

# Abstract

This document aims to provide the purpose and guidelines for creating and submitting an MEP (MXC Evolution Proposal). It outlines the process and standards for proposing changes and improvements to the MXC chain.

# Motivation

The MEP process is essential for the structured and effective evolution of the MXC chain. It allows for community input and consensus building on improvements, new features, and changes to the MXC chain.

# Specification

## What is a MEP?

MEP stands for MXC Evolution Proposal. A MEP is a design document providing information to the MXC community, or describing a new feature for MXC or its processes or environment. The MEP should provide a concise technical specification of the feature and the rationale for the feature.

## MEP Rationale

The MEP process is the primary mechanism for changes to the MXC protocol, for information and processes around MXC. Because MEPs are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

## MEP Types

- **Standards**: A Standards MEP describes changes or improvements to the MXC protocol or core components.
- **Informational**: An Informational MEP describes an MXC design issue, or provides general guidelines or information to the MXC community, but does not propose a new feature.
- **Process**: A Process MEP describes a process surrounding MXC, or proposes a change to (or an event in) a process.

## MEP Workflow

After an idea has been accepted, every subsequent status alteration is initiated by the MEP author and evaluated by the MEP editors. To update the status, a pull request should be used.

**Idea**: If there's a concept you believe could improve the MXC ecosystem but you're unsure of its MEP potential, it's recommended to engage with the community before investing significant effort. Share your idea in the appropriate MXC community channels to gather initial feedback.

**Pre-Draft**: If your idea receives positive reception, the next step is to formalize it into a Pre-Draft. This Pre-Draft document should adhere to the MEP format. Once completed, create a pull request for the Pre-Draft. The MEP editors will review it and provide feedback.

**Draft**: Once the Pre-Draft is accepted by the community and reviewed by the MEP editors, it can be merged. The pull request number will serve as the MEP number, marking it as an official MEP. The MEP editors will add the status, and the community will then track and maintain it. The MEP author is responsible for advancing the proposal, which can include updates through additional pull requests.

**Final**: Upon finalizing the proposal, a reference implementation should be provided. This implementation acts as a blueprint for what the final product should look like and how it should function.

**Enabled**: The proposal is activated on the MXC mainnet. If the proposal involves a hard fork, the fork number should be reached at this stage.

Additional distinctive statuses entail:

**Living**: An MEP that will be maintained over the long term, similar to this MEP.

**Stagnant**: An MEP enters the Stagnant state if it has not been updated for more than 6 months.

**Withdrawn**: An MEP that has been abandoned and will not be implemented, often due to a change in circumstances or prerequisites that no longer hold true.

## 5. MEP Format

For maintaining clarity and organization within MEPs, a specific format is advised (MEP1 is the exception). This includes:

- Preamble: This is a brief metadata section about the MEP, designed to be placed at the top of the document. Below is an example:

```md
<pre>
  MEP: 112
  Title: Introduction of zkEVM for IoT and Location Proof
  Status: Draft
  Type: Idea
  Created: 2023-04-20
  Author(optional): This could be a name or an email.
  Description(optional): Proposed introduction of zkEVM for improved IoT and Location Proof functionality.
  Discussions(optional): Could be a link to the MXC forum where the topic is debated.
</pre>
```

## 6. Reference

- Ethereum Improvement Proposals: [https://github.com/ethereum/EIPs](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1.md)

- Bitcoin Improvement Proposals: <https://github.com/bitcoin/bips>

- Bnb-chain Improvement Proposals: <https://github.com/bnb-chain/BEPs>

## 7. License

All the content are licensed under [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
