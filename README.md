# Bitz-on-eclipse
Detailed Guide to Bitz Miner CLI on Eclipse Network

What is Bitz?
The first ePOW commodity token that anyone can mine on Eclipse.
5M max supply.
NOT pre-mined + ZERO team/insider allocations.
Token address: https://eclipsescan.xyz/token/64mggk2nXg6vHC1qCdsZdEFzd5QGN4id54Vbho4PswCF


let's get started ->

1. Open command prompt (right click and run as admin)

wsl --install   (run this command it will take some time to install and if asked for password input your preferred password)

after successful installation -> restart your computer

now search "ubuntu" in search bar and run it as administrator.

2. Install Rust

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

wait for few mins

3. Install Solana CLI

curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash

this will take sometime so don't panic and wait until it finish.

after successful installation you'll get output like this -
Installed Versions:
Rust: rustc 1.85.0 (4d91de4e4 2025-02-17) 
Solana CLI: solana-cli 2.1.14 (src:3ad46824; feat:3271415109, client:Agave) 
Anchor CLI: anchor-cli 0.30.1 
Node.js: v23.8.0 
Yarn: 1.22.1

4. Create a local keypair/Wallet

solana-keygen new

(take note of your public key and secret phrase (displayed after generation))

5. Set the rpc to Eclipse mainnet:

solana config set --url https://eclipse.helius-rpc.com

(using helius rpc since it works flawlessly)

6. Install Bitz using Cargo

cargo install bitz

(this will take sometime so wait until it finishes)

7. Exporting wallet to backpack

cat ~/.config/solana/id.json

(copy the numbers including [] and open backpack-> import->privatekey->paste to import)

now send 0.0055 eth to that wallet address which will be used as gas fee for mining $BITZ token.




