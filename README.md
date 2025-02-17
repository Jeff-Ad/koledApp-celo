<!-- TABLE OF CONTENTS -->

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->

## About The Project

Celo Composer allows you to quickly build, deploy, and iterate on decentralized applications using Celo. It provides a number of frameworks, examples, and Celo specific functionality to help you get started with your next dApp.

<p align="right">(<a href="#top">back to top</a>)</p>

## Built With

Celo Composer is built on Celo to make it simple to build dApps using a variety of front-end frameworks.

- [Celo](https://celo.org/)
- [Solidity](https://docs.soliditylang.org/en/v0.8.15/)
- [Next.js](https://nextjs.org/)
- [React.js](https://reactjs.org/)
- [Material UI](https://mui.com/)
- [React Native](https://reactnative.dev/)
- [Flutter](https://docs.flutter.dev/)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- GETTING STARTED -->

## Getting Started

To build your dApp, you'll need to install the dependencies, create a new project, and run the following commands:

## Prerequisites

- Node

## How to use Celo Composer

The easiest way to get started with Celo Composer is using `@celo/celo-composer`. This is a CLI tool enables you to quickly start building dApps on Celo for multiple frameworks including React, React Native (w/o Expo), Flutter and Angular. You can create the dApp using default Composer templates provided by Celo. To get started, use the following command:

```bash
npx @celo/celo-composer create
```

#### Output

![Output-1](./images/readme/image-1.png)

- Select the framework you like and please enter.

![Output-2](./images/readme/image-2.png)

- Enter the project name and the starter project will the create in present working directory.

### Get testnet funds and install dependencies

```sh
cd hardhat
yarn install
npx hardhat create-account # prints a private key + account
```

1. Create `packages/hardhat/.env` and paste the line containing the private key into it, so it looks something like this:

`PRIVATE_KEY="0xba28d5cea192f121db5f1dd7f501532170bb7bb984c4d3747df3e251e529f77d"`

2. Fund the account from the faucet [here](https://celo.org/developers/faucet). Once the account is funded, deploy the contracts with:

```sh
yarn deploy
```

## Supported Frameworks

### <u>React</u>

- Creating examples and experiment with React for your libraries and components.
- Start the dApp with `yarn dev`/`npm run dev` and you are good to go.
- Support for Website and Progressive Web Application.
- Works with all major crypto wallet.

Check here to learn more about [Celo Composer - React](./packages/react-app/README.md)

### <u>React Native</u>

- You don't need to configure anything. A reasonably good configuration of both development and production builds is handled for you so you can focus on writing code.
- Support for Android and IOS.
- Works with [Expo](https://expo.dev/) and without Expo.
- Working example app - The included example app shows how this all works together.
- Easy to use and always updated with latest dependencies.

Check here to learn more about [Celo Composer - React Native](./packages/react-native-app/README.md)

### <u>Flutter</u>

- One command to get started - Type `flutter run` to start development in your mobile phone.
- Works with all major mobile crypto wallets.
- Support for Android, IOS (Web, Windows, and Linux coming soon).
- Working example app - The included example app shows how this all works together.
- Easy to use and always updated with latest dependencies.

Check here to learn more about [Celo Composer - Flutter](./packages/flutter-app/README.md)

### <u>Angular</u>

- Creating examples and experiment with Angular for your libraries and components.
- Easy to setup and use.

Check here to learn more about [Celo Composer - Angular](./packages/angular-app/README.md)

## Review

- Edit smart contracts in `packages/hardhat/contracts`.
- Edit deployment scripts in `packages/hardhat/deploy`.
- Edit frontend in `packages/react-app/pages/index.tsx`.
- Open <http://localhost:3000> to see the app.

You can run `yarn deploy --reset` to force re-deploy your contracts to your local development chain.

## Deploy Your DApp

This repo comes with a `netlify.toml` file that makes it easy to deploy your front end using [Netlify](https://www.netlify.com/). The `toml` file contains instructions for Netlify to build and serve the site, so all you need to do is create an account and connect your GitHub repo to Netlify.

## Developing with local devchain

You can [import account account keys](https://metamask.zendesk.com/hc/en-us/articles/360015489331-How-to-import-an-Account) for the local development chain into Metamask. To print the private keys of the local chain accounts `cd /packages/hardhat` and run

```shell
npx hardhat devchain-keys
```

If you are working on a local development blockchain, you may see errors about `the tx doesn't have the correct nonce.` This is because wallets often cache the account nonce to reduce the number of RPC calls and can get out of sync when you restart your development chain. You can [reset the account nonce in Metamask](https://metamask.zendesk.com/hc/en-us/articles/360015488891-How-to-reset-your-account) by going to `Settings > Advanced > Reset Account`. This will clear the tx history and force Metamask to query the appropriate nonce from your development chain.

**Note:** You can get a local copy of mainnet by forking with Ganache. Learn more about [forking mainnet with Ganache here.](https://trufflesuite.com/blog/introducing-ganache-7/index.html#1-zero-config-mainnet-forking)

## React library choices

The example UI in `packages/react-app` uses the [Next.js](https://nextjs.org/) React framework, and [react-celo](https://www.npmjs.com/package/@celo/react-celo) Celo library to get you started with building a responsive, web3 DApp quickly. Feel free to use it as a reference and use whatever web3 packages you are familiar with.

## The Graph

**Using the Graph is not a requirement for building a web3 application. It is more of a convenience for when your application is reading a lot of data from a blockchain.**

Its suggested to only adding support for the Graph when you need it, avoid premature optimization.

The `/packages/subgraphs` directory includes an example subgraph for reading data from the example `Storage.sol` contract. The Graph is a blockchain data indexing service that makes it easier to read data from EVM blockchains. You can read more about how the Graph works and how to use it in the [README here](/packages/subgraphs/README.md).

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->

## 🔭 Learning Solidity

📕 Read the docs: <https://docs.soliditylang.org>

- [Primitive Data Types](https://solidity-by-example.org/primitives/)
- [Mappings](https://solidity-by-example.org/mapping/)
- [Structs](https://solidity-by-example.org/structs/)
- [Modifiers](https://solidity-by-example.org/function-modifier/)
- [Events](https://solidity-by-example.org/events/)
- [Inheritance](https://solidity-by-example.org/inheritance/)
- [Payable](https://solidity-by-example.org/payable/)
- [Fallback](https://solidity-by-example.org/fallback/)

📧 Learn the [Solidity globals and units](https://solidity.readthedocs.io/en/v0.6.6/units-and-global-variables.html)

## Support

Join the Celo Discord server at <https://chat.celo.org>. Reach out on the dedicated repo channel [here](https://discord.com/channels/600834479145353243/941003424298856448).

<!-- ROADMAP -->

## Roadmap

See the [open issues](https://github.com/celo-org/celo-composer/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTRIBUTING -->

## Contributing

As a contributor, you can add your own dApp to this repository and include it as a tab for others to access. Follow the steps below and reference existing files for additional details to help you get started.

If you decide to try this out and find something confusing, consider opening an pull request to make things more clear for the next developer that comes through. If you improve the user interface or create new components that you think might be useful for other developers, consider opening a PR.

We will happily compensate you for contributions. Anywhere between 5 and 50 cUSD (or more) depending on the work. This is dependent on the work that is done and is ultimately up to the discretion of the Celo Foundation developer relations team.

You can view the associated bounty on Gitcoin [here](https://gitcoin.co/issue/celo-org/celo-progressive-dapp-starter/17/100028587).

<p align="right">(<a href="#top">back to top</a>)</p>

### How to Contribute a new dApp

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

- Create a new smart contract in `packages/hardhat/contracts`.
- Add a new deployment script within `packages/hardhat/deploy/00-deploy.js` using the name of your smart contract.
- Deploy your Smart Contract from within packages/hardhat using `yarn deploy`
- Add a new component named `ContractName.tsx` to `packages/react-app/components` to create front end of your dApp.
- Export component using `packages/react-app/components/index.tsx` using `export * from './ContractName`
- Import component to `packages/react-app/pages/index.tsx` by adding contract to `import { ContractName } from "@/components";`
- Add tab within tabs component in `packages/react-app/pages/index.tsx` and replace # with tab number.

```jsx
<Tab label="Contract Label" {...a11yProps(#)} />
```

- Add tab panel to page replacing `#` with tab number and `ContractName` with your smart contract name

```jsx
<TabPanel value={value} index={#}>
    <GreeterContract contractData={contracts?.ContractName} />
</TabPanel>
```

You should now be able to view your new dApp from [http://localhost:3000](http://localhost:3000).

<p align="right">(<a href="#top">back to top</a>)</p>

## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<!-- CONTACT -->
## Contact

- [@CeloDevs](https://twitter.com/CeloDevs)
- [Discord](https://discord.com/invite/6yWMkgM)

<p align="right">(<a href="#top">back to top</a>)</p>
