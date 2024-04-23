# DV Processing
Processing this set of binary files that use your crypto wallets and notify the dv-backend of new transactions in the building.

## 💵 Support currency
- [x] Bitcoin
- [x] USDT (TRC20)
- [ ] ETH
- [ ] USDT (ERC20)

## ⚙️ Requirements
* Linux based server
* Postgresql 15+
* Systemd or any init system


 ## Install

1. Clone this repository on you server
2. Copy `config.yaml.example` to `config.yaml`
3. In config change credential for access Database, Explorers, Blockchain Node
4. Copy `processing.service` and `blockparser@.service` on `/etc/systemd/system/`
5. Change on this service file path to you bin files
6. Start demons:

    ```systemctlc start processing```
    
    ```systemctlc start blockparser@btc```
    
    ```systemctlc start blockparser@tron```