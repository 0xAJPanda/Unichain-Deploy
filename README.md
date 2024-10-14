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

### Clone CryptoConsole Repo

```
git clone https://github.com/stealeruv/Unichain-Deploy.git "ccuniscripts"
```

### Deploy Helloworld

```
forge create ccuniscripts/helloworld.sol:HelloWorld --rpc-url unichain --private-key {YourPrivateKey}
```

**Explorer** : https://sepolia.uniscan.xyz/

### Deploy ERC20 token

```
forge create ccuniscripts/erc20.sol:Console --constructor-args <youraddress> --rpc-url unichain --private-key {YourPrivateKey}
```

### Send to Another Address

```
cast send <ContractAddress> "transfer(address,uint256)" <receiveraddress> 100000000000000000000  --rpc-url unichain  --private-key <yourprivkey>
```

**Follow Me : **: https://x.com/0xAJPAnda 🫰
