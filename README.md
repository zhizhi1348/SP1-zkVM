# SP1-zkVM
![Cover](https://github.com/zhizhi1348/SP1-zkVM/blob/main/SP1-Cover.png)
# Generating ZK Proof via Succinct SP1
**SP1 is an open source zkVM which generate zkProof for transaction to prove execution process to the verifier, So in this guide we'll learn how to generate a zkProof by SP1**

[Succinct Twitter](https://x.com/SuccinctLabs)

[Succinct Documentation](https://docs.succinct.xyz/)
## Install dependencies
```
sudo apt update && sudo apt upgrade -y
sudo apt install cmake pkg-config libssl-dev build-essential -y

# install Rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source "$HOME/.cargo/env"

# install SP1
curl -L https://sp1.succinct.xyz | bash
source /root/.bashrc
sp1up

# check version
cargo +succinct --version
```
![First](https://github.com/zhizhi1348/SP1-zkVM/blob/main/First.png)
## Create an SP1 Project
```
cargo prove new fibonacci
cd fibonacci/script
```
### execute the program without proof
```
RUST_LOG=info cargo run --release -- --execute
```
![Second](https://github.com/zhizhi1348/SP1-zkVM/blob/main/Second.png)
### execut the program with proof
```
RUST_LOG=info cargo run --release -- --prove
```
![third](https://github.com/zhizhi1348/SP1-zkVM/blob/main/Third.png)

