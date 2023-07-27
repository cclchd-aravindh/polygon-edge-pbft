# Polybft consensus

---

**Important**

Need to set the IBFT rootchain details in polygon-edge.sh

Path - docker/local/polygon-edge.sh

```bash
    ROOT_CHAIN_RPC=""
    MOCK_ERC20=""
    PRIVATE_KEY=""
```
---

#### use `polybft` consensus
* `cd core-contracts && npm install && npm run compile && cd -` - install `npm` dependencies and compile smart contracts
* `go run ./consensus/polybft/contractsapi/artifacts-gen/main.go` generate needed code
* `export EDGE_CONSENSUS=polybft` - set `polybft` consensus
* `docker-compose -f ./docker/local/docker-compose.yml up -d --build` - deploy environment

#### stop / destroy 
* `docker-compose -f ./docker/local/docker-compose.yml stop` - stop containers
* `docker-compose -f ./docker/local/docker-compose.yml down -v` - destroy environment



