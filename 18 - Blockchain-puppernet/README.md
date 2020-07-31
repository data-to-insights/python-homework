Proof of Authority Development Chain
submitted by Pani Maddi (exec Vice President - Blockchain Innovations)
ZBank

Following is the high level process to setup a testnet blockchain
1) Create test accounts(nodes)
2) Create and configure "genesis" block
3) Start chain between the accounts(nodes)
4) Initiate a test transaction and validate succesful completion

Detailed Process
1) Create test accounts(nodes)
On "Terminal" navigate to "Ethereum" environment and into "Blockchain-Tools" directory
Create test node 1 using command - "./geth account new --datadir node1"
Create test node 2 using command - "./geth account new --datadir node2" 
"shot1 - Node1 creation" & "shot2 - Node2 creation" are screenshots for the 2 nodes creation

2) Create and configure "genesis" block
./puppeth "to initiate Etherium private network manager"
puppernet "for network name"
2 "to configure new genesis"
1 "to create new genesis from scratch" 
2 "for proof-of-authority"
account addresses for pre-funding (this for node1 and node2 created earlier)
chainID

3) Start chain between the accounts(nodes)
./geth init puppernet.json --datadir node1 "initiate node1"
./geth init puppernet.json --datadir node2 "initiate node2"
./geth --datadir node1 --unlock "node1 address" --mine --rpc --allow-insecure-unlock
./geth --datadir node2 --unlock "node2 address" --mine --port 30304 --bootnodes "enode from node1" --ipcdisable
"shot3 - Started mining" is screenshot with mining started

4) Initiate a test transaction and validate succesful completion
open "MyCrypto" app
Change network to "puppernet"
Using keystore file open node1
Send transaction to node2 address
"shot4 - Initiated transaction (pending status)", "shot5 - Transaction Succesful", "shot6 - Another succesful transaction" are some example screenshots
