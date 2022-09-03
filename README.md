# Solana Validator Node Discovery


Building off of work from [bitcoin peer discovery](https://github.com/jnaulty/bitcoin-peers-discovery), I was curious about understanding the distribution of Solana validators on active on the network.

Solana makes this incredibly easy with the join of two JSON-RPC calls: [getClusterNodes](https://docs.solana.com/developing/clients/jsonrpc-api#getclusternodes) and [getVoteAccounts](https://docs.solana.com/developing/clients/jsonrpc-api#getvoteaccounts)


With this information, I can:

* acquire network address of all nodes on Solana
* identify all validators on the network 


The network address gives valuable information regarding the physical distribution of the Solana Validators.


## Insights


Measured on September 2, 2022

### Validator Distribution by Country

* `26.5%` network addresses were traced to German ISPs
* `20.5%` network addresses were traced to American ISPs
* `27.9%` network addresses were traced to Finnish and French ISPs

![solana-validators-by-country](figures/Solana-Validator-Node-Distribution.png)

![solana-validators-by-country-geo]("figures/Solana-Validator-World-Distribution.png")

### Validator Distribution by ISP

```
Organization Distribution Stats
Hetzner Online GmbH       0.363958
OVH SAS                   0.233216
RELIABLESITE              0.070671
WEBNX                     0.060071
PACKET                    0.042403
IS-AS-1                   0.028269
...
```

![solana-validators-node-isp-distribution](figures/Solana-Validator-Node-ISP-Distribution.png")