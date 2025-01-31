### Polygon Mainnet

RelayHub: [0x6C28AfC105e65782D9Ea6F2cA68df84C9e7d750d](https://explorer-mainnet.maticvigil.com/address/0x6C28AfC105e65782D9Ea6F2cA68df84C9e7d750d)

Forwarder: [0xdA78a11FD57aF7be2eDD804840eA7f4c2A38801d](https://explorer-mainnet.maticvigil.com/address/0xdA78a11FD57aF7be2eDD804840eA7f4c2A38801d)

Paymaster: [0x9d47218ce8b8F123Efbb1Db3E0DdBe6490Cf77E1](https://explorer-mainnet.maticvigil.com/address/0x9d47218ce8b8F123Efbb1Db3E0DdBe6490Cf77E1)

VersionRegistry: [0x4Fe8824c885D67613848c94a15dce7680897f33E](https://explorer-mumbai.maticvigil.com/address/0x4Fe8824c885D67613848c94a15dce7680897f33E)

#### Recommeneded Server configuration
gsn-relay-config.json:
```json
{
  "baseRelayFee": 0,
  "pctRelayFee": 70,
  "relayHubAddress": "0x6C28AfC105e65782D9Ea6F2cA68df84C9e7d750d",
  "ownerAddress": "<OWNER_ADDRESS>",
  "gasPriceFactor": 1,
  "confirmationsNeeded": 1,
  "ethereumNodeUrl": "https://rpc-mainnet.maticvigil.com/",
  "coldRestartLogsFromBlock": 22051314,
  "registrationBlockRate": 1000,
  "pastEventsQueryMaxPageSize": 900,
  "maxGasPrice": 1e12,
  "workerMinBalance": 0.5e18,
  "workerTargetBalance": 0.5e18
}
```
#### Recommeneded client configuration
```js
  // add the following fields to your GSNConfig:
  const gsnConfig: Partial<GSNConfig> = {
    relayLookupWindowBlocks: 990,
    relayRegistrationLookupBlocks: 990,
    pastEventsQueryMaxPageSize: 990,
  }
  const gsnProvider = RelayProvider.newProvider({provider: web3Provider, config: gsnConfig})
  await gsnProvider.init()
```
