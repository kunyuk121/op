## EVM Chain Compatible Inscription Automation Mint Scripts


## 🛠 Instructions for use


### Step 1: Install nodejs first.


First, go to the official Nodejs website to download and install the corresponding version for your computer's operating system.


```bash
https://nodejs.org/en
```


Then check the installed version to see if the installation was successful.


```bash
node -v
npm -v
```


If you prefer to use yarn, install yarn
```bash
npm i -g yarn
```


### Step 2: Downloading the script source code
First, use git to clone the source code locally.
```bash
git clone https://github.com/sfter/evm-inscription-mint.git

cd evm-inscription-mint
```
If you don't have git installed on your Windows computer, go to the following website to download and install the git software
```bash
https://gitforwindows.org
```


### Step 3: Rename config.js.example in the current directory to config.js.
```bash
cp config.js.example config.js
```


### Step 4: Modify the config.js configuration file in the current directory.
```javascript
const config = {
    // Set the number of hits you want to make here. It's recommended that you don't make more than 50 hits at a time, or else you'll be unlinked.
    repeatCount: 1,

    // How many times you want to increase the current gas.
    increaseGas: 1.2,

    // Your wallet's private key
    privateKey: "", 


    // Inscription json data (replace it with the json format data of the inscription you want to play)
    tokenJson: 'data:,{"p": "fair-20", "op": "mint", "tick": "fair", "amt": "1000"}', 

    // RPC nodes (evm-compatible chains are fine) use the node address of whichever chain you're playing on
    // eth => https://mainnet.infura.io/v3
    // arb => https://arb1.arbitrum.io/rpc
    // polygon => https://polygon-rpc.com
    // op => https://mainnet.optimism.io
    // linea => https://mainnet.infura.io/v3
    // scroll => https://rpc.scroll.io
    // zks => https://mainnet.era.zksync.io
    rpcUrl: "https://arb1.arbitrum.io/rpc"
}
```


### Step 5: Install the dependencies
```bash
npm i
```
or
```bash
yarn install
```


### Step 6: Run the Mint script program
```shell
node index.js
```
or
```shell
yarn start
```
or
```shell
npm run start
```
