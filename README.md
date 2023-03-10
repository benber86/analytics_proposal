# Proposal to fund an analytics platform for Curve

## Index

- [Overview](#overview)
  - [Sentence summary](#sentence-summary)
  - [Summary](#summary)
- [Proposers](#proposers)
  - [Team overview](#team-overview)
  - [Team roles and responsibilities](#team-roles-and-responsibilities)
- [Long-term vision and specifications](#long-term-vision-and-specifications)
  1. [Dedicated analytics platform](#1-dedicated-analytics-platform)
  2. [Alternative DAO front-end](#2-alternative-dao-front-end)
  3. [Interface with Curve team, DAO, integrating protocols and users](#3-interface-with-curve-team-dao-integrating-protocols-and-users)
  4. [Open code-base](#4-open-code-base)
  5. [LLAMMA/crvUSD dashboard](#5-llammacrvusd-dashboard)
- [One-year roadmap](#one-year-roadmap)
- [Budget](#budget)
  - [Salaries](#salaries)
  - [Design, infrastructure and operational costs](#design-infrastructure-and-operational-costs)

## Overview

### Sentence summary

We apply for a **$128,000 grant to create a dedicated analytics platform for Curve** that will provide real-time metrics for all of Curve's pools, DAO, and future lending activities.

### Summary

We propose to develop a dedicated, **real-time analytics platform** that provides both high-level and detailed metrics for Curve's pools, including but not limited to:
- High-level pool metrics (bonding curves, historical volume, balances, prices)
- MEV monitoring
- Pool revenue
- Market depth 

An MVP of the future proposed platform is available for the sUSD pool at: <a href="https://www.curvemonitor.com">curvemonitor.com</a> 

<p align="center"><img src="https://user-images.githubusercontent.com/25791237/221824730-b7d9cd75-b105-4fc3-8ad5-b0ee1466a58a.png" height=308 width=238></img></p>


Additionally, we propose to build an **alternative, fast & user-friendly DAO front-end** that includes statistics about veCRV, bribes, and pool health metrics to better inform voters. The platform will build on the existing Curve DAO page on the <a href="https://llama.airforce/#/curve/dao/proposals">LLama Airforce website</a> but will move to a separate domain.

The proposal is for **$128,000 in funding for one year to pay for one full-time developer as well as design and infrastructure costs**:
- $100,000 will go to pay a full-time developer salary for Philipp. 
- $20,000 will be spent on design and infrastructure costs with any unused funds returned to the DAO at the end of the grant period. 

The developer will work with the Llama Airforce team - which is already receiving funding. At the end of the grant period, we will submit an activity report to the DAO detailing the features delivered over the period. If the progress is deemed satisfactory, we will then apply for a renewal of the grant for another year, revising the terms based on an updated roadmap and forecasted infrastructure costs. We see the platform as a critical component of the growth of the Curve ecosystem over time and therefore aim to anchor our collaboration with the DAO within a long-term perspective. Our team will collaborate closely with the Curve core team and other teams within the DAO. We aim to create an open-source codebase that is easy for external developers to integrate with and contribute to.

We offer below a detailed overview of our vision and the features we aim to deliver over a multi-year horizon. We also provide a roadmap of what we intend to accomplish during our first year of funding and a budget. Part of the budget is allocated for unforeseen infrastructure and personnel costs and will be refunded to the DAO if unspent at the end of the one-year period.

## Proposers

### Team overview

- Philipp spent the last 2 years working full-time as a backend dev in a crypto hedge fund building dashboards, portfolio tracking tools, and trading bots. Philipp contributed extensively to the new dashboard MVP. Philipp will receive $100,000.
- Alunara and Benny have been offering Curve-related analytics on llama.airforce and have actively participated in various Curve DAO activities since 2021. 


### Team roles and responsibilities

- **Alunara**: Front-end development, DevOps
- **Benny**: Back-end development, subgraphs, management and liaison with other teams within the DAO & integrating protocols
- **Philipp**: Back-end development, DevOps


## Long-term vision and specifications

### 1. Dedicated analytics platform

Unlike other AMMs like <a href="https://info.uniswap.org/">Uniswap</a> or <a href="https://dune.com/balancerlabs">Balancer</a>, Curve does not have a dedicated analytics page. DeFi-wide analytics platforms like <a href="https://defillama.com/protocol/curve">Defi Llama</a> and community sites focused on the Curve ecosystem like <a href="https://llama.airforce/">Llama Airforce</a> do provide valuable data about Curve, but this situation nonetheless has severe limitations. Namely, the analytics focus on high-level metrics (TVL, Volume) but often lack the level of depth required for the proper management of the pools (parameter setting, protocol design decisions for future pools). The spread of information across multiple websites, few of which are focused solely on Curve, also hinders discoverability. To solve these problems we offer to build a dedicated platform for Curve analytics at curvemonitor.com, that provides both high-level and more detailed metrics. It will offer a one-stop shop for all information and data related to Curve pools.

We have developed an MVP for what a future dashboard would look like for a standard Curve pool. This **real-time dashboard allows users to follow trading activity, including miner extractable value (MEV) activity, and monitor the historical performance of the pool by displaying assets balances, price fluctuations, and bonding curves**. The real-time dashboard has already proved its usefulness when it **helped identify the transaction that eventually led to the recovery of $152 millions** from the Wormhole hacker (Link once news is released). We are committed to working closely with the Curve core team and the research and risk team to continue improving and enhancing these dashboards. 

Our current roadmap for improvements is as follows:

- Making the MVP dashboard available for all mainnet Curve pools
- Expanding historical data availability to the lifetime of each pool
- Adding new charts and features to the current dashboard: 
    - Histogram of price ranges to assess historical peg and volatility of a pair
    - Comparison of LP token price performance vs holding strategy vs xy=k 0 fee AMM, with IL calculator
    - Market depth chart (amount required to move price by x%)
    - Historical pool revenue
    - Overlay indicator of pool parameter changes on historical charts to gauge their effect
- Extending support to pools on all chains where Curve is deployed
- Expanding MEV tracking to arbitrage trades
- Optimizing the user interface for a better and more user-friendly experience
- Offering alerts and data export features


### 2. Alternative DAO front-end

The new Curve website currently lacks a dedicated DAO page and the classic website's DAO page is hampered by extremely slow loading times, confusing navigation, and a lack of essential features, such as the option to post new proposals or the decoding of calldata for governance proposals. To increase voter engagement and the dynamism of the DAO's governance, we offer to build an alternative DAO front end that would be faster and more user-friendly than the current one. We see this task as synergetic with the development of pool dashboards, as the **DAO front-end should offer appropriate pool health metrics to help users make more informed decisions** and pool parameter changes are subject to the DAO's approval. We also aim to **integrate voting options on the UI for veCRV derivatives** such as vlCVX to offer all voters in the ecosystem a unified and intuitive experience.

We recently released a governance vote page on llama.airforce as a first stepping stone to this project. The list of future planned developments is as follows:

- Add the option to vote directly using veCRV, vlCVX, or other veCRV derivatives with governance rights on the governance vote page
- Create a page for gauge weight votes
- Add new metrics when displaying gauge candidates to guide voter decisions: TVL and volume changes, incentives posted, and fees collected over the past 2 rounds.
- Develop a UI for vote creation, including templates for the most common actions: parameter changes, gauge addition, and gauge removal
- (Subject to further discussion and approval from Curve team): Create a marketplace contract and UI where users with no veCRV can post a proposal and a small bounty. Users with 2.5k veCRV can then post the proposal on their behalf and claim the bounty for gas reimbursement
- Historical tracking of veCRV incentives on different marketplaces (votemarket, warden, votium, bribe.crv.finance)
- Profile page to track users' voting history


### 3. Interface with Curve team, DAO, integrating protocols and users

The Curve core team and other teams within the DAO regularly gather data and produce analytics to inform decision-making processes. In certain instances, third-party companies or community members may be contracted or volunteer to generate specific reports and research. However, a significant proportion of these outputs are disseminated on disparate self-hosted domains or third-praty platforms (Dune, Flipside...), forgotten in git repositories, and/or left unmaintained. To address this issue, we propose to expand our responsibilities to include working directly with external contributors to ensure that their output, if deemed significant enough, can be integrated into a **continuously updated and maintained dashboards on our analytics platform**. By adopting this approach, we will also **ensure continuity in the analytics knowledge base for Curve**, enabling us to provide guidance to protocols and users seeking Curve-related metrics. Additionally, we will be able to explain the calculation methodology and origins of the data used in these metrics. 

- Making a web UI for users to run in-browser pool simulations using the research team's CurveSim package
- Work with the Curve core team and research team to provide them with the data streams and metrics they need. For instance:
    - Provide needed historical data for the research team's CurveSim package
    - Create a simulator to estimate changes in volume and revenue at different fee levels to set more competitive pool fees.
- Ensure high availability and proper documentation for all our public API endpoint
- Maintain a decentralized data source for generic Curve pools/DAO metrics on the Graph
- Field analytics-related questions on Telegram and Discord


### 4. Open code-base


To **promote open collaboration and facilitate contributions** we will work to consolidate the existing codebase which is currently fragmented across multiple git organizations and repositories, establish guidelines for contributors and improve documentation to make it easier for people to reuse our code. 

- Ensure that all repositories within the codebase maintain a minimum level of documentation
- Create a git organization and migrate the various existing repositories to it
- Implement concise contribution guidelines and templates for issues/PR


### 5. LLAMMA/crvUSD dashboard

This part can only be speculative until the release of LLAMMA and its associated UI, however, we can anticipate that this new feature will require detailed metrics to inform both core developers' and users' decisions. 


## One-year roadmap

Our most immediate goal is the delivery of the pool dashboard for Ethereum mainnet based on the current MVP. We will then work on delivering the gauge weight pages and allowing veCRV lockers to vote from the UI. Once these main milestones are achieved we want to take some time to reorganize and consolidate the codebase and our infrastructure. This will likely include a significant amount of refactoring, migration of databases and cloud services, setting up monitoring tools as well as access management tasks. The remainder of the grant period will be dedicated to expanding the dashboard's charts, the DAO page's features and working on supporting additional chains, starting with Polygon/Matic. Matic is supported by both Llama nodes and the Graph and while the chain-wide variety of pools (3CRV-based tricrypto, CRV/tricrypto LP token pair, lending pools, forex pools) makes it a challenging first addition it will also help ensure that our code generalizes to other L1s. 

| Period           | Tasks                                                                        |
|------------------|------------------------------------------------------------------------------|
| Q2 2022          | Bringing the pool dashboard MVP to production for all Ethereum mainnet pools |
| Q3 2022          | Codebase and infrastructure reorganization, migrations                       |
| Q4 2022          | DAO gauge weight page & DAO dashboards                                       |
| Q1 2023          | Proposal creation page + templates on DAO, additional pool charts            |


## Budget

### Salaries

- Total: $100,000
    - Philipp: Full-time (40h/w) - $100,000
    - Alunara: Current Llama Airforce grant
    - Benny: Current Llama Airforce grant

### Design, infrastructure, and operational costs

Infrastructure and design costs are estimated. Unused funds at the end of the grant period will be returned to the DAO.

- Total: $28,000
    - Designer contractor for pool dashboard and website: $16,000 (4 weeks @ $100/h)
    - Domain names & ENS: $100
    - Cloud services (Hosting, static public IPs, CDN, load balancer): $6000 ($500 * 12)
    - Archival node access for Ethereum mainnet & Polygon: $600 ($49/m on Alchemy)
    - Tenderly subscription: $800 ($67/m)
    - Operational costs (gas costs for contract deployments & transactions, 2500 veCRV for proposal creation): $4500

Unused funds at the end of the grant period will be returned to the DAO.

