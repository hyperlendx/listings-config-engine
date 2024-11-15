# Listings Config Engine

The contract is used to add new assets to the HyperLend markets

---

ListingsConfigEngine can either be deployed on its own or using the ConfigEngineFactory contract.

```
- Create & encode the proposal
- Deploy ConfigEngine instance (or use ConfigEngineFactory)

- Make ConfigEngine contract riskAdmin on the pool using PoolConfigurator
- Make ConfigEngine contract listingsAdmin on the pool using PoolConfigurator

- run simulations...
- call executeProposal()

- Remove ConfigEngine from riskAdmin
- Remove ConfigEngine from listingsAdmin
```

---

Run simulations: `npx hardhat run scripts/simulation.js --network hardhat`
(uncomment `forking` variable in `networks: hardhat` in `hardhat.config.js` first to simulate against forked network)

---

Tests:

`npx hardhat test`