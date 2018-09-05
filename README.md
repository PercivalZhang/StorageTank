# StorageTank Blockchain

StorageTank blockchain is a decentralized network used for data storage and exchange.
  - enough cheap resource fee
  - complete off-chain data storage
  - decentralized storage network 
  - customized data descriptive metadata
  - convenient data search based on self-descriptive metadata
  - multiple source chains support(eos plus ethereum)

### Storage Node

  - file or data is stored into ipfs network and hashId based on data content is the unique identifer of data
  - new and update metadata operations both required user's signature to ensure no unexpected modification before saved into storage node
  - each data or file stored in ipfs network has a metadata defination with json format through hashId
  - metadata supports customized segement except predefinded fields
  - decentralized metadata storage
  - strong and convenient search based on metadata
  
### Side chain Node
side chain forked from EOS to support data storage and exchange scenario
  - much more cheap resource fee
  - customized block explorer

we provide contracts to manage the relationship between source chain account and our side chain account.
 - eos side chain contract for data exchange
   contract for data exchange
 - inter-blockchain communication
     - eos side chain contract
       - release side chain asset to side chain account after receiving proof of locked asset on source chain
       - lock side chain asset and provide proof of locked asset on side chain
     - source chain contract
       - lock source chain asset and provide proof of locked asset on source chain
       - release source chain asset after receiving proof of locked asset on side chain
![inter-blockchain com](http://47.99.61.209/ipfs/QmPgpTr8RR9f9AcenktZmSjyvnQ3d5LCYqjkspKdJt9gdZ)