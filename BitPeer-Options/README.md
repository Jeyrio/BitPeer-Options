# BitPeer Options (btc-options-v1)  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)  

Decentralized P2P options trading protocol with Bitcoin exposure tracking on Stacks blockchain.  

## 📖 Overview  
Non-custodial options trading contract featuring:  
- BTC-tracked settlement  
- European-style expiry options (CALL/PUT)  
- Decentralized price oracle  
- On-chain position tracking 


## 🛠️ Contract Architecture  
```clarity
(define-contract btc-options-v1)
(define-map BTCBalances {holder:principal} {balance:uint})
(define-map Options {option-id:uint} {creator:principal, buyer:(optional principal)...})