# Go-Simple-Storage-Fcc
this is a golang version of Charter 5 Ethers-simple-storage-fcc code. 
Follow the blog for more detail information. 

[https://medium.com/@kunalsagar/deploy-solidity-contract-using-golang-go-simple-storage-fcc-b247b29ffa18](https://medium.com/@kunalsagar/deploy-solidity-contract-using-golang-go-simple-storage-fcc-b247b29ffa18)

## Clone the repo
    
```
    git clone https://github.com/kunalrsagar/go-simple-storage-fcc
```

## Download dependencies
Download all your dependencies
```
go get all
```

## Build
Build abi, bin & auto-generate SimpleStorage.go file 
```
solc --optimize --abi --bin ./SimpleStorage.sol -o build

mkdir api

abigen --abi=./build/SimpleStorage.abi --bin=./build/SimpleStorage.bin --pkg=api --out=./api/SimpleStorage.go

```

## Ganache
make sure ganche is running. 

## Environment variables
set RPC_URL & Wallets PRIVATE_KEY
```
export RPC_URL=<local_ganache_url:port>
export PRIVATE_KEY=<Wallet Private key>
```

## Run the deploy.go
```
go run deploy.go
```