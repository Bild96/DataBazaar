# 💾 DataBazaar
![Screenshot from 2022-11-20 12-46-48](https://user-images.githubusercontent.com/52472445/202898557-80ac4770-aa77-4041-9cd3-00c6a671a05a.png)

Quick Start
===========

To run this project locally:

1. Prerequisites: Make sure you have Node.js ≥ 14 installed (https://nodejs.org), then use it to install [yarn]: `npm install --global yarn` (or just `npm i -g yarn`)
2. Install dependencies: `yarn install` (or just `yarn`)

Setup
======
```
git clone https://github.com/Bild96/DataBazaar.git
cd  DataBazaar
yarn install
yarn test
```

Deploy Smart Contract
=====================

Every smart contract in NEAR has its [own associated account][NEAR accounts]. 
When you run `yarn dev`, your smart contracts get deployed to the live NEAR TestNet with a throwaway account. When you're ready to make it permanent, here's how.


Step 0: Install near-cli
--------------------------

You need near-cli installed globally. Here's how:

    npm install --global near-cli

This will give you the `near` [CLI] tool. Ensure that it's installed with:

    near --version


Step 1: Create an account for the contract
------------------------------------------

Visit [NEAR Wallet] and make a new account. You'll be deploying these smart contracts to this new account.

Now authorize NEAR CLI for this new account, and follow the instructions it gives you:

    near login

Step 2: deploy!
---------------

One command:

    yarn deploy

As you can see in `package.json`, this builds & deploys smart contracts to NEAR TestNet.

Note down the smart contract account id from the console and update it in src/config.js:1


Run the Frontend
================

Run the following commands from the near-registry folder

```
cd src
yarn install
yarn start
```

Then visit http://localhost:1234 from your browser to test the Near Registry

Deploy the Frontend using netlify
=================================

Run the following commands from the near-registry folder

```
cd src
yarn build
yarn global add netlify-cli
netlify login
netlify deploy --prod
```

Then follow the instructions given by the netlify cli and specify `./dist` as the publish directory


App Link (NEAR Testnet)
=======================
https://DataBazaar.netlify.app/


  [NEAR]: https://nearprotocol.com/
  [yarn]: https://yarnpkg.com/
  [AssemblyScript]: https://docs.assemblyscript.org/
  [smart contract docs]: https://docs.nearprotocol.com/docs/roles/developer/contracts/assemblyscript
  [asp]: https://www.npmjs.com/package/@as-pect/cli
  [NEAR accounts]: https://docs.nearprotocol.com/docs/concepts/account
  [NEAR Wallet]: https://wallet.nearprotocol.com
  [near-cli]: https://github.com/nearprotocol/near-cli
  [CLI]: https://www.w3schools.com/whatis/whatis_cli.asp
  [create-near-app]: https://github.com/nearprotocol/create-near-app
  [NEAR Frontend]: https://docs.near.org/docs/api/naj-quick-reference


Credits
===========
https://github.com/near-examples/guest-book/
