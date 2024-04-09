# Tornado

![image](https://github.com/tHeStRyNg/tornado/assets/118682909/a5525da8-38e5-4118-a328-6e0e340be0d4)

Tornado is a **fully decentralized** **non-custodial** **protocol** allowing private transactions in the crypto-space.

### Scope
- Anonymous Non-Custodial Ethereum Privacy Solution Deposit / Withdraw
- Because Maintaining Financial Privacy is Essential to Preserve our Freedom.

## Building locally

- Install [Node.js](https://nodejs.org) ``` version 14 ```
- If you are using [nvm](https://github.com/creationix/nvm#installation) (recommended) running `nvm use` will automatically choose the right node version for you.
- Install [Yarn](https://yarnpkg.com/en/docs/install)
- Install dependencies: `yarn`
- Copy the `.env.example` file to `.env`
- Replace environment variables with your own personal.
- Build the project to the `./dist/` folder with `yarn generate`.

## Development builds

To start a development build (e.g. with logging and file watching) run `yarn dev`.

## Deploy on IPFS

- Make sure you set `PINATA_API_KEY` and `PINATA_SECRET_API_KEY` environment variables in `.env`
- To deploy a production build run `yarn deploy:ipfs`.
- Info on how to here --< https://knowledge.pinata.cloud/en/articles/6191471-how-to-create-an-pinata-api-key
 
Important:
- You will need paid version so can store html

## Architecture

### The Basic Web Infrastructure (_not Circles_)

![image](https://github.com/tHeStRyNg/tornado/assets/118682909/b8d9e9b2-d5e0-4f69-97ad-6b45b2ba266d)


For detailed explanation on how things work, checkout [Tornado Docs]([https://nuxtjs.org](https://github.com/tHeStRyNg/tornado/tree/master/docs)).

## Update cached files

- For update deposits and withdrawals events use `yarn update:events {chainId}`
- For update encrypted notes use `yarn update:encrypted {chainId}`
- For update merkle tree use `yarn update:tree {chainId}`

#### NOTE!

After update cached files do not forget to use `yarn update:zip`

### Example for Ethereum Mainnet:

```
yarn update:events 1
yarn update:encrypted 1
yarn update:tree 1

yarn update:zip
```

### Example for Binance Smart Chain:

```
yarn update:events 56
yarn update:encrypted 56

yarn update:zip
```

#### Dependancies

- WebSnark --> https://github.com/poma/websnark
A fast zkSnark proof generator written in native Web Assembly. 
websnark is used to generate zkSnark Proofs from the browser.
This module generates highly optimized Web Assembly modules for the low level cryptographic primitives.
- SnarkJS  --> https://github.com/iden3/snarkjs
This is a JavaScript and Pure Web Assembly implementation of zkSNARK and PLONK schemes. It uses the Groth16 Protocol (3 point only and 3 pairings), PLONK and FFLONK.

#### Custom Configuration
 For RPC you can use any network (ETH, POLY, etc) RPC for your anonymity.
 We are currently running the service cross https://cloudflare-eth.com ^_^

 Enjoy !!!
