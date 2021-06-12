# Setup
```bash
npm install -g truffle
npm install
```

Create a `.env` file in the root directory and set the following variables:
```bash
MNEMONIC="<your mnemonic>"
INFURA_PROJECT_ID="<your infura project id>"
```

Then you can deploy to a given (test) net.
```bash
truffle migrate --network rinkeby
```

# Usage
There are two addtional function to this ERC721 that can be called.

The `setMinter` function call only be called by the owner (deployer) of this contract. With that it is possible to whitelist new address that can mint new NFTs and also set a limit for them how many NFTs they can mint.

The `mint` function can be called (by an artist) to actually mint the NFT as long as that address is whitelisted and below its token allowance.
