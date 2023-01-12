# analytics_roadmap


- Creation of a comprehensive Curve analytics platform with real time dashboards for all pools across multiple chains
- Design and implement an alternative, data-rich DAO front-end for improved decision-making by voters.
- Open-source the codebase to encourage community participation and external contributions
- Interface with the Curve team, DAO, integrating protocols and users
- Creation of a LLAMMA/CrvUSD dashboard


## 1. Dedicated analytics platform

Unlike other AMMs like <a href="https://info.uniswap.org/">Uniswap</a> or <a href="https://dune.com/balancerlabs">Balancer</a>, Curve does not have a dedicated analytics page. DeFi-wide analytics platforms like <a href="https://defillama.com/protocol/curve">Defi Llama</a> and community sites focused on the Curve ecosystem like <a href="https://llama.airforce/">Llama Airforce</a> do provide valuable data about Curve, but this situation nonetheless has severe limitations. Namely, the analytics focus on high level metrics (TVL, Volume) but lack the level of depth required for the proper management of the pools (parameter setting, protocol design decisions for future pools). The spread of information accross multiple websites, few of which are focused solely on Curve, also hinders discoverability. To solve these problems we offer to build a dedicated platform for Curve analytics at curvemonitor.com,that provides both high level and more detailed metrics. It will offer a one-stop-shop for all information and data related to Curve pools, increasing discoverability.

We have developed an MVP for what a future dashboard would look like for a standard Curve pool. This real-time dashboard allows allows users to follow trading activity, including miner extractable value (MEV) activity, monitor the historical performance of the pool by displaying assets balances, price fluctuations, and bonding curves.  We are committed to working closely with the Curve core team and the research and risk team to continue improving and enhancing these dashboards. 

Our current roadmap for improvements is as follows:

- Making the MVP dashboard available for all mainnet Curve pools
- Expanding historical data availability to the lifetime of each pool
- Adding new charts to the current dashboard: 
    - Histogram of price ranges to assess historical peg and volatility of a pair
    - Comparison of LP token price performance vs holding strategy vs xy=k 0 fee AMM, with IL calculator
    - Market depth chart (amount required to move price by x%)
    - Historical pool revenue
    - Overlay indicator of pool parameter changes on historical charts to gauge their effect
- Extending support to pools on all chains where Curve is deployed
- Optimizing the user interface for a better and more user-friendly experience
- Offering alerts and data export features


## 2. Alternative DAO front-end

The new Curve website currently lacks a dedicated DAO page and the classic website's DAO page is hampered by extremely slow loading times, confusing navigation and a lack of essential features, such as the option to post new proposals or the decoding of calldata for governance proposals. To increase voter engagement and the dynamism of the DAO's governance, we offer to build an alternative DAO front end that would be faster and more user-friendly than the current one. The front-end will offer additional metrics to help users make more informed decisions. We also aim to integrate with veCRV derivatives such as vlCVX to offer all voters in the ecosystem a unified and intuitive voting experience.

We recently released a governance vote page on llama.airforce as a first stepping stone to this project. The list of future developments is as follows:

- Add the option to vote directly using veCRV, vlCVX or other veCRV derivatives with governance rights on the governance vote page.
- Create a page for gauge weight votes
- Add new metrics when displaying gauge candidates to guide voter's decisions: TVL and volume changes, incentives posted and fees collected over the past 2 rounds.
- Develop a UI for vote creation, including templates for the most common actions: parameter changes, gauge addition and gauge removal. 
- (Subject to further discussion and approval from Curve team): Create a marketplace contract and UI where users with no veCRV can post a proposal and a small bounty. Users with 2.5k veCRV can then post the proposal on their behalf and claim the bounty for gas reimbursement. 
- Historical tracking of veCRV incentives on different marketplaces (votemarket, warden, votium, bribe.crv.finance)
- Profile page to track users' voting history

## 3. Open code-base




## 4. Interface with Curve team, DAO, integrating protocols and users

- Work with contributors contracted to do punctual specific tasks. For instance to turn a research report into a continuously updated dashboard, reproduce dashboards from third-party platforms (Dune, Flipside...)
- Work with the Curve core team and research team to provide them with the data stream they require.

