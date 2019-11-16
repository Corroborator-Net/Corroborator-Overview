# Corroborator Feature Roadmap
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

- Other use cases:
  - Not just images!
  - Other image verification plays
  - Plug-in application, not a standalone

