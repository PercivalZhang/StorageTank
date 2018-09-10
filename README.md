# StorageTank Blockchain

StorageTank blockchain is a decentralized network used for data storage and exchange.
  - enough cheap resource fee
  - complete off-chain data storage
  - decentralized storage network 
  - customized data descriptive metadata
  - convenient data search based on self-descriptive metadata
  - multiple source chains support(eos plus ethereum)

### Design Sketch

![sub systems design](http://47.99.61.209/ipfs/QmdJwGzcTtjsfMSB4PeboHU9w4k6p9Z97Ge3JutEStBhXD)

### Storage Node

  - file or data is stored into ipfs network and hashId based on data content is the unique identifer of data
  - new and update metadata operations both required user's signature to ensure no unexpected modification before saved into storage node
  - each data or file stored in ipfs network has a metadata defination with json format through hashId
  - metadata supports customized segement except predefinded fields
  - decentralized metadata storage
  - strong and convenient search based on metadata
  
### Side Chain Node
> A sidechain is a separate blockchain that is attached to 
> its parent blockchain(source chain or main chain) using a two-way peg.

**Asset Registration and Exchange Contract:** 
- regist asset into side chain with minimum data.
- handle asset exchange.

**Inter-chain Contract:**
- inter-chain token exchange.

The two-way peg enables interchangeability of assets at a predetermined rate between the parent blockchain and the sidechain. The original blockchain is usually referred to as the ‘main chain’ or 'source chain' and all additional blockchains are referred to as ‘sidechains’.

Assets can be moved to the sidechain and then back to the source chain.

side chain forked from EOS to support data storage and exchange scenario
  - much more cheap resource fee
  - customized block explorer

### Inter-blockchain Communication 

A user on the parent chain first has to send their coins to an output address, where the coins become locked so the user is unable to spend them elsewhere. Once the transaction has been completed, a confirmation is communicated across the chains followed by a waiting period for extra security. After the waiting period, the equivalent number of coins is released on the sidechain, allowing the user to access and spend them there. The reverse happens when moving back from a sidechain to the main chain.

Contracts are constructed on both chains to hanlde the communications between source chain account and our side chain account.
 - inter-blockchain communication
     - eos side chain contract
       - release side chain asset to side chain account after receiving proof of locked asset on source chain
       - lock side chain asset and provide proof of locked asset on side chain
     - source chain contract
       - lock source chain asset and provide proof of locked asset on source chain
       - release source chain asset after receiving proof of locked asset on side chain
![inter-blockchain com](http://47.99.61.209/ipfs/QmPgpTr8RR9f9AcenktZmSjyvnQ3d5LCYqjkspKdJt9gdZ)
