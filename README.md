# Nesa-Node-Run-Guide
In this step-by-step walkthrough, I’ll show you how to set up and run a Nesa Miner Node on your PC, laptop, or VPS from start to finish.

![image alt](https://github.com/CryptoGurujiOG/Nesa-Node-Run-Guide/blob/667769218059ce07719717b36bfed58f15b8d2ea/Image1.jpg)

## Minimum Hardware Requirements

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
# Step 3:

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
