# Solana Validator Node Discovery


Building off of work from [bitcoin peer discovery](https://github.com/jnaulty/bitcoin-peers-discovery), I was curious about understanding the distribution of Solana validators active on the network.

Solana makes this incredibly easy with the combination of two JSON-RPC calls: 
* [getClusterNodes](https://docs.solana.com/developing/clients/jsonrpc-api#getclusternodes) 
* [getVoteAccounts](https://docs.solana.com/developing/clients/jsonrpc-api#getvoteaccounts)


With this information, I can:

* identify all validators on the network  
* acquire network address of all nodes on Solana



The network address gives valuable information regarding the physical distribution of the Solana Validators.


# September 3, 2022 Report


`tl;dr` updates since Yesterday's report:

* Percent of Solana Validators covered from scan: 95.35%


Improvements:

* shodan api instead of ipapi.co allowed for less rate limiting and perhaps more accurate info


Increased IP Analysis from `328` to `1846` nodes

* `27` unique countries
* `153` unique ISPs


## Validator Distribution by Country

With the updated stats:

* USA has the most validators: `31.6%`
* Germany comes in second: `24.5%`
* Finland comes in third: `10.1%`

```
Country Distribution Stats
US    0.315591
DE    0.244624
FI    0.100538
FR    0.092473
CH    0.050000
CA    0.048387
GB    0.025806
RU    0.025806
PL    0.023656
NL    0.015591
```
![solana-validators-by-country](figures/shodan_data_sep3_2022/Solana-Validator-Node-Distribution.png)

![solana-validators-by-country-geo](figures/shodan_data_sep3_2022/Solana-Validator-World-Distribution.png)

## Validator Distribution by ISP


```
Organization Distribution Stats
Hetzner Online GmbH                 0.250813
OVH SAS                             0.085590
Alabanza, Inc.                      0.066089
Hetzner Online AG                   0.057421
ReliableSite.Net LLC                0.057421
Max Goeldi trading as Goeldi Tec    0.050379
WebNX, Inc.                         0.042795
Interserver, Inc                    0.035211
University of Winnipeg              0.025460
Packet Host, Inc.                   0.023835
```

![solana-validators-node-isp-distribution](figures/shodan_data_sep3_2022/Solana-Validator-Node-ISP-Distribution.png)

## Europe Distribution Info

Two European ISPs take up `59%` of the Solana Validators ISP Distribution they are [Hetzner Online GmbH](https://en.wikipedia.org/wiki/Hetzner) and [OVH SAS](https://en.wikipedia.org/wiki/OVHcloud).




![solana validators in europe](figures/shodan_data_sep3_2022/solana-validators-in-europe.png)


### German Distribution

Top German ISPs

```
Hetzner Online GmbH          0.606593
Hetzner Online AG            0.232967
OVH GmbH                     0.085714
myLoc managed IT AG          0.013187
IP-Projects GmbH & Co. KG    0.010989
Contabo GmbH                 0.008791
marbis GmbH                  0.008791
Oracle Public Cloud          0.006593
```

![solana validators in Germany Bar Chart](figures/shodan_data_sep3_2022/Solana-Validator-German-ISP-Distribution-bar.png)

![solana validators in Germany](figures/shodan_data_sep3_2022/SSolana-Validator-German-Distribution.png)

## USA Distribution Info

Top 10 ISPs in USA
```
Alabanza, Inc.                      0.207836
ReliableSite.Net LLC                0.180579
WebNX, Inc.                         0.134583
Interserver, Inc                    0.110733
DXC US Latin America Corporation    0.052811
Enzu Inc                            0.027257
Equinix Services, Inc.              0.025554
RackNerd LLC                        0.018739
TeraSwitch Networks Inc.            0.018739
Perfect International, Inc          0.013629
```

![solana validators in USA bar chart](figures/shodan_data_sep3_2022/Solana-Validator-USA-Distribution-barchart.png)

![solana validators in USA](figures/shodan_data_sep3_2022/Solana-Validator-USA-Distribution.png)


----------------------------------------------------------------------------



# September 2, 2022 Report


## Validator Distribution by Country

Solana Validators network addresses were traced to 19 unique countries.

* `26.5%` network addresses were traced to German ISPs
* `20.5%` network addresses were traced to American ISPs
* `27.9%` network addresses were traced to Finnish and French ISPs

Distribution Breakdown by [Country Code](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)

```
DE    0.265018
US    0.204947
FI    0.151943
FR    0.127208
GB    0.049470
PL    0.042403
CA    0.042403
NL    0.031802
RU    0.024735
LT    0.010601
UA    0.010601
IE    0.010601
JP    0.007067
IN    0.003534
RO    0.003534
ES    0.003534
SG    0.003534
TR    0.003534
SC    0.003534
```

![solana-validators-by-country](figures/Solana-Validator-Node-Distribution.png)

![solana-validators-by-country-geo](figures/Solana-Validator-World-Distribution.png)

One quick conclusion from the World Distribution From this dataset, it appears there is not a lot of nodes on the African, Asian, and South American continents.

## Validator Distribution by ISP

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

![solana-validators-node-isp-distribution](figures/Solana-Validator-Node-ISP-Distribution.png)



## Europe Distribution Info

Two European ISPs take up `59%` of the Solana Validators ISP Distribution they are [Hetzner Online GmbH](https://en.wikipedia.org/wiki/Hetzner) and [OVH SAS](https://en.wikipedia.org/wiki/OVHcloud).




![solana validators in europe](figures/solana-validators-in-europe.png)


### German Distribution

Top German ISPs

```
Hetzner Online GmbH          0.800000
OVH SAS                      0.106667
Contabo GmbH                 0.026667
myLoc managed IT AG          0.026667
IP-Projects GmbH & Co. KG    0.013333
diva-e Datacenters GmbH      0.013333
PACKET                       0.013333
```

![solana validators in Germany Bar Chart](figures/Solana-Validator-German-ISP-Distribution-bar.png)

![solana validators in Germany](figures/Solana-Validator-German-Distribution.png)

## USA Distribution Info

Top 10 ISPs in USA
```
RELIABLESITE             0.310345
WEBNX                    0.293103
IS-AS-1                  0.137931
PACKET                   0.086207
TIER-NET                 0.051724
PERFECT-INTERNATIONAL    0.034483
AMAZON-AES               0.017241
SERVER-MANIA             0.017241
LEVEL3                   0.017241
TERASWITCH               0.017241
```

![solana validators in USA bar chart](figures/Solana-Validator-USA-Distribution-barchart.png)

![solana validators in USA](figures/Solana-Validator-USA-Distribution.png)

## Special Thanks

Thanks for making this information easy to acquire!

* Solana makes this data free to all who can connect to the network
* `ip` information was retrieved by [ipapi.co](https://ipapi.co)