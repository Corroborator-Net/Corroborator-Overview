# Corroborator
> Open &amp; Trustless Data Verification

---

#### Welcome to Corroborator!

### [Overview Presentation Slides](https://docs.google.com/presentation/d/1tid3rLwj4DxNinqXEinlbSFWoJ9HQ7RwI4ALeHtcZn8/edit?usp=sharing)

---

## Table of Contents

- [Overview](#overview)
- [Our Tools](#our-tools)
- [Demo](#demo)
  - [Data Validation](#data-validation)
  - [Open Validation Tools](#open-validation-tools)
- [License](#license)

## Overview

How do auditors trust integrity and provenance? 
**Corro**borators to come to our aid.

A Trustless data verification system:
- Signed user & device - *cryptographic proof*
- Fingerprint on public DB - *blockchain*
- Distributed across auditors  - *hybrid on/offline*

[Watch a video demo](https://youtu.be/XFNveoZJn0c)

[Presentation Slides Overview](https://docs.google.com/presentation/d/1tid3rLwj4DxNinqXEinlbSFWoJ9HQ7RwI4ALeHtcZn8/edit?usp=sharing)


## Our Tools

| Project | Link | Completeness |
|----------|---------|--------------|
| iOS Image App | https://github.com/Corroborator-Net/Corroborator-iOS  | **PoC** |
| Auditor Smart Contract | https://github.com/Corroborator-Net/ETH-Contract | **PoC** |
| Custom Auditor Interface | *N/A - use [Open Validation Tools](#open-validation-tools)* | **TODO** |


## Demo

Using **Corro**borator is easy. Here we provide a sample image that we want to audit with our system. 

1. Download the [Demo Picture](QmVbHUYa4T5XH7Bu9oRRHAPWeAkFLqUHP2YervPWF1xdYH.jpeg)
2. Check that the downloaded image CID (`QmVbHUYa4T5XH7Bu9oRRHAPWeAkFLqUHP2YervPWF1xdYH`) matches what you can obtain on an IPFS gateway and/or the IPFS desktop client (See [Open Validation Tools](#open-validation-tools))
    - Use a *gateway* to see the file by CID ([here is one](https://gateway.pinata.cloud/ipfs/QmVbHUYa4T5XH7Bu9oRRHAPWeAkFLqUHP2YervPWF1xdYH))
    - Use the *Desktop Client* **files explorer** to add/upload the demo file and cross-verify that the file indeed has the same CID generated as the file viewed at a gateway.
3. Verify the CID was published on the blockchain. The demo file was published [on the rinkeby ethereum testnet ](https://rinkeby.etherscan.io/tx/0xf57277877c5d9a1546c27eac92ed4e6024bb667366f89220478db5f0bec55307) (transaction hash: `0xf57277877c5d9a1546c27eac92ed4e6024bb667366f89220478db5f0bec55307`)
    - At the bottom of the page, Click to `show more`
    - View the `input data` as `UTF-8`. The CID || picture timestamp || location (in that order)  _should_ be apparent there. You can also validate the timestap of the transaction itself ot cross-check the providance of the recorded data.
  

### Data Validation

Using **[IPFS](https://ipfs.io)** we are able to *simultaniously obtain and validate the integrity of data*. If you trust that the Finderprint (Content Identifier - CID) of the data is valid, you are able to use a **gateway** online. If you do not, you are able to **cross-validate** the data & figerprint by use of an *IPFS node Client*. Pending needs, you are able to use either or both. (See [Open Validation Tools](#open-validation-tools) for options)

Given the Data's *metadata*, one is able to extract and verify a *signing athority*. This is an **ethereum public key**. Each **corro**borator is assigned one to *sign the data and publish the fingerprint to the ethereum blockain*. Using a *block explorer*, anyone is able to verify:
- The signing athority's key
- The fingerprint published
- The timestamp of the fingerprint addition to the blockchain
(See [Open Validation Tools](#open-validation-tools) for options)

### Open Validation Tools

| Project | Link | What it Does |
|----------|---------|--------------|
| Ethereum MAINNET Block Explorer | https://blockchair.com/ | Figerprint & Data Provenance (Production)|
| Ethereum RINKEBY TESTNET Block Explorer | https://rinkeby.etherscan.io/ | Figerprint & Data Provenance (Testing)|
| IPFS Gateway | https://gateway.pinata.cloud/ipfs/<PROVIDE_CID_FINGERPRINT> | Fingerprint & Data Validation (online)|
| IPFS Desktop | https://github.com/ipfs-shipyard/ipfs-desktop | Fingerprint & Data cross-validation Client (download)|
| Text Difference Tool | https://www.diffchecker.com/ | Crosscheck CIDs and Hashes|

## License

TBA
