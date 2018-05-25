
See also:
* https://sawtooth.hyperledger.org/docs/core/nightly/master/glossary.html
* https://sawtooth.hyperledger.org/docs/core/releases/1.0/architecture/poet.html#definitions


Address (aka State Address) - For Sawtooth, each radix address (or Node ID) into a Merkle Trie is 70 hex characters (35
bytes). The first 6 characters, the prefix, encode the name space (of the TF) and the remaining bytes are implementation
-dependent.
The prefix is usually the first 6 characters of the SHA-512 hash of the namespace, or a hex word for base name spaces.
See the list of TF prefixes in the Appendix

AVR - Attestation Verification Report - Response body signature, signed with the IAS Report Key
back pressure - flow-control technique to help prevent Denial of Service attacks; used by Sawtoot
Batch - A set of transactions that must be made together (atomic commit) to maintain state consistency
Block - A set of records of permanent transactions; these blocks are linked into a blockchain.
        A block is similar to a page in a ledger book, where the ledger book is a blockchain
Blockchain - a single-link list of blocks.  The blockchain is immutable, distributed, and cryptographically secured
Block ID - 128 hex character ID (64 bytes) identifying a block in a blockchain
BFT - Byzantine Fault Tolerance - consensus possible with malicious actors (Byzantine Generals Problem);
        stronger than CFT; uses voting
C - signup delay; number of blocks a validator has to wait before participating in elections (when using PoET)
C Test - test that a block-claiming validator follows C, signup delay
CFT - Crash Fault Tolerance - consensus possible even with failed components
Client - any program that creates a transaction; interfaces with the validator using REST.
        Does not have to be a web-based app
Consensus algorithm - method to decide what block to add next to a blockchain
Classical Consensus - uses an agreement or voting mechanism (vs. Nakamoto-style consensus)
Docker - a light-weight OS-level VM technology which isolates processes into separate "containers"
PoET - Proof of Elapsed Time (optional Nakamoto-style consensus algorithm used for Sawtooth)
CSV - comma separated values.  E.g.: a,b,c,d
Curve325519 - An ECDH (Elliptic Curve Diffie-Hellman) key agreement protocol used by Sawtooth
        - Used by validators in ZMQ connections to exchange keys
Data model - Can be any format (CSV, protobufs, etc.)
Deterministic - means consistent, or the same. For Sawtooth, serialization must be deterministic,
        meaning the encoding is always in the same order and always the same for the same data.
        Many JSON libraries do not encode data deterministically.
EPID - Enhanced Privacy ID - an anonymous credential system; used by PoET
Enclave - SGX protected area of data and code to provide confidentiality and integrity even against privileged malware
EVM - Ethereum Virtual Machine  - executes machine-independent code for Ethereum.  Supported by SETH on Sawtooth
Gossip - A message broadcast mechanism that uses forwarding to random peers (Sawtooth Validator nodes)
Hyperledger - A family of distributed ledgers sponsored by The Linux Foundation, including Sawtooth
IAS - Intel Attestation Server - used to authenticate PoET SGX keys; runs in public Internet
        - At https://as.sgx.trustedservices.intel.com/
IntKey - Integer key TP - sample Sawtooth TP that implements set/increment/decrement/show operations
K - Claim limit, number of blocks a validator can publish before it must signup again (when using PoET)
K Test - test a block-claiming validator follows K, claim limit before another signup
Marshalling - serialization of data
Merkle Tree (or Trie) - a radix search tree data structure with addressable nodes. Used to store state
Nakamoto-sytle Consensus - uses some soft of Proof of Work mechanism (vs. Classical Consensus)
Node ID - Address
Nonce - A one-time number; usually random, but must not predictably repeat (such as after reboot/restart)
Payload - data processed by the TP and only the TP. Can be any format (CSV, protobufs, etc.)
        - Data model is defined by TF
        - Payload is encoded using MIME's Base64 (A-Za-z0-9+/) + "=" for 0 mod 4 padding.
PBFT - Practical Byzantine Fault Tolerance - a "classical" consensus algorithm that uses a state machine
Permissioned Blockchain (aka Private Blockchain) - participants must ID themselves to a network (e.g., Hyperledger Sawto
oth or Hyperledger Fabric)
Permissionless Blockchain (aka Public Blockchain) - anyone can join network (e.g., Bitcoin, Ethereum)
PoET - Proof of Elapsed Time (optional Nakamoto-style consensus algorithm used for Sawtooth)
        PoET with SGX has BFT. PoET Simulator has CFT.
PoW - Proof of Work - completing work (CPU-intensive Nakamoto-style consensus algorithm)
PoS - Proof of Stake - consensus algorithm based on the most wealth or age (stake)
Private Blockchain - See Permissioned Blockchain
Proposal - proposed block from a validator to add to a blockchain
Protobuf - Serialization/data interchange library used by Sawtooth
PDO - Private Data Object - blockchain objects that are kept private through encryption
Public Blockchain - See Permissionless Blockchain
Raft - Consensus algorithm that elects a leader for a term of arbitrary time.
        Raft is CFT, but not BFT
REST -  Representational State Transfer - industry-standard web-based API.
        REST is available on a Sawtooth validator node through TCP port 8008
TF - Transaction Family. Consists of the Client, State, and TP
TP - Transaction Processor - processes transactions for a specific TF
        - Runs on Validator
        - Similar to a Ethereum "smart contract" or Bitcoin "chain code"
Sawtooth - permissioned blockchain platform for running distributed ledgers
SETH -  Ethereum-compatible Sawtooth Transaction Processor. Suppors running Ethereum Virtual Machine
secp256k1 - An ECDSA (Elliptic Curve DSA) cryptographic algorithm used by Sawtooth with a 32-byte key
        - Used for Validator and TP; same algorithm used by Bitcoin
Serialization - a scheme to encode data as a byte stream.  For Sawtooth the serialization must be deterministic.
        meaning the encoding is always in the same order and always the same for the same data.
        Protobufs are often used in Sawtooth Serialization, but that is not a requirement.
        A simpler alternative, for example, is CSV.
SGX - Intel Software Guard Extensions - specialized hardware that provides enclaves with protected code and data
        - Used to implement PoET SGX
State - the current information for each Transaction Family.  The global state is stored in a Merkle Tree.
        View local validator through http://localhost:8008/state
State Address - See Address
Sybil Attacks - using forged identities in a blockchain network to subvert the reputation system; named after the book a
nd movie
Validator - validates transactions and sends to the appropriate TP; proposes new blocks for block chain
Validator - validates transactions and sends to the appropriate TP; proposes new blocks for block chain
        - usually in a network of validator nodes
XO - Example Sawtooth TP that implements the Tic-tac-toe game
Z Test - test a block-claiming validator is not winning too frequently
ZMQ (aka 0MQ, ZeroMQ) - Message Transport API available on Linux; used by Sawtooth Validator nodes
ZKP - Zero Knowledge Proof - one party proving they know a value x without conveying x