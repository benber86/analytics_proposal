# Proposal to fund an analytics team for the Curve ecosystem


## Overview

### Sentence summary

We propose to develop a dedicated, real-time analytics platform for Curve that provides a one-stop-shop for both high-level and detailed metrics on Curve's pools, DAO and future lending activities.

### Summary

We propose to develop a dedicated, real-time analytics platform that provides both high-level and detailed metrics for the Curve ecosystem. This platform will increase discoverability by serving as a comprehensive source for all relevant information and data on Curve's pools. Additionally, we propose to build an alternative, user-friendly DAO front-end that includes pool health metrics. Our team will collaborate closely with the Curve core team and other teams within the DAO. We aim to create an open-source codebase that is easy for external developers to integrate with and contribute to.

The proposal is for $200,000 in funding for a one-year period to pay for one full-time developer and two part-time developers, as well as infrastructure costs. At the end of the grant period, we will submit an activity report to the DAO detailing the features delivered over the period. If the progress is deemed satisfactory, we will then apply for a renewal of the grant for another year, revising the terms based on an updated roadmap and forecasted infrastructure costs. We see the platform as a critical component of the growth of the Curve ecosystem over time and therefore aim to anchor our collaboration with the DAO within a long-term perspective.

We offer a below a detailed overview of our vision and the features we aim to deliver over a multi-year horizon. We also provide a roadmap of what we intend to accomplish during our first year of funding and a budget. Part of the budget is allocated for unforeseen infrastructure and personnel costs and will be refunded to the DAO if unspent at the end of the one-year period.

## Proposers

### Team overview

- Alunara and Benny have been offering Curve related analytics on llama.airforce and have actively participated in various Curve DAO activities since 2021. 
- Philipp spent the last 2 years working full time as a backend dev in a crypto hedge fund building dashboards, portfolio tracking tools and trading bots. Philipp contributed extensively to the new dashboard MVP.

### Team roles and responsibilities

- **Alunara**: Front-end development, DevOps
- **Benny**: Back-end development, Subgraph development & maintenance, Management and liaison with other teams within the DAO and integrating protocols
- **Philipp**: Back-end development, DevOps

## Vision and specifications

### 1. Dedicated analytics platform

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


### 2. Alternative DAO front-end

The new Curve website currently lacks a dedicated DAO page and the classic website's DAO page is hampered by extremely slow loading times, confusing navigation and a lack of essential features, such as the option to post new proposals or the decoding of calldata for governance proposals. To increase voter engagement and the dynamism of the DAO's governance, we offer to build an alternative DAO front end that would be faster and more user-friendly than the current one. We see this task as synergetic with the development of pool dashboards, as the DAO front-end should offer appropriate pool health metrics to help users make more informed decisions and pool parameter changes are subject to the DAO's approval. We also aim to integrate voting options on the UI for veCRV derivatives such as vlCVX to offer all voters in the ecosystem a unified and intuitive experience.

We recently released a governance vote page on llama.airforce as a first stepping stone to this project. The list of future planned developments is as follows:

- Add the option to vote directly using veCRV, vlCVX or other veCRV derivatives with governance rights on the governance vote page
- Create a page for gauge weight votes
- Add new metrics when displaying gauge candidates to guide voter's decisions: TVL and volume changes, incentives posted and fees collected over the past 2 rounds.
- Develop a UI for vote creation, including templates for the most common actions: parameter changes, gauge addition and gauge removal
- (Subject to further discussion and approval from Curve team): Create a marketplace contract and UI where users with no veCRV can post a proposal and a small bounty. Users with 2.5k veCRV can then post the proposal on their behalf and claim the bounty for gas reimbursement
- Historical tracking of veCRV incentives on different marketplaces (votemarket, warden, votium, bribe.crv.finance)
- Profile page to track users' voting history


### 3. Interface with Curve team, DAO, integrating protocols and users

The Curve core team and other teams within the DAO regularly gather data and produce analytics to inform decision-making processes. In certain instances, third-party companies or community members may be contracted or volunteer to generate specific reports and research. However, a significant proportion of these outputs are disseminated on disparate self-hosted domains or third-praty platforms (Dune, Flipside...), forgotten in git repositories, and/or left unmaintained. To address this issue, we propose to expand our responsibilities to include working directly with external contributors to ensure that their output, if deemed significant enough, can be integrated into a continuously updated and maintained dashboards on our analytics platform. By adopting this approach, we will also ensure continuity in the analytics knowledge base for Curve, enabling us to provide guidance to protocols and users seeking Curve-related metrics. Additionally, we will be able to explain the calculation methodology and origins of the data used in these metrics. 

- Making a web UI for users to run in-browser pool simulations using the research team's CurveSim package
- Work with the Curve core team and research team to provide them with the data streams and metrics they need. For instance:
    - Provide needed historical data for the research team's CurveSim package
    - Create a simulator to estimate changes in volume and revenue at different fee levels to set more competitive pool fees.
- Ensure high availability and proper documentation for all our public API endpoint
- Maintain a decentralized data source for generic Curve pools/DAO metrics on the Graph
- Field analytics-related questions on Telegram and Discord


### 4. Open code-base


In an effort to promote open collaboration and facilitate contributions we will work to consolidate the existing codebase which is currently fragmented accross multiple git organizations and repositories, establish guidelines for contributors and improve documentation to make it easier for people to reuse our code. 

- Ensure that all repositories within the codebase maintain a minimum level of documentation
- Create a git organization and migrate the various existing repositories to it
- Implement concise contribution guidelines and templates for issues/PR


### 5. LLAMMA/crvUSD dashboard

This part can only be speculative until the release of LLAMMA and its associated UI, however we can anticipate that this new feature will require detailed metrics to inform both core developers and users' decisions. 

## Roadmap

## Budget
