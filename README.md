# 🚀 Sui NFT Workshop – My First On-Chain NFT

Welcome to my **mini workshop project** on Sui ✨  
This repo contains a simple Move contract that mints NFTs with a `name`, `description`, and `image_url`.

And yes… I actually deployed it on **Sui Testnet** 😏  

---

## 📦 Contract Info

- **Module name**: `my_nft`
- **Package ID**: [`0x3726e57491d7735739b99b9c1f146b9b78cb757e85756490ee33c350e25a049f`](https://explorer.sui.io/package/0x3726e57491d7735739b99b9c1f146b9b78cb757e85756490ee33c350e25a049f?network=testnet)
- **Publisher address**: [`0x70c0ce113a0878880608a943dc600ebbf49286ffe4feb00ebeda8e7971b73df1`](https://explorer.sui.io/address/0x70c0ce113a0878880608a943dc600ebbf49286ffe4feb00ebeda8e7971b73df1?network=testnet)

---

## ✅ Proof of Deployment

| Action        | Explorer Link                                                                                                                                                 |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 📦 Publish tx | [7RW6im5zPtdt1umXkTx9cYnftVC3HosEaiUdHwvVrh4o](https://explorer.sui.io/transaction/7RW6im5zPtdt1umXkTx9cYnftVC3HosEaiUdHwvVrh4o?network=testnet) |
| 🎨 Mint tx    | [2TZBN1Nra8ZvJkG3ryjRpZiXc9djdnRp3p1g1nhEXwjq](https://explorer.sui.io/transaction/2TZBN1Nra8ZvJkG3ryjRpZiXc9djdnRp3p1g1nhEXwjq?network=testnet) |

Minted object:
- **Object ID**: [`0x1a20635225361aab7ee35403ca01125e5818f858ec0ec7679b4feaa8f00bbcda`](https://explorer.sui.io/object/0x1a20635225361aab7ee35403ca01125e5818f858ec0ec7679b4feaa8f00bbcda?network=testnet)  
- **Type**: `my_nft::MyNFT`  
- **Owner**: my wallet (👋 that’s me)

---

## 🔧 How I Did It

```bash
# build locally
sui move build

# publish to testnet
sui client publish . --gas-budget 100000000

# mint NFT (PTB call with String args)
sui client ptb \
  --move-call "0x3726e57491d7735739b99b9c1f146b9b78cb757e85756490ee33c350e25a049f::my_nft::mint" \
  '"My Cool NFT"' \
  '"This is a description for my NFT"' \
  '"https://example.com/image.png"' \
  --gas-budget 10000000

## 🖼️ Screenshots

Proof or it didn’t happen 😏  

### 1. 📦 Package Published
![Publish Proof](screenshots/publish_tx.png)  
*Explorer view showing the package published successfully.*  

---

### 2. 🎨 NFT Mint Transaction
![Mint Proof](screenshots/mint_tx.png)  
*Transaction on Sui testnet that minted the NFT.*  

---

### 3. 🪙 NFT Object Details
![Object Proof](screenshots/explorer_object.png)  
*Explorer view of the actual minted `MyNFT` object with fields `name`, `description`, and `image_url`.*  

---

## 🌈 What’s Next?

- Add a `recipient` param → so I can mint directly to a friend’s address.  
- Build a tiny React frontend to connect wallet + click “Mint”.  
- Maybe… drop an NFT collection just for fun? 🤔  

---

### 💡 Fun fact

Gas fees for minting this NFT: **0.00285668 SUI**.  
Cheaper than my morning coffee ☕.

---

### ✨ Author
Made with 🧑‍💻 + 🪄 by **Adine Vikash**