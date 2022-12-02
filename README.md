# Kickstart

`Ethereum crowdfunding system`

<p align="center">
  <img alt="made for ethereum" src="https://img.shields.io/badge/made_for-ethereum-771ea5.svg">
  <img alt="MIT license" src="https://img.shields.io/badge/license-MIT-blue.svg">
</p>

Kickstart allows you to create and manage campaigns in the Goerli network using Ethereum smart contracts.

The idea was inspired by [Kickstarter](https://www.kickstarter.com).

---

***Packages utilized:***

- [Next.js](https://nextjs.org/) - Server Rendered Apps
- [Web3Js](https://web3js.readthedocs.io/en/1.0/) - Ethereum Javascript API
- [Semantic UI](https://react.semantic-ui.com/) - User Interface

<!-- ![Ethereum Campaigns Project](https://i.imgur.com/ZJnIbFN.gif) -->

## Prerequisites

- [Metamask browser extension](https://metamask.io/) installed and account.

- Some ether balance using [Goerli Authenticated Faucet](https://goerlifaucet.com).

- In the absence of Metamask, the project will fall back to using [Infura node](https://infura.io/) to access the Goerli network.

## Smart Contract

- The contract for Kickstart is deployed at address `0xD7d2347d300718479321E63CA28832454fba9250` and is available inside [ethereum/contracts](https://github.com/minhtran241/kickstart/tree/main/ethereum/contracts). You can explore the deployed contract on TESTNET Goerli (GTH) Blockchain Explorer (Etherscan) at [here](https://goerli.etherscan.io/address/0xD7d2347d300718479321E63CA28832454fba9250)

- Kickstart will interact with the deployed the contract to create campaigns.

## Quickstart

***Note:*** You have to set up all the environment variables before doing this step

*Deploy by connecting to Infura node (specific provider)*

```sh
yarn compile

yarn test

yarn deploy
```

## Running the project

```sh
npm run dev
```

Go to the browser at address <http://localhost:3000> to access the web page.

Next.js performs server-side rendering of the pages and hot reloading as you make any changes to the code.

## Operations

### Create Campaign

You can create a campaign by specifying the minimum pledge amount required.

Once the campaign is created, you become the manager of the campaign and will be able to create requests which need to be approved by the backers.

Any user who backs below the requirement for the campaign will have their transaction rejected.

### View Campaign

Shows details of the campaign such as the address of the account which created the campaign, minimum pledge amount required, campaign balance, number of people who have pledged for the campaign, and number of requests created by the manager.

### Back the Campaign

Allows you to pledge and back to the campaign.

### View Requests

List the requests created by the manager for the campaign.

Backers can approve the requests.

Once the approval criteria are met, the manager can finalize the request for payment to the recipient.

### Add Request

The manager of a campaign can create a request which will be fulfilled by the recipient.

Once equal or more than 50% of the campaign backers approve the request, the manager can finalize the payment to the vendor.
