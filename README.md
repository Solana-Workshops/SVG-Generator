# SVG Generator

## 🎬 Recorded Sessions
| Link | Instructor | Event |
| ---- | ---------- | ----- |
| [<img src="https://raw.githubusercontent.com/Solana-Workshops/.github/main/.docs/youtube-icon.png" alt="youtube" width="20" align="center"/> Recording](https://youtu.be/eajOS-_0PCk) | Joe Caulfield | N/A |

## 📗 Learn

To learn more about how this dApp works see [How it Works](#how-it-works) below.   
   
You can find the on-chain program in `svg-generator/` and the frontend application that will interface with our program can be found in `app/`.   
   
Built using `npx create-solana-dapp -f next -p native`.   

### About the Solana dApp Scaffold
This workshop, like many others in the Solana Workshops collection, is built using the dApp Scaffold. This scaffold provides a huge handful of out-of-the-box NextJS configs and functionality to get up & running fast with building a dApp on Solana.   
   
Amongst other things, this scaffold gives you:
* Wallet connection support for popular wallets
* Airdrop functionality & components
* User SOL balance store
* Navbar & Footer
* Basic NextJS file structure layout

### How to Build & Run

You'll need to deploy this program to the Solana blockchain before you can successfully run the frontend. You can do this in two ways:
1. Run the `cicd.sh` bash script to build the program with `cargo` and deploy it. Make sure your local Solana configs are targeting the proper cluster; ie. `solana config set -ud` (devnet).
2. Import the program (Rust) code into the [Solana Playground IDE](https://beta.solpg.io) by using the "Import from GitHub" option. You'll want to select `native` and then import the GitHub url that routes to the `workshop-dapps/svg-generator/svg-generator` directory. You should see `src` and `Cargo.toml` if you're in the right place. Then just click "Build" and "Deploy" in the wrench & hammer tab.
   
Next you can choose to run the test or launch the frontend.   
   
To run the test: `yarn install && yarn run test` (in the root directory).   
   
To launch the frontend: `yarn install && yarn dev` (in the `app/` directory).

### How it Works

This Solana program is designed to generate an SVG string from some random inputs.   
   
It's simply going to build a string from a handful of arrays, which house various strings that will change based on the random number (indices) provided.   

Then it will write this string - which represents an SVG image - to a new account on Solana's blockchain.   
   
Our frontend will then be able to render this account's data with a simple read.

#### How Our dApp Works:
![](./svg_generator.jpg)
#### How Solana Transactions Work:
![](./solana_transactions.jpg)
#### Putting it all Together:
![](./writing_data.jpg)

### Active Program ID:
```shell
FQfryewWanut6Am7n17HnM6QftRnRKW7DvjYHNtarDWb
```