# Nesa-Node-Run-Guide
## In this step-by-step walkthrough, I’ll show you how to set up and run a Nesa Miner Node on your PC, laptop, or VPS from start to finish.

![image alt](https://github.com/CryptoGurujiOG/Nesa-Node-Run-Guide/blob/667769218059ce07719717b36bfed58f15b8d2ea/Image1.jpg)

## Minimum Hardware Requirements:

- CPU: 4 Cores minimum
- RAM: 8 GB minimum
- Storage: 100 GB SSD minimum
- Internet: Stable connection

---

- If you want to run Nesa node on your pc/laptop, then install WSL using this 👉 [Guide](https://github.com/CryptoGurujiOG/Install-Ubuntu-on-Windows-using-WSL)
- If you want to run Nesa node on a VPS, then watch my video guide 👉 [Video](https://youtu.be/NK431xjj7yA)

---

# Step 1:

## Update system and install dependencies:

```
sudo apt update && sudo apt upgrade -y
```
# Step 2:

- 🖥️ PC and Laptop users: Install and run the latest version of Docker Desktop on your device - [Link](https://www.docker.com/products/docker-desktop/)

## Install Docker:

```
sudo apt install -y ca-certificates curl gnupg lsb-release
curl -fsSL https://get.docker.com | sh
sudo usermod -aG docker $USER
newgrp docker
docker --version
```

# Step 3:

## Install Screen to Run Node in Background:

```
sudo apt update
sudo apt install screen -y
```

## Create Screen:

```
screen -S nesa
```

# Step 4:

## Install Python Dependencies:

```
sudo apt install -y python3-dev build-essential libffi-dev libssl-dev pkg-config
```

## Create Virtual Environment:

```
python3 -m venv ~/.nesa/venv
source ~/.nesa/venv/bin/activate
```

## Upgrade Pip:

```
pip install --upgrade pip setuptools wheel
```

## Install Required Packages:

```
pip install --prefer-binary \
  ecdsa \
  base58 \
  mospy-wallet \
  httpx \
  betterproto \
  ripemd-hash
```

# Step 5:

## Run Nesa Bootstrap Script:

```
bash <(curl -s https://raw.githubusercontent.com/nesaorg/bootstrap/master/bootstrap.sh)
```

## When prompted:

- Choose Node Name and Press Enter
- Select Continue and Press Enter
- Enter Referral Code 👉 `nesa1rgl2hxy07jmu7dfpyhjdl4fh9qqvl2vq50d3cc` 
- Press Enter
- Select Continue and Press Enter

---

# Step 6:

## Create API key (Access Token):

- Visit: https://huggingface.co/
- Click Sign Up
- Enter email, Create password & Enter
- Create username, Enter Full name
- Click Create Account
- Open your mail and confirm your email
- Click on Profile icon
- Select Access Tokens
- Click Create new token
- Enter Token name: like Nesa Node, etc
- Scroll down and click Create token
- Copy and save your Access Token

---

Go back to the Terminal

- Paste the API key (Access Token) and Press Enter
- Select Continue and Press Enter
- Select Generate new wallet and Press Enter
- Save Private Key, Wallet Address, and Public Key (important)
- Click Yes, I have saved it, and Press Enter
- Select Check Balance and Press Enter
- Fund Your Wallet
- Copy node wallet address

---

# Step 7:

## Claim Testnet $NES Tokens:

Option 1

- Visit: https://beta.nesa.ai/
- Register your account
- Click Wallet (top right corner)
- Click Nesa Faucet (top right corner)
- Connect your Keplr wallet
- Click Request Tokens
- Open your Keplr wallet
- Click Deposit, Search Nesa, and Enable it
- Click Send, Search Nesa, and select it
- Click Send, Paste node wallet address
- Enter amount 1 NES
- Click Next and Appprove

Option 2

- You can ask testnet $NES in our Telegram chat group: [Join](https://t.me/CryptoGurujiOG/3444)

---

Go back to the Terminal

- Select Check Balance and Press Enter
- Select Continue and Press Enter
- Select Start Node Now and Press Enter
- Deposit amount (NES): 0.1 and Press Enter
- Select Next and Press Enter
- Select Submit Deposit and Press Enter
- Select Back and Press Enter
- Now your node is running and contributing

## Detach screen safely, it will keep Node Running in the Background:

## Detach Screen:

```
CTRL + A + D
```

## Reattach Screen:

```
screen -r nesa
```

- You can restart, stop, and check Node status using this command:

```
bash <(curl -s https://raw.githubusercontent.com/nesaorg/bootstrap/master/bootstrap.sh)
```
---

⚠️  I will share a step-by-step video guide on my Twitter and YouTube very soon.

📢 Make sure to follow us for regular updates

- Twitter: https://x.com/CryptoGurujiOG
- Youtube: https://www.youtube.com/@CryptoGurujiOG
- Telegram: https://t.me/CryptoGurujiOG
