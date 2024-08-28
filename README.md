# Ethereum Node on Akash Network using Nethermind

**Nethermind** is a high-performance, highly configurable Ethereum execution client built on .NET that runs on Linux, Windows, and macOS and supports Clique, Aura, and Ethash. With breakneck sync speeds and support for external plugins, it provides reliable access to rich on-chain data thanks to a high-performance JSON-RPC interface and node health monitoring with Grafana and Seq.

Check Nethhermind [docs](https://docs.nethermind.io/)

## Deploy on Akash guide

- Create and fund a Keplr or Leap wallet
  - [Keplr wallet](https://akash.network/docs/getting-started/token-and-wallets/#keplr-wallet)
  - [Leap wallet](https://akash.network/docs/getting-started/token-and-wallets/#leap-cosmos-wallet)
- Visit https://console.akash.network/
- Connect your wallet
  - You need to have at least 0.5 AKT in your wallet
- Press the deploy button
- Select "Build your template"
- (Optional) Name your deployment
- Select YAML and paste the [deploy.yaml](deploy.yaml) contents
- Press "Create Deployment"
- Accept wallet transaction
- Review bids and select provider
- Accept provider transaction
- Wait a couple of seconds (docker image download and container setup) and check the logs
- Go to LEASES and press the URI
- Check the [Akash docs](https://akash.network/docs/deployments/cloudmos-deploy/) if you have and questions
- Node is up!

## Ping the rpc interface

```
curl -H "Content-Type: application/json" -X POST --data '{"jsonrpc":"2.0","method":"web3_clientVersion","params":[],"id":67}' <URI>
```

Other rpc request examples can be found [here](https://ethereum.org/en/developers/docs/apis/json-rpc/)
