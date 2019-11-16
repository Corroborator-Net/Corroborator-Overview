# Corroborator
_Open &amp; Trustless Data Verification_

---

## Table of Contents

- [Overview](#overview)
- [Corroborator Applications](#corroborator-applications)
- [Open Source Tools Used](#open-source-tools-used)
- [Roadmap](#roadmap)

## Overview

How do auditors trust integrity and provenance? 
**Corro**borators to come to our aid.

A Trustless data verification system:
- Cryptographicly signed image data and metadata (user,device, location, ect.) - *at time of capture*
- All data distributed across users & auditors  - _**optional** hybrid on/offline mesh_
- Fingerprint of data logged on (public or private) database - *secure blockchain*

#### :arrow_right: [Presentation Slides Overview](https://docs.google.com/presentation/d/1oSWLNg2lRhOPF8C443hx2zEwzoMVN6uKILMJgBBiU50/)
- Presenter notes are provided in the slides for a **narative of the presentation**.
- A **video recording** of the earliest presentation is also avalible on [YouTube](https://www.youtube.com/watch?v=XFNveoZJn0c)

## Corroborator Applications

| Project | Link | Completeness |
|----------|---------|--------------|
| Ethereum Smart Contract | https://github.com/Corroborator-Net/ETH-Contract | **PoC** |
| _Reporter_: iOS Image Capture App | https://github.com/Corroborator-Net/Corroborator-Reporter | **PoC** |
| _Auditor_: Verfication Webapp Platform | https://github.com/Corroborator-Net/Corroborator-Auditor | **PoC** |

Using **Corro**borator is _easy_. See our app repositories from [Our tools](#our-tools) above for **guided walkthroughs and demos** of the applications.

***NOTE:** For the demo, a deployed audit smart contract on the Ethereum Rinkbey Testnet  is ready for you ([details here](https://github.com/Corroborator-Net/Corroborator-Contract)). This is **hard coded** in our app at the moment! If you want a new audit log created, please reach out to us.*

### Open Source Tools Used
| Tool | Description |
|----------|---------|
| [IPFS](https://ipfs.io/) |  Using a local [JS node](https://js.ipfs.io/) we are able to *simultaniously obtain and validate the integrity of data* in a browser. If you obtain the fingerprint (Content Identifier - CID) of the data is valid, you are able to use a **gateway** online. You are also able to **cross-validate** the data & figerprint by use of an *IPFS node Client*. Pending needs, you are able to use either a gateway, local node, or both. |
| [Pinata](https://pinata.cloud/) | IPFS pinning service |https://pinata.cloud/ |
| [Ethereum](https://ethereum.org/) | Lock in  provenance of data and metadata. Given the Data's *metadata*, one is able to extract and verify a *signing athority*. This is an **ethereum public key**. Each **corro**borator is assigned one to *sign the data and publish the fingerprint to the ethereum blockain*. Using a *block explorer*, anyone is able to verify: the signing athority's key, the fingerprint published, and the timestamp of the fingerprint addition to the blockchain. |
| [Atra](https://atra.io/) | Ethereum Services and Tools|
| [Quasar](https://quasar.dev) | A [Vue](https://vuejs.org/) Webapp Framework |

## Roadmap

Planned future work:

- No external API calls
  - We use native IPFS and Ethereueum clients for all applications
  
- Asymmetric crypto (not the PIN symmetric we use now)
  - Log creator's public key used to encrypt logbook data for reporter 
  - Reporter's priv. key used to sign image, signature embedded in image
  - Reporter encrypts CID with priv. Key used to report & sign data
  - (optionally use a different keypair than one used for blockchain?)
  - Biometric unlock of secure enclave for they keys of reporter
  
- Logbook Creator Application
  - Customize the smart contract and deploy it on a blockchain
  - Auditor contract permissions reporters (pub keys) to read/write to log

- Serverless roadmap:
  - Critical mass of devices means no need for a central server at all.
  - Redundancy is an easy and natural next step for the data. Not hard to impliment.
  - All FOSS based on IPFS so infra is being improved all the time, and at lower cost
  - Portability: Not locked into any particular provider/tech stack. Nothing is proprietary!
- Blockchain Public Key integration
  - User and/or device specific
  - Signing of data
  - Provisioning of writing of the logbook contract
  - Private key used in court to verify singer ID
  - **Signing of data from reporter ensures that no other party can spoof the data itself, or submit a log entry**
  
- Corroborator Relay/Node App & device
  - Mesh integration
  - Redundancy of data (fingerprint and/or data)
    - Optionally can have outside agency and/or whistleblower host to further reduce the need for trust of any party using the system
  - Reliability of reporting in low/no network areas
  - More tamper resistant

- Explore Other Use Cases and Markets:
  - Not just images!
  - Other image verification plays
  - Plug-in application, not a standalone

## License

GNU Affero General Public License v3.0
