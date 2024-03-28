
# Solana Basic SLP-Token with Metadata

Basic implementation of SLP-Token with Metadata creation and deployment to Solana blockchain. Token can be published on any Solana DEX by adding enough liquidity for your token to be traded.



## Run Locally

Clone the project

```bash
  git clone https://github.com/sagaratalatti/SLP-Token.git
```

Go to the project directory

```bash
  cd SLP-Token
```

Install dependencies

```bash
  npm install
  npm install -g ts-node
```

Create new wallet

```bash
  ts-node wallet.ts
```

```
Generated new KeyPair. 

Wallet PublicKey:  6DYM5UaFfGi7syhyPNY2GTE3yoxhdwvvGpF3pWh9jV9X
Wallet PrivateKey: 6qPbcYMWkVMCsAkSeh75pfUg6WS8wnosm
Wrote secret key to guideSecret.json.
```

## Create JSON metadata for token.json

Upload image to any image hosting or IPFS of your choice and set the image URL and and token information in token.json file. 

```
    "name": "Solano",
    "symbol": "SOLA",
    "description": "Woofing its way to Solana, bringing Solano to the masses.",
    "image": "https://storage.googleapis.com/***.appspot.com/bonzo.jpeg"

```
Upload token.json file to any file hosting of your choice make sure the file stays on the server forever. 

## Add metadata to mint.ts 

Add your uploaded token.json file url to metadata of your SLP-Token.

```
const metadata = {
    name: "Solano",
    symbol: "SOLA",
    uri: "https://storage.googleapis.com/***.appspot.com/token.json"
}
```

You can set number of tokens to be minted in `createAndMint()` function

`amount: 42000000000_00000000, // Set your mint amount here.`

Create & Mint Tokens

```bash
  ts-node mint.ts
```




