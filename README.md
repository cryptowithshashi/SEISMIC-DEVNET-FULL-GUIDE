
# SEISMIC DEVENET FULL GUIDE

Welcome! This walkthrough is quick and requires only a minute of actual attention, with the rest being just waiting.

If you run into any issues, check the FAQ section, where we’ve resolved 10 common errors. You can also join the Seismic Discord server and ask your questions in the #devnet channel.

Please note that this is not an incentivized testnet.




## OVERVIEW

#### Seismic Official Links


| Siesmic Devnet | Links     |
| :-------- | :------- | 
| Network Name | Seismic devnet |
| Currency Symbol | ETH |
| Chain ID | 5124 |
| RPC URL (HTTP) | `https://node-2.seismicdev.net/rpc |
| RPC URL (WS) | wss://node-2.seismicdev.net/ws |
| Explorer| https://explorer-2.seismicdev.net/ |
| Faucet | https://faucet-2.seismicdev.net/ |


## SETUP GUIDE STEP - BY - STEP

## Deploy an encrypted contract

Install Rust

```bash
  curl https://sh.rustup.rs -sSf | sh
```
Install jq for mac
```bash
  brew install jq

```
Install jq for ubuntu
```bash
  sudo apt install jq
```
Install sfoundryup
```bash
  curl -L \
     -H "Accept: application/vnd.github.v3.raw" \
     "https://api.github.com/repos/SeismicSystems/seismic-foundry/contents/sfoundryup/install?ref=seismic" | bash
source ~/.bashrc
```
Run sfoundryup
```bash
  sfoundryup
```
Clone repository
```bash
  git clone --recurse-submodules https://github.com/SeismicSystems/try-devnet.git
```
```bash
  cd try-devnet/packages/contract/
```
Deploy contract
```bash
  bash script/deploy.sh

```

## Interact with an encrypted contract

Install Bun

```bash
  curl -fsSL https://bun.sh/install | bash
```
 Install node dependencies
```bash
  cd try-devnet/packages/cli/
  bun install

```
Send transactions
```bash
  bash script/transact.sh
```


## FAQ ANSWERED FROM SEISMIC

1. What if I'm on Windows?

We recommend using WSL to run commands as if you were on a Linux machine. Run

```bash
  wsl --install
```
Now restart your computer. After booting back up, you should be able to run the below command and follow the rest of the steps like normal


```bash
  wsl

```
---
2. I'm stuck at 1108/1112 when running sfoundryup.
Some machines take up to an hour to do this step. If it takes longer, ask a question in our Discord's #devnet channel.

---

3. I'm getting Command failed: cargo build --bins --release.

Means your machine doesn't have Cargo. If you're on Linux, run
```bash
  sudo apt update && sudo apt install -y build-essential
  sudo apt install cargo -y

```
---

4. I'm getting jq (command not found)?
Means step #2 didn't work. If you're on Linux, run:
```bash
  sudo apt-get install jq

```
---

5. I'm getting Address not funded. Please check if your faucet transaction went...
Means your wallet has no testnet ETH. Please go to the faucet, enter the address the script gave you, and wait for the green confirmation.

---

6. I'm getting Command 'brew' not found?
Means your machine doesn't have the Homebrew package manager. Run:
```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

```

---

7. I'm getting linker 'cc' not found.
You can resolve it by running:

```bash
  sudo apt update && sudo apt install -y build-essential
  sudo apt install cargo -y

```

---

8. I'm getting command not found: sfoundryup.
If this comes up even after you complete step #3 successfully, restart your terminal. You should be able to run it after.

----

9. I'm getting info: aborting installation.
Means you aren't selecting an option for your Rust installation. Run the curl command again, and press Enter.

---

10. I'm getting Command: 'bun' not found.
You need to add bun to your PATH. You can either do this temporarily in your current terminal via the command below (you'll have to do it for every new window):

```bash
  export PATH="/home/$(whoami)/.bun/bin:$PATH"

```

```bash
  export PATH="/home/$(whoami)/.bun/bin:$PATH"

```
----


### FINAL STEP OF SEISMIC DEVNET 
If you have done all these steps, send a screenshot in the Seismic Discord on the #devnet channel. Let the photos include interactions on encrypted contract and deploy

## ABOUT ME

Twitter -- https://x.com/SHASHI522004

Github -- https://github.com/cryptowithshashi

Telegram -- https://t.me/crypto_with_shashi


Disclaimer -- I did not create or write any of these codes; they are all available on the official Seismic website. This repository was created solely to help the community, with no other intentions. If you have any questions or concerns, feel free to chat with us on Telegram.
