# Corroborator
_Open &amp; Trustless Data Verification_

---

## Table of Contents

- [Overview](#overview)
- [Corroborator Applications](#corroborator-applications)
- [Demos and Walkthougs](#demos-and-walkthougs)
  - [Data Validation](#data-validation)
  - [Alternative Open Source Validation Tools](#alternative-open-source-validation-tools)
- [License](#license)

## Overview

How do auditors trust integrity and provenance? 
**Corro**borators to come to our aid.

A Trustless data verification system:
- Cryptographicly signed image data and metadata (user,device, location, ect.) - *at time of capture*
- All data distributed across users & auditors  - _**optional** hybrid on/offline mesh_
- Fingerprint of data logged on (public or private) database - *secure blockchain*

#### :arrow_right: [Presentation Slides Overview](https://docs.google.com/presentation/d/1tid3rLwj4DxNinqXEinlbSFWoJ9HQ7RwI4ALeHtcZn8/edit?usp=sharing)
- Presenter notes are provided in the slides for a **narative of the presentation**.
- A **video recording** of the earliest presentation is also avalible on [YouTube](https://www.youtube.com/watch?v=XFNveoZJn0c)


## Corroborator Applications

| Project | Link | Completeness |
|----------|---------|--------------|
| Ethereum Smart Contract | https://github.com/Corroborator-Net/ETH-Contract | **PoC** |
| _Reporter_: iOS Image Capture App | https://github.com/Corroborator-Net/Corroborator-Reporter | **PoC** |
| _Auditor_: Verfication Webapp Platform | https://github.com/Corroborator-Net/Corroborator-Auditor | **PoC** |


## Demos and Walkthougs

Using **Corro**borator is _easy_. See our app repositories from [Our tools](#our-tools) for guided walkthroughs of the applications. 

### Open Source Tools Used
| Tool | Description |
|----------|---------|
| [IPFS](https://ipfs.io/) |  Using a local [JS node](https://js.ipfs.io/) we are able to *simultaniously obtain and validate the integrity of data* in a browser. If you obtain the fingerprint (Content Identifier - CID) of the data is valid, you are able to use a **gateway** online. You are also able to **cross-validate** the data & figerprint by use of an *IPFS node Client*. Pending needs, you are able to use either a gateway, local node, or both. |
| [Pinata](https://pinata.cloud/) | IPFS pinning service |https://pinata.cloud/ |
| [Ethereum](https://ethereum.org/) | Lock in  provenance of data and metadata. Given the Data's *metadata*, one is able to extract and verify a *signing athority*. This is an **ethereum public key**. Each **corro**borator is assigned one to *sign the data and publish the fingerprint to the ethereum blockain*. Using a *block explorer*, anyone is able to verify: the signing athority's key, the fingerprint published, and the timestamp of the fingerprint addition to the blockchain. |
| [Atra](https://atra.io/) | Ethereum Services and Tools|
| [Quasar](https://quasar.dev) | A [Vue](https://vuejs.org/) Webapp Framework |

### Alternative Open Source Validation Tools

As and alternative to _[Corroborator Auditor](https://github.com/Corroborator-Net/Corroborator-Auditor)_, you can still use _[Corroborator Reporter](https://github.com/Corroborator-Net/Corroborator-Reporter)_ and **watch the watchers** with other 3rd party open source tools:

| Project | Link | What it Does |
|----------|---------|--------------|
| Ethereum MAINNET Block Explorer | https://blockchair.com/ | Figerprint & Data Provenance (Production)|
| Ethereum RINKEBY TESTNET Block Explorer | https://rinkeby.etherscan.io/ | Figerprint & Data Provenance (Testing)|
| IPFS Gateway | https://gateway.pinata.cloud/ipfs/<PROVIDE_CID_FINGERPRINT> | Fingerprint & Data Validation (online)|
| IPFS Desktop | https://github.com/ipfs-shipyard/ipfs-desktop | Fingerprint & Data cross-validation Client (download)|
| Text Difference Tool | https://www.diffchecker.com/ | Crosscheck CIDs and Hashes|

#### Alternative Data Validation Walththough
1. Download the [Demo Picture](/src/statics/QmYXzRsLsWHTg3xTPx7ksEpN7w8JgwpiZ4whnq6phaDrZR.jpeg)
2. Check that the downloaded image CID (`QmYXzRsLsWHTg3xTPx7ksEpN7w8JgwpiZ4whnq6phaDrZR`) matches what you can obtain on an IPFS gateway and/or the IPFS desktop client (See [Open Validation Tools](#open-validation-tools))
    - Use a *gateway* to see the file by CID ([here is one](https://gateway.pinata.cloud/ipfs/QmYXzRsLsWHTg3xTPx7ksEpN7w8JgwpiZ4whnq6phaDrZR))
    - Use the *Desktop Client* **files explorer** to add/upload the demo file and cross-verify that the file indeed has the same CID generated as the file viewed at a gateway.
3. Verify the CID was published on the blockchain. The demo file was published [on the rinkeby ethereum testnet ](https://rinkeby.etherscan.io/tx/) (transaction hash: ``)
    - At the bottom of the page, Click to `show more`
    - View the `input data` as `UTF-8`. The CID || picture timestamp || location (in that order)  _should_ be apparent there. You can also validate the timestap of the transaction itself ot cross-check the providance of the recorded data.
  


## License

TBA
