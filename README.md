# Corroborator
> Open &amp; Trustless Data Verification

---

#### Welcome to Corroborator! (To be Added) ~[Watch a video demo](https://www.youtube.com/)~  to get started.

### [Overview Presentation Slides](https://docs.google.com/presentation/d/1tid3rLwj4DxNinqXEinlbSFWoJ9HQ7RwI4ALeHtcZn8/edit?usp=sharing)

---

## Table of Contents

- [Overview](#overview)
- [How Corroborator Works](#how-corroborator-works)
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

(To be Added) ~[![Watch a video demo](img/TBD.png)](https://www.youtube.com/)~

[Presentation Slides Overview](https://docs.google.com/presentation/d/1tid3rLwj4DxNinqXEinlbSFWoJ9HQ7RwI4ALeHtcZn8/edit?usp=sharing)


## How Corroborator Works

**TBW**
- Image App
- Auditor Interface

### Our Tools

| Project | Link | Completeness |
|----------|---------|--------------|
| Image App | https://github.com/Corroborator-Net | **PoC** |
| Auditor Smart Contract | https://github.com/Corroborator-Net/ETH-Contract | **PoC** |
| Custon Auditor Interface | *N/A - use [Open Validation Tools](#open-validation-tools)* | **TODO** |


## Demo

Using **Corro**borator is easy. Here we provide a sample image that we want to audit with our system. 

**The file** TODO - ADD ME!!

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
| Ethereum Block Explorer |https://blockchair.com/ | Figerprint & Data Provenance  |
| IPFS Gateway | https://gateway.pinata.cloud/ipfs/<PROVIDE_CID_FINGERPRINT> | Fingerprint & Data Validation (online)|
| IPFS Desktop | https://github.com/ipfs-shipyard/ipfs-desktop | Fingerprint & Data cross-validation Client (download)|


## License

TBA
