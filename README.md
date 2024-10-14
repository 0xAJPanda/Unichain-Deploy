### Unichain Contract Deployment

This can be done on WSL, VPS, or gitpod

### Install foundry

```
curl -L https://foundry.paradigm.xyz | bash
```

```
source /root/.bashrc
```

```
foundryup
```

```
forge --version
```

### Create a working directory

```
mkdir uniswapcontract  && cd uniswapcontract

```

### Edit foundry.toml

```
nano foundry.toml
```

Paste :

```
[rpc_endpoints]
unichain = "https://sepolia.unichain.org"
```

CTRL+X, then Y and ENTER

### Clone OpenZeppelin

```
git clone https://github.com/OpenZeppelin/openzeppelin-contracts.git "openzeppelin"
```

### Clone this repo

```
git clone https://github.com/0xAJPanda/Unichain-Deploy.git "ccuniscripts"
```

### Deploy Helloworld

```
forge create ccuniscripts/helloworld.sol:HelloWorld --rpc-url unichain --private-key {YourPrivateKey}
```

**Explorer** : https://sepolia.uniscan.xyz/

Paste your public address to see your transaction on the explorer

### Deploy ERC20 token

```
forge create ccuniscripts/erc20.sol:Console --constructor-args <youraddress> --rpc-url unichain --private-key {YourPrivateKey}
```

### Send to Another Address

```
cast send <ContractAddress> "transfer(address,uint256)" <receiveraddress> 100000000000000000000  --rpc-url unichain  --private-key <yourprivkey>
```

**Follow Me : **: https://x.com/0xAJPAnda 🫰
