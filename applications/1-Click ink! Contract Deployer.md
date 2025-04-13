# 📝 Name of your Project

## 🌟 Project Overview

Please provide the following:

- Streamlining ink! Smart contract deployment across Polkadot parachains with a single click.
- The 1-Click ink! Contract Deployer is a lightweight, user-friendly tool designed to simplify the deployment of ink! smart contracts on any WASM-compatible Polkadot parachain, such as Astar, Aleph Zero and Shiden. By offering both a web interface and integration with GitHub Actions, this tool enables devs to upload, configure, and deploy their contracts efficiently. It eliminates common deployment issues, fostering rapid prototyping and smoother onboarding for developers new to the Polkadot ecosystem.
- This tool would be built to seamlessly interface with the Polkadot ecosystem by targetting WASM-compatible parachains that support ink! smart contracts. It utilizes the substrate framework's capabilities, ensuring compatibility and smooth operation within the Polkadot network. By simplifying this deployment process, it fosters the development and integration of decentralized applications across parachains, promoting interoperability and the tight growth of the ecosystem
- My team is interested in enhancing the developer experience within the ecosystem. We recognize that the complexity of deploying ink! smart contracts can be a barrier to entry for many developers. By creating the 1-click ink! contract deployer, we mainly aim to lower the barrier thereby making it easier for developers to bring their ideas to life on polkadot parachains. Our goal is to foster innovation, accelerate dev cycles, and contribute to the growth of the community

### 🔍 Project Details

We expect applicants to have a solid idea about the project's expected final state. Therefore, please submit (where relevant):

- Frontend (next.js[react], css), tooling[rust+ink! CLI tools], backend[golang], integration layer[polkadot.js and susbstrate RPC], ci/cd automation, talisman wallet integration for trans. signing )
- The architecture consists of two primary deployment channels:
   Web Interface Flow:
  1. Upload .contract bundle (WASM + metadata).

2. Parse metadata and let the user configure constructor arguments and gas limits.
3. Deploy to the selected parachain using Polkadot.js API and a connected wallet.

   CI/CD Flow via GitHub Actions:
1. Developers include a .deploy.yml config file in their repository.
2. On push or release tag, GitHub Actions automatically compiles and deploys the contract using a secure deploy key or wallet integration.
N/B: Both flows share a backend service that handles metadata validation, chain querying, and error reporting.
- Proof of Concept
We’ve already prototyped the following components:
1. A working CLI wrapper for ink! compilation and metadata extraction.
2. minimal web interface that successfully reads metadata and renders constructor inputs.
3. Basic support for Polkadot.js API interactions


- Mockups/designs of any UI components
We’re finalizing mockups for:
1. Drag-and-drop contract upload UI with real-time metadata parsing.
2. Constructor configuration screen with dynamic input fields and validation.
3. A deployment dashboard showing status, transaction hashes, and links to explorer.
4. GitHub Action setup helper with auto-generated .yml based on user input.

- Data models / API specifications of the core functionality
  Contract model
  {
  "name": "GodinT",
  "version": "0.1.0",
  "wasm_hash": "0xabc123...",
  "metadata": { ... },
  "constructor": "new",
  "args": ["1000000"],
  "deployer_address": "5G..."
}
   API Endpoints
1. POST /upload: Accepts contract bundle, parses metadata.
2. POST /deploy: Triggers deployment, returns status + transaction hash.
3. GET /status/:txHash: Retrieves status of the deployment.
4. GET /chains: Lists available parachains and their current block number, chain state, fees, etc.
   
- What your project is *not* or will *not* provide or implement
1. This tool dosnt offer a snmart contract IDE
2. also wont replace Substrate/ink! documentation, however, may link them to where helpful
3. while this enables multi-chain deployments, our aim doesnt include to support every parachain immediately--however, we'll priotize Astar, shiden,ALEPH Zero and expand based on usage and feedback. 
  
  - This is a place for you to manage expectations and clarify any limitations
    1. This tool isnt a contract editor or IDE
    2. The initial parachain support is limited.
    3. There's no in-built testing.
    4. Absence of private key management
    5. Limited advance features at launch 

### 🧩 Ecosystem Fit

Help us locate your project in the Polkadot landscape and what problems it tries to solve by answering each of these questions:

- Where and how does your project fit into the ecosystem?
  The 1-click ink! contract deployer is positioned as a **developer experience enhancer** within the Polkadot smart contract ecosystem. It specifically serves the ink! contract workflow; a unique aspect of Substrate-based chains and integrates directly with parachains that support WASM execution like Astar and Alpher zero.
  By focusing on this deployment layer, it complements existing efforts around tooling like ink!, substrate; and acts as a bridge between development and execution. It's not trying to compete with IDEs or contract SDKs, instead its solving a very specific pain: getting from "compiled contract" to "live on chain" without friction.
- Who is your target audience?
mainly those who are motivated to build but slowed down by tooling gaps or steep learning curves. like smart contract devs, opensource contributors, etc.
- What need(s) does your project meet?
it lowers the onboarding barriers for new devs, enables ci/cd style workflow, saves time for devs deploying ink! smart contracts and finally it allows developers test deployments across multiple parachains with little effort.
- Are there any other projects similar to yours in the Polkadot ecosystem?
  yes theere are a few tools in the ecosystem with some overlap but none focused squarely on what mine offers. 
  - If so, how is your project different?
    
  - If not, why might such a project not exist yet?
    there are few reasons for this : The ink! and substrate ecosystem is still relatively young, and most early tools focused on core primitives rather than DX improvements, and also many projects are parachain-specific, generalized, thereby making interoperable tooling not an immediate priority. then finally, previously, there have been limited demand for CI-style workflows or no-code deployment flows, but this is changing fast as the ecosystem matures and more developers onboard.

> **Note**: We prioritize projects building on Plaza/Polkadot Hub, games, and DeFi applications, though all types of projects will be considered.
## 👥 Team

- **Team Name:** Name of your team. If you apply as a legal entity, please use its name.
  G-DeArk 
- **Contact Name:** Full name of the contact person in your team
Isaac Arogbonlo
- **Contact Email:** Contact email
arogbonloi@gmail.com
- **Website:** Your website, GitHub org, blog, or similar
github username : Arogbonlo
medium: https://medium.com/@arogbonloisaac
### Team members

Please list the legal name of all grant beneficiaries. Solo developers (1-person teams) are eligible for funding.
Isaac Arogbonlo

#### LinkedIn Profiles (if available)
https://www.linkedin.com/in/arogbonloisaac/

### Team Code Repos

- https://github.com/{your_organisation}/{project_1}
- https://github.com/{your_organisation}/{project_2}

Please also provide the GitHub accounts of all team members:

- https://github.com/Arogbonlo

### Team's experience

Please describe the team's relevant experience, including any previous blockchain projects or contributions to the ecosystem.

## 📊 Development Status

If you've already started implementing your project, please provide a link and a description of the code. Otherwise, please provide some documentation on the research and other work you have conducted before applying.

## 📅 Development Roadmap

This section should break the development roadmap down into milestones and deliverables. Since these will be part of the agreement, please describe *the functionality we should expect in as much detail as possible*, plus how we can verify and test that functionality.

**Important notes:**
- Each milestone is capped at **$5,000 USD**
- Milestones must be delivered within **3 months** of approval
- The maximum grant amount is **$10,000 USD** per application (up to **$15,000 USD** per project in exceptional cases)
- You will only receive payment after successful milestone delivery

### Overview

- **Estimated Duration:** Duration of the whole project (maximum 3 months)
- **Full-Time Equivalent (FTE):**  Average number of full-time employees working on the project
- **Total Costs:** Requested amount in USD for the whole project (maximum $10,000 USD)

> Note that deliverables 0a to 0d are mandatory. Please adapt their specification to your project.

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can... |
| 0c. | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Article | We will publish an **article** that explains what was done/achieved as part of the grant. |
| 1. | Feature X | We will create a feature that will... (Please describe in detail) |
| 2. | Feature Y | The Y feature will... (Please describe in detail) |
| 3. | Feature Z | The Z feature will... (Please describe in detail) |

### 💰 Budget Breakdown

Please provide a breakdown of your budget by milestone:

| Milestone | Deliverables | Cost (USD) | Estimated Completion |
| --- | --- | --- | --- |
| 1 | Features X, Y | $5,000 | 1.5 months |
| 2 | Feature Z | $5,000 | 1.5 months |
| **Total** | | **$10,000** | **3 months** |

## 🔮 Future Plans

Please include:

- How you intend to continue development after the Fast-Grant
- Any plans for seeking additional funding (other grants, VC funding, etc.)
- Your vision for the project's growth and impact in the Polkadot ecosystem

## ℹ️ Additional Information

Here you can add any additional information that you think is relevant to this application, such as:

- Work you have already done
- If there are any other teams who have already contributed to the project
- Other funding you may have applied for

Remember that the Fast-Grants Programme is designed as a first step for promising projects. We're looking for projects that can continue to grow beyond this initial funding.
