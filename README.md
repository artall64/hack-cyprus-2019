# Crypto payment button
Project on the hack-cyprus-2019 hackathon

### Idea for to be implemented: 
Crypto paying widget for the merchants suplied wiht trezor blockbook based backend.

### Prerequisites & assumption
- Merchant has bitcoin address or seed pharase. For the demo purposes we seed and address will be created using https://iancoleman.io/bip39/ website.
- Merchant want have simple way to receive payments and been notified when incoming transaction is in:
  - Transaction pool
  - In the block with one or more confirmations

### Setup flow
- Merchant comes / registers on the project website and comes goes to his personal dashboard
- Merchant specifies bitcoin address or xpub address that he wants to receive money to
- Merchant specify webhook that he wants to be called
- Merchant copies to clipboard webcomponent snippet
- Merchant paste webcomponent to his website (as a sample website we will use `wix` or `tilda` based template)

### Purchase flow
- Customer opens merchant website
- Customer chooses item and clicks `pay with bitcoin` button
- Modal dialog with QR code should be shown. Modal dialog should be created via WebComopnent. QR code should contain payment details.
- User uses his mobile wallet to scan QR and send transaction
- Blockbook based backend detects new transaction in pool or withint the block and calls webhook specified by merchant

### Task to be done, critical path:
- [ ] Very simple mechant dashboard
- [ ] Button WebComponent 
- [ ] Modal dialog WebComponent
- [ ] Develop block monitoring backend 
- [ ] Record 1 minute video

### Optional task:
- [ ] Setup TS + Rollup build system for web component
- [ ] Guide on webcomopnet customization
- [ ] Docker compose setup for monitoring backend, and mock of merchant backend
- [ ] API for merchant to automatically add address for monitoring
