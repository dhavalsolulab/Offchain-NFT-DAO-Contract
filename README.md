# Offchain-DAO-NFT

- An off-chain DAO with multiple voting tokens.
- Voting tokens can be ERC721.

## Contract: NFT.sol

This contract deploys an **ERC721 token with voting rights**.

- Name: "ERC721VotingToken"
- Symbol: "ERC721VT"

- This token will also be used to vote on proposals created in the MultiTokenDAO contract.

- Each token delegated gives 1 voting power.

- The contract owner can call the **mint()** function to mint tokens to an address.
  It takes the target address and the token metadataURI as arguments.

- Users would need to call **delegate()** function and pass their own address as argument in order to create a snapshot of their voting power, as only holding the tokens does not give an address the equivalent voting power.

---

## Important Step

```bash
create .env file in root directory.
```

```bash
    ADMIN_PV_KEY=
    BSC_API_KEY=
    ETH_API_KEY=
    POLYGON_API_KEY=
    BSC_RPC_URL=
    POLYGON_RPC_URL=
    ETH_RPC_URL=

```

## Run Locally

Clone the project

```bash
  git clone https://github.com/dhavalsolulab/Offchain-NFT-DAO-Contract.git
```

Go to the project directory

```bash
  cd Offchain-NFT-DAO-Contract
```

Install dependencies

```bash
  npm install
```

Compile

```bash
  npx hardhat compile
```

Test

```bash
  npx hardhat test
```

Deploy

```bash
  node scripts/deploy.js
```

Deploy on Rinkeby

```bash
  npx hardhat run scripts/deploy.js --network rinkeby
```

Verify Contract

```bash
npx hardhat verify --network rinkeby <YOUR_CONTRACT_ADDRESS>
```

Help

```bash
  npx hardhat help
```

# Check on Rinkeby Explorer

## Deploy Contract

- [NFT](https://rinkeby.etherscan.io/address/0x7f097e8850be2811a50bed289884e1345e6f5674)
- [Treasury](https://rinkeby.etherscan.io/address/0x5347325bfdbf667b70e8e62c08336629915f7633#code)
