# MediBloc Techinical Whitepaper(ENG)v0.3

## Abstract 
The name of MediBloc’s mainnet is Panacea and it means “a remedy for all ills.” MediBloc is developing a blockchain based health information platform that provides [patient centric health information / reliable health information / personalized health information] under the vision of ‘showing innovative paradigm through developing a patient centric health information solution and build a world of healthy lives for everyone.’ Panacea is a core technology that will realize MediBloc’s vision and will make an ecosystem of patient centric health information collection, management, and utilization possible. Many problems that patients face these days will be cured and improved through Panacea and patient’s healthcare experience will be reinvented. Panacea is a health information protocol, a public blockchain with independent network. On Panacea, records are made and validated through nodes’ validation; once a record is successfully put on the blockchain, it cannot be forged or falsified. The core function of Panacea is to record hash value of health information and to prove the integrity and ownership of the data through the hash value. Panacea can be utilized freely with its cryptocurrency, MED coin. 

## Panacea’s Consensus Mechanism
Panacea blockchain uses DPOS(Delegated Proof of Stake) consensus mechanism with PBFT(Practical Byzantine Fault Tolerance) algorithm. In DPOS consensus mechanism with PBFT algorithm, validators(block producers), that are decided by votes of network participants, efficiently produce new blocks at a high speed while synchronizing the blocks. In Panacea, the group that validates and produces blocks are called Validators and when they successfully fulfill their duties as validators they are rewarded with MED mainnet coin based on the number of votes they received as an incentive. Those with MED mainet coins that are not selected as validators can vote for validators, contribute in block validating process and receive incentives after each block creation is completed. 

 ![Image of Simplified Panacea Architecture](https://github.com/medibloc/whitepaper/blob/master/Simplified%20Panacea%20Architecture.png) 

## Features of Panacea’s consensus mechanism
### Slashing

Panacea utilizes PBFT algorithm and this algorithm is special for its ability to filter out insincere validator. If a validator does not validate block faithfully or acts maliciously, the staked coins of the validator and the voters will be slashed. In other words, voters role of choosing a right validator is as important as validators role of acting faithfully. As a result, the voters are motivated to vote for suited validators and, ultimately, lead virtuous cycle of the blockchain. This algorithm and method will upgrade data validation, security and reliability that are required for a successful medical blockchain and will be the forte of Panacea.

### One Block Finality

Panacea’s one block finality mechanism complements weak spots of existing blockchain. Existing blockchains use “First - block production and then - consensus” mechanism that are exposed to various risk of malicious attack, Panacea uses one block finality mechanism, which is “First - consensus and then - block production”, that yields 100% reliable consensus mechanism. With this feature, there will never be any forks. 

## Incentives
Validators that receive more votes from the voters(the mandators) will have more frequent block producing turns as it will have more probability to be selected as a block producer. Validator will be rewarded with MED, MediBloc coin, that are gathered through inflation(minting) and gas fee. Validators can set their own rate of commission and the voters(the mandators) who voted for a specific validator will be incentivized according to the voting rate from the total incentives that the validator has received minus the rate of commision that the validator has set. The voters(the mandators) can check the validators’ information and the rate of commission through Panacea explorer. The inflation rate is adjusted based on the amount of staked coins on Panacea. If the amount of staked coins is decreased, the inflation rate will go up and vice versa. Hence, as more coins are staked by the validators of Panacea, the circulated supply of MED mainnet coin will decrease while maintaining its value. 

## Node construction of Panacea
The validators of Panacea will be selected by votes from the users. Candidates will be divided into different classes such as regular user, healthcare companies, medical institutions, etc. Some of the nodes could be healthcare companies or medical nodes that cooperates with MediBloc. Before the token swap of QRC20 and ERC20 tokens to the mainnet coin, MediBloc will be operating all the validators(nodes); after a successful token swap and selection of validators, MediBloc will burn or airdrop all the incentives it received as validator. 

## Verifiable health information hash value
In MediBloc platform, health information/data are managed in the form of Merkle tree. In case of services that utilize  a specific data format/messaging protocol(e.g. HL7-FHIR), the data go through “Merklizing” process and MediBloc provides software tools and guides to have these services easily utilize data through Panacea The merit of Merkle tree approach is that the users can share parts of the data while guaranteeing its integrity. The data owner will record root hash of Merkle Tree on Panacea, the blockchain. Due to Merkle Tree’s properties, even if the owner of the data only share part of the data, the receiver could still check the integrity of the data through Merkle proof and root hash.  Through this trait, data could be de-identified easily by omitting the personal information or could be checked for integrity before the actual data gets transferred/traded. The original data, which is converted into Merkle tree format, is stored in users’ smartphone devices. Since only the root hash of the original data will be stored on blockchain, there are no restrictions in the methods of encryption in sharing / storing the data. Even if the current encryption method loses its security because of the increase in computing power, new encryption method could be implemented at the service level  while not interfering with the records on the blockchain. 

## Panacea’s role
Through Panacea, data is managed by the data owners and the owners can safely update, send, utilize, and record the hash value of the health information.Many problems that patients face these days will be cured and improved through Panacea and patient’s healthcare experience will be reinvented. 

All the activities on Panacea could be checked through transactions(In case of personal health information, only the hash value will be stored)

Supporting the collection of patients’ health information from websites, mobile applications, etc. 

Receiving patients’ consents to utilize their health information

Empowering patients to have control over the collected health information

Allowing healthcare companies and medical institutions to trust patient managed data

Enabling the utilization of patient-consented data
