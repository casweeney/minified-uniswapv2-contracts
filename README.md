# minified-uniswapv2-contracts
This is a minified working UniswapV2 smart contracts

## Setup
This is contract has been minified, so no need to scaffold a hardhat or foundry project for it.

- Use Remix IDE to deploy
- Deploy the Factory contract first and pass feeSetter address in the constructor
- After deploying Factory.sol, call the INIT_PAIR_HASH function to get the Init_hash
- Deploy the WETH9.sol next
- Inside the UniswapV2Library contract found in the Router.sol, change the Init_hash in the pairFor() function, please remove the 0x prefix
- Deploy the Router02 contract
- Deploy the Multicall.sol

### Note: Deploying Router02 will throw a contract code exceed 24576 error, to fix this, check optimization on your remix deployment tab and set the runs to 500

### Your contract is set to be connected to the V2 interface

# Happy Coding
