# analytics_roadmap


- Creation of a comprehensive Curve analytics platform with real time dashboards for all pools across multiple chains
- Design and implement an alternative, data-rich DAO front-end for improved decision-making by voters.
- Creation of a LLAMMA/CrvUSD dashboard
- Open-source the codebase to encourage community participation and external contributions
- Interface with the Curve team, DAO, integrating protocols and users


## 1. Dedicated analytics platform

Unlike other AMMs like <a href="https://info.uniswap.org/">Uniswap</a> or <a href="https://dune.com/balancerlabs">Balancer</a>, Curve does not have a dedicated analytics page. DeFi-wide analytics platforms like <a href="https://defillama.com/protocol/curve">Defi Llama</a> and community sites focused on the Curve ecosystem like <a href="https://llama.airforce/">Llama Airforce</a> do provide valuable data about Curve, but this situation nonetheless has severe limitations. Namely, the analytics focus on high level metrics (TVL, Volume) but lack the level of depth required for the proper management of the pools (parameter setting, protocol design decisions for future pools). The spread of information accross multiple websites, few of which are focused solely on Curve, also hinders discoverability. To solve these problems we offer to build a dedicated platform for Curve analytics at curvemonitor.com,that provides both high level and more detailed metrics. It will offer a one-stop-shop for all information and data related to Curve pools, increasing discoverability.

We have developed an MVP for what a future dashboard would look like for a standard Curve pool. This real-time dashboard allows allows users to follow trading activity, including miner extractable value (MEV) activity, monitor the historical performance of the pool by displaying assets balances, price fluctuations, and bonding curves.  We are committed to working closely with the Curve core team and the research and risk team to continue improving and enhancing these dashboards. Our current roadmap/task list for improvements is as follows:

- Making the MVP dashboard available for all mainnet Curve pools
- Expanding historical data availability to the lifetime of each pool
- Adding new charts to the current dashboard: histogram of price ranges to assess historical peg and volatility of a pair, comparison of LP token price performance vs holding vs xy=k with IL calculator, market depth chart, collected fees chart
- Extending support to pools on all chain where Curve is deployed
- Optimizing the user interface for a better and more user-friendly experience
- Offering alert and export features


## 2. Alternative DAO front-end






